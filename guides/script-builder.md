# Script Builder

Script Builder lets you create automated browser scenarios without writing code. Available on Base plan and above.

## What you can automate

- Account registration flows
- Form filling
- Navigation sequences
- Cookie population (warm-up)
- Repetitive actions across many profiles

## Creating a script

1. Go to **Script Builder** in the left sidebar
2. Click **New script**
3. Give the script a name
4. Add actions step by step using the visual editor:
   - Navigate to URL
   - Click element
   - Type text
   - Wait for element
   - Take screenshot
   - Execute JavaScript
5. Save the script

## Running a script on a profile

**Single profile:**
1. Open the 3-dot menu next to the profile
2. Click **Script run**
3. Select the script to execute
4. Click Run

**Multiple profiles:**
1. Select profiles with checkboxes
2. In the bulk operations bar, click **Run script**
3. Select the script
4. Click Run

The script executes on each selected profile using its own proxy and fingerprint.

## Supported platforms

Script Builder works on Windows, Linux, and macOS.

## For advanced automation

If you need more complex logic (loops, conditionals, API calls), use the [Automation API](../api/basic-automation.md) with Puppeteer, Playwright, or Selenium instead.
