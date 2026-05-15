# Profile Creation via API

Create browser profiles programmatically using the Dolphin Anty REST API.

## Prerequisites

1. Dolphin Anty app running and logged in
2. Valid API token — see [Creating an API token](api-token.md)

## Getting fingerprint data

Before creating a profile, fetch a real User-Agent and WebGL values from the Dolphin Anty fingerprint API.

### Get a User-Agent

```http
GET https://dolphin-anty-api.com/fingerprints/useragent
  ?browser_type=chrome
  &browser_version=120
  &platform=Windows
Authorization: Bearer YOUR_API_TOKEN
```

### Get WebGL info

```http
GET https://dolphin-anty-api.com/fingerprints/webgl
  ?browser_type=chrome
  &platform=Windows
Authorization: Bearer YOUR_API_TOKEN
```

## Create a profile

```http
POST https://dolphin-anty-api.com/browser_profiles
Content-Type: application/json
Authorization: Bearer YOUR_API_TOKEN

{
  "name": "Profile Name",
  "platform": "windows",
  "browserType": "anty",
  "mainWebsite": "none",
  "useragent": {
    "mode": "manual",
    "value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 ..."
  },
  "webrtc": {
    "mode": "altered",
    "ipAddress": ""
  },
  "canvas": {
    "mode": "noise"
  },
  "webgl": {
    "mode": "noise"
  },
  "webglInfo": {
    "mode": "manual",
    "vendor": "Google Inc. (NVIDIA)",
    "renderer": "ANGLE (NVIDIA GeForce RTX ...)"
  },
  "timezone": {
    "mode": "auto"
  },
  "locale": {
    "mode": "auto"
  },
  "cpu": {
    "mode": "manual",
    "value": 4
  },
  "memory": {
    "mode": "manual",
    "value": 8
  },
  "doNotTrack": 0,
  "osVersion": "10"
}
```

## Important notes

- User-Agent mode must be `"manual"` when providing a custom value — the custom UA only works in manual mode
- Fetch both User-Agent and WebGL values from the fingerprint endpoints above rather than constructing them manually
- The profile ID is returned in the response — save it for starting/stopping the profile via the local API

## Response

A successful request returns the created profile object including its `id`:

```json
{
  "data": {
    "id": 123456,
    "name": "Profile Name",
    "platform": "windows",
    ...
  }
}
```

Use this `id` with the local API to start the profile:

```
GET http://localhost:3001/v1.0/browser_profiles/123456/start?automation=1
```

## Full API reference

For the complete list of parameters and their allowed values, see the official API documentation at [docs.dolphin-anty-cdn.com](https://docs.dolphin-anty-cdn.com/index.html).
