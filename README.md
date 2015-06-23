Optimize images for use on the web
================================================

The script `optimg.bash` creates a bash-function `optimg` which takes a list of image-files to process for optimizing their size.

Its intended use is to optimize images in a website to improve the rating on services like "Google PageSpeed".



Get Going
------------------------------------------------

Here is a seqence of commands to get going.

```
source optimg.bash
rsync -a orig/ test/
optimg test/*
```

The output should looks something like this, stating what files were processed and a percentage on how much the filesize was reduced.

```
PNG-image:  test/1start.png  .......................................  99.15
JPEG-image: test/bakgrund-topp.jpg  ................................   8.74
JPEG-image: test/footer.jpg  .......................................  76.83
Saved  43  kB.
```



Demonstration
------------------------------------------------

Here is an asciicast of the commands to get going.

[![asciicast](https://asciinema.org/a/22233.png)](https://asciinema.org/a/22233)



Tools used
------------------------------------------------

External tools are used to optimize the images. 

* JPEG uses `jpegtran`.
* PNG uses `optipng` and `pngcrush`.



Credits and equal projects
------------------------------------------------

I was inspired by the Gist made by lgiraudel, [lgiraudel/optimize.sh](https://gist.github.com/lgiraudel/6065155). I just wanted a simpler script.



Revision
------------------------------------------------

v1.0.0 (2015-06-23)

* First release.


```
 .  
..:  Copyright (c) 2015 Mikael Roos, me@mikaelroos.se
```
