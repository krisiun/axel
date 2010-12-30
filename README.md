This file only shows new features added since version 2.4, original README is still available.

## Branch: master

Contains original axel, except for couple modications:

* MAX_REDIR is set to 25, since there are plenty of URLs which will be redirected more than 5 times.
* Length of allowed redirect url increased from 255 to 1000. (Youtube download was not working).

## Branch: unicode-progressbar

Displays awesome progress bar using unicode characters. If your console does not support unicode, don't turn it on.

* New command-line argument `-u` or `--unicode` that switches to unicode output.
* New config file option `unicode_output = 1`
* Detects width of the console/terminal.

## Branch: reactivation

Implements something silimar to [dynamic segmentation](http://www.internetdownloadmanager.com/support/segmentation.html). Finished connections will be reactivated on a different segment of file.

* There are no new config file or argument options.

## Branch: no-clobber

Skip files that are already downloaded (don't clobber from `wget`).

* New command-line argument `-c` or `--no-clobber`.
* New config file option `no_clobber = 1`

## Firefox cookies

It is not a good idea to read cookies from sqlite file, since firefox does not
write **all** cookies to the disk. Instead there is a flashgot extension for
firefox that integrates it with various download managers. **Flashgot 1.2.8** and newer has a better support for axel.
[Forum thread](http://forums.informaction.com/viewtopic.php?f=11&t=5543).

## Branch: content-disposition

Recognize `Content-disposition` in HTTP headers, and save with appropriate filename.

* There are no new config file or argument options.

## Planned branch: https


## Branches: releaseX

These branches are used to merge several features together for testing. I will consider merging only semi-stable features. This branch may not always contain latest version of features (merging is done periodically).

# Extra notes

Testing is done on:

* Ubuntu 10.10 GNU/Linux
* FreeBSD 7.1 (thanks to bagside/bagvapp)
* OpenSolaris 2008.5 SunOS 5.11 (thanks to bagside/bagvapp)
* OpenBSD 3.8 (thanks to [Will Backman](http://cisx1.uma.maine.edu/~wbackman/vmware-images/))
* NetBSD (thanks to [Philip A. Nelson](http://cs.wwu.edu/faculty/phil/classes/vm-ldc.cd/))

Original README, CHANGELOG and license were not modified.

## Contact

Here on github, or email: [emiraga@gmail.com](mailto:emiraga@gmail.com)
