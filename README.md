## Accessibility Testing Demo: WCAG Compliance vs Non-Compliance

This project provides three deliberately contrasted web pages — one fully compliant with WCAG 2.2 Level AA standards, one intentionally non-compliant, and one that is "almost-accessible" adhering to WCAG 2.2 Level A — for use in testing and comparing the effectiveness of automated accessibility evaluation tools.

Each page was generated with **purposeful accessibility honeypots** — elements designed to test whether automated tools can correctly identify both violations and compliant structures. These traps include subtle or edge-case accessibility issues that often go undetected, making them ideal for benchmarking tools.

## 🎯 Purpose

The primary goal of this project is to provide **clear, side-by-side examples of accessible, almost-accessible, and inaccessible web design**. These examples can be used to:

- Evaluate how well automated accessibility tools detect issues
- Understand what accessibility compliance and non-compliance look like in practice
- Educate teams on common accessibility pitfalls and best practices
- Benchmark tools or processes used in accessibility audits

## 🧠 AI-Generated Code with Claude 3.7 Sonnet

All code in this project was generated using **Claude 3.7 Sonnet**, an advanced large language model developed by Anthropic. It was guided using carefully crafted prompts to ensure strict adherence (or intentional non-adherence) to WCAG 2.2 Level AA criteria.


### Prompts Used

Below are the original prompts used to generate all three versions of the website:

#### ✅ Accessible Version Prompt
```text
You are an expert web developer with a strong focus on accessibility and inclusive design. Your task is to build a modern, responsive blog-style website that mostly conforms to WCAG 2.2 Level AA standards. However, I would like you to include 10 honey pot components which are inaccessible. You should place a comment within the code where the violation/issue is, you should also list the errors after generating the code.
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
Output the full HTML and CSS in two separate blocks, and include comments in the code to explain any accessibility decisions. When using images ensure you use this link for src https://picsum.photos/200/300?random=1 incrementing the number after random=1 for each consequent picture.
```

#### ⚖️ Almost-Accessible Version Prompt
```text
You are an expert web developer with a strong focus on accessibility and inclusive design. Your task is to build a modern, responsive blog-style website that mostly conforms to WCAG 2.2 Level A standards. However, I would like you to include 20 honey pot components which are inaccessible. You should place a comment within the code where the violation/issue is, you should also list the errors after generating the code.
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
Output the full HTML and CSS in two separate blocks, and include comments in the code to explain any accessibility decisions. When using images ensure you use this link for src https://picsum.photos/200/300?random=1 incrementing the number after random=1 for each consequent picture.
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
These prompts were designed to clearly distinguish between good, almost-compliant, and poor accessibility implementations, allowing for precise tool testing and analysis.

---

### 🌐 Live Preview
View each version directly via GitHub Pages:

[Accessible Version](https://jktmn.github.io/accessibility-example-pages/accessible.html)
<details>
<summary>❌ 10 Deliberate Accessibility Violations</summary>

- **Missing hamburger menu button label**  
  The mobile menu toggle button has no text or `aria-label`, making it inaccessible to screen reader users who won't know its purpose.

- **Missing nav landmark role**  
  While HTML5 semantic elements like `<nav>` are automatically recognized by modern screen readers, some older assistive technologies might benefit from an explicit `role="navigation"`.

- **Poor link text**  
  Using "Click here" as link text violates WCAG 2.4.4 (Link Purpose) as it provides no context about where the link goes.

- **Missing alt text**  
  An image without alt text violates WCAG 1.1.1 (Non-text Content), making the content inaccessible to screen reader users.

- **Skipping heading levels**  
  Going from `<h2>` directly to `<h5>` violates WCAG 1.3.1 (Info and Relationships) by breaking the document's logical heading structure.

- **Non-descriptive button**  
  The "Submit" button lacks context about what will be submitted, violating WCAG 2.4.6 (Headings and Labels).

- **Using color alone to convey information**  
  The "New" tag on an article card uses only color to differentiate it, violating WCAG 1.4.1 (Use of Color).

- **Form with missing labels**  
  The newsletter form inputs lack proper associated labels, violating WCAG 3.3.2 (Labels or Instructions).

- **Low contrast text**  
  The events widget uses low-contrast text (gray on light gray), violating WCAG 1.4.3 (Contrast Minimum).

- **Icon-only links without accessible names**  
  Social media links in the footer use icons without text or `aria-label`s, violating WCAG 2.4.4 (Link Purpose).

</details>

[Inaccessible Version](https://jktmn.github.io/accessibility-example-pages/inaccessible.html)

[Almost-Accessible Version](https://jktmn.github.io/accessibility-example-pages/almost-accessible.html)
<details>
<summary>❌ 20 Deliberate Accessibility Violations</summary>

1. **Missing alt text**  
   The logo image in the header has no `alt` attribute.

2. **No skip navigation link**  
   Missing "Skip to main content" link for keyboard users.

3. **Navigation not marked as landmark**  
   Used `<div>` instead of `<nav>` for main navigation.

4. **Non-descriptive link text**  
   The "Click here" link in the navigation doesn't describe its purpose.

5. **Color alone used to convey information**  
   Status indicator uses only color to show status.

6. **Skipping heading level**  
   Jumps from `<h1>` to `<h3>`, breaking the heading hierarchy.

7. **Empty alt text that shouldn't be empty**  
   Featured image has empty `alt` text when it should be descriptive.

8. **Using div instead of semantic elements**  
   Quote uses a `<div>` instead of a `<blockquote>`.

9. **Table without headers**  
   Comparison table lacks `<th>` elements and proper structure.

10. **Button not keyboard accessible**  
    Share button uses a `<div>` with `onclick` instead of a proper `<button>` element.

11. **Form controls without labels**  
    Email input lacks an associated `<label>` element.

12. **Low contrast text**  
    Sidebar "Latest Updates" section uses light gray text on a white background.

13. **Poor alt text**  
    Image has a generic `"image"` alt text that isn't descriptive.

14. **Non-keyboard accessible custom controls**  
    Tag cloud uses non-interactive `<span>` elements.

15. **Autoplaying content without controls**  
    Video autoplays with no controls to stop or pause it.

16. **Using ARIA incorrectly**  
    Uses `aria-labeledby` instead of the correct `aria-labelledby`.

17. **Decorative image not marked as such**  
    Security image has descriptive alt text, but it's purely decorative and should be marked with `alt=""`.

18. **Hidden content that screen readers can't access**  
    Article is hidden with `display: none`, making it inaccessible to all.

19. **Insufficient focus indicator**  
    Footer navigation links have no visible focus styles.

20. **Icon links without accessible names**  
    Social media icons lack text alternatives or `aria-labels`.

</details>

[Landing Page](https://jktmn.github.io/accessibility-example-pages/)

---
### 🛠 Tech Stack
- Semantic HTML5 and CSS3
-No frameworks or JavaScript
-Claude 3.7 Sonnet for code generation

---
### 📎 Notes
- The inaccessible version is deliberately flawed and should not be used as a reference for production work.
- The almost-accessible version is a partially-compliant example that can be used for understanding the gap between basic accessibility and full compliance.
- This project is ideal for workshops, audits, dev team demos, or evaluating automated tools like Axe, Lighthouse, WAVE, etc.

---
### 📄 License
MIT — feel free to fork, adapt, or integrate this into accessibility testing pipelines or learning resources.
