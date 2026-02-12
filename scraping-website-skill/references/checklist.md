# Production Scraper Checklist

## Reliability & Error Handling
- [ ] Retries with exponential backoff for 5xx errors.
- [ ] Proper handling of 403 (Forbidden) and 429 (Too Many Requests).
- [ ] Validation of JSON schema before processing.
- [ ] Logging of failed requests and unexpected response formats.

## Rate Limiting & Stealth
- [ ] Respect `robots.txt` (if applicable).
- [ ] Random delays between requests.
- [ ] User-Agent rotation.
- [ ] Proxy support (if needed for high volume).

## Maintenance
- [ ] Alerting for when the API structure changes.
- [ ] Versioning of the scraping logic.
- [ ] Periodic checks of data quality.

## Storage & Scale
- [ ] Incremental loading (don't re-scrape what you already have).
- [ ] Deduplication logic.
- [ ] Batch inserts for large datasets.
