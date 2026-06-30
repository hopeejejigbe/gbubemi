# Gbubemi Blog — Setup Guide

This is your Astro-powered blog, styled in Gbubemi's brand (Rhodamine Red → Hot Pink gradient, Satoshi font). It's built to sit at `gbubemi.com/blog`, separate from your existing landing page.

## First-time setup

1. Install Node.js if you don't have it (nodejs.org)
2. Open a terminal in this folder and run:
   ```
   npm install
   ```
3. To preview it locally before publishing:
   ```
   npm run dev
   ```
   Then open the URL it gives you (usually http://localhost:4321)

## Writing a new blog post

You never touch HTML or CSS. Every post is a single Markdown file in:

```
src/content/blog/
```

To write a new post:

1. Duplicate the existing file `virtual-tryon-dark-skin-honest-review.md`
2. Rename it to match your new post (e.g. `size-10-shopping-guide.md`)
3. Edit the top section between the `---` lines (this is called frontmatter):

```
---
title: "Your Post Title Here"
description: "One sentence describing the post — shows in Google search results"
pubDate: 2026-07-15
author: "Hope Ejejigbe"
tags: ["Size Inclusive", "Shopping Tips"]
draft: false
---
```

4. Below the second `---`, just write your post in plain text. Use:
   - `## ` before a line for a section heading
   - `**text**` to make text bold
   - `- ` before a line for a bullet point
   - `> ` before a line for a styled quote
   - Leave a blank line between paragraphs

5. Save the file. That's it — it's now a post.

## Publishing to your live site

1. Run the build command:
   ```
   npm run build
   ```
2. This creates a `dist` folder — that's your finished, ready-to-upload site
3. Upload the contents of `dist` into a `/blog` folder inside your existing Cloudflare Pages project (alongside your homepage files)
4. Push/redeploy as you normally do for gbubemi.com

## Draft posts

Set `draft: true` in any post's frontmatter to hide it from the live blog while you're still working on it. Flip it to `false` when ready to publish.

## Brand reference (for anyone editing styles)

- Rhodamine Red: `#E5007E`
- Hot Pink: `#FF4DA6`
- Gradient angle: 135deg
- Font: Satoshi (loaded via Fontshare)

## Questions

If anything breaks or looks off, bring the error message back to this conversation and we'll fix it together.
