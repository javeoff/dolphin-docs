# Profile Setup Guidelines

Follow these guidelines to create profiles that blend in naturally with real users.

## Use default fingerprint settings

When you create a profile and click **New fingerprint**, Dolphin Anty generates settings based on real user data. These defaults are optimal — leave them unchanged unless you have a specific technical reason to modify them.

Parameters safe to customize:
- Timezone
- Language
- Geolocation
- CPU core count
- RAM amount
- Screen resolution
- Media devices (microphone, camera)

Parameters to avoid changing:
- Do Not Track (DNT) — very few real users enable this; changing it makes your profile stand out
- Canvas noise — Dolphin Anty generates values close to real ones automatically
- User-Agent — only change if you need a specific browser version

## Match the OS to your real device

Anti-fraud systems detect discrepancies between the reported OS and system-level signals like fonts. If you're on Windows, use Windows profiles. If you're on macOS, use macOS profiles.

## Keep User-Agents up to date

Outdated User-Agents trigger detection on sites like Pixelscan.net. To update:

1. Open the profile for editing
2. Go to the **Advanced** tab
3. Click **Update** next to the User-Agent field

## Use a clean proxy per profile

Assign a dedicated proxy to each profile. Sharing one proxy across multiple profiles defeats the purpose of isolation — sites can link accounts by IP.

For proxy recommendations, see [Proxy types](../proxies/proxy-types.md).

## Don't open the same profile on multiple devices simultaneously

Opening one profile on two devices at the same time causes sync conflicts and can corrupt session data.

## Add extensions through the app, not inside profiles

Extensions added directly inside a profile window can cause issues. Always add extensions through the dedicated **Extensions** section in the Dolphin Anty main menu.
