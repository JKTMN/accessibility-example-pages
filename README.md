# Accessibility Testing Demo: WCAG Compliance vs Non-Compliance

This project provides two deliberately contrasted web pages — one fully compliant with WCAG 2.2 Level AA standards, and one intentionally non-compliant — for use in testing and comparing the effectiveness of automated accessibility evaluation tools.

## 🎯 Purpose

The primary goal of this project is to provide **clear, side-by-side examples of accessible and inaccessible web design**. These examples can be used to:

- Evaluate how well automated accessibility tools detect issues
- Understand what accessibility compliance and non-compliance look like in practice
- Educate teams on common accessibility pitfalls and best practices
- Benchmark tools or processes used in accessibility audits

## 🧠 AI-Generated Code with Claude 3.7 Sonnet

All code in this project was generated using **Claude 3.7 Sonnet**, an advanced large language model developed by Anthropic. It was guided using carefully crafted prompts to ensure strict adherence (or intentional non-adherence) to WCAG 2.2 Level AA criteria.

### Prompts Used

Below are the original prompts used to generate both versions of the website:

#### ✅ Accessible Version Prompt
```text
You are an expert web developer with a strong focus on accessibility and inclusive design. Your task is to build a modern, responsive blog-style website that fully conforms to WCAG 2.2 Level AA standards.

Requirements:
Use semantic HTML5 to ensure proper document structure and assistive technology compatibility.

Use CSS (no frameworks like Bootstrap or Tailwind) to style the site with:

High contrast, accessible color choices

Responsive layout (works on mobile, tablet, desktop)

Focus styles for keyboard navigation

Include:

A <header> with a site title and navigation menu

A <main> section with at least one tech-related blog post (you can choose the topic)

Headings structured properly (<h1> to <h3>, etc.)

Descriptive alt text for all images

A <footer> with contact or copyright info

ARIA landmarks and attributes only when necessary (avoid overuse)

Clear link text (no "click here")

Ensure the website passes basic accessibility checks (e.g. keyboard navigable, readable by screen readers)

Avoid using JavaScript unless absolutely necessary

Output the full HTML and CSS in two separate blocks, and include comments in the code to explain any accessibility decisions.
```


#### ❌ Inaccessible Version Prompt
```text
You are a web developer tasked with creating a completely inaccessible blog-style website. Your goal is to ignore all accessibility best practices and build a site that fails to meet WCAG 2.2 standards in every possible way.

Requirements:
Use non-semantic HTML elements as much as possible (e.g., lots of <div>s and <span>s instead of proper tags).

Style the site with poor contrast (e.g., light gray text on a white background), tiny font sizes, and avoid focus outlines.

Make sure the layout is not responsive — fixed widths and pixel-perfect placement that breaks on mobile.

Include:

A <div>-based structure instead of semantic sections like <header>, <main>, <footer>.

Headings that skip levels or use no actual heading tags (e.g., use <b> or <p> styled to look like headings).

Images without alt text or with meaningless alt attributes like alt="image".

Links with vague or non-descriptive text like "Click here" or "More".

No keyboard navigation or focus indicators — hide outlines and avoid tabindex.

Decorative or flashing elements that distract users.

Use ARIA roles incorrectly or redundantly if included at all.

Include inline styles, avoid separation of content and presentation.

Overuse or misuse JavaScript for core functionality (e.g., make links work only with onclick handlers).

Output the full HTML and CSS in two separate blocks. Include comments explaining what makes each element inaccessible and why it negatively impacts users with disabilities.
```


These prompts were designed to clearly distinguish between good and poor accessibility implementations, allowing for precise tool testing and analysis.

## 🌐 Live Preview

View each version directly via GitHub Pages:

- [Accessible Version](https://jktmn.github.io/accessibility-example-pages/accessible.html)
- [Inaccessible Version](https://jktmn.github.io/accessibility-example-pages/inaccessible.html)
- [Landing Page](https://jktmn.github.io/accessibility-example-pages/)

> 🔧 Replace `your-username` and `your-repo-name` with your actual GitHub information.

## 🛠 Tech Stack

- Semantic HTML5 and CSS3
- No frameworks or JavaScript
- Claude 3.7 Sonnet for code generation

## 📎 Notes

- The **inaccessible version** is deliberately flawed and should not be used as a reference for production work.
- This project is ideal for workshops, audits, dev team demos, or evaluating automated tools like Axe, Lighthouse, WAVE, etc.

## 📄 License

MIT — feel free to fork, adapt, or integrate this into accessibility testing pipelines or learning resources.
