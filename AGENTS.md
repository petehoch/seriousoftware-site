# Serious Software Website — Agent Instructions

## Project
This repository is the public website for **Serious Software**.

Local repository: `/Users/petehoch/Dev/seriousoftware-site`  
Public site: `https://seriousoftware.com`

The site is hosted by **GitHub Pages**. GoDaddy is used only for domain registration and DNS; do not use or depend on GoDaddy website-building/hosting tools.

## Purpose
The site initially serves two purposes:
1. A simple, professional public home for Serious Software.
2. The product site, support site, privacy information, and web-based user manual for **FetchBag**.

Design the structure so additional Serious Software products can be added later.

## FetchBag Context
FetchBag is an Apple-platform productivity app being developed for the RevenueCat **Shipaton**, targeting Christopher Lawley's Productivity Challenge.

It brings reusable content together in one focused place:
- Text snippets
- Images
- Files
- Documents

It should be more purpose-built than Notes without becoming a general-purpose file manager.

The core problem is **retrieval, not storage**. Users should be able to retrieve content from whatever context they remember: people, places, dates, purpose, content, usage history, and relationships.

Working tagline:

> **Everything. Relevant. Connected.**

FetchBag should feel professional, fast, polished, native to the Apple ecosystem, and useful to Apple power users. Avoid cute dog/fetch branding.

## Website Goals
The site should feel like the public presence of a small, thoughtful independent Apple software company.

Prioritize:
- Professional, restrained design
- Fast page loads
- Accessibility
- Responsive layout
- Excellent typography
- Clear navigation
- Minimal visual clutter
- Easy maintenance

Explain FetchBag clearly without excessive marketing language. Documentation should help users accomplish tasks quickly.

## Technical Direction
Start deliberately simple:
- Semantic HTML
- CSS
- Minimal vanilla JavaScript only where clearly useful
- GitHub Pages

Do **not** introduce React, Next.js, Vue, a database, CMS, npm build tooling, or another framework unless there is a demonstrated need and the change is discussed first.

Avoid third-party dependencies merely for convenience. The site should work as static files served directly by GitHub Pages.

## Proposed Structure

```text
seriousoftware-site/
├── index.html
├── fetchbag/
│   ├── index.html
│   ├── manual/
│   │   ├── index.html
│   │   ├── getting-started.html
│   │   ├── adding.html
│   │   ├── fetching.html
│   │   └── connections.html
│   └── support/
│       └── index.html
├── privacy/
│   └── index.html
├── assets/
│   ├── css/
│   │   └── site.css
│   └── images/
├── AGENTS.md
└── README.md
```

This is a starting point, not a requirement to create every page immediately. Prefer directory-based `index.html` pages where they produce cleaner URLs.

## Serious Software Home Page
The root site should provide a restrained introduction to Serious Software and its products. FetchBag will initially be the primary product.

Conceptually:

**Serious Software**

**FetchBag**  
*Everything. Relevant. Connected.*

Provide a short explanation and useful destinations such as:
- Learn More
- User Guide
- Support

Do not make Serious Software appear larger or more established than it is. Never invent testimonials, customers, awards, partners, usage statistics, or other claims.

## FetchBag Product Site
Explain FetchBag around the problem it solves: people repeatedly need information they already possess, but retrieving the right thing at the right moment creates friction.

FetchBag stores reusable content and connects it to useful context so it can be fetched again quickly.

Potential product vocabulary:
- Add
- Fetch
- Recently Fetched
- Frequently Fetched
- Relevant Now
- Connections
- Kits

Do not describe speculative features as shipping features. Website copy and documentation must reflect the actual app.

## FetchBag User Guide
The canonical FetchBag manual should be web-based rather than primarily a PDF.

Potential topics:
- Getting Started
- Adding to FetchBag
- Fetching Something
- Working with Text
- Working with Images
- Working with Files and Documents
- People
- Places
- Dates
- Purpose
- Connections
- Relevant Now
- Kits
- Favorites
- Search
- Sharing
- Keyboard Shortcuts
- FAQ

Only document functionality that exists or is explicitly labeled as forthcoming. Significant help topics should eventually have stable URLs suitable for direct links from FetchBag and support responses.

## Support and App Store URLs
Provide stable pages suitable for App Store Connect, likely:

- `https://seriousoftware.com/fetchbag/` — product/marketing
- `https://seriousoftware.com/fetchbag/support/` — support
- `https://seriousoftware.com/privacy/` — privacy

Do not invent privacy claims. The privacy policy must accurately reflect FetchBag's actual data collection, storage, synchronization, analytics, RevenueCat usage, and other services.

## Documentation Workflow
Treat documentation as source-controlled product work.

When FetchBag behavior changes:
1. Determine whether the user guide is affected.
2. Update relevant documentation.
3. Keep terminology synchronized with the app UI.
4. Never describe planned behavior as current behavior.

Add screenshots as the UI stabilizes. Prefer current screenshots over mockups in user documentation.

## Design Direction
Aim for a modern Apple-productivity aesthetic without imitating Apple's website.

Prefer:
- Strong typography
- Generous whitespace
- Clear hierarchy
- Subtle borders/material effects where appropriate
- Excellent readability
- Responsive layouts
- Useful current screenshots
- Minimal chrome

Avoid:
- Heavy animation
- Visual gimmicks
- Stock photography
- Generic SaaS landing-page patterns
- Excessive gradients
- Fake dashboard mockups
- Cute dog imagery based on “Fetch”
- Unnecessary tracking

Accessibility is required. Use semantic elements, sufficient contrast, keyboard-accessible interactions, meaningful alt text, and visible focus states.

## SEO and Performance
Public pages should eventually have useful titles, meaningful meta descriptions, correct heading hierarchy, canonical URLs where appropriate, social-sharing metadata where useful, and appropriate favicon/app imagery.

Keep the site lightweight. Prefer static assets, optimized images, system fonts or carefully justified web fonts, minimal JavaScript, and no unnecessary analytics or trackers.

## Repository Practices
- Preserve Git history.
- Make focused, incremental changes.
- Keep the site deployable throughout development.
- Never commit secrets, credentials, API keys, certificates, or private user information.
- Do not change DNS, GitHub Pages configuration, or deployment architecture unless explicitly requested.
- Avoid third-party dependencies unless strongly justified.
- Explain substantial architectural changes before implementing them.
- Keep generated/build artifacts out of Git unless intentionally required by GitHub Pages.

## Relationship to the FetchBag App
The FetchBag Xcode application is maintained separately at:

`/Users/petehoch/Dev/hackaton2026`

Do not move application source code into this repository. The website may use approved screenshots, icons, descriptions, and documentation derived from the app, but the repositories should remain independently maintainable.

## Current Workflow
- **Xcode + Codex** — FetchBag development
- **VS Code + Codex** — Serious Software website
- **GitHub** — source control
- **GitHub Pages** — website hosting
- **GoDaddy** — domain registration and DNS only

Work with this setup rather than introducing new tooling without a concrete benefit.

## Immediate Task
When beginning work in this repository:
1. Inspect existing files before changing them.
2. Preserve the functioning GitHub Pages deployment.
3. Summarize the existing site structure.
4. Propose the smallest useful next step.
5. Build the Serious Software home page and FetchBag documentation incrementally.
6. Keep the site functional after each meaningful change.

The first goal is not a large website. It is a small, polished, maintainable foundation that can grow alongside FetchBag.
