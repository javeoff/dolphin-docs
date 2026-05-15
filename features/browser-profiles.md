# Browser Profiles

Browser profiles are the core unit of Dolphin Anty. Each profile is an isolated browser environment with its own fingerprint, cookies, local storage, and proxy connection.

## Creating a profile

### Single profile

1. Go to **Browser Profiles** in the left sidebar
2. Click the **+** button (top-right corner)
3. Enter a profile name
4. Set a proxy (optional)
5. Paste cookies (optional)
6. Choose a profile type: Facebook, Google, TikTok, Crypto, or None
7. Click **New fingerprint** to generate or review the fingerprint
8. Click **Create profile**

### Mass profile creation

Create many profiles at once using a spreadsheet template:

1. Download the import template (xlsx format) from the create profile screen
2. Fill in profile data without altering the column structure
3. Click **Check data** to validate your file
4. Configure fingerprint settings for each column (Off, Manual, Real, Noise, Random, or Altered)
5. Click **Create profile**

### Smart Data Import

Drag and drop a `.txt`, `.csv`, or `.xlsx` file onto the import area. Dolphin Anty automatically detects the data structure and maps columns. You can rename columns and use macros for profile names:

- `{{EMAIL.LOGIN}}` — login part of an email address
- `{{COUNT.ID}}` — sequential number
- `{{DATE}}` — current date

## Starting and stopping profiles

- **Start**: Click **Start** next to the profile name
- **Stop**: Close the browser window or click **Stop** in the app

## Profile operations (3-dot menu)

| Action | Description |
|--------|-------------|
| Add to folder | Move profile into an existing folder |
| Edit | Modify name, proxy, tags, fingerprint parameters |
| History | View when and by whom the profile was launched |
| Cloud Sync | Enable or disable cloud synchronization |
| Show permissions | View which team members have access |
| Profile password | Require a password to launch (admin/creator only) |
| Script run | Execute a saved automation script |
| Export/Import | Transfer cookies or local storage |
| Cookie robot | Auto-fill cookies for specified websites |
| Copy profile | Duplicate with same or randomized fingerprints |
| Pin on top | Keep profile at the top of the list |
| Delete | Move to trash (48-hour recovery on Base+ plans) |

## Bulk operations

Select multiple profiles using the checkboxes on the left. A blue control panel appears with these options:

- Mass start / stop
- Launch in synchronizer
- Assign to folder
- Run script
- Add/change tags
- Change status
- Update proxy
- Export cookies and local storage
- Transfer profiles to another user
- Grant access rights
- Mass delete

## Organizing profiles

### Filtering
Filter profiles by:
- Assigned user
- Tags
- Statuses
- Profile type (Facebook, Google, TikTok, etc.)
- Proxy type
- Notes content
- Folder

You can apply up to 5 filters simultaneously.

### Folders
Group profiles into folders for easier navigation. Folders support granular access permissions for team members.

### Tags, statuses, and notes
Use tags and statuses to categorize profiles by niche, state, or any other criteria. Notes store free-form text visible in the profile list. See [Organization features](organization.md) for details.

## Editing a profile

Open the 3-dot menu and click **Edit**. The profile editor has two tabs:

**General**
- Profile name
- Proxy
- Tags and status
- Cookies

**Advanced**
- WebRTC mode (Real, Altered, Disabled)
- Canvas noise
- WebGL settings
- Timezone
- Language
- Geolocation
- GPU
- Memory
- Screen resolution
- Media devices

## Copying profiles

Two copy modes are available via the 3-dot menu → **Copy profile**:

- **Identical**: Same fingerprint and all settings
- **Randomized**: Same settings, new fingerprint generated

## Deleting profiles

Deleted profiles go to the trash bin on Base, Team, and Enterprise plans. They remain recoverable for 48 hours. Free and Starter plans delete profiles permanently.
