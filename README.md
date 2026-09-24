# MultiComp Lab website

Source for the MultiComp Lab website (http://multicomp.cs.cmu.edu/), built with [Hugo](https://gohugo.io/).
Every push to `main` rebuilds the site and deploys it to GitHub Pages via GitHub Actions
(`.github/workflows/hugo.yml`).

The content was recovered from the Wayback Machine snapshot of the old WordPress site (2026-03-11).
Page bodies keep their original HTML (`content/**/*.html`) and the templates reproduce the old WordPress
theme markup, so the site looks exactly like the old one. New pages can be written in Markdown (`.md`).
Theme files stay at their old paths (`static/wp-content/themes/multicomp/`, `static/wp-includes/`, ...).

## Where things live

| What | File(s) |
| --- | --- |
| People and previous members | `data/people.yaml`, `data/previous_members.yaml` |
| Publications (all years, categories, research topics) | `data/publications.yaml` |
| Projects | `data/projects.yaml` |
| News posts | `content/news/*.html` (or `.md` for new posts) |
| Research topics | `content/research/*.html`, overview pages `content/multimodal-machine-learning.html` etc. |
| Resources (datasets, software, courses, ...) | `content/resources/*.html`, `content/datasets.html` etc. |
| FAQ | `content/faq/*.html` (questions are in the `faqs:` list of each file) |
| Home page text | `content/_index.html` |
| Sidebar menus (Research, Resources, FAQ) | `data/menus.yaml` |
| Top navigation | `hugo.toml` (`[[menus.left]]`, `[[menus.right]]`) |
| Images and PDFs | `static/wp-content/uploads/...` (kept at the old URLs so existing links still work) |
| Legacy pages kept verbatim (not linked anywhere) | `static/2017/05/`, `static/research/page/2/`, ... |
| Page templates | `layouts/` |

## Common edits

**Add a publication** – add an entry at the top of `data/publications.yaml`:

```yaml
- year: 2026
  citation: '<p>A. Author, L.-P. Morency. Paper Title. <strong>NeurIPS</strong>, 2026.</p>'
  links:
  - name: PDF
    url: https://arxiv.org/abs/xxxx.xxxxx
  categories:      # optional: book-chapters, journal-articles, refereed-conference-papers, refereed-workshop-papers
  - refereed-conference-papers
  research:        # optional: file names from content/research/, shows the paper on that topic page
  - multimodal-representation
```

`citation` is HTML (as on the old site). The year page (`/2026/`) and category pages are generated
automatically, 10 entries per page like the old site (`/2026/page/2/` for the next 10).

**Add a lab member** – add them to the right group in `data/people.yaml`. Put the photo in
`static/images/people/` and reference it as `/images/people/name.jpg`:

```yaml
  - name: Jane Doe
    photo: /images/people/jane-doe.jpg
    website: https://janedoe.github.io
    scholar: https://scholar.google.com/citations?user=XXXX
    bio: <p>Jane Doe is a PhD student at the Language Technologies Institute ...</p>
```

When someone leaves, move their entry to `data/previous_members.yaml`. Empty groups are hidden.

**Add a news post** – create `content/news/my-post.md`:

```markdown
---
title: Four papers accepted at ACL 2026
date: 2026-05-01
display_date: May 1, 2026
image: /images/news/acl2026.jpg
excerpt: Four papers accepted at ACL 2026
news_categories: [Conferences]
news_months: ["2026-05"]
---

Text of the post in Markdown.
```

For a month that has no archive page yet, also add `content/news_months/2026-05/_index.md` with
`title: 2026/05` and `url: /2026/05/post_type-news/` (copy an existing one).

## Preview locally

```bash
brew install hugo      # or see https://gohugo.io/installation/
hugo server
```

Then open http://localhost:1313/.

## Deployment and domain

1. In the repository settings, go to Pages and set **Source** to **GitHub Actions**.
2. Each push to `main` runs the workflow and deploys the site.
3. To serve the site at multicomp.cs.cmu.edu, ask SCS Computing Facilities to point the DNS record
   for `multicomp.cs.cmu.edu` to `cmu-multicomp-lab.github.io` (CNAME), then enter the domain under
   Settings → Pages → Custom domain and enable "Enforce HTTPS".

The site uses root-relative links, so it must be served from the root of a domain
(it cannot live under a sub-path like `user.github.io/some-repo/`).
