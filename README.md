=============
packages-keep
=============

Maintain apt's manually-installed status by keeping a separate
configuration file /etc/apt/packages.keep.

This tries to address the following problems in `apt-get autoremove`:

- Using apt-get marks packages manually installed. However, often you
  install several packages and figure out soon that it doesn't do what
  you want. How do you remember which packages you played with?

- State information is kept in `/var/lib/apt/extended_states`, which
  is not completely human-friendly.

For this reason it is useful to keep the 'is this package wanted'
information in a separate file which is updated only manually. There
are also other similar tools such as `debfoster`, but it is cleaner to
use the feature built in apt.
