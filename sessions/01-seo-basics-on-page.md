# Session 1: SEO Basics & On-Page SEO

> Module: **SEO, AEO & GEO** · Session 1 of 3
> Today: what SEO is, how search engines work, and on-page SEO using the HTML you already know.

---

## Learning objectives

- Explain the difference between SEO, AEO and GEO
- Describe how a search engine crawls, indexes and ranks a page
- Write a good `<title>` and meta description
- Use headings, `alt` text, clean URLs, links and semantic tags correctly

---

## 1. Three Words, One Goal

| Term | Full form | Goal |
|------|-----------|------|
| **SEO** | Search Engine Optimization | Rank your page in Google's normal results (blue links) |
| **AEO** | Answer Engine Optimization | Get your content shown as a *direct answer* (featured snippet, voice assistant, "People also ask") |
| **GEO** | Generative Engine Optimization | Get your website *mentioned or cited* by AI tools such as ChatGPT, Gemini, Perplexity and Google AI Overviews |

**Goal of all three:** when someone searches, *your* website should appear.

This course covers them in order:

- Session 1: SEO basics and on-page SEO (today)
- Session 2: technical SEO and tools
- Session 3: AEO and GEO

---

## 2. How a Search Engine Works

```
1. CRAWL   →   2. INDEX   →   3. RANK
(read)         (save)         (sort)
```

1. **Crawling:** Google's robot (**Googlebot**) visits pages and follows links.
2. **Indexing:** Google saves the page in its large database (the *index*).
3. **Ranking:** when someone searches, Google sorts the saved pages and shows the best ones first.

> If your page is not **crawled** and **indexed**, it can never **rank**.

---

## 3. Types of SEO

| Type | Where | Examples |
|------|-------|----------|
| **On-page SEO** | Inside your HTML and content | title, meta description, headings, alt text |
| **Technical SEO** | Website setup | speed, mobile-friendly, sitemap, robots.txt, HTTPS |
| **Off-page SEO** | Outside your website | backlinks, Google Business Profile, social media |

Today we focus on **on-page SEO**, because it is just HTML.

---

## 4. Keywords

A **keyword** is what people type into Google.

| Short keyword | Long-tail keyword |
|---------------|-------------------|
| `shoes` | `black running shoes for men in Karachi` |
| Very hard to rank | Easier to rank, more specific visitors |

**Tip:** pick **one main keyword per page** and use it naturally in the title, heading and text. Do not repeat it again and again. That is called *keyword stuffing*, and Google does not reward it.

---

## 5. On-Page SEO with HTML

### 5.1 `<title>`: the most important tag

```html
<title>Black Running Shoes for Men | ShoeHub Karachi</title>
```

- It is the blue clickable line in Google results.
- Keep it around **50–60 characters**.
- Put the main keyword near the start.
- Every page needs a **different** title.

### 5.2 Meta description

```html
<meta name="description" content="Buy comfortable black running shoes for men in Karachi. Free delivery, easy returns. Shop now at ShoeHub.">
```

- It is the grey text under the title in Google results.
- Aim for around **150–160 characters**.
- Write it like a short advertisement.

### 5.3 Language and viewport

```html
<html lang="en">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- `lang` tells search engines and screen readers the page language.
- `viewport` makes the page mobile-friendly. Google checks the **mobile** version first.

### 5.4 Headings: proper order

```html
<h1>Black Running Shoes for Men</h1>   <!-- only ONE h1 per page -->
  <h2>Why Choose Our Shoes</h2>
    <h3>Lightweight Design</h3>
  <h2>Customer Reviews</h2>
```

- Use only **one `<h1>`** per page.
- Do not skip levels just to change font size. Use CSS for size.

### 5.5 Images and `alt` text

```html
<!-- ❌ Bad -->
<img src="IMG_2034.jpg">

<!-- ✅ Good -->
<img src="black-running-shoes.jpg" alt="Black running shoes for men, side view">
```

- Google cannot "see" images. It reads `alt`.
- Use meaningful file names with hyphens.

### 5.6 Clean URLs

| ❌ Bad | ✅ Good |
|--------|---------|
| `site.com/page?id=123` | `site.com/running-shoes` |
| `site.com/Product_Page_FINAL2.html` | `site.com/contact.html` |

- Use lowercase letters and hyphens (`-`). Keep URLs short and readable.

### 5.7 Links

```html
<!-- ❌ Bad -->
<a href="about.html">Click here</a>

<!-- ✅ Good -->
<a href="about.html">Read about our company</a>
```

- Link text should explain where the link goes.
- Link your own pages to each other. This is **internal linking**.

### 5.8 Semantic HTML

```html
<header> <nav> <main> <article> <section> <footer>
```

Instead of only `<div>`, these tags help search engines understand the page structure.

---

## 6. Complete example: SEO-friendly `<head>`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Black Running Shoes for Men | ShoeHub Karachi</title>
  <meta name="description" content="Buy comfortable black running shoes for men in Karachi. Free delivery, easy returns. Shop now at ShoeHub.">
</head>
<body>
  <header>
    <nav>
      <a href="index.html">Home</a>
      <a href="shoes.html">All Shoes</a>
      <a href="contact.html">Contact Us</a>
    </nav>
  </header>

  <main>
    <h1>Black Running Shoes for Men</h1>
    <img src="black-running-shoes.jpg" alt="Black running shoes for men, side view">
    <p>Our black running shoes are lightweight and comfortable for daily running.</p>

    <h2>Why Choose Our Shoes</h2>
    <p>...</p>
  </main>

  <footer>
    <p>&copy; 2026 ShoeHub Karachi</p>
  </footer>
</body>
</html>
```

A full working version is in [`examples/seo-starter/index.html`](../examples/seo-starter/index.html).

---

## 7. See it yourself (live demo)

1. Search anything on Google and look at the **title** and **description** of each result.
2. Open any website, right-click and choose **View Page Source**. Find `<title>` and `<meta name="description">`.
3. Search `site:wikipedia.org` to see pages Google has indexed from that site.

---

## 8. On-page SEO checklist ✅

- [ ] Unique `<title>` (50–60 characters) with the main keyword
- [ ] Meta description (150–160 characters)
- [ ] `lang` and `viewport` added
- [ ] Only one `<h1>`, headings in order
- [ ] Every `<img>` has a meaningful `alt`
- [ ] Clean file names and URLs
- [ ] Descriptive link text (no "click here")
- [ ] Semantic tags used

---

## 9. Class activity / homework

Take your **website assignment** and fix it with the checklist above:

1. Choose one main keyword for each page.
2. Add a proper title and meta description to every page.
3. Fix headings so each page has one `<h1>`.
4. Add `alt` text to all images and rename the image files.
5. Replace any "click here" links.

**Bonus:** ask an AI assistant:

> *"Write an SEO title (under 60 characters) and meta description (under 160 characters) for a page about [your topic]."*

Then check it yourself. Is it accurate? Is the length correct?

---

**Next session:** [Technical SEO](02-technical-seo.md)
