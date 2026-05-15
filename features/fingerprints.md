# Fingerprint Management

Every browser profile in Dolphin Anty has a unique fingerprint — a set of parameters that identify the browser to websites. Dolphin Anty spoofs these parameters at the browser engine level, not via JavaScript, making the spoofing undetectable by standard methods.

## What is a browser fingerprint?

When you visit a website, it can read dozens of signals from your browser to identify you: your screen size, installed fonts, graphics card model, audio processing behavior, and more. Combining these signals creates a "fingerprint" that can track you even without cookies.

## Parameters you can control

Dolphin Anty lets you configure over 20 fingerprint parameters:

| Parameter | Description |
|-----------|-------------|
| User-Agent | Browser version string reported to websites |
| Platform | OS type (Windows, macOS, Linux, iOS, Android) |
| Screen resolution | Display size reported to websites |
| CPU cores | Number of logical processors reported |
| RAM | Memory amount reported |
| Timezone | Browser timezone |
| Language | Browser language and locale |
| Geolocation | GPS coordinates |
| WebRTC | IP address handling for WebRTC connections |
| Canvas | 2D rendering fingerprint |
| WebGL | 3D graphics fingerprint |
| WebGPU | GPU fingerprint |
| ClientHints | Chrome's structured browser version data |
| Audio | Audio processing fingerprint |
| Media devices | Microphone, camera, speaker identifiers |
| Device name | Device name reported to websites |
| Webcam parameters | Camera specification fingerprint |
| Fonts | Installed font list |
| Do Not Track | DNT header value |

## Desktop and mobile fingerprints

You can generate fingerprints for any OS, including iOS and Android. Mobile fingerprints let you simulate phone or tablet browsing sessions from a desktop computer.

## Fingerprint modes

For most parameters, you can choose how Dolphin Anty handles the value:

- **Real**: Uses your actual device value
- **Noise**: Slightly modifies the real value to be unique
- **Altered**: Replaces with a plausible generated value
- **Manual**: You specify the exact value
- **Random**: Generates a completely random value
- **Off**: Disables spoofing for that parameter

The default settings use a combination of Real, Noise, and Altered to produce the most convincing fingerprints.

## How Canvas noise works

Dolphin Anty generates Canvas noise that is close to the real value but uniquely different per profile. The noise value is tied to the profile — it doesn't change between sessions, which is how real users behave. Changing the noise level does not produce visible differences; the system handles this automatically.

## WebRTC configuration

| Mode | Behavior |
|------|----------|
| Real | Shows your actual IP through WebRTC |
| Altered | Replaces WebRTC IP with the proxy IP |
| Disabled | Blocks WebRTC entirely |

Use **Altered** when you want WebRTC to report the proxy IP. Use **Disabled** only if the site requires WebRTC to be absent.

## Updating User-Agents

Keep User-Agents current to avoid detection by tools like Pixelscan.net:

1. Open the profile editor
2. Go to the **Advanced** tab
3. Click **Update** next to the User-Agent field

## Bulk fingerprint refresh

On Base, Team, and Enterprise plans:

1. Select multiple profiles using checkboxes
2. Click the 3-dot menu in the bulk operations bar
3. Choose **Refresh fingerprints**

## Best practices

- Match the profile OS to your real device OS
- Leave default settings unless you have a specific reason to change them
- Keep User-Agents updated — outdated agents are a common detection signal
- Don't set Do Not Track to enabled — it makes profiles statistically unusual

## Detection checkers

You can test your profile's fingerprint at:
- [Pixelscan.net](https://pixelscan.net) — checks for common inconsistencies
- [BrowserLeaks.com](https://browserleaks.com) — detailed parameter inspection
- [CreepJS](https://abrahamjuliot.github.io/creepjs/) — advanced fingerprint analysis
