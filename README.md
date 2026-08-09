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

The RSVP form posts to a Formspree form created at formspree.io:

```
https://formspree.io/f/xkjwjnyk
```

Submissions show up in the Formspree dashboard and are emailed to the account
that owns the form. To manage notification settings, export responses, or add
spam filtering, log in at [formspree.io](https://formspree.io).
