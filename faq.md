# FAQ

## Browser profiles

**Why do I see "Timeout exceeded 60001 ms" when starting a profile?**
The most common causes are a slow or unstable proxy and a slow internet connection. To fix it: check your proxy speed, switch to a faster network, or install a VPN alongside the proxy. Also clear cache in the profile if it has accumulated a lot of data.

**Why won't my profile start with no error message?**
If only one or a few profiles won't start, check the proxy connection — Dolphin Anty blocks profile launch if the proxy fails to prevent IP leaks. If all profiles fail to start, your antivirus software may be interfering. Known conflicts: RAV Endpoint, Bitdefender, Avast. Add Dolphin Anty to your antivirus exclusions.

**What is "Error 409: Datadir damaged"?**
This means the profile data files are corrupted, usually because your system drive has less than 10–15 GB of free space or the app was shut down unexpectedly. Free up disk space, then try duplicating the profile. If that doesn't work, contact support.

**Can deleted profiles be recovered?**
Free and Starter plans permanently delete profiles. Base, Team, and Enterprise plans keep deleted profiles in a trash bin for 48 hours, after which they are permanently removed.

**Why don't my profiles appear in the list?**
Check whether a filter is active. Disable all active filters and verify you're in "All profiles" view rather than a specific folder. Also confirm you're logged into the correct account.

**Can I open the same profile on two devices at once?**
This is technically possible but causes sync conflicts and may corrupt session data. Always stop a profile on one device before opening it on another.

---

## Proxies

**My proxy check passes but websites are still blocked.**
The proxy IP may be listed in platform-specific blocklists. Try a different proxy from a different subnet or provider.

**WebRTC still shows my real IP even with "Altered" mode.**
Your proxy provider may have a WebRTC leak. Test at [BrowserLeaks WebRTC](https://browserleaks.com/webrtc). Switch to a provider that properly handles WebRTC or set WebRTC to "Disabled."

**What proxy format does Dolphin Anty accept?**
Any of these formats work:
- `host:port`
- `host:port:login:password`
- `login:password@host:port`
- `socks5://host:port:login:password`

---

## Fingerprints and spoofing

**I changed the Canvas noise but nothing seems different.**
Dolphin Anty generates noise that is close to the real value but uniquely different per profile. The system controls this automatically — you don't need to change the noise level manually.

**Should I set a different OS than my real device?**
No. Anti-fraud systems can detect OS mismatches through system-level signals like installed fonts. Always match the profile OS to your actual device OS.

**How do I update outdated User-Agents?**
Edit the profile → Advanced tab → click **Update** next to the User-Agent field. Do this periodically, especially after major Chrome updates.

**Why is Pixelscan detecting my profile?**
Common causes: outdated User-Agent, poor proxy quality (flagged IP), or OS mismatch in the profile settings. Update the User-Agent, test with a clean residential proxy, and verify the profile OS matches your real OS.

---

## Teamwork

**How many users does each plan include?**
Every plan includes 1 user by default (the account owner). Additional users must be purchased separately. Prices: Base +$10/user, Team +$20/user, Enterprise +$25/user.

**Can multiple users log into the same account?**
Yes. Multiple users can be logged in to the same account simultaneously without being blocked.

**What's the difference between transferring and sharing a profile?**
Transferring moves the profile to another user's account — it disappears from yours. Sharing gives another user access to the profile while it stays in your account.

---

## API and automation

**Does the Free plan support API automation?**
No. Starting profiles through the API requires the Starter plan or above.

**I'm getting "Unauthorized" errors from the API.**
Your API token is missing, expired, or was deleted. Go to your personal area → API section and generate a new token.

**Can I run Dolphin Anty on a server without a display?**
Dolphin Anty requires a graphical environment. For headless automation on Linux servers, use a virtual display like Xvfb, then connect to profiles with the `headless=1` API parameter.

**Where do I get the modified ChromeDriver for Selenium?**
Download it from the Basic Automation documentation in the Dolphin Anty help center at [help.dolphin-anty.com](https://help.dolphin-anty.com/en/).

---

## Pricing and billing

**What is the minimum subscription period?**
One month. There are no annual commitments required.

**Can I switch between plans?**
Yes. Upgrade or downgrade via the Payment section in your personal area.

**Can I have more than 500 profiles?**
Profile counts follow plan tiers. For 500+ profiles you need the Enterprise plan ($299/month for up to 1,000, scaling to 50,000+) or the Custom plan. Contact sales for custom pricing.

---

## Security and account safety

**How do I prevent my Dolphin Anty account from being compromised?**
Enable two-factor authentication in your personal area. Use a strong, unique password. Never share your API tokens — treat them like passwords.

**Does Dolphin Anty store my account passwords?**
No. Dolphin Anty does not have access to the passwords you use on third-party platforms inside your profiles.

---

## Support

Reach support through:
- **Live chat widget**: Bottom-right of [dolphin-anty.com](https://dolphin-anty.com)
- **In-app support button**: Bottom-right corner of the Dolphin Anty application
- **Telegram bot**: [@dolphinsupport_en_bot](https://t.me/dolphinsupport_en_bot)
