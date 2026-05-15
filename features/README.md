# Features Overview

Dolphin Anty provides a complete set of tools for managing multiple browser identities at scale.

## Core capabilities

| Feature | Available on |
|---------|-------------|
| [Browser profiles](browser-profiles.md) | All plans |
| [Fingerprint management](fingerprints.md) | All plans |
| [Proxy integration](../proxies/README.md) | All plans |
| [Tags, statuses, notes](organization.md) | All plans |
| [Profile synchronizer](synchronizer.md) | Starter and above |
| [Teamwork & permissions](teamwork.md) | Base and above |
| [Script Builder automation](../guides/script-builder.md) | Base and above |
| [API automation](../api/README.md) | Starter and above |
| [Cloud sync](cloud-sync.md) | All paid plans |
| [Mass operations](browser-profiles.md#bulk-operations) | All plans |

## Feature highlights

### Fingerprint engine
Control over 20 parameters including User-Agent, Canvas, WebGL, WebGPU, ClientHints, fonts, screen resolution, CPU, RAM, audio, media devices, and more. All spoofing occurs at the browser engine level — no detectable JavaScript injections.

### Profile synchronizer
Run actions on a master profile and have every synchronized profile mirror those actions in real time. Ideal for bulk account farming and parallel campaign management.

### Automation-ready
Start profiles via the local REST API and connect Puppeteer, Playwright, or Selenium to automate any workflow. The API runs on `localhost:3001` while the app is open.

### Team management
Add users, assign roles (Admin, Teamlead, User), share profiles with specific permissions, and set creation limits per user.
