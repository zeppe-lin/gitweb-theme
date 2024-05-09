OVERVIEW
========

This directory contains gitweb-theme, an alternative theme for gitweb.

This theme is basically a fork of [kogakure theme][1] with CSS modifications of
[linaro theme][2].

[1]: https://github.com/kogakure/gitweb-theme
[2]: http://git.linaro.org/infrastructure/gitweb-linaro-theme.git

What has changed are colors, fonts, and the logos.  The following files have
been removed: README.markdown, setup.


INSTALL
=======

The installation of this stylesheet is very easy.  Just copy the following
files to the directory where gitweb static files is located (usually
`/usr/share/gitweb`):

```sh
sudo cp -f git-favicon.png git-logo.png gitweb.css /usr/share/gitweb/static/
```

Be aware that this command will overwrite the original files!  So, make sure
you have made a backup.

Also, note that after upgrading git package, these files will be overwritten.
In case of Zeppe-Lin, you can set pkgadd(8) to never upgrade these files.  Edit
`/etc/pkgadd.conf` and add the following lines:

```
UPGRADE  ^usr/share/gitweb/static/git-favicon.png$  NO
UPGRADE  ^usr/share/gitweb/static/git-logo.png$     NO
UPGRADE  ^usr/share/gitweb/static/gitweb.css$       NO
```


LICENSE
=======

Same as the gitweb-theme upstream, MIT license.
See LICENSE file for copyright and license details.
