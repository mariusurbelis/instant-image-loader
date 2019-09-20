# Instant Image Loader

Solution used to make a website load images perceptually faster by first loading a smaller file into the place of the original. After the original file is loaded it is simply swapped instead of the smaller.

### Purpose
In this day and age servers are powerful and internet connections are fast. However, not everyone has access to these resources. Thus, this solution will help someone with a low-power server like a Raspberry Pi with a slow connection or an image-heavy website.

### Usage
Load the script into the HTML file.
Add this line to the `<head>` of the document: `<script src="imageloader.js"></script>`

After the script is loaded you need to add a class called `lazy` to your image.
This can be achieved by typing: `<img class="lazy">`.

You will have to create two versions of the image. First one will have to be the smaller/more compressed version of the file. And the second one can stay as is (the original file).

The image that is loaded first will go in the `src=""` and the full-size image will go into `data-src=""`.

In full the image code will look something like this:
`<img class="lazy" src="path-to-smaller-image" data-src="path-to-original-image">`
