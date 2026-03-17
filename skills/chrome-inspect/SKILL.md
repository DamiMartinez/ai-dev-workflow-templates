---
name: chrome-inspect
description: >
  Inspects browser tabs using Chrome DevTools — use this skill whenever the user wants to inspect,
  debug, or interact with anything in the browser: DOM elements, CSS classes, cookies, localStorage,
  sessionStorage, network requests, console logs, or any page content. Triggers on phrases like
  "check the cookie", "inspect the element", "what's in localStorage", "look at the tab",
  "check the session", "go to [tab] and inspect", "what does [page] show", "open devtools",
  or any request to interact with the browser via DevTools. If the user mentions a specific tab
  or URL, go directly to it — no need to ask. If it's ambiguous, list the open tabs and ask.
---

## Process

### Step 1 — Find the right tab

**If the user specified a tab or URL:** call `list_pages` to get page IDs, find the matching tab, then go straight to Step 2.

**If the user did NOT specify a tab:** call `list_pages`, show a grouped summary to the user, and ask which tab they want to inspect. Wait for their answer, then proceed.

### Step 2 — Switch to the tab

Call `select_page(pageId, bringToFront=true)` to make it the active context.

### Step 3 — Get an overview (run in parallel)

Call both of these at the same time:
- `take_screenshot` — visual view of the page
- `take_snapshot` — a11y DOM tree (also reveals which element is selected in DevTools Elements panel)

### Step 4 — Inspect what was asked

Choose the right tool based on what the user wants:

| User wants | Tool to use |
|---|---|
| Cookies, localStorage, sessionStorage, JWT, tokens | `evaluate_script` with the storage script below |
| A specific element's class, text, attributes | `take_snapshot` (already done) — find it by uid, or use `evaluate_script` |
| Network requests / API calls | `list_network_requests` |
| Console errors or logs | `list_console_messages` |
| Run custom JS in the page | `evaluate_script` |
| Click / fill / interact with the page | `click`, `fill`, `press_key` |
| Full page screenshot | `take_screenshot(fullPage=true)` |

### Storage inspection script

Use this when asked about cookies, sessions, tokens, or any stored data:

```js
() => ({
  cookies: document.cookie,
  localStorage: Object.fromEntries(Object.entries(localStorage)),
  sessionStorage: Object.fromEntries(Object.entries(sessionStorage))
})
```

If the result contains a JWT (starts with `eyJ`), decode and summarize the payload (base64 decode the middle segment) — show email, role, expiry, and any other useful fields.

## Output format

- Always show the screenshot so the user can see the page state
- Summarize findings clearly — don't just dump raw JSON
- For JWTs: decode and present the meaningful fields, not the raw token
- If an element is selected in DevTools (shown in snapshot as `[selected in the DevTools Elements panel]`), call it out explicitly with its tag, text, and classes
- If there's nothing interesting in a storage area (empty), say so briefly

## Tips

- `take_snapshot` is faster than a screenshot for DOM inspection — prefer it when you just need the element tree
- `evaluate_script` runs in the **page** context, not the DevTools console — `$0` won't work here (it's a DevTools-only variable)
- To find a specific element's class programmatically: `() => document.querySelector('selector').className`
- Network requests and console messages accumulate since page load — filter by URL pattern if there are many
