# MUST Student Account Interface

## Project Description

This is a simple two-page front-end web application for Mbarara University of Science and Technology. It demonstrates a student login interface and a create account interface. It is a student learning project, not an official university service.

## Technologies Used

- HTML5 for page structure and form elements.
- CSS3 for colors, spacing, layout, and the blurred background.

No JavaScript, PHP, databases, frameworks, external fonts, or installation tools are used.

## Pages

- `index.html`: the Login page, with Student Number or Email and Password fields.
- `create-account.html`: the Create Account page, with Full Name, Student Number, Email, optional Phone Number, Password, and Confirm Password fields.

## Images

The uploaded official university logo is stored at `images/must-logo.png`. It is centred above the full university name on both pages. CSS sets its width to 120px and uses `height: auto` to keep its proportions.

The Login page uses a single centred white form card. The Create Account page keeps the CSS-only blurred Login background, including the logo. The original gate photograph remains at `images/must-gate.jpg` as an unused asset; neither page displays it.

## How to Run the Project

1. Download or copy the complete `MUST-Login-System` folder.
2. Open that folder.
3. Open `index.html` in a web browser. No server or installation is required.
4. Use **Create Account** below the login form to open the second page.
5. Use **Login** below the registration form, or the close link at its top, to return.

Keep both HTML files, `styles.css`, and the `images` folder together so that the relative paths continue to work. You can edit the files in any plain text editor.

## Project Structure

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

## Limitations

This project is a front-end demonstration built using HTML and CSS only. The Login and Create Account buttons do not connect to a database because no server-side technology is used. They intentionally use `type="button"`, so clicking them does not submit or send any entered details. They do not sign a student in or create an account.

The forms include `required` attributes and suitable input types to demonstrate HTML concepts. Since the buttons do not submit forms, clicking them does not trigger the browser's submission validation. Password matching is not checked. Use sample details when demonstrating the interface.

## Documentation

See [documentation/project-documentation.md](documentation/project-documentation.md) for a beginner-friendly explanation of the HTML, CSS, navigation, accessibility, and limitations.
