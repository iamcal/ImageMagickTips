ImageMagickTips
===============

How to actually do common things in IM


Resize an image to 128x128 or less:

    convert IN.png -bordercolor transparent -resize 128x128 png32:OUT.png

Resize an image to 128x128 exactly, adding borders as needed:

    convert IN.png -bordercolor transparent -resize 128x128 -border 50 -gravity center \
        -crop 128x128+0+0 +repage png32:OUT.png
