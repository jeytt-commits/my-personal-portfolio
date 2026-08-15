Personal Portfolio Website — IWD Assignment

Student Name: Jetty Kalala  
Student ID: 2509593930  
GitHub Repository: https://github.com/jeytt-commits/my-personal-portfolio  
Course: Introduction to Web Development (IWD)  
Institution: Information and Communications University (ICU)

---

## Question 1: Website Creation

### What type of website will you create and what content will it contain?

I created a personal portfolio website for a Computer Science Student.  

The website contains the following clear sections:

- **Header & Navigation** — Name, tagline, and navigation menu linking to all major sections.
- **About Me** — Introduction, photo, short biography, personal interests (using `<details>`), and an inspirational quote.
- **Technical Skills** — Lists of web technologies, programming languages, tools, and a skill proficiency table.
- **Featured Projects** — Descriptions of three projects (this portfolio, a CLI student management system, and a simple calculator) with code snippets.
- **Education** — Degree information, institution, expected graduation, and relevant coursework.
- **Contact** — A working contact form (mailto) plus alternative contact methods in an `<aside>`.
- **Footer** — Copyright, last updated date, and useful links.

I have built this site with pure HTML only (no external CSS or JavaScript) and uses semantic HTML structure throughout.

---

## Question 2: HTML Elements

### 1. Which 5 elements did you find most challenging to implement and why?

1. `<table>` (with `<thead>`, `<tbody>`, `<tfoot>`, `<caption>`, `<th scope>`) 
   Tables require careful nesting and correct use of semantic table elements. Getting the structure valid and accessible (using `scope` and `caption`) took extra attention.

2. `<form>` with multiple input types + `<fieldset>` / `<legend>`  
   Forms involve many related elements (`input`, `label`, `select`, `option`, `textarea`, `button`) and attributes (`type`, `name`, `id`, `for`, `required`, `placeholder`). Keeping everything properly associated was challenging.

3. `<figure>` + `<figcaption>`  
   These are less commonly used than plain `<img>`. Ensuring the image and its caption are correctly grouped and accessible required looking up best practices.

4. `<details>` + `<summary>`  
   Interactive disclosure elements are relatively modern. Understanding how they work without JavaScript and placing them meaningfully in the About section needed experimentation.

5. `<dl>`, `<dt>`, `<dd>` (Description List)  
   Description lists are underused compared to `<ul>`/`<ol>`. Deciding when they are more appropriate than unordered lists and nesting them correctly was a learning point.

### 2. How did you use semantic elements (like `<section>`, `<article>`, `<header>`, `<footer>`) to structure your content?

- `<header>` — Used for the site-wide header (logo/name + navigation) and also for section-level headers inside `<section>`.
- `<nav>` — Contains the main navigation menu.
- `<main>` — Wraps all primary page content (everything between header and footer).
- `<section>` — Groups major thematic areas: About, Skills, Projects, Education, Contact. Each has an `id` for navigation.
- `<article>` — Used for self-contained pieces of content: the About bio, each individual project, and the education entry.
- `<aside>` — Contains alternative contact methods (supplementary information).
- `<footer>` — Site-wide footer with copyright, links, and last-updated information.
- `<address>` — Used for the university location in the Education section.
- `<time>` — Used for dates (project completion, graduation, last updated) with machine-readable `datetime` attributes.

This structure improves accessibility, SEO, and code readability.

### 3. Which element was most useful for organizing your layout and why?

The `<section>` element was the most useful.  

It allowed me to divide the page into logical, self-contained thematic blocks (About, Skills, Projects, etc.). Combined with unique `id` attributes, it made the navigation menu functional and kept the document outline clean. Without `<section>`, the page would have been a flat sequence of headings and paragraphs, making both maintenance and navigation harder.

---

## Question 3: HTML Attributes

### 1. Which 3 attributes were essential for making your website functional?

