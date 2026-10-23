# SEO, AEO & GEO: Web Visibility for Developers

A hands-on course that teaches how Google, answer engines and AI tools (ChatGPT, Gemini, Perplexity, Google AI Overviews) find, read and cite websites, and how to build pages that get found. Every lesson uses plain HTML, so you can start with what you already know.

**Goal of the course:** when someone searches, *your* website should appear, whether it is a blue link on Google, a direct answer in a snippet, or a source cited by an AI.

---

## What you will learn

- How search engines crawl, index and rank pages
- **On-page SEO:** `<title>`, meta description, headings, `alt` text, clean URLs, links, semantic HTML
- **Technical SEO:** `robots.txt`, `sitemap.xml`, speed, mobile-friendliness, HTTPS, Open Graph previews
- **AEO (Answer Engine Optimization):** writing for featured snippets and "People also ask", FAQ content and FAQ schema (JSON-LD)
- **GEO (Generative Engine Optimization):** structuring and proving content so AI tools can read and cite it, including AI bot rules and `llms.txt`
- Free tools: Lighthouse, PageSpeed Insights, Google Search Console, Bing Webmaster Tools, Rich Results Test, Schema Validator, Open Graph preview

## Who this is for

- Students and beginners who know basic HTML
- Web designers who build sites for clients and want them to rank
- Anyone who wants to be found by both Google and AI assistants

## Prerequisites

- Basic HTML (tags, attributes, links, images)
- A web browser (Chrome recommended, for Lighthouse and DevTools)
- A free Google account (for Search Console)
- Optional: a free GitHub Pages or Netlify account to put a practice site online

---

## Course structure

The course is one module, **SEO, AEO & GEO**, split into three sessions.

| # | Session | Main topics | Hands-on |
|---|---------|-------------|----------|
| 1 | [SEO Basics & On-Page SEO](sessions/01-seo-basics-on-page.md) | How search works, keywords, title, meta, headings, alt text, links | Fix the on-page SEO of your own website |
| 2 | [Technical SEO](sessions/02-technical-seo.md) | `robots.txt`, `sitemap.xml`, speed, mobile, HTTPS, Open Graph, Lighthouse | Run Lighthouse and PageSpeed, add `robots.txt` and `sitemap.xml` |
| 3 | [AEO & GEO](sessions/03-aeo-geo.md) | Answer-friendly content, JSON-LD FAQ schema, AI citations, `llms.txt`, E-E-A-T | Write an FAQ with schema and run the AI citation test |

Each session has:

- Concepts with short explanations
- Copy-paste HTML and config examples
- A checklist you can tick off
- Homework in [`assignments/`](assignments/README.md)

---

## Repository layout

```
seo-aeo-geo-course/
├── README.md                  ← you are here
├── sessions/                  ← lecture notes, one file per session
│   ├── 01-seo-basics-on-page.md
│   ├── 02-technical-seo.md
│   └── 03-aeo-geo.md
├── examples/                  ← working starter files to copy and edit
│   ├── seo-starter/index.html
│   ├── robots.txt
│   ├── sitemap.xml
│   ├── llms.txt
│   └── faq-schema.html
├── assignments/
│   └── README.md              ← homework and the final project brief
└── resources/
    └── references.md          ← official docs, tools and further reading
```

## Quick start

1. Read the sessions in order: `01` → `02` → `03`.
2. Open `examples/seo-starter/index.html` in your browser and compare it with your own page.
3. Do the homework in `assignments/README.md`.
4. Bookmark `resources/references.md` for the tools you will use after the course.

## Learning outcome

By the end of the course you should be able to take any small website and:

- Write a unique title and meta description for each page
- Structure headings and images so search engines and screen readers understand the page
- Add `robots.txt`, `sitemap.xml` and Open Graph tags
- Write answer-first content with an FAQ section and valid FAQ schema
- Measure the result with Lighthouse and Search Console, and check how AI tools cite your site

## Contributing

Corrections, typo fixes and better examples are welcome. Open an issue or a pull request.

## License

Add a license before publishing. MIT is a common choice for course material and code: <https://choosealicense.com/licenses/mit/>
