# Week 6

## Prerequisites
 
Install GitHub Desktop, open it and connect it to your GitHub account. Ideally use Twine locally so you don’t lose any of your work, but you can also use the online version.

### Install

- [GitHub Desktop](https://desktop.github.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Twine](https://twinery.org/)

### Accounts

Make sure you have set up accounts on the following sites.

- [GitHub account](https://github.com/)

## Create and Publish a Twine Story

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

### Deploy Via GitHub Pages

We now use the repository on GitHub to deploy the site with GitHub pages.

1. Go to "Settings" on your repository for your work on GitHub.
2. Click on "Pages" in the sidebar under the section "Code and automation".
3. Under the "Branch" heading on the "GitHub Pages" page change "None" to "main".
4. Leave "/(root)" selected and click "Save".
5. Your project will deploy and a link to your project will be available on the "GitHub pages" page of your repository. You may need to refresh the page for it to appear and it may take a few minutes.

Your Twine story should now be published. Every time you make a change, save over the `index.html`, commit the change and push to GitHub your Twine story will be published though this may take up to 10 minutes before the changes are visible.

## Extend the Twine Story

### Add an Image to a Passage

1. Create a `images` folder/directory in the same folder/directory as the `index.html`.
2. Add the image for your Twine story to that folder/directory.
3. In your Twine story add an image element with a relative reference to your image file. So if your image is called `example.jpg` add the following image element:
   ```html
   <img class="story-image" src="./images/example.jpg" alt="an example" />
   ```

### Change the Story Styles

1. In the top menu of Twine click "Story" to reveal the menu options for your story
2. Select "Stylesheet"
3. Add styles for the story, links and change the font

Example styles:

```css
@import url('https://fonts.googleapis.com/css2?family=Homemade+Apple&display=swap');

tw-story {
  font-family: 'Homemade Apple', cursive;
  color: #FFF;
  background-color: #000;
}

.story-image {
  width: 100%;
}

tw-link, tw-link:link, tw-link:visited, tw-link.visited {
  color: #FFF;
  text-decoration: underline;
}
tw-link:focus, tw-link:hover, tw-link:active, tw-link.visited:hover {
  color: #FFF;
  text-decoration: none;
}
```

### Adding a Linked Image

1. [Add an image to the passage as shown in the week 5 exercise](week5.md#add-an-image-to-a-passage)
   ```html
   <img class="story-image" src="./images/example.jpg" alt="an example" />
   ```
2. Treat the image HTML the same as link text in a Harlowe link. So if the passage you are linking to is called "Another room", in your passage you would have:
   ```html
   [[<img class="story-image" src="./images/example.jpg" alt="an example" />->Another room]]
   ```

### Adding Audio

1. Create an `audio` folder/directory in the same folder/directory as the `index.html`.
2. Add the sound file for your Twine story to that folder/directory.
3. In your Twine story add an audio element with a relative reference to your sound file. So if your sound file is called `example.mp3` add the following audio element:
   ```html
   <audio src="./audio/example.mp3" autoplay loop></audio>
   ```

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