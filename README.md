This is a snapshot of Steve deRosier's Buildroot archive directory. It comes
in handy when trying to build older versions of Buildroot that specify old
download packages that don't exist anymore.

Quick start
-----------

        git clone git@github.com:cal-sierra/br-package-archive.git ~/br-package-archive
        export BR2_DL_DIR="~/br-package-archive"


Details
-------

To use, you can clone this and then set your `BR2_DL_DIR` to the path. Buildroot
will then use packages from this directory, as well as storing any new packages
it downloads here also. You should always use this feature of Buildroot (with
or without this project) to cache projects instead of downloading them all the
time.

Older versions of buildroot will need the `BUILDROOT_DL_DIR` environment
variable instead.

The packages in the archive are not exhaustive and will not find every possible
package that could be enabled in buildroot. It was originally started for the
Laird WB series of SoMs. It should have sufficient packages in it for nearly
every possible WB40, WB45 and WB50 build from original release through GA7.
Additionally it will build for PiiGAB's mb900s, and several forms of Atmel's
Linux4SAM development boards. Other than that, I do not know.

And, there's no guarantee any of this works for you. It works for me. No
warrantee for any purpose. I use these files, Buildroot automatically downloaded
them to my system. Buildroot verified them via it's own internal systems (which
use md5 and sha1 hashes IIRC). I've never manually touched, opened, or changed
these files. But of course you only have my word for that, so you should
validate them on your own and use them at your own risk.
