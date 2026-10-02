# whitneyloy.com

A proposed replacement for whitneyloy.com, built as a single static page: plain HTML and CSS, no build step and no CMS.

To preview it, open `index.html` in a browser.

## What's there today

The current site is a 25-year-old splash page with:

- an orange-branch illustration
- "Whitney Loy" set in thin green type
- the tagline "cultivating ideas"
- ten services in light gray (public relations, marketing, development, fundraising, advertising, social media, online marketing, event planning, design, innovation)
- an email address, phone number and "new york, ny"

**Keep:** the orange-and-green identity and the word *cultivating*. In fundraising, cultivation is how you build relationships with donors, so the tagline fits the work better now than it did then.

**Fix:**

| Problem | Why it matters | In the proposal |
| --- | --- | --- |
| No HTTPS ("Not Secure" in the browser) | Browsers warn visitors, and search engines rank it lower. | Host on a service that provides free automatic HTTPS. |
| Ten services, no focus | Readers can't tell what you're known for. | Three focus areas: fundraising, events, marketing and storytelling. |
| No current role or proof of work | It reads as a freelance pitch from 2000, not a nonprofit CEO. | Your current role up front, an About section, numbers and press. |
| Light-gray text on white | Hard to read and fails accessibility contrast. | Every text color meets the WCAG AA contrast standard, with a dark mode. |
| Phone number public | Brings spam and robocalls. | Email only, plus LinkedIn. |
| Fixed desktop layout | Most visits now come from phones. | Responsive layout, checked at phone width. |

## The proposed page

One scrolling page with five sections:

1. **Hero:** "Cultivating the people and resources that help good work *grow*," with your role and two buttons.
2. **About:** a short bio in the first person, with a headshot slot.
3. **What I do:** three focus areas that replace the old list of ten, followed by three headline numbers.
4. **Press and conversations:** starts with the TriNet interview.
5. **Contact:** email and social links.

## Before launch

All copy is a first draft based on public information; rewrite anything that doesn't sound like you. Highlighted text (anything with `class="todo"`) is a placeholder. Before going live:

- [ ] Confirm the facts:
  - the CEO title and McCarton Foundation description
  - the McCarton link (`https://www.mccarton.org/`)
  - the University of Missouri degree
- [ ] Fill in the three numbers under "By the numbers", or remove that block.
- [ ] Add a headshot: replace `.portrait-placeholder` with an `<img>`; a portrait-shaped photo (about 4:5) works best.
- [ ] Swap the drawn orange for the original orange-branch illustration if you still have the file: a transparent PNG or an SVG.
- [ ] Add your LinkedIn URL; decide whether Instagram belongs here.
- [ ] Add more press items, or keep just the one.
- [ ] Optional: add a share image (`og:image`) so links preview nicely on LinkedIn and in iMessage.

## Hosting

The recommended host is GitHub Pages: it's free, comes with HTTPS and deploys every time this repo changes. Netlify and Cloudflare Pages work the same way.

1. In this repo's GitHub page, go to Settings → Pages, set Source to "Deploy from a branch", and choose the branch and `/ (root)`.
2. Under Custom domain, enter `whitneyloy.com`, then tick **Enforce HTTPS** once it's available.
3. At your domain registrar, point the domain at GitHub Pages, following [GitHub's custom-domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site):
   - four `A` records for `whitneyloy.com`
   - a `CNAME` record for `www`
4. Keep email working: change only the `A` and `CNAME` records for the website. Leave any `MX` records alone, because those deliver mail to whitney@whitneyloy.com.
