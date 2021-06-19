INSTALLING on Fedora
--------------------

**NOTE: [libopensmtpd](https://github.com/murty2/libopensmtpd) must be install first.**

\# Make sure these are installed first: make gcc mandoc

sudo dnf install make gcc mandoc

make -f Makefile.gnu

sudo make -f Makefile.gnu install

\# You can remove rpms you installed: sudo dnf erase make gcc mandoc