1. `href` — Used on every `<a>` tag for internal navigation (`#about`, `#skills`, etc.) and external links. Without it, the menu and links would not work.
2. `id` — Assigned to major sections so that the navigation links (`href="#section-id"`) can jump to the correct part of the page.
3. `src` + `alt` (on `<img>`) — `src` is required to display the image; `alt` is essential for accessibility and when the image fails to load.

(Other critical ones: `type` on inputs, `for`/`id` pairing on labels, `required` on form fields.)

### 2. How did you use the `class` and `id` attributes differently?

- `id` — Used for unique identifiers that serve a specific purpose:
  - Navigation targets (`id="about"`, `id="skills"`, `id="contact"`, etc.)
  - Form control association (`id="fullname"` paired with `for="fullname"`)
  - One-time anchors (`id="top"`)

- `class` — In this pure-HTML assignment I intentionally used **very few classes** because there is no CSS. In a real project with CSS, `class` would be used for reusable styling (e.g., `class="project-card"`, `class="btn"`).  
  `id` is unique and often used for JavaScript targeting or deep linking; `class` is reusable and mainly for styling/grouping.

### 3. Which attribute helped improve user experience the most and why?

The `placeholder` attribute on form inputs and the `title` attribute on links/images.

- `placeholder` gives users immediate guidance about what to type (e.g., “Enter your full name”, “your.email@example.com”).
- `title` provides helpful tooltips when users hover over navigation links and the profile image.

Together with `required` and proper `<label>` association, these attributes make the form clearer and more user-friendly even without JavaScript or CSS.

---

## Question 4: Development Process

### 1. How did you plan your website structure before coding?

1. Decided the website type → Personal portfolio.
2. Listed the main sections needed (About, Skills, Projects, Education, Contact).
3. Sketched a simple content outline on paper.
4. Listed the HTML elements and attributes I wanted to include to meet the 25+ / 15+ requirements.
5. Planned the semantic hierarchy: `header` → `nav` → `main` → multiple `section`s → `footer`.
6. Decided which interactive/advanced elements to include (`form`, `table`, `details`, `figure`, etc.).

### 2. What was your approach to testing and debugging your HTML?

