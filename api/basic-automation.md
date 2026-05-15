# Basic Automation

Dolphin Anty supports automation via DevTools Protocol. You start a profile through the local API, then connect your automation framework to the running browser instance.

## Supported frameworks

- **Puppeteer** (JavaScript/Node.js)
- **Playwright** (JavaScript, Python, Java, C#)
- **Selenium** (requires a modified ChromeDriver)

## Step 1: Start a profile for automation

Send a GET request to start the profile in automation mode:

```
GET http://localhost:3001/v1.0/browser_profiles/PROFILE_ID/start?automation=1
```

For headless mode (no visible browser window):
```
GET http://localhost:3001/v1.0/browser_profiles/PROFILE_ID/start?automation=1&headless=1
```

The response includes the port and WebSocket endpoint needed to connect:

```json
{
  "automation": {
    "port": 50568,
    "wsEndpoint": "/devtools/browser/..."
  }
}
```

## Step 2: Connect your automation framework

### Puppeteer (JavaScript)

```javascript
const puppeteer = require('puppeteer-core');

const response = await fetch(
  `http://localhost:3001/v1.0/browser_profiles/${profileId}/start?automation=1`
);
const { automation } = await response.json();

const browser = await puppeteer.connect({
  browserWSEndpoint: `ws://localhost:${automation.port}${automation.wsEndpoint}`,
  defaultViewport: null,
});

const page = await browser.newPage();
await page.goto('https://example.com');
```

### Playwright (JavaScript)

```javascript
const { chromium } = require('playwright');

const response = await fetch(
  `http://localhost:3001/v1.0/browser_profiles/${profileId}/start?automation=1`
);
const { automation } = await response.json();

const browser = await chromium.connectOverCDP(
  `ws://localhost:${automation.port}${automation.wsEndpoint}`
);
const context = browser.contexts()[0];
const page = context.pages()[0];
await page.goto('https://example.com');
```

### Selenium

Selenium requires a modified ChromeDriver to avoid detection on target websites. Download the current version from the Basic Automation documentation in the Dolphin Anty help center.

## Step 3: Stop the profile

When your script is done, stop the profile:

```
GET http://localhost:3001/v1.0/browser_profiles/PROFILE_ID/stop
```

Or call `browser.disconnect()` in your script (this disconnects the automation but does not stop the profile).

## Plan requirements

Automation (starting profiles via API) requires the **Starter plan or above**. The Free plan cannot start profiles through the API.

Cookie import and export via the API requires **Base plan or above**.

## Headless mode

Headless mode runs the browser without a visible window. This is useful for server-side automation.

Note: Some websites detect and block headless browsers. If you encounter detection in headless mode, switch to visible mode (`automation=1` without `headless=1`) and run on a machine with a display.

## Running without a GUI

Dolphin Anty does not support OS environments without a graphical interface. If you need headless operation, use the `headless=1` parameter while running on a GUI system, or use a virtual display (e.g., Xvfb on Linux).
