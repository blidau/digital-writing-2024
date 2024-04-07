# Week 5

## Create a Simple Website

- Download [GitHub Desktop](https://desktop.github.com/)
- Download [Visual Studio Code](https://code.visualstudio.com/)
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
  - Links to your two remix exercises
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

## Writing Hypertext Fiction

- How is it different from fiction?
- How is it different from games?
- How do you plan fiction?
- How could you plan hypertext fiction?

### Create a Short Branching Fiction Story

Write a short branching fiction story. It should be nine short paragraphs in length and each paragraph should link to or be linked from at least two others.

## Create and Publish a Twine Story

### Prerequisites

Install GitHub Desktop, open it and connect it to your GitHub account. Ideally use Twine locally so you don’t lose any of your work, but you can also use the online version.

#### Accounts

Make sure you have set up accounts on the following sites. Use your GitHub account to sign up to Netlify.

- [GitHub account](https://github.com/)
- [Netlify account](https://www.netlify.com/)

#### Install

- [GitHub Desktop](https://desktop.github.com/)
- [Twine](https://twinery.org/)

### Set Up a Local Repository

To save a history of your changes to your story and to allow you to easily publish it online you will need to set up a repository.

1. Create a local folder/directory for all your projects on your computer. Every time you start a new repository you will want to create it in this folder. Call it anything you like but easy to find like `digital-writing-projects`.
2. Go to GitHub Desktop and create a new repository. Give it the name `digital-writing-twine` and for the "Local Path" select the folder you created in the previous step. Select the "Initialize this repository with a README" checkbox and click "Create Repository".

### Create a Twine Story

In Twine you will need to create a story, add a passage and save the commit in GitHub Desktop.

1. Open Twine and select "+ Story". Call the story anything you want.
2. An "Untitled Passage" will be present. Double-click on the passage.
3. Change the title from "Untitled Passage" to another name and edit the passage content. Close the passage.
4. Select "Build" from the menu at the top to show the build options.
5. Select "Publish to File" and navigate to the repository that you created. There should only be a "README.md" in the directory. Save your file as `index.html` (this is very important as when the story is published on Netlify it will make it easier to navigate to).
6. Go to GitHub Desktop and your repository should show changes. Add the comment "Add first passage" where "Summary (required)" is shown and click "Commit to main".

### Add Another Twine Passage

Add one more passage to Twine.

1. Go back to your Twine story and open the first passage by double-clicking on it.
2. Select the text you want to link to the next passage and put two square brackets on either side. So if the text is "You are sitting in a park" and you want the link to be the word "park" the edited text should look like "You are sitting in a [[park]]" and then close the passage.
3. A second passage should now appear. Double-click on the second passage and add text to the passage.
4. Select "Publish to File". Select the `index.html` in your Twine story folder and save over it.
5. Go to GitHub Desktop and your repository should show changes. Add the comment "Add second passage" where "Summary (required)" is shown and click "Commit to main".

### Publish to GitHub

Publish your repository to GitHub.

1. Go to GitHub Desktop and in the top row select "Publish repository".
2. Uncheck "Keep this code private" (this should be public so that it can be part of your folio).
3. Click "Publish Repository".
4. Go to GitHub in your web browser and confirm that the repository is there.

### Deploy Via Netlify

We now use the repository on GitHub to deploy the site with Netlify.

1. Go to Netlify and select "Add new site" and "Import an existing project".
2. Select "GitHub" for your Git provider.
3. Under "Pick a repository" select your repository.
4. Under "Site settings, and deploy!" leave all settings as default and click "Deploy site"

Your Twine story should now be published. Every time you make a change, save over the `index.html`, commit the change and push to GitHub your Twine story will deploy the changes to Netlify.

## Extend the Twine Story

### Add an Image to a Passage

1. Create a `images` folder/directory in the same folder/directory as the `index.html`.
2. Add the image for your Twine story to that folder/directory.
3. In your Twine story add an image element with a relative reference to your image file. So if your image is called `example.jpg` add the following image element:
   ```html
   <img class="story-image" src="./images/example.jpg" alt="an example" />
   ```