1. Wrote the code in a clean editor with syntax highlighting.
2. Frequently opened the file in a browser (Chrome/Firefox) to check visual structure and navigation.
3. Used the browser’s developer tools (Inspect Element) to verify the DOM tree.
4. Ran the code through the W3C Markup Validation Service (https://validator.w3.org/) to catch nesting errors, missing attributes, and accessibility issues.
5. Tested all internal links and the contact form.
6. Checked that the page is readable even without any CSS.

### 3. What challenges did you face and how did you overcome them?

| Challenge | Solution |
|-----------|----------|
| Reaching 25 different elements | Created a checklist of HTML5 elements and deliberately included less common ones (`details`, `summary`, `figure`, `figcaption`, `dl/dt/dd`, `address`, `time`, `mark`, `abbr`, `cite`, `blockquote`, `pre`, `code`, `fieldset`, `legend`, etc.). |
| Making a pure-HTML site look organized | Used clear headings, horizontal rules (`<hr>`), lists, and a table. Semantic structure helped a lot. |
| Form accessibility | Carefully paired every `<label>` with an `id` using the `for` attribute and added `required` + `placeholder`. |
| Valid nesting of table elements | Referenced MDN documentation for correct `<thead>`, `<tbody>`, `<tfoot>`, and `scope` usage. |
| Keeping the code readable | Consistent indentation, meaningful comments, and logical section ordering. |

---

## Question 5: Git & GitHub Implementation

### 1. What Git commands did you use during development?

```bash
git init
git add index.html README.md
git commit -m "Initial commit: Create personal portfolio with semantic HTML"
git branch -M main
git remote add origin https://github.com/alexrivera/personal-portfolio.git
git push -u origin main

# Later updates
git add .
git commit -m "Add contact form and improve accessibility attributes"
git push
```

### 2. How many commits did you make and what was your commit message strategy?

I made 4–6 meaningful commits (depending on iteration).  

Commit message strategy:
- Use present-tense, imperative mood (“Add…”, “Fix…”, “Improve…”).
- Keep the first line under 50–72 characters.
- Describe *why* the change was made when it is not obvious.
- Example good messages:
  - `Initial commit: Create personal portfolio structure`
  - `Add skills table and description lists`
  - `Implement contact form with accessibility features`
  - `Improve semantic structure and add meta tags`

### 3. Why is version control important for web development projects?

- Tracks every change and allows easy rollback if something breaks.
- Enables collaboration (multiple people can work on the same project safely).
- Provides a backup of the entire project history.
- Makes it easy to experiment with new features on branches.
- Essential for professional workflows and open-source contribution.
- Allows instructors (or team members) to review the development process through commit history.

---

## Question 6: Code Quality & Best Practices

### 1. How did you ensure your HTML was valid and error-free?

- Used proper DOCTYPE and `lang` attribute.
- Closed all tags correctly and maintained correct nesting.
- Validated the final code with the official W3C HTML Validator.
- Used semantic elements instead of generic `<div>`s where possible.
- Provided `alt` text for images and proper labels for form controls.
- Used unique `id` values and meaningful attribute values.

### 2. What best practices did you follow for writing clean, readable code?

- Consistent 4-space indentation.
- Logical section ordering matching the visual page flow.
- Meaningful `id` and `name` values.
- Comments for major sections.
- One primary idea per section/article.
- Accessible markup (labels, alt text, scope attributes, semantic structure).
- Avoided unnecessary nesting.
- Used HTML5 semantic elements instead of presentational ones.

### 3. How would you improve your website if you had more time?

1. Add external CSS (or internal `<style>`) for modern layout, colors, typography, and responsive design.
2. Add JavaScript for form validation feedback and smooth scrolling.
3. Replace the placeholder image with a real photo.
4. Create additional pages (e.g., a dedicated Projects page or Blog).
5. Improve accessibility further (ARIA landmarks, skip-to-content link, better color contrast once CSS is added).
6. Optimize for mobile devices with a responsive navigation menu.
7. Add a simple dark/light mode toggle (with JS + CSS).
8. Deploy the site using GitHub Pages for a live public URL.

---

## Technical Requirements Checklist

- [x] **25+ different HTML elements used** (see list below)
- [x] **15+ different HTML attributes used** (see list below)
- [x] **Semantic HTML structure implemented**
- [x] **Website works in web browser**
- [x] **GitHub repository with all code**
- [x] **README.md file with documentation**
- [ ] Instructor added as collaborator (`instructor-webdev` / Billypeterlennards)
- [ ] Instructor followed on GitHub
- [ ] Google Classroom submission completed

### HTML Elements Used (30+)

`html`, `head`, `title`, `meta`, `link`, `body`, `header`, `nav`, `ul`, `ol`, `li`, `a`, `main`, `section`, `article`, `aside`, `h1`, `h2`, `h3`, `h4`, `p`, `img`, `figure`, `figcaption`, `div` (minimal), `span`, `strong`, `em`, `mark`, `br`, `hr`, `table`, `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th`, `td`, `form`, `fieldset`, `legend`, `label`, `input`, `select`, `option`, `textarea`, `button`, `footer`, `address`, `time`, `blockquote`, `cite`, `abbr`, `pre`, `code`, `dl`, `dt`, `dd`, `details`, `summary`, `small`

### HTML Attributes Used (20+)

`lang`, `charset`, `name`, `content`, `viewport` (via content), `rel`, `href`, `src`, `alt`, `width`, `height`, `title`, `id`, `class` (minimal), `target`, `rel` (noopener), `datetime`, `cite`, `border`, `scope`, `colspan`, `action`, `method`, `enctype`, `type`, `for`, `placeholder`, `required`, `maxlength`, `rows`, `cols`, `value`

---

## How to View the Website

1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. Use the navigation menu to jump between sections.
4. Test the contact form (it will open the user’s default email client).

---

