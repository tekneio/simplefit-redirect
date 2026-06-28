# simplefit-redirect

Path-preserving redirect: **simplefit.tekneio.com -> streak.tekneio.com**

This repo exists only to keep the old domain `simplefit.tekneio.com` working. It is served on GitHub Pages and 301/JS-redirects every request to the canonical site **https://streak.tekneio.com**, preserving the path.

## How it works

`CNAME` sets the custom domain `simplefit.tekneio.com`. `404.html` catches every unknown path and `index.html` handles the root; both run `location.replace("https://streak.tekneio.com" + location.pathname + location.search + location.hash)`. So `simplefit.tekneio.com/privacy.html` redirects to `streak.tekneio.com/privacy.html` with the path kept.

## Notes

Canonical site lives in `tekneio/simplefit` (streak.tekneio.com). Do NOT delete this repo or its `CNAME` file. Full runbook: `simplefit-marketing/DOMAIN_SETUP.md` (local).
