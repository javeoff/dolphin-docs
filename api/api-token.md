# Creating an API Token

API tokens authenticate your requests to the Dolphin Anty API. You can create multiple tokens with different expiration dates.

## Steps

1. Go to [dolphin-anty.com](https://dolphin-anty.com) and log in
2. In your personal area, click **API** in the left menu
3. Enter a name for the token (e.g., `automation-script`, `puppeteer-bot`)
4. Set an expiration date
5. Click **Generate**
6. Copy the token immediately and store it securely

The token is shown **only once**. You cannot view it again after leaving the page. If you lose it, delete the old token and generate a new one.

## Using the token

Include the token in the `Authorization` header of every API request:

```
Authorization: Bearer YOUR_API_TOKEN
```

Or authenticate through the local login endpoint before making other requests:

```http
POST http://localhost:3001/v1.0/auth/login-with-token
Content-Type: application/json

{"token": "YOUR_API_TOKEN"}
```

A successful response returns `{"success": true}`.

## Managing tokens

From the **API** section in your personal area:
- View all active tokens (names and expiration dates)
- Delete tokens that are no longer needed
- Create new tokens at any time

## Common errors

**"Unauthorized" response**
Your token is missing from the request, expired, or was deleted. Generate a new token and update your scripts.

**API unavailable**
The Dolphin Anty app must be running and you must be logged in. The API does not work when the app is closed.
