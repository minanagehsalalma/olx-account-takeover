# When “Try Again Later” Still Means “You Guessed Right”

Historical security write-up about an OLX account-takeover bug caused by a verification-code flow that still leaked the correct code during lockout.

## Live Page

- [Article](index.html)

## Repo Contents

- `index.html` — the published write-up
- `pages.css` — styling for the article
- `assets/` — only the images used by the article

## Summary

The core issue was simple:

> the application said “try again later,” but it still reacted differently to the correct code than to a wrong one

That leak was not limited to one screen. The same verification behavior was reused across account flows including password reset, which raised the impact to full account takeover. The platform also lacked session revocation on password change, which meant access could persist even after the victim rotated their password.

## GitHub Pages

This repository is meant to be published directly with GitHub Pages from the root of the default branch.

