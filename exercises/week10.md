# Week 10

## Create a Simple Website

- Create a folder/directory for your class repositories
- Create a new repository `<username>.github.io` in GitHub Desktop
- Add the base empty files:
  - `index.html`
  - `css/styles.css`
- Add basic `HTML` to the `index.html`:
  ```html
  <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Your name</title>
      <meta name="description" content="Your name">
      <meta name="author" content="Your name">

      <!-- Stylesheet -->
      <link rel="stylesheet" href="./css/styles.css" type="text/css" />
    </head>
    <body>
    </body>
  </html>
  ```
- Update the `index.html` with content such as:
  - Your name
  - Your photo
  - Links to your two your exercises
  - Publications
  - Artist statement
  - Biography
  ```html
  <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Your name</title>
      <meta name="description" content="Your name">
      <meta name="author" content="Your name">

      <!-- Google font -->
      <link rel="preconnect" href="https://fonts.googleapis.com" />
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
      <link href="https://fonts.googleapis.com/css2?family=Palette+Mosaic&display=swap" rel="stylesheet" />

      <!-- Stylesheet -->
      <link rel="stylesheet" href="./css/styles.css" type="text/css" />
    </head>
    <body>
      <h1>Your name</h1>
      <p>
        Something about you.
      </p>
    </body>
  </html>
  ```
- Add styles to the `styles.css`
- Update the `styles.css` with styles such as:
  - Font
  - Background and text colour
  - Layout changes
  ```css
  body {
    color: white;
    background-color: black;
    font-family: 'Palette Mosaic', cursive;  /* an example font that must match the Google font you have imported into your HTML */
  }
  ```

## Folio as a GitHub Pages Website

Follow the instructions on [GitHub Pages](https://pages.github.com/) to publish your folio as a themed website.
