# hssrf2-redirector

Temporary public redirector for authorized Meta Muse bug-bounty research (Phase 12, hypothesis H-SSRF-2).

Single page (`index.html`) that redirects — via `<meta http-equiv="refresh">` (primary) plus a JS `window.location.replace` fallback — to the official Meta researcher canary endpoint `https://www.internalfb.com/intern/bug-bounty/get-canary-token/`.

Purpose: test whether the Muse `browser.open` fetch layer follows a redirect from a public user-owned URL to that endpoint, or blocks it. No other target. To be deleted after the test at the coordinator's decision.
