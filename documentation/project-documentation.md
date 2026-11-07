# MUST Student Account Interface: Project Documentation

## 1. Introduction

The MUST Student Account Interface is a simple front-end web application for a university project. It represents account access for students at Mbarara University of Science and Technology. It contains a Login page and a Create Account page, built using HTML and CSS only. It is a learning demonstration rather than an official university service.

## 2. Project Objective

The objective is to demonstrate basic HTML and CSS skills through a university login and account creation interface. The project shows how to organise files, create labelled form fields, add an image, link pages, and make a layout readable on different screen sizes.

## 3. System Users

The main users represented by this interface are students. A student can view both pages and practise entering sample account details. A lecturer can use the code and this documentation to review the student's understanding.

## 4. Pages of the System

### Login Page

`index.html` allows a student to enter a student number or email and a password. The uploaded official university logo is centred above the full university name. The login fields and button use a single centred white form card. A Create Account link opens the registration page.

### Create Account Page

`create-account.html` allows a student to enter personal account information: full name, student number, email, optional phone number, password, and confirm password. It shows the same logo above the full university name, and includes a Create Account button and links back to the Login page.

The registration form appears over a blurred copy of the logo-based Login page. This effect is created with CSS. The registration page is still a separate HTML file, not a JavaScript pop-up. The form stays clear and the page scrolls when necessary. Neither page displays the gate photograph.

## 5. Navigation

The Login page contains `<a href="create-account.html">` to open the Create Account page. The registration page contains links with `href="index.html"` to return to the Login page. The close symbol also returns to `index.html`.

These are relative links. They work because both HTML files are in the same folder. Each page loads the same stylesheet with `<link rel="stylesheet" href="styles.css">`. Each logo uses `src="images/must-logo.png"`.

## 6. HTML Concepts Used

| Concept | How it is used |
| --- | --- |
| Headings | `h1` identifies the university and `h2` introduces page sections. |
| Paragraphs | `p` groups the account navigation links. |
| Forms | `form` groups related account fields. |
| Labels | Each `label` has a `for` value matching its input's `id`. Clicking the label focuses that input. |
| Inputs | `input` provides fields for the student's details. The `name` describes each field. |
| Buttons | `button` displays the Login and Create Account actions. Both use `type="button"` and are demonstration controls. |
| Links | `a` connects the two pages. |
| Images | `img` displays the uploaded official university logo, with descriptive `alt` text. |
| Required attribute | `required` marks compulsory fields. The phone field is optional. |
| Email input type | `type="email"` describes an email address field. A submitting form could use it for a browser email-format check. |
| Password input type | `type="password"` masks characters on screen. Masking does not authenticate or save a password. |
| Telephone input type | `type="tel"` describes a phone number field and may show a telephone keypad on mobile. It does not enforce a particular phone format. |

The `autocomplete` attribute tells a browser what kind of information a field contains. Each page also includes a character encoding, a unique title, and the viewport setting for mobile screens.

## 7. CSS Concepts Used

Both pages share `styles.css`. Comments divide it into sections.

| Concept | How it is used |
| --- | --- |
| Selectors | Element selectors such as `body` and class selectors such as `.login-card` choose which elements to style. |
| Background | A light page background and white form areas separate the main content. |
| Colors | Dark blue headings and text, green buttons and links, and plain light gray card borders give the pages a simple university style. White forms sit on a light gray background. |
| Borders | Simple borders outline inputs and cards. `border-radius` softens corners. |
| Padding | Space inside cards, inputs, and buttons keeps text away from their edges. |
| Margin | Space outside elements separates sections. `margin: 0 auto` centres a limited-width card. |
| Width | `max-width` keeps each centred form card from becoming too wide. The login layout has a single column. |
| Text alignment | `text-align: center` centres the login page's university heading and the navigation links. |
| Simple responsive styling | One `@media (max-width: 760px)` rule reduces spacing on smaller screens. The layout stays in one column. University headings use 30px on larger screens and 24px on smaller screens. |
| Blur effect | `filter: blur(5px)` blurs only `.login-backdrop`. A separate light, partly transparent overlay contains the clear registration card. |

The registration background uses `position: fixed` to stay behind the form. The foreground uses `position: relative` and normal page scrolling. The close link uses `position: absolute` to sit at the top right of its card.

The logo uses `width: 120px` and `height: auto` so it keeps its original proportions. It is centred above the full university name on both pages and also appears in the decorative blurred Login background. `box-sizing: border-box` includes padding and borders in an element's width. Focus outlines make keyboard navigation visible. No animations, Grid layouts, frameworks, or external fonts are used.

## 8. Accessibility

- Both pages declare `<html lang="en">`.
- Every input has a visible label linked to its unique ID.
- Each page has a meaningful, unique title containing Login or Create Account and the full university name.
- The university logos have descriptive alt text.
- Text and form fields use readable fonts, suitable spacing, and contrasting colors.
- Links, inputs, and buttons can be reached with the keyboard and have visible focus outlines.
- The close link has an accessible label explaining where it leads.
- The decorative blurred background has `aria-hidden="true"` and contains no interactive controls. Screen readers can focus on the actual registration form.

## 9. File Structure

```text
MUST-Login-System/
|-- index.html
|-- create-account.html
|-- styles.css
|-- README.md
|-- images/
|   |-- must-logo.png
|   `-- must-gate.jpg (unused original photograph)
`-- documentation/
    `-- project-documentation.md
```

`index.html` is the starting page. `create-account.html` contains registration. `styles.css` styles both pages. `README.md` explains how to run the project. The `images` folder contains the uploaded official logo and the original gate photograph. The gate photograph is retained as an unused asset and is not displayed by either page. The `documentation` folder contains this document.

## 10. Limitations

- No database is used.
- No actual authentication occurs.
- Accounts and entered information are not saved by the application.
- The buttons do not submit forms or send details. They use `type="button"` to keep this demonstration static.
- The `required` and email attributes show HTML concepts, but clicking these buttons does not run submission validation.
- The two password fields are not compared. Checking whether they match would require extra programming.
- HTML and CSS are used for demonstration only. A real account system would need server-side processing and secure data handling.

## 11. Conclusion

This project demonstrates how HTML and CSS can create a clear, connected two-page interface. It provides practice with semantic page structure, labelled forms, images, relative links, shared styles, simple responsive layouts, and a CSS blur effect. It also shows the difference between designing an account interface and building a working authentication system.
