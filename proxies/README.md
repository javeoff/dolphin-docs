# Proxies

Proxies assign unique IP addresses to your browser profiles. Each profile should use a dedicated proxy to prevent account linkage.

## Supported proxy types

| Type | When to use |
|------|-------------|
| HTTP | Basic web traffic, widely supported |
| SOCKS4 | Older protocol, TCP only |
| SOCKS5 | Supports TCP and UDP, recommended for most use cases |

For a detailed comparison, see [Proxy types explained](proxy-types.md).

## Quick start

1. Go to **Browser Profiles** and create or edit a profile
2. In the **Proxy** field, enter your proxy in one of the supported formats:
   - `host:port`
   - `host:port:login:password`
   - `login:password@host:port`
   - `http://host:port` (with protocol prefix)
   - `socks5://host:port:login:password`
3. Click the arrow button to verify the proxy's connection, geolocation, and timezone
4. Save the profile

## Managing proxies

Go to the **Proxy** section in the left sidebar to manage all proxies across your account:

- Add proxies in bulk
- Edit proxy credentials
- Share proxies with team members
- Delete unused proxies

See [Editing and sharing proxies](editing-sharing-proxies.md) for details.

## Integrated proxy partners

Dolphin Anty has direct integrations with several proxy providers. These are configured through the Partners section:

- **NodeMaven** — residential proxies (promo code: DOLPHIN35)
- **ResiProx** — residential proxies
- **Asocks** — mobile and residential proxies (promo code: DOLPHINANTY15)
- **ThorData** — mobile proxies
- **NaProxy** — residential and datacenter proxies

## Rotational proxies

If your proxy provider gives you a rotation link (URL that returns a new IP on each request), enter the rotation URL in the proxy settings. A rotation control button appears on the profile list for easy IP changes.

## Articles in this section

- [Proxy types explained](proxy-types.md)
- [How to add a proxy](add-proxy.md)
- [Check proxy connection](check-proxy.md)
- [Editing and sharing proxies](editing-sharing-proxies.md)
