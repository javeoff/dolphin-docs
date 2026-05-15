# API & Automation

Dolphin Anty provides a local REST API that lets you create profiles, start and stop them, and integrate with browser automation tools like Puppeteer, Playwright, and Selenium.

## Requirements

- Dolphin Anty app must be running and logged in
- API is available on `localhost:3001` by default
- Requests must originate from the same machine running Dolphin Anty
- Automation (starting profiles via API) requires Starter plan or above

## Authentication

Dolphin Anty supports two authentication methods:

**API token (recommended):**
```
Authorization: Bearer YOUR_API_TOKEN
```

**Login/password via local endpoint:**
```http
POST http://localhost:3001/v1.0/auth/login-with-token
Content-Type: application/json

{"token": "YOUR_API_TOKEN"}
```

See [Creating an API token](api-token.md) to generate your token.

## Key endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /v1.0/browser_profiles/{id}/start` | Start a profile |
| `GET /v1.0/browser_profiles/{id}/start?automation=1` | Start a profile for automation |
| `GET /v1.0/browser_profiles/{id}/start?automation=1&headless=1` | Start in headless mode |
| `GET /v1.0/browser_profiles/{id}/stop` | Stop a profile |
| `POST /v1.0/browser_profiles` | Create a new profile |
| `GET /v1.0/browser_profiles` | List profiles |

Full API documentation: [docs.dolphin-anty-cdn.com](https://docs.dolphin-anty-cdn.com/index.html)

## Articles in this section

- [Creating an API token](api-token.md)
- [Basic automation with Puppeteer, Playwright, and Selenium](basic-automation.md)
- [Profile creation via API](profile-creation-template.md)
