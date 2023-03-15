custom build of sxiv

![sxiv](http://xyb3rt.github.io/sxiv/img/logo.png "sxiv")

**Simple X Image Viewer**

The sole purpose of sxiv is to be the perfect image viewer for me. It is free
software so that you can use it and modify it for your needs. Please file a bug
report if something does not work as documented or expected. Contributions are
welcome but there is no guarantee that they will be incorporated.


Features
--------

* Basic image operations, e.g. zooming, panning, rotating
* Customizable key and mouse button mappings (in *config.h*)
* Thumbnail mode: grid of selectable previews of all images
* Ability to cache thumbnails for fast re-loading
* Basic support for multi-frame images
* Load all frames from GIF files and play GIF animations
* Display image information in status bar


Screenshots
-----------

**Image mode:**

![Image](http://xyb3rt.github.io/sxiv/img/image.png "Image mode")

**Thumbnail mode:**

![Thumb](http://xyb3rt.github.io/sxiv/img/thumb.png "Thumb mode")


Dependencies
------------

sxiv requires the following software to be installed:

  * Imlib2
  * X11
  * Xft
  * freetype2
  * fontconfig
  * giflib (optional, disabled with `HAVE_GIFLIB=0`)
  * libexif (optional, disabled with `HAVE_LIBEXIF=0`)

Please make sure to install the corresponding development packages in case that
you want to build sxiv on a distribution with separate runtime and development
packages (e.g. *-dev on Debian).


Building
--------

sxiv is built using the commands:

    $ make
    # make install

Please note, that the latter one requires root privileges.
By default, sxiv is installed using the prefix "/usr/local", so the full path
of the executable will be "/usr/local/bin/sxiv".

You can install sxiv into a directory of your choice by changing the second
command to:

    # make PREFIX="/your/dir" install

The build-time specific settings of sxiv can be found in the file *config.h*.
Please check and change them, so that they fit your needs.
If the file *config.h* does not already exist, then you have to create it with
the following command:

    $ make config.h


Usage
-----

Please see the [man page](http://xyb3rt.github.io/sxiv/sxiv.1.html) for
information on how to use sxiv.
