# Scraper Specification Template

## Target Information
- **URL**: [Target URL]
- **Purpose**: [What data is being extracted]

## API Endpoints Discovered

### [Endpoint Name]
- **Method**: [GET/POST/etc.]
- **URL**: [Full API URL]
- **Auth**: [Headers/Cookies required]
- **Query Parameters**:
  - `param1`: [Description/Value]
- **Request Body** (if POST):
  ```json
  [JSON Structure]
  ```
- **Response Shape**:
  ```json
  [JSON Structure]
  ```
- **Pagination Strategy**: [How to fetch the next page]

## Data Model
[Description of the final data structure to be stored]

## Implementation Example
```python
import requests

def fetch_data():
    # Implementation based on discovered API
    pass
```
