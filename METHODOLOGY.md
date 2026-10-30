# Methodology

This describes how I approach a target. It does not include exploit details.

## 1. Target selection
- I focus on self-hosted and smaller vendor platforms with a published VDP or security contact.
- I avoid large crowdsourced programs where duplicate rates are high, though I have also reported findings there.
- I read the scope and disclosure terms before testing. If they are unclear, I ask first.

## 2. Reconnaissance
- Map the application from the browser: pages, forms, API calls, and how state is kept (session, cart, token).
- Note which requests change state and which checks protect them (tokens, method, origin, step order).
- Use public sources such as open-source repositories when the vendor publishes them.

## 3. Testing
- Manual, one variable at a time. Every test changes one thing from a known baseline.
- Use only my own accounts. Do not access other users' data beyond confirming a boundary is broken, and stop there.
- Keep test actions reversible. Cancel test orders, remove test data, and record what was cleaned up.
- No destructive payloads, no persistence, and no data extraction beyond what a proof needs.

## 4. Verification
- Reproduce every finding twice before reporting it.
- Check whether it is already known (public advisories, CVE records) and say so in the report if it overlaps.
- Separate what I confirmed from what I inferred.

## 5. Reporting
- Root cause, reproduction steps, observed result, impact, and a fix suggestion.
- A "what I checked and found solid" section, so the vendor knows what was covered.
- Scope limits stated plainly.

See [DISCLOSURE.md](DISCLOSURE.md) for timelines and what I publish.
