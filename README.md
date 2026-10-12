# Your personal website

One file, `index.html`, is the whole site. No coding tools, no build step, no cost.

## 1. Fill in your details

Open `index.html` in any text editor (Notepad, VS Code, or GitHub's own editor later).

- **Top of the file (Step 1):** your name and the one-line description that Google and WhatsApp/LinkedIn link previews show.
- **The content block (Step 2):** everything between `EDIT YOUR CONTENT BELOW` and `END OF YOUR CONTENT`.

The page reads like a letter: a few paragraphs (`paragraphs`), where highlighted phrases tear open a panel of details right below their paragraph (`panels`).

Formatting you can use inside any text:

| Type this                          | You get                                         |
|------------------------------------|-------------------------------------------------|
| `[[phrase\|panel-id]]`             | a highlighted phrase that opens that panel      |
| `[text](https://example.com)`      | a link                                          |
| `==text==`                         | highlighter                                     |
| `**text**`                         | **bold**                                        |
| `*text*`                           | *italic*                                        |

To add a new panel:
1. Add an entry under `panels`, for example `"talks": { text: ["I spoke at ..."] }`.
2. Point a phrase at it in a paragraph: `I have given a few [[talks|talks]].`

A panel can hold `text` (paragraphs), `papers` (title, authors, venue, summary, links), `groups` (headed lists), `timeline`, `quotes`, and a short italic `note`. Copy an existing panel and change it, since that's the easiest way to get the shape right.

Every panel has its own link, so `yoursite/#ai-disclosure` opens straight to that research.

Things to keep in mind:
- Keep the quote marks and commas exactly as they are. If the page goes blank, a missing comma or quote is almost always why.
- Apostrophes inside `"double-quoted"` text are fine. Just don't put a `"` inside one.

## 2. Add your photo and CV

Put these two files in the same folder as `index.html`:

- `photo.jpg`: a portrait or square photo, ideally under 500 KB. Until you add one, the site shows your initials on a yellow square.
- `cv.pdf`: your CV. Use the `cv.pdf` made for this site.

To preview, double-click `index.html` and it opens in your browser.

## 3. Publish it free on GitHub Pages

1. Sign up at [github.com](https://github.com) (free). Your username becomes your web address, so pick a good one.
2. Click **+ → New repository**. Name it exactly `yourusername.github.io` (with your real username). Set it to **Public** and click **Create repository**.
3. Click **uploading an existing file**, drag in `index.html`, `photo.jpg`, `cv.pdf` and the whole `blog` folder (drag the folder itself so the file stays inside it), and click **Commit changes**.
4. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main** and folder **/ (root)**, then **Save**.
5. Wait a minute or two, then open `https://yourusername.github.io`. That's your live site, with free HTTPS.

**To update later:** open `index.html` in your repository on GitHub, click the pencil icon, edit, and click **Commit changes**. The live site refreshes within a minute or two.

## 4. Optional: your own domain (the only paid part)

Want `yourname.com` instead of `yourusername.github.io`?

1. Buy the domain from any registrar (Namecheap, Cloudflare, GoDaddy, Hostinger, etc.).
2. In your repository: **Settings → Pages → Custom domain**, type your domain, and **Save**.
3. At your registrar's DNS settings, add:
   - four **A** records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - a **CNAME** record for `www` pointing to `yourusername.github.io`
4. Once GitHub confirms the domain (this can take a few hours), tick **Enforce HTTPS**.

GitHub's guide, in case its steps have changed: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
