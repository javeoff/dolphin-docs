# Check Proxy Connection

Before using a proxy with important accounts, verify that it connects correctly and returns the expected geolocation.

## In-app proxy check

1. Open the Proxy section or the profile editor
2. Find the proxy you want to test
3. Click the **arrow (→)** button next to it

Dolphin Anty checks:
- **Connection**: Whether the proxy responds
- **Geolocation**: Country and city of the IP
- **Timezone**: Timezone associated with the IP location

If the check fails, the proxy is offline or the credentials are incorrect.

## Matching timezone to proxy location

When you assign a proxy with geolocation checking enabled, Dolphin Anty can automatically set the profile's timezone to match the proxy's location. This prevents a mismatch that could signal to websites that the timezone doesn't match the apparent location.

## Common proxy issues

**Proxy check passes but profiles won't load websites**
The proxy may be blocked by specific platforms. Try a different proxy from a different subnet or provider.

**WebRTC shows a different IP despite Altered mode**
Your proxy provider may have a WebRTC leak. Test the profile at [BrowserLeaks WebRTC](https://browserleaks.com/webrtc) to confirm.

**Timeout errors when starting profiles**
Slow proxy speed is a common cause of `Timeout exceeded 60001 ms` errors. Try a faster proxy or enable a VPN at the system level alongside the proxy.

**Site access blocked by geolocation**
Some websites block access from specific countries or IP ranges. Switch to a proxy from an accepted region.
