# Assignments

Each session ends with homework. Complete them in order. Use the files in `examples/` as a starting point.

---

## Homework 1: On-page SEO (after Session 1)

1. Choose **one main keyword** for each page of your website.
2. Give every page a unique `<title>` (50–60 characters) with the keyword near the start.
3. Write a meta description for every page (150–160 characters).
4. Make sure each page has exactly one `<h1>`, and headings follow in order.
5. Add meaningful `alt` text to every image and rename the image files with hyphens.
6. Replace every "click here" link with descriptive link text.

**Submit:** your updated HTML files, plus a short list of the keyword you chose for each page.

---

## Homework 2: Technical SEO (after Session 2)

1. Add a `robots.txt` file at the root of your site. Make sure it does not block important pages.
2. Create a `sitemap.xml` that lists every public page with full URLs.
3. Add Open Graph tags (`og:title`, `og:description`, `og:image`, `og:url`) to your home page.
4. Run **Lighthouse** on your home page. Write down the SEO and Performance scores.
5. Fix two issues from the Lighthouse report and run the test again.
6. Run **PageSpeed Insights** on one large website and write down its mobile score.

**Submit:** your `robots.txt`, `sitemap.xml`, the two Lighthouse scores before and after, and one sentence about what you changed.

---

## Homework 3: AEO and GEO (after Session 3)

1. Write 3–5 real questions your visitors would ask, with short direct answers.
2. Add those questions as visible headings on a page, with FAQPage JSON-LD schema.
3. Test the page in the **Rich Results Test** and fix any errors.
4. Run the **AI citation test**: ask the same question in ChatGPT, Perplexity and Google. Record which sites were cited and your guess about why.
5. Add an "About" section that shows who wrote the content, and a visible "Last updated" date.

**Submit:** the FAQ page, a screenshot of the Rich Results Test result, and your AI citation test notes.

---

## Final project

Take one small website (a shop, a portfolio, a school or a service business) and apply all three sessions:

| Area | What to deliver |
|------|-----------------|
| On-page SEO | Unique titles, meta descriptions, headings, alt text |
| Technical SEO | `robots.txt`, `sitemap.xml`, Open Graph tags, Lighthouse scores before and after |
| AEO | FAQ section with valid FAQPage schema |
| GEO | About section, updated date, a short `llms.txt` (optional) |

**Write a one-page report** covering:

1. The main keyword and the reason you chose it
2. Your Lighthouse scores before and after
3. Two problems you found and how you fixed them
4. What you would do next to be cited by AI tools

**Grading guide**

| Criteria | Points |
|----------|--------|
| On-page SEO complete on all pages | 20 |
| Technical SEO files and tags in place | 20 |
| Lighthouse improvement with evidence | 15 |
| Valid FAQ schema that passes the Rich Results Test | 20 |
| AI citation test with thoughtful analysis | 15 |
| Final report clarity | 10 |
| **Total** | **100** |
