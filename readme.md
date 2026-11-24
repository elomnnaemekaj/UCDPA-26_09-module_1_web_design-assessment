
# JUNE SPORTS WEARS

### PLAY HARD, LOOK SHARP.

A responsive, multi-page sportswear website developed as part of the **UCD Professional Academy – Full Stack Software Development Diploma, Module 1: Web Design Assessment**.

- **GitHub Repository:** [View Source Code](https://github.com/elomnnaemekaj/UCDPA-26_09-module_1_web_design-assessment)
- **GitHub Pages Live Website:** [Visit JUNE SPORTS WEARS](https://elomnnaemekaj.github.io/UCDPA-26_09-module_1_web_design-assessment/index.html)
- **AI Chat:** [View AI-Assisted Development Conversation](https://chatgpt.com/share/6b0221c8-eacc-83ed-912d-9485f6c14237)

## Table of Contents

- [Project Overview](#project-overview)
- [Website Pages](#website-pages)
- [Technologies](#technologies)
- [HTML Structure and Semantic Elements](#html-structure-and-semantic-elements)
- [CSS Organisation and Styling Techniques](#css-organisation-and-styling-techniques)
- [Contact Table and Form](#contact-table-and-form)
- [Responsive Design](#responsive-design)
- [AI-Assisted Development](#ai-assisted-development)
- [Deployment and Version Control](#deployment-and-version-control)
- [Future Improvements](#future-improvements)

## Project Overview

JUNE SPORTS WEARS is a sportswear website concept designed for athletes, sports officials and sports enthusiasts. The website promotes sportswear across different sporting activities, with an inclusive approach to its intended audience.

The design uses a black, green, green-yellow and white colour scheme. Its visual identity is supported by product imagery, icons, a consistent navigation header and a reusable footer.

The website focuses on presenting the brand, providing contact information and offering a basic account interface.

**Slogan:** PLAY HARD, LOOK SHARP.

## Website Pages

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Introduces the brand and displays sportswear categories. |
| About | `pages/about.html` | Presents the brand, its mission, vision and promise. |
| Contact | `pages/contact.html` | Displays contact information, opening hours and a message form. |
| Account | `pages/account.html` | Provides the account login interface. |

## Technologies

- **HTML5:** Defines the structure and content of the website.
- **CSS3:** Controls layout, colours, typography, spacing, backgrounds and responsive behaviour.
- **Bootstrap:** Provides an external framework and reusable styling resources.
- **Bootstrap Icons / SVG:** Used for interface and informational icons.
- **Git and GitHub:** Used for version control and repository management.
- **GitHub Pages:** Used to host the website.

## HTML Structure and Semantic Elements

The project uses HTML5 semantic elements to organise content and improve readability.

| Element | Purpose |
|---|---|
| `<header>` | Contains the brand logo and navigation area. |
| `<nav>` | Groups the main navigation links. |
| `<main>` | Holds the primary content of each page. |
| `<section>` | Separates content into meaningful sections. |
| `<article>` | Groups independent or self-contained content where appropriate. |
| `<aside>` | Holds supporting information. |
| `<footer>` | Contains the website footer and supporting links. |
| `<table>` | Presents structured opening-hours information. |
| `<form>` | Groups the contact form controls. |
| `<fieldset>` and `<legend>` | Group related form controls and identify their purpose. |

Each page includes a document type declaration, language attribute, character encoding and viewport metadata.

## CSS Organisation and Styling Techniques

CSS is separated into external stylesheets to make the project easier to maintain and organise.

```text
assets/
└── css/
    ├── header.css
    ├── style.css
    ├── footer.css
    ├── about.css
    ├── contact.css
    └── account.css
```

The header and footer stylesheets provide shared styling, while the other stylesheets control page-specific layouts.

### 1. Universal Selector and Box Sizing

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

The universal selector (`*`) targets every element. The rule removes default browser margins and padding and applies `border-box` sizing. This makes the declared width and height include padding and borders, helping to control element dimensions.

### 2. Class Selectors

A class selector starts with a full stop (`.`).

```css
.card-item {
    display: flex;
    flex-direction: column;
    align-items: center;
}
```

The `card-item` class can be assigned to multiple HTML elements. This allows the same styling to be reused across several product-category cards.

Classes are useful for reusable styles, such as `.logo`, `.link-item` and `.main-section`.

### 3. ID Selectors

An ID selector starts with a hash (`#`).

```css
#submit {
    background: green;
    color: white;
    border-radius: 10px;
}
```

The `submit` ID identifies a particular element, in this example the contact form's Submit button.

IDs are useful when styling a unique element. An ID should be unique within an HTML document.

### 4. HTML Tag Selectors

A tag selector targets elements by their HTML element name.

```css
header {
    display: flex;
    justify-content: space-between;
}

footer {
    display: flex;
    align-items: center;
}
```

These selectors apply styling to matching HTML tags. They are useful when a general style should apply to all elements of that type.

### 5. Child Combinator

The `>` symbol selects a direct child of an element.

```css
.logo > h1 {
    color: white;
    font-size: 40px;
}
```

This selects an `<h1>` that is an immediate child of an element with the `logo` class. It does not select every heading nested further inside that element.

The child combinator helps target specific parts of a component without affecting unrelated nested elements.

### 6. First-Child Pseudo-Class

The `:first-child` pseudo-class selects an element only when it is the first child of its parent.

```css
.btn-solid:first-child {
    border-radius: 10px 10px 0 0;
}
```

This targets an element with the `btn-solid` class when it is the first child of its parent. It can be used to style the beginning of a group of adjacent controls.

### 7. nth-child() Pseudo-Class

The `:nth-child()` pseudo-class selects an element according to its position among its siblings.

```css
.btn-solid:nth-child(3) {
    border-radius: 0 0 10px 10px;
}
```

This targets an element with the `btn-solid` class when it is the third child of its parent.

Unlike a class selector, `:nth-child()` uses the element's position rather than a manually assigned class name. It is useful when different elements in a group need different styling.

### 8. CSS Custom Properties

```css
:root {
    --brand-green: greenyellow;
    --white: #ffffff;
    --green: green;
    --backround: black;
}
```

Custom properties store reusable values. They are accessed using the `var()` function:

```css
body {
    color: var(--backround);
    background: var(--white);
}
```

This makes it easier to maintain a consistent colour scheme and update repeated values.

### 9. Background Images and Overlays

```css
.main-section {
    background:
        linear-gradient(
            rgba(106, 103, 103, 0.75),
            rgba(147, 134, 134, 0.75)
        ),
        url("../images/09.jpg") no-repeat center center / cover;
}
```

The linear gradient creates a translucent overlay over the background image. The `no-repeat` value prevents the image from repeating, while `cover` scales it to fill the available area.

### 10. Flexbox and Media Queries

Flexbox is used to align and distribute elements within containers.

```css
display: flex;
justify-content: space-between;
align-items: center;
```

Media queries adjust the layout at different screen widths:

```css
@media screen and (max-width: 650px) {
    /* Responsive styles */
}
```

This allows elements to change dimensions, direction and spacing on smaller devices.

## Contact Table and Form

### Opening-Hours Table

The Contact page uses an HTML table to present business opening hours.

The table contains:

- `<thead>` for column headings.
- `<tbody>` for the data rows.
- `<tr>` for each table row.
- `<th>` for heading cells.
- `<td>` for individual data cells.

This is an appropriate use of a table because days and opening times are related tabular information. It allows visitors to identify the relevant opening hours for each day.

### Contact Form

The contact form provides a structured interface for visitors to enter their details and prepare a message.

It includes:

- Text input for the visitor's name.
- Email input for the visitor's email address.
- A select control for the message subject.
- A textarea for the message.
- A Submit button.

The `required` attribute provides basic browser-side validation for required fields, while `type="email"` checks that the email input follows a recognised email format.

The Submit button triggers the browser's form submission process. A working message-delivery feature requires a configured form endpoint or back-end service; the HTML interface alone does not send messages to the website owner.

## Responsive Design

The project uses flexible layouts, percentage-based widths, Flexbox and CSS media queries to adapt page content to different screen sizes.

The navigation, homepage content, contact sections and footer include responsive styling rules.

The intended result is a consistent experience across desktop, tablet and mobile devices.

## AI-Assisted Development

AI tools were used as supplementary learning and development support during the project. The assistance focused on understanding CSS properties, resolving styling questions and exploring implementation approaches. Suggestions were reviewed and incorporated by the developer where appropriate.

The screenshot below provides evidence of an AI-assisted discussion about CSS background image properties, including `background-repeat` and `background-size: cover`.

### AI Chat Screenshot

![Screenshot of AI-assisted CSS discussion](assets/images/ai-css-assistance.png)

**AI conversation:**  
[View the ChatGPT conversation](https://chatgpt.com/share/6b0221c8-eacc-83ed-912d-9485f6c14237)

## Deployment and Version Control

The project is hosted using GitHub Pages.

Git and GitHub were used for version control and project management. Development changes were made in the `dev` branch, allowing updates to be reviewed and refined before being merged into the `main` branch.

The `main` branch serves as the final production version used for deployment. This workflow keeps development changes separate from the production version until they are ready to be integrated.

## Future Improvements

The following features have been identified as possible future enhancements:

- Connecting the contact form to a message-handling service or back-end system.
- Implementing functional account registration and user authentication.
- Adding fully functional shopping-cart and search features.
- Expanding product information and introducing online purchasing functionality.
- Conducting further accessibility, browser compatibility and responsive testing.

These enhancements are acknowledged as opportunities for further development. However, they all fall beyond the scope of the current Module 1 Web Design Assessment.

The project therefore focuses on meeting the requirements and objectives of the assigned front-end website development task.

---

**JUNE SPORTS WEARS — PLAY HARD, LOOK SHARP.**
