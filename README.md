# MultiComp Lab website

Source for the MultiComp Lab website (http://multicomp.cs.cmu.edu/), built with [Hugo](https://gohugo.io/).
Every push to `main` rebuilds the site and deploys it to GitHub Pages via GitHub Actions
(`.github/workflows/hugo.yml`).

The content was recovered from the Wayback Machine snapshot of the old WordPress site (2026-03-11)
and converted to Markdown/YAML. The look is the original WordPress theme (`static/theme/style.css`).

## Where things live

| What | File(s) |
| --- | --- |
| People and previous members | `data/people.yaml`, `data/previous_members.yaml` |
| Publications (all years, categories, research topics) | `data/publications.yaml` |
| Projects | `data/projects.yaml` |
| News posts | `content/news/*.md` |
| Research topics | `content/research/*.md`, overview pages `content/multimodal-machine-learning.md` etc. |
| Resources (datasets, software, courses, ...) | `content/resources/*.md`, `content/datasets.md` etc. |
| FAQ | `content/faq/*.md` (questions are in the `faqs:` list of each file) |
| Home page text | `content/_index.md` |
| Sidebar menus (Research, Resources, FAQ) | `data/menus.yaml` |
| Top navigation | `hugo.toml` (`[[menus.left]]`, `[[menus.right]]`) |
| Images and PDFs | `static/wp-content/uploads/...` (kept at the old URLs so existing links still work) |
| Page templates | `layouts/` |

## Common edits

**Add a publication** – add an entry at the top of `data/publications.yaml`:

```yaml
- year: 2026
  citation: 'A. Author, L.-P. Morency. Paper Title. **NeurIPS**, 2026.'
  links:
  - name: PDF
    url: https://arxiv.org/abs/xxxx.xxxxx
  categories:      # optional: book-chapters, journal-articles, refereed-conference-papers, refereed-workshop-papers
  - refereed-conference-papers
  research:        # optional: file names from content/research/, shows the paper on that topic page
  - multimodal-representation
```

The year page (`/2026/`) and category pages are generated automatically.

**Add a lab member** – add them to the right group in `data/people.yaml`. Put the photo in
`static/images/people/` and reference it as `/images/people/name.jpg`:

```yaml
  - name: Jane Doe
    photo: /images/people/jane-doe.jpg
    website: https://janedoe.github.io
    scholar: https://scholar.google.com/citations?user=XXXX
    bio: Jane Doe is a PhD student at the Language Technologies Institute ...
```

When someone leaves, move their entry to `data/previous_members.yaml`. Empty groups are hidden.

**Add a news post** – create `content/news/my-post.md`:

```markdown
---
title: Four papers accepted at ACL 2026
date: 2026-05-01
image: /images/news/acl2026.jpg
news_categories: [Conferences]
---

Text of the post in Markdown.
```

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
