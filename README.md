# Marley & James — Wedding Website

Static site, single page: `index.html`. No build step.

## Deploy to Netlify

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project → GitHub**.
2. Select this repo (`jhickok13/marley-and-james-wedding`) and the branch you want live.
3. Build settings:
   - Build command: *(leave blank)*
   - Publish directory: `.`
4. Deploy. Netlify gives you a live `*.netlify.app` URL, and auto-redeploys on every push to that branch.
5. Optional: add a custom domain under Site settings → Domain management.

## RSVP form (Formspree)

The RSVP form posts to Formspree's no-signup email endpoint:

```
https://formspree.io/james.hickok0@gmail.com
```

**One-time activation:** the first real submission triggers a confirmation email
from Formspree to james.hickok0@gmail.com. Click the confirmation link in that
email to activate the form — after that, every submission is emailed to that
address automatically.

> Note: I couldn't reach formspree.io from this sandbox to verify this endpoint
> live (network egress to that domain is blocked here), so test it with a real
> submission once the site is deployed. If it doesn't trigger a confirmation
> email, switch to the dashboard-issued endpoint described below instead.

To get a nicer dashboard (all responses in one place, spam filtering, CSV
export) instead of relying on the email-only flow:

1. Sign up free at [formspree.io](https://formspree.io).
2. Create a new form, copy its endpoint (looks like `https://formspree.io/f/xxxxxxxx`).
3. Replace the `action` attribute on `<form id="rsvpForm">` in `index.html` with that endpoint.
