# Cookie Robot and Smart Paste

## Cookie Robot

Cookie Robot automatically visits specified websites inside a profile to build up a natural browsing history and set cookies. This helps warm up new accounts and makes profiles appear more like real users.

### How to use Cookie Robot

1. Open the 3-dot menu next to the profile
2. Click **Cookie robot**
3. Enter the URLs you want the profile to visit
4. Click **Start**

The browser runs through the list of URLs automatically, collecting cookies and building session data. Let it complete before using the account for main activities.

### Use cases
- Warming up fresh Facebook or Google accounts
- Building browsing history before running ads
- Populating cookies on newly registered accounts

## Smart Paste

Smart Paste recognizes data structures in files and automatically maps them to profile fields during mass profile creation.

### Supported file formats
- `.txt`
- `.csv`
- `.xlsx`

### How to use Smart Paste

1. Prepare a file with your data (email, password, proxy, cookies, etc.)
2. In the profile creator, drag and drop your file onto the import area
3. Dolphin Anty parses the file and displays a column mapping table
4. Click the pencil icon on any column to remap it to the correct field
5. Configure fingerprint settings for the batch
6. Click **Create profiles**

### Macros for profile naming

Use these macros in the profile name template to generate unique names:

| Macro | Output |
|-------|--------|
| `{{EMAIL.LOGIN}}` | Login part of an email address |
| `{{COUNT.ID}}` | Sequential number starting from 1 |
| `{{DATE}}` | Current date |

Example: `Profile {{COUNT.ID}} - {{EMAIL.LOGIN}}` produces `Profile 1 - john.doe`, `Profile 2 - jane.smith`, etc.

## Importing and exporting cookies manually

To import cookies to a single profile:
1. Open the 3-dot menu → **Import**
2. Paste or upload the cookie data (Netscape format or JSON)

To export cookies from a profile:
1. Open the 3-dot menu → **Export**
2. Save the cookie file

For bulk cookie export across many profiles, use the bulk operations bar (select profiles → **Export cookies**).
