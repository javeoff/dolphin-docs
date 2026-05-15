# How to Add a Proxy

You can add proxies to Dolphin Anty in three ways: during profile creation, via the Proxy section, or directly from the profile list.

## During profile creation or editing

1. Open the profile creator or the profile editor (3-dot menu → **Edit**)
2. In the **Proxy** field, click **New Proxy**
3. Enter the proxy in any supported format:
   ```
   host:port
   host:port:login:password
   login:password@host:port
   socks5://host:port:login:password
   ```
4. Click the arrow (→) button to verify the connection, geolocation, and timezone
5. Save the profile

If you've added the proxy before, select it from the list of saved proxies instead.

## Via the Proxy section

1. Click **Proxy** in the left sidebar
2. Click **Add Proxy** (top-right corner or center button)
3. Enter the proxy details
4. Click **Save**

The proxy is now saved in your account and can be assigned to any profile.

## From the profile list

1. Locate the **Proxy** column in the Browser Profiles list
2. Click the pencil (✏️) icon next to the profile
3. Choose one of three options:
   - No proxy
   - New proxy (enter details)
   - Existing proxy (select from saved list)

## Bulk proxy assignment

On paid plans, you can change proxies for multiple profiles at once:

1. Select profiles using checkboxes
2. In the bulk operations bar, click **Change proxy**
3. Enter or select a proxy
4. Apply

## Rotational proxies

If your provider gives you a URL that rotates the IP on each request:

1. In the proxy settings, enter the rotation URL in the designated field
2. After saving, a rotation button appears in the profile list row
3. Click it to request a new IP without restarting the profile

## Verifying a proxy

Click the arrow (→) button next to any saved proxy to check:
- Connection status (pass/fail)
- Detected IP and country
- Timezone assigned to that IP

This helps confirm the proxy is working and that the geolocation matches your profile settings.
