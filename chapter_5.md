# Chapter 4 : Images

This chapter will teach how to:
* Include an image in your web pages using HTML
* Pick which image format to use
* Show an iamge at the right size
* Optimize an image for use on the web to make pages load faster

There are companies who sell **stock images**:
* Sells images you pay to use
* All images are subject to copyright
  * Either take/make it yourself
  * or buy it

Websites to buy stock photos from:
* [www.istockphoto.com](www.istockphoto.com)
* [www.gettyimages.com](www.gettyimages.com)
* [www.veer.com](www.veer.com)
* [www.sxc.hu](www.sxc.hu)
* [www.fotolia.com](www.fotolia.com)

It is advised to create a folder for all of the images the site uses `(/images)`
* Subfolders may be added within the `image` folder depending on their purpose

Add images using the `<img>` tag. 
* is an empty element, no closing tag.
* should end with `' /'` 

Attributes include:
* `src`: where to find the image file. 
  * usually a relative URL pointing to an image on own site.
* `alt`: text description of the image in case the image cannot be seen
  * Use `alt` with empty quotes if the image is just for decoration/appearance purposes
* `title`: additional information about the image
  * Most browsers display the content of this attribute in a tooltip when the user hovers over the image.
* `height`: height of the image in pixels
* `width`: width of the image in pixels

```
The size of images is increasingly being specified by CSS rather than HTML
```

Placing images **before** block elements (`<p>`,`<h1>`) is wise
* Else the text will flow around the image (not pretty)
  * May use CSS `float` property for the text to wrap around the image
* If the text flows right up to the edge of an image it may become hard to read
  * May use the CSS `padding` and `margin` property to add a gap between text and images.

**OLD CODE**: Aligning Images horizontally and vertically
* Align attribute is no longer used in HTML5
* But may still be used in older websites
* CSS is used instead nowadays
* left, right, top, middle, bottom

Three rules for creating images:
1. Save images in the right format
  * jpeg, gif, png..
  * Wrong format may be slow to load, look less sharp..
2. Save images at the right size
  * If the image is smaller than the width/height specified, the image may be distorted/stretched.
  * If larger, will take longer to load on the page.
3. Measure images in pixels
  * not in centimeters or inches

Tools to edit/save images:
* Adobe Photoshop
  * Photoshop Elements
* Adobe Fireworks
* Pixelmator
* PaintShop Pro
* Paint.net

Online Editors:
* [www.photoshop.com](www.photoshop.com)
* [www.pixlr.com](www.pixlr.com)
* [www.splashup.com](www.splashup.com)
* [www.ipiccy.com](www.ipiccy.com)

Many different colours in a picture : Use *JPEG*

WHen a picture has an area that is filled with exactly the same colour (flat colour) : Use *GIF*
* Logos, illustrations, and diagrams often use flat colours.

The images used on website should be saved at the same width and height that you want them to appear on the page.
* By reducing/increasing image size, or changing shape (by cropping)
  * Cropping images may cause loss of valuable information if NOT done carefully.
  * Depends on the image
* But increasing image size could result in poor quality (blurry or blocky)

```
Vector Images
- resolution-independent
- commonly created in programs (ex Adobe Illustrator)
- Vector images can be increased in dimensions without affecting the image quality
- currently requires saving bitmap version of vector image to display on website
- SVG (Scalable Vector Graphics) is a new format which can be displayed directly on the web
  without the need to save a bitmap version
```

Animated GIFs naturally has larger size than normal GIF files
* may take longer to load
* excess GIFs is not advised
* should only be used for simple illustrations (ex loading sign)
* can be created using Adobe Photoshop

Transparent GIFs can be used only when the transparent part of the image has straight edges
* Otherwise transparent PNG has to be used
* In older browsers (ex IE6) transparent PNGs are not fully supported
  * can work around this issue using JavaScript
  * the script can be found in the tools section of [the website](www.htmlandcssbook.com/) accompanying this book. 

`<figure>` element (*HTML 5*) can be used to contain images and their caption so that the two are associated.
* Can have more than one images inside the `<figure>` element as long as they all share the same caption.
* Browsers sometimes indent the contents of `<figure>` element.

`<figcaption>` element (*HTML 5*) allows to add caption to an image.
* Before these elements (including `<figure>`) there was no way to associate an `<img>` element with its caption.

Older browsers (does not understand HTML5) simply ignores the new elements and display the content of them.

Therefore looks somewhat like:
```html
<figure>
  <img src="(img src)" alt="(alt text)" />
  <br /> (not always necessary)
  <figcaption> (caption text) </figcaption>
</figure>
```

### Summary
* The `<img>` element is used to add images to a web page
* You must always specify a `src` attribute to describe the content of an image
* You should save images at the size you will be using them on the web page and in the appropriate format
* Photographs are best saved as JPEGs; illustrations or logos that use flat colors are better saved as GIFs.
