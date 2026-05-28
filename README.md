# Farnham Trusted

Farnham's trusted local business index — built with Hugo and PaperMod, hosted on GitHub Pages.

---

## First-time setup

### Prerequisites
- [Hugo](https://gohugo.io/installation/) installed
- [Git](https://git-scm.com/) installed

### Steps

```bash
# 1. Clone the repo
git clone https://github.com/FarnhamTrusted/farnhamtrusted.github.io
cd farnhamtrusted.github.io

# 2. Add the PaperMod theme
git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod

# 3. Run locally
hugo server -D
```

Visit http://localhost:1313 to preview.

---

## Adding a business

Copy the template below into the correct section folder:

```
content/
├── trades-home/       # Plumbers, electricians, builders, decorators
├── food-drink/        # Cafes, restaurants, pubs
├── health-wellbeing/  # Dentists, physio, gyms, salons
├── shops-retail/      # Independent shops
├── professional-services/ # Accountants, solicitors, estate agents
└── community-leisure/ # Classes, clubs, venues
```

### Business entry template

Create a new file e.g. `content/trades-home/my-business.md`:

```markdown
---
title: "Business Name"
date: 2024-01-01
description: "One line description of the business."
tags: ["plumber", "farnham"]
cover:
  image: "/images/business-logo.jpg"
  alt: "Business Name logo"
  relative: false
hidemeta: false
---

**Trade:** Plumbing & Heating  
**Area covered:** Farnham, Alton  
**Phone:** 07700 000000  
**Rating:** ⭐⭐⭐⭐⭐  

[Visit Website](https://example.com) | [Email](mailto:hello@example.com)

---

A short paragraph about the business.
```

### Adding a logo/image

Drop the image into `static/images/` and reference it in the front matter as `/images/filename.jpg`.

---

## Deploying

Push to `main` — GitHub Actions builds and deploys automatically.

```bash
git add .
git commit -m "Add new business listing"
git push
```
