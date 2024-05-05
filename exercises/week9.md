# Week 9

## Images in Twine

### Scaling Images

In-text images can be scaled in different ways.

#### Scaling All Images

If you want to scale all images the same way it is easiest to apply the scaling to the image element.

To scale all images to 100% of the passage width:

1. Open "Story"->"Stylesheet" from the menu
2. Add the following:
   ```css
   img {  /* this selects all image (img) elements */
     width: 100%;
   }
   ```

#### Scaling Images by Class

If you want to scale only certain images or sets of images in different ways it is best to use a class. Classes are more specific than targeting the element which means you can have 100% set for all images and use a class to set another width for other images.

To add a class which scales an image to 50% of the passage width:

1. Open "Story"->"Stylesheet" from the menu
2. Add the following:
   ```css
   .story-image-smaller {  /* this selects all elements with the story-image-smaller class not just images */
     width: 50%;
   }
   ```
   Or
   ```css
   img.story-image-smaller {  /* this selects all images with the story-image-smaller class */
     width: 50%;
   }
   ```
3. Open the passage with the image
4. Add the class to the image. If you have the following image in a passage:
   ```html
   <img src="./images/example.jpg" alt="an example" />
   ```
   When you add the class it will be:
   ```html
   <img class="story-image-smaller" src="./images/example.jpg" alt="an example" />
   ```

#### Scaling Images with Style

If you want to scale all the images in different ways it is probably still better to use classes or ids to select them but you can also directly apply styles to the image element. The style attribute is more specific than targeting the class or element so it will take precedence over those.

To change the width of a specific image to 30% of the passage width:

1. Open the passage with the image
2. Add a style attribute with the style to the image. If you have the following image in a passage:
   ```html
   <img src="./images/example.jpg" alt="an example" />
   ```
   When you add the style it will be:
   ```html
   <img style="width: 30%;" src="./images/example.jpg" alt="an example" />
   ```

### Images with the CSS Grid Layout

A simple way to show images is to use the CSS grid layout.

To use the grid layout to display an image to the right-hand side of the text:

1. Open the passage
2. Add the text "This is example text" and the image:
   ```html
   <img src="./images/example.jpg" alt="an example" />
   ```
3. Add `div` elements with the class (as shown) around the text and image:
   ```html
   <div class="story-room"><div class="story-text">This is example text.</div><div class="story-image"><img src="./images/example.jpg" alt="an example" /></div></div>
   ```
4. Open "Story"->"Stylesheet" from the menu
5. Add the following:
   ```css
   .story-room {
     display: grid;  /* sets the display to grid on the surrounding div */
     grid-template-columns: 50% 50%;  /* sets each column to 50% */
   }
   .story-text {
     grid-column: 1;  /* sets which column the text appears in */
     grid-row: 1;
     box-sizing: border-box;
     padding: 10px;
   }
   .story-image {
     grid-column: 2;  /* sets which column the image appears in */
     grid-row: 1;
   }
   ```

If you want the image to appear on the left and the text on the right, then swap the values for `grid-column`.

### Image Maps

#### Prerequisite

1. Make sure you have your Twine set up with the passages already created or a list of passages. You will use the names of the passages when setting up your image map.
2. Have an image ready for the image map.

#### Creating an Image Map

1. Upload your image to the [Image Map Generator](https://www.image-map.net/)
2. Create an area on the map for each of the passages you want linked. For each area choose the shape you want (if it is irregular then you will want to select "Poly")
3. For each area leave "Link" and "Target" blank and ensure that "Title" has the name of the passage you want linked.
4. Select "Show Me The Code!" and copy the code shown and paste it into the passage with where you want your image.
5. Update the `img` tag on the page and ensure it is pointing to your image.

#### Linking the Image Map

1. Download the latest [`harlowe-macro-api.zip` from Chapel's Unofficial Custom Macro Framework for Harlowe](https://github.com/ChapelR/harlowe-macro-api/releases).
2. Open `macro.js` and copy the contents into your Twine story JavaScript (Story->JavaScript).
3. To the bottom of the passage with your image map add:
   ```html
   <script>
    $('area').on('click', function(e){
	  e.preventDefault();
	  Harlowe.goto(this.alt);
    });
   </script>
   ```

#### Scaling the Image Map

1. Copy the [contents of the Image Map Resizer](https://raw.githubusercontent.com/davidjbradshaw/imagemap-resizer/master/js/imageMapResizer.min.js) to the top of your Twine story JavaScript (Story->JavaScript).
3. Update the script element at the bottom of the passage with your image map to:
   ```html
   <script>
    $('area').on('click', function(e){
	  e.preventDefault();
	  Harlowe.goto(this.alt);
    });
    $('map').imageMapResize();
   </script>
   ```
