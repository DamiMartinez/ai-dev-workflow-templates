---
name: scraping-website-skill
description: Systematically discover hidden JSON APIs for web scraping using Chrome DevTools MCP. Use when the user needs to scrape a website and wants to find the underlying APIs instead of parsing HTML.
---

# Scraping Website Skill

This skill guides you through the process of discovering hidden APIs that power modern websites, enabling more efficient and robust scraping than traditional HTML parsing.

## Workflow

### 1. Initial Exploration
- Use `chrome-devtools.navigate` to open the target URL.
- Analyze the page structure and identify elements that trigger data loads (filters, pagination, "Load More" buttons, search bars).

### 2. Monitoring Network Traffic
- Clear the network log using `chrome-devtools.clear_network_requests` (if available) or just start watching.
- Use `chrome-devtools.list_network_requests` to see ongoing requests.
- **Filter for JSON**: Focus on requests with `resourceType: "xhr"` or `"fetch"` and check their `content-type` for `application/json`.
- Ignore images, CSS, fonts, and tracking scripts (e.g., Google Analytics).

### 3. Systematic Interaction
- For each UI interaction (e.g., clicking a "Search" button):
  - Execute the interaction using `chrome-devtools.click` or `chrome-devtools.fill`.
  - Immediately call `chrome-devtools.list_network_requests` to capture the resulting API call.
  - Inspect the request details: method, URL, headers (especially `Authorization` or custom headers), and query parameters.
  - Inspect the response body to verify it contains the desired data.

### 4. Analysis and Documentation
- Document each relevant endpoint using the [scraper-template.md](references/scraper-template.md).
- Identify how pagination is handled (e.g., `offset`, `page`, `cursor`).
- Identify any mandatory headers or tokens.

### 5. Production Readiness
- Review the [checklist.md](references/checklist.md) to ensure the scraper design is robust.
- Summarize requirements for data modeling, frequency, and storage.

## Deliverables

Upon completion, you must produce:
1. **Google Doc**: A full technical specification including:
   - Discovered API documentation.
   - Production scraper requirements.
   - At least one concrete Python/Node.js scraper example.
2. **Markdown File**: An optimized version of the same content to be saved locally and used as context for future implementation steps.

## Example Request
"I want to scrape the product list from `example.com/products`. They have infinite scroll and several filters (category, price range). Help me find the API that provides the data."
