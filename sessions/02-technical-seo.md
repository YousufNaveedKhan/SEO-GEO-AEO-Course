# Session 2: Technical SEO

> Module: **SEO, AEO & GEO** · Session 2 of 3
> Last session: on-page SEO (title, meta, headings, alt).
> Today: make your site easy for search engines to read, fast, and safe, then measure it with free tools.

---

## Learning objectives

- Write a `robots.txt` file and avoid blocking your whole site by mistake
- Create a `sitemap.xml` and submit it to Google
- Explain why speed, mobile-friendliness and HTTPS matter
- Add Open Graph tags so shared links look right on WhatsApp and Facebook
- Run Lighthouse and PageSpeed Insights and fix two issues

---

## 1. `robots.txt`: rules for robots

A small text file in the root folder of your site: `yoursite.com/robots.txt`

```txt
User-agent: *
Allow: /
Disallow: /admin/

Sitemap: https://yoursite.com/sitemap.xml
```

- `User-agent: *` applies the rules to all robots.
- `Disallow` tells robots not to crawl that folder.
- ⚠️ `Disallow: /` blocks your **whole website**. Be careful.

👉 Check any site: `google.com/robots.txt`, `daraz.pk/robots.txt`

A working example is in [`examples/robots.txt`](../examples/robots.txt).

---

## 2. `sitemap.xml`: map of your website

A sitemap tells Google which pages exist.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yoursite.com/</loc>
  </url>
  <url>
    <loc>https://yoursite.com/about.html</loc>
  </url>
  <url>
    <loc>https://yoursite.com/contact.html</loc>
  </url>
</urlset>
```

- Every `<loc>` must be a full URL with `https://`.
- After your site is online, submit the sitemap in **Google Search Console** (Session 2, section 6).

A working example is in [`examples/sitemap.xml`](../examples/sitemap.xml).

---

## 3. Speed, mobile and HTTPS

| Factor | Why it matters | Quick fix |
|--------|----------------|-----------|
| **Speed** | Slow sites lose visitors | Compress images, use `.webp`, add `loading="lazy"` |
| **Mobile-friendly** | Google checks the mobile version first | `viewport` meta tag and Bootstrap or responsive CSS |
| **HTTPS** | Secure sites are trusted | SSL certificate (free on most hosting) |

```html
<img src="shoes.webp" alt="Black running shoes" loading="lazy">
```

---

## 4. Open Graph: link preview on WhatsApp and Facebook

```html
<meta property="og:title" content="ShoeHub Karachi – Running Shoes">
<meta property="og:description" content="Comfortable running shoes with free delivery.">
<meta property="og:image" content="https://yoursite.com/images/preview.jpg">
<meta property="og:url" content="https://yoursite.com/">
```

Without these tags, a shared link may show no image, or a random one.

---

## 5. Off-page SEO (quick idea)

- **Backlinks:** other websites linking to yours. Quality matters more than quantity.
- **Google Business Profile:** important for local shops and "near me" searches.
- **Social media profiles:** link them to your website.

---

## 6. Tools for this session

### Check your website

| Platform | Use | Link |
|----------|-----|------|
| **Lighthouse** (Chrome DevTools) | SEO, speed and accessibility scores | F12 → Lighthouse tab → Analyze |
| **PageSpeed Insights** | Speed and mobile score of a live site | pagespeed.web.dev |
| **Google Search Console** | Check indexing, submit your sitemap, see search clicks | search.google.com/search-console |
| **Bing Webmaster Tools** | The same for Bing | bing.com/webmasters |
| **Open Graph preview** | See the link preview before sharing | opengraph.xyz |

### Keyword research

| Platform | Use | Link |
|----------|-----|------|
| **Google Search** | Autocomplete, "People also ask", "Related searches" | google.com |
| **Google Trends** | Compare what is popular (set the country to Pakistan) | trends.google.com |
| **AnswerThePublic** | Questions people ask about a topic | answerthepublic.com |
| **Ubersuggest** | Keyword ideas and volume (limited free use) | neilpatel.com/ubersuggest |
| **Google Keyword Planner** | Keyword volume (needs a Google Ads account) | ads.google.com |

### Free hosting (to test on a live URL)

- **GitHub Pages:** pages.github.com
- **Netlify:** netlify.com (drag and drop a folder)

Tool names, links and features change over time. If a link has moved, search for the tool name.

---

## 7. Lab: Lighthouse and PageSpeed

**Step 1: Lighthouse on your own site**

1. Open your website.
2. Press F12, go to the **Lighthouse** tab, and click **Analyze**.
3. Note the **SEO** and **Performance** scores.
4. Fix two issues from the report.
5. Run the test again and compare the scores.

**Step 2: PageSpeed on a big site**

1. Open pagespeed.web.dev.
2. Test `daraz.pk` or any large website.
3. Write down the mobile score and the top suggestion.

**Step 3: Read the source of a big site**

1. Open `view-source:` followed by the address of any large website.
2. Find `<title>`, the meta description, `og:` tags and `application/ld+json`.

---

## 8. Session 2 checklist ✅

- [ ] `robots.txt` exists at the root and does not block important pages
- [ ] `sitemap.xml` exists and lists every public page with full URLs
- [ ] Site is mobile-friendly (viewport tag, responsive layout)
- [ ] Images are compressed and use `loading="lazy"`
- [ ] Site loads over HTTPS
- [ ] Open Graph tags added (title, description, image, url)
- [ ] Lighthouse SEO and Performance checked, two issues fixed

---

**Previous session:** [SEO Basics & On-Page SEO](01-seo-basics-on-page.md)
**Next session:** [AEO & GEO](03-aeo-geo.md)
