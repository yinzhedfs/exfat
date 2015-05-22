# Prerequisites #

If there are no binary packages for your OS or you want to get the most recent version, you should compile from source. To do this under GNU/Linux you need to install the following packages:
  * `subversion` (if you wish to get the source from the repository, see below),
  * `scons`,
  * `fuse-devel` (or `libfuse-dev`),
  * `gcc`.

# Getting the Source #

Download tarball with source from the [Downloads](http://code.google.com/p/exfat/downloads/list) section or directly from the repository:
```
svn co http://exfat.googlecode.com/svn/trunk/ exfat-read-only
```

# Compiling #

Change directory and compile:
```
cd exfat-read-only
scons
```
Then install the driver:
```
sudo scons install
```

# Mounting #

Modern GNU/Linux distributions will mount exFAT volumes automatically—util-linux-ng 2.18 (was renamed to util-linux in 2.19) is required for this. Anyway, you can mount manually (you'll need root privileges):
```
sudo mount.exfat-fuse /dev/sdXn /mnt/exfat
```
where `/dev/sdXn` is the volume special file, `/mnt/exfat` is a mountpoint.

# Feedback #

If you have any questions, issues, suggestions, bug reports, patches, etc. please send an e-mail to the [mailing list](mailto:exfat@googlegroups.com) ([archive](http://groups.google.com/group/exfat)). Do not use the comment field at the bottom of this page, it's for commenting this article itself.