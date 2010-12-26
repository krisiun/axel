New functionality is implemented in different branches.

## Branch: master

Contains original axel, except for couple modications:

* MAX_REDIR is set to 25, since there are plenty of URLs which will be redirected more than 5 times.
* Length of allowed redirect url increased from 255 to 1000. (Youtube download was not working).

## Branch: unicode-progressbar

Displays awesome progress bar using unicode characters. If your console does not support unicode, don't turn it on.

* New command-line argument `-u` or `--unicode` that switches to unicode output.
* New config file option `unicode_output = 1`

## Branch: reactivation

Implements something silimar to [dynamic segmentation](http://www.internetdownloadmanager.com/support/segmentation.html). Finished connections will be reactivated on a different segment of file.

* There are no new config file or argument options.

## Branch: no-clobber

Skip files that are already downloaded (don't clobber from `wget`).

* New command-line argument `-c` or `--no-clobber`.
* New config file option `no_clobber = 1`

## Firefox cookies

It is not a good idea to read cookies from sqlite file, since firefox does not write all cookies to the disk. Instead there is a flashgot extension for firefox that integrates it with various download managers. I plan to modify flashgot to include better support for axel.

* [http://github.com/emiraga/flashgot](http://github.com/emiraga/flashgot)

## Branch: content-disposition

Recognize `Content-disposition` in HTTP headers, and save with appropriate filename.

* There are no new config file or argument options.

## Planned branch: multi-url-arguments

Give multiple files (not mirrors) on command line.

## Planned branch: https

Not sure about this one.

## Branches: releaseX

These branches are used to merge several features together. I will consider merging only semi-stable features.

# Extra notes

I test my code only using HTTP connections on linux. Sorry, for potential incompatibilities, all fixes are welcome.

Original README and CHANGELOG were not modified.

Also, license from axel is unchanged.

## Contact

Here on github, or email: [emiraga@gmail.com](mailto:emiraga@gmail.com)
