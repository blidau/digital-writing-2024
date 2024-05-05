# Week 8

## Images in Twine

### Background Images Using Tags

To set per passage background images in Twine we can use tags on the passage and then use these tags to set the background image where a passage is tagged.

1. Add the intended background image to the images folder like in the [add an image to a Twine passage exercise](week6.md#add-an-image-to-a-passage)
2. Select the passage for the background image
3. Below the passage name select the "+ Tag" button and add a tag called "example-background" (the tag can be called anything so long as there are no spaces)
4. Open "Story"->"Stylesheet" from the menu
5. Add the following styles to show the background image (in this example we expect a background image called `background-example.jpg`)
   ```css
   tw-story[tags~="example-background"] {  /* the tag added in step 2 */
     background-image: url(./images/background-example.jpg);  /* the image added in step 1 */
     background-size: cover;  /* cover the whole element */
     background-repeat: no-repeat;  /* do not repeat the background image */
   }
   ```
