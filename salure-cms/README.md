# [Dad's Name] — Real Estate Site (editable, no code)

The design is the same bold/energetic build as before. The difference: all the actual content
(name, phone, listings, testimonials, bio) now lives in `content/site.json` instead of being
hardcoded in the HTML, and there's a simple editor at `/admin` so your dad can change it himself.

## One-time setup

1. **Create a free GitHub repo** and push this whole folder to it.
2. **Sign up at netlify.com** (free) and connect it to that GitHub repo.
   - Build command: leave blank
   - Publish directory: leave as the repo root (`.`)
3. In the Netlify dashboard for your new site, go to **Site configuration → Identity** and click
   **Enable Identity**.
4. Under **Identity → Registration**, set it to **Invite only** (so random people can't sign up
   and edit the site).
5. Under **Identity → Services**, enable **Git Gateway**. This is what lets the `/admin` editor
   save changes back to GitHub without your dad needing a GitHub account.
6. Go to the **Identity** tab, click **Invite users**, and send an invite to your dad's email.
   He'll get an email to set a password.

## What your dad does from here on

1. Go to `https://<your-site>.netlify.app/admin`
2. Log in with the email/password from the invite
3. Edit any field — his name, phone, listings, testimonials, photos — in a plain form
4. Click **Publish**

That's it. No code, no GitHub, no HTML. Netlify rebuilds and republishes automatically within
about a minute of him publishing.

## Custom domain

Site configuration → Domain management → Add a domain, once one's purchased.

## If you'd rather test locally first

Just open `index.html` in a browser — it reads `content/site.json` directly. The `/admin` editor
only works once it's deployed to Netlify with Identity + Git Gateway turned on, since it needs
somewhere real to save changes to.
