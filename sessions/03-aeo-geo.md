# Session 3: AEO & GEO

> Module: **SEO, AEO & GEO** · Session 3 of 3
> Last session: technical SEO, robots.txt, sitemap, Open Graph, Lighthouse.
> Today: answer-first content (AEO), FAQ schema, and making your content readable and citable by AI tools (GEO).

---

## Learning objectives

- Write headings and answers that can appear in featured snippets
- Add valid FAQ schema (JSON-LD) to a page
- Explain how GEO differs from SEO and AEO
- Apply the content habits that make AI tools more likely to cite a site
- Run an AI citation test and explain the results

---

## Part A: AEO (Answer Engine Optimization)

Sometimes Google **answers the question directly**, without the user clicking a link:

- **Featured snippet:** the answer box at the top of results
- **People also ask:** a list of related questions
- **Voice assistants:** Google Assistant, Siri, Alexa

### A.1 How to write for answers

1. Use the **question as a heading**.
2. Give a **short, direct answer** (about 40–60 words) right below it.
3. Then explain in more detail.

```html
<h2>What is the best running shoe for beginners?</h2>
<p>The best running shoe for beginners is lightweight, cushioned and
fits comfortably. Look for good heel support and a breathable upper.</p>
<p>...more detail...</p>
```

- Use **lists** and **tables**. Search engines often use them for snippets.
- Add an **FAQ section** to important pages.

### A.2 Schema markup (JSON-LD)

Schema markup is extra code that tells search engines **exactly** what your content is.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Do you deliver all over Pakistan?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, we deliver to all cities in Pakistan within 3–5 days."
      }
    },
    {
      "@type": "Question",
      "name": "Can I return shoes?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, returns are accepted within 7 days."
      }
    }
  ]
}
</script>
```

Other common types: `Organization`, `LocalBusiness`, `Product`, `Article`, `Person`.

**Rules to remember**

- The questions and answers in the schema must also be **visible on the page**. Do not hide them.
- Only mark up content that is real. Made-up FAQs or reviews can lead to penalties.

💡 **Tip:** you can ask an AI assistant to generate FAQPage JSON-LD for your questions. Always test the output in the Rich Results Test (Part D).

A working example is in [`examples/faq-schema.html`](../examples/faq-schema.html).

---

## Part B: GEO (Generative Engine Optimization)

People now also ask **AI tools** instead of Google: ChatGPT, Gemini, Perplexity, Copilot, and Google **AI Overviews / AI Mode**.

AI tools read websites and write an answer, sometimes with **sources (citations)**.

**GEO means making AI tools mention or cite your website.**

### B.1 SEO vs AEO vs GEO

| | SEO | AEO | GEO |
|-|-----|-----|-----|
| Where | Google blue links | Answer box, voice | AI chat answers |
| Goal | Rank high | Be the answer | Be cited or mentioned |
| User | Clicks your link | Reads the answer | Reads the AI's summary |

> Good SEO is the foundation of AEO and GEO. AI tools also use search results.

### B.2 How to make content AI-friendly

1. **Clear structure:** headings, short paragraphs, lists, tables.
2. **Direct answers:** answer the question in the first lines.
3. **Facts and numbers:** stats, prices, dates. AI tools favour specific information.
4. **Show expertise:** author name, experience, an "About Us" page. Google calls this **E-E-A-T**: Experience, Expertise, Authoritativeness, Trust.
5. **Keep content updated:** show a "Last updated" date.
6. **Be mentioned elsewhere:** reviews, social media, directories, forums.
7. **Do not hide text in images:** AI reads text, not pictures.
8. **Do not block AI bots** in `robots.txt` if you want to be cited.

### B.3 AI bots in `robots.txt`

```txt
# Allow OpenAI's bot
User-agent: GPTBot
Allow: /

# Block a bot (example)
User-agent: CCBot
Disallow: /
```

Bot names change over time. Check each AI company's documentation before you write rules for a specific bot.

### B.4 `llms.txt` (proposed idea)

`llms.txt` is a proposed Markdown file at `yoursite.com/llms.txt`. It gives AI tools a short summary of your site.

It is **not an official standard yet**. It is good to know, but not required.

```md
# ShoeHub Karachi
> Online store for running and casual shoes in Pakistan.

## Pages
- [Products](https://yoursite.com/shoes.html): All shoes with prices
- [FAQ](https://yoursite.com/faq.html): Delivery and returns
```

A working example is in [`examples/llms.txt`](../examples/llms.txt).

---

## Part C: Platforms to check AI answers (GEO)

| Platform | What to observe |
|----------|-----------------|
| **ChatGPT** (with search) | Which websites it cites |
| **Perplexity** | Sources, shown clearly with numbers |
| **Google AI Overviews / AI Mode** | The AI summary above Google results |
| **Gemini / Copilot** | How answers differ between AI tools |

---

## Part D: Validate your markup

| Platform | Use | Link |
|----------|-----|------|
| **Rich Results Test** | Test your schema and FAQ markup | search.google.com/test/rich-results |
| **Schema Validator** | Validate any schema code | validator.schema.org |

Run your FAQ page through the Rich Results Test before you publish it.

---

## Part E: Class activities 🎯

**1. FAQ page**
Pick your website topic. Write 3–5 real questions and short answers. Add them to the page as visible content, then add FAQPage schema and test it.

**2. Keyword questions**
Pick your project topic. Use Google autocomplete and "People also ask" to find 5 real questions.

**3. AI citation test**
Ask the **same question** in ChatGPT, Perplexity and Google:

> *"Best place to learn web designing in Karachi"*

Write down:
- Which websites were cited?
- Why do you think they were chosen?
- What is different about their pages (structure, facts, about page, updated date)?

**4. Add to your project**
- FAQ section with FAQPage schema, tested in the Rich Results Test
- An "About" section that shows who wrote the content
- A visible "Last updated" date

---

## Final checklist ✅

**AEO**
- [ ] Question headings with short, direct answers
- [ ] FAQ section with FAQPage schema
- [ ] Lists and tables where they help

**GEO**
- [ ] Clear, structured, factual content
- [ ] About page and author information (trust)
- [ ] Updated content with a visible date
- [ ] AI bots not blocked by accident

**Whole course**
- [ ] Session 1 checklist complete
- [ ] Session 2 checklist complete
- [ ] Session 3 checklist complete

---

> **Remember:** write for **humans first**. If your content is genuinely useful and clearly structured, Google, answer engines and AI tools will all find it easier to use. 🚀

**Previous session:** [Technical SEO](02-technical-seo.md)
