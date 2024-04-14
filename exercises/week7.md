# Week 7

## Inform 7

1. Go to the [Inform 7 releases page](https://github.com/ganelson/inform/releases) and download a copy of Inform.

### Create an Inform 7 Story

1. Create a repository on [GitHub](https://github.com/) with a `README.md` file
2. Add a new file to the repostitory called `.gitignore` and add the following contents:
   ```
   # mac
   .DS_Store

   # inform
   *Build
   *Index
   *.plist
   *.blurb
   *.rtf
   *.iFiction
   *.skein
   ```
3. Commit the change
4. Clone the repository locally with [GitHub Desktop](https://desktop.github.com/) by selecting "File" -> "Clone Repository" and choosing your repository from the list
5. Open Inform 7 and create a new project and call it `Example`
6. Save the project in your repository directory
7. Add some text to the file leaving the name of the project and your name where Inform adds it. Make sure to include "Release along with an interpreter." on the line between your story title and the story text:
   ```
   "Story title" by Your name

   Release along with an interpreter.

   The Living Room is a room. West is The Kitchen. The Living Room has the description "The room is well lit."

   The Kitchen is a room. The Kitchen has the description "This is where we cook."
   ```
8. Click "Go!" to test
9. Click "Release" to release
10. Commit the change
11. Push to GitHub

### Publish the Inform 7 Story with Netlify

1. Go to [Netlify](https://www.netlify.com/)
2. Select "Add a new site"
3. Select "Import an existing project"
4. Select "GitHub" as your Git provider
5. Select the repository that you created for your Inform story
6. Leave the branch to deploy as `main`
7. For the "Publish directory" make this `Example.materials/Release` if your Inform project is called `Example` otherwise this will need to be `Your project name.materials/Release`
8. Click "Deploy site"

#### Adding a Cat to the Living Room

```
The cat is an animal in the Living Room. The printed name of the cat is "a fluffy cat".

Understand "pet [something]" and "stroke [something]" as petting.

Petting is an action applying to one visible thing.

Carry out petting the cat:
    say "You pet the cat and it purrs contentedly."

Understand "pick up [something]" and "take [something]" as picking up.

Picking up is an action applying to one thing.

Carry out picking up the cat:
    say "You pick up the cat and it meows softly as it settles into your arms.";
    move the cat to the player.
```

## Bitsy

You will be editing your Bitsy story in the Bitsy Game Maker.

### Create a Bitsy Game

1. Open GitHub Desktop and create a new repository for your Bitsy game
2. Go to the [Bitsy Game Maker](https://ledoux.itch.io/bitsy)
3. Select "Run tool"
4. There are a lot of different things that you can do with Bitsy so look at this [Bitsy tutorial](https://www.shimmerwitch.space/bitsyTutorial.html) and make some changes to your Bitsy game
5. Select "download game" depending on your browser set up this will either download the file to where that is configured or give you a choice
   - If given a choice save it as `index.html` in the repository you created in step 1
   - Otherwise, find where it has downloaded to and copy it as an `index.html` into the repository you created
6. Commit the change
7. Push to GitHub

### Publish the Bitsy Game with Netlify

1. Go to [Netlify](https://www.netlify.com/)
2. Select "Add a new site"
3. Select "Import an existing project"
4. Select "GitHub" as your Git provider
5. Select the repository that you created for your Bitsy game
6. Leave the branch to deploy as `main`
7. Click "Deploy site"
