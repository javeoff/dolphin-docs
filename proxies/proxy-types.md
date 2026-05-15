# Proxy Types

Choosing the right proxy type affects detection resistance, speed, and cost.

## HTTP proxies

HTTP proxies route web traffic over the HTTP protocol. They are the most widely supported type and work with virtually all websites.

- **Protocol prefix**: `http://`
- **Use case**: General browsing, most social media platforms
- **Limitation**: Does not support UDP traffic

## SOCKS4 proxies

An older proxy protocol that operates at the transport layer, supporting TCP connections.

- **Protocol prefix**: `socks4://`
- **Use case**: Legacy setups or providers that only offer SOCKS4
- **Limitation**: No authentication support in the basic version, no UDP

## SOCKS5 proxies

The most capable proxy protocol. Supports TCP, UDP, and authentication.

- **Protocol prefix**: `socks5://`
- **Use case**: Recommended for most multi-accounting scenarios
- **Advantages**: Full protocol support, works with WebRTC when configured correctly

## Residential vs. datacenter proxies

| Type | Description | Detection risk | Cost |
|------|-------------|----------------|------|
| Residential | IPs assigned to real home internet users | Low | Higher |
| Mobile | IPs from mobile carrier networks | Very low | Highest |
| Datacenter | IPs from server farms | Higher | Lower |

For accounts on platforms with strict anti-fraud (Facebook Ads, Google Ads), residential or mobile proxies are strongly recommended. Datacenter proxies are acceptable for lower-risk platforms or scraping.

## Proxy format reference

Dolphin Anty accepts these input formats:

```
host:port
host:port:login:password
login:password@host:port
http://host:port
http://login:password@host:port
socks5://host:port:login:password
```

## Checking proxy quality

A proxy IP showing up in anti-fraud databases will trigger account flags regardless of your fingerprint quality. Test proxy IPs at:

- [IPQualityScore](https://www.ipqualityscore.com/free-ip-lookup-proxy-vpn-test) — checks fraud scores
- [Scamalytics](https://scamalytics.com) — proxy and VPN detection
- [IPInfo.io](https://ipinfo.io) — geolocation and ISP data
