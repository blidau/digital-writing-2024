# Technical Questions

- [How do you add image maps in Twine?](./exercises/week9.md#image-maps)
- How do you make text lines appear over time in Twine?
- How do you make letters appear over time in Twine?
- How do make text appear on click (rather than going to a new passage) in Twine?
- [How do you show background videos in Twine?](#how-do-you-show-background-videos-in-twine)
- [How can you use different fonts on different passages in Twine?](#how-can-you-use-different-fonts-on-different-passages-in-twine)
- How can you style a conversation like it appears on a phone in Twine?
- How can you add dialogue choices in Bitsy?

## How do you show background videos in Twine?

Adding a background video to a Twine passage is similar to adding audio or a foreground image. First, add a `video` directory to your Twine project directory (much like you have for audio and images). Then add the video file to the `video` directory. For instance, if you have a video called `video.mp4` you would add it to the `video` directory. As we are using GitHub the file cannot be larger than 25MB. If it is larger than this you will need to cut or compress the video.

Once you've added the video to your video directory, add the following to the passage in which you want the video to appear (update the filename to the name of your video):

```html
<video autoplay loop muted class="background-video">
  <source src="video.mp4" type="video/mp4">
</video>
```

That will show the video inline with the text. As we want to show the video in the background we need to adjust the styles. Add a tag to the passage called `video`. We will use that tag to change the styles on the passage where we want the video to appear in the background. Then add the following to your Twine Story Stylesheet (Story->Stylesheet):

```css
/* Style the background where the video will appear */
tw-story[tags~="video"] {
  background-color: transparent;
}

/* Style the video element */
.background-video {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%; 
  min-height: 100%;
  z-index: -100; /* Place the video behind everything */
}
```

## How can you use different fonts on different passages in Twine?

First select all the fonts you want to use in your piece from [Google Fonts](https://fonts.google.com/). For each font you click on select "Get font". When you've picked all the fonts you want to use select "Get embed code". From that screen select "@import" and copy the text **between** `<style>` and `</style>` into your Twine Story Stylesheet (Story->Stylesheet).

For instance, if I wanted to use Libre Baskerville, Oswald, and Jacquard 12, I would select each font and when the final font was selected I would click "Get embed code". After selecting "@import", I would copy the following to the top of my Twine Story Stylesheet:

```css
@import url('https://fonts.googleapis.com/css2?family=Jacquard+12&family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Oswald:wght@200..700&display=swap');
```

To apply a different style to specific passages follow the base [instructions for adding background colours to passages using tags](./exercises/week8/#background-images-using-tags). Instead of changing the background image the font is changed. For my example fonts, Libre Baskerville and Jacquard 12 are static fonts and Oswald is a variable font. To apply a static font I can copy the suggested style into the stylesheet for the specific tag. So for Libre Baskerville I would add the following, for the tag `night`:

```css
tw-story[tags~="night"] {
  font-family: "Libre Baskerville", serif;
  font-weight: 400;
  font-style: normal;
}
```

For Oswald, a variable font, I need to replace the `<weight>` with a weight (how bold the font is) that I want to use. The options given for Oswald vary between 200 to 700. To match the weighting I've used for Libre Baskerville, I'll select 400. So for Oswald I would add the following, for the tag `day`:

```css
tw-story[tags~="day"] {
  font-family: "Oswald", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}
```

The fonts then should appear as expected in the Twine passages with the tags `night` and `day`.
