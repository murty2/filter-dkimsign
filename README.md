INSTALLING on Fedora
--------------------

**NOTE: [libopensmtpd](https://github.com/murty2/libopensmtpd) must be install first.**

\# Make sure these are installed first: make gcc mandoc

sudo dnf install make gcc mandoc

make -f Makefile.gnu

sudo make -f Makefile.gnu install

\# You can remove rpms you installed: sudo dnf erase make gcc mandoc

## How to use the new option -D

filter-dkimsign -d domain.com -D -k keyfile -s selector

Here, domain determined from From: header will be used in DKIM signing. If domain from From: header cannot be determined, then it will fallback to domain.com (the argument of -d)

The benefit of using -D option is that you do not have to specify -d option 100 times, assuming you have 100 domains.

**CAUTION: If you use -D option, first make sure that domain (used in From: header) has DKIM configured for it in DNS properly. Otherwise mail can bounce (unless your domain has proper DMARC configuration and your SPF alignment succeeds)**
