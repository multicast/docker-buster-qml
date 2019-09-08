# buster-qml

![Pulls](https://img.shields.io/docker/pulls/mkovac/buster-qml.svg)
![Stars](https://img.shields.io/docker/stars/mkovac/buster-qml.svg)

This is my [Qt5 QML](https://doc.qt.io/qt-5/qtqml-index.html) development
environment. Based on
[Debian](https://debian.org/) [Buster](https://wiki.debian.org/DebianBuster)
[container image](https://hub.docker.com/r/mkovac/buster), adding 
common development tools and [QtCreator IDE](https://doc.qt.io/qtcreator/).

## Usage

I prefer to run container and a `bash` shell and keep this in background,
then run `QtCreator` in other terminal. The following commands include
necessary environment variables and switches for painless usage:

    $ docker run --rm -ti --name qtcreator \
        --device /dev/dri:/dev/dri \
        --volume /tmp/.X11-unix:/tmp/.X11-unix \
        --env DISPLAY=$DISPLAY \
        --env http_proxy=http://proxy:3128 \
        --env https_proxy=http://proxy:3128 \
        --env QT_SELECT=qt5 \
        --volume $HOME/qml:/home/developer/qml:Z \
        mkovac/buster-qml \
        bash
    $ docker exec -ti qtcreator su - developer -c qtcreator

## Notes

If you like the image, star it. Send comments or package suggestions to
include in daily build as [github issue or pull
request](https://github.com/multicast/docker-buster-qml).

# Packages

    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name                                    Version                      Architecture Description
    +++-=======================================-============================-============-===============================================================================
    ii  adduser                                 3.118                        all          add and remove users and groups
    ii  adwaita-icon-theme                      3.30.1-1                     all          default icon theme of GNOME
    ii  apt                                     1.8.2                        amd64        commandline package manager
    ii  apt-utils                               1.8.2                        amd64        package management related utility programs
    ii  at-spi2-core                            2.30.0-7                     amd64        Assistive Technology Service Provider Interface (dbus core)
    ii  avahi-daemon                            0.7-4+b1                     amd64        Avahi mDNS/DNS-SD daemon
    ii  base-files                              10.3+deb10u1                 amd64        Debian base system miscellaneous files
    ii  base-passwd                             3.5.46                       amd64        Debian base system master password and group files
    ii  bash                                    5.0-4                        amd64        GNU Bourne Again SHell
    ii  bind9-host                              1:9.11.5.P4+dfsg-5.1         amd64        DNS lookup utility (deprecated)
    ii  binfmt-support                          2.2.0-2                      amd64        Support for extra binary formats
    ii  binutils                                2.31.1-16                    amd64        GNU assembler, linker and binary utilities
    ii  binutils-common:amd64                   2.31.1-16                    amd64        Common files for the GNU assembler, linker and binary utilities
    ii  binutils-x86-64-linux-gnu               2.31.1-16                    amd64        GNU binary utilities, for x86-64-linux-gnu target
    ii  bsdutils                                1:2.33.1-0.1                 amd64        basic utilities from 4.4BSD-Lite
    ii  build-essential                         12.6                         amd64        Informational list of build-essential packages
    ii  bzip2                                   1.0.6-9.2~deb10u1            amd64        high-quality block-sorting file compressor - utilities
    ii  ca-certificates                         20190110                     all          Common CA certificates
    ii  clang                                   1:7.0-47                     amd64        C, C++ and Objective-C compiler (LLVM based)
    ii  clang-7                                 1:7.0.1-8                    amd64        C, C++ and Objective-C compiler
    ii  cmake                                   3.13.4-1                     amd64        cross-platform, open-source make system
    ii  cmake-data                              3.13.4-1                     all          CMake data files (modules, templates and documentation)
    ii  coreutils                               8.30-3                       amd64        GNU core utilities
    ii  cpp                                     4:8.3.0-1                    amd64        GNU C preprocessor (cpp)
    ii  cpp-8                                   8.3.0-6                      amd64        GNU C preprocessor
    ii  curl                                    7.64.0-4                     amd64        command line tool for transferring data with URL syntax
    ii  dash                                    0.5.10.2-5                   amd64        POSIX-compliant shell
    ii  dbus                                    1.12.16-1                    amd64        simple interprocess messaging system (daemon and utilities)
    ii  dbus-user-session                       1.12.16-1                    amd64        simple interprocess messaging system (systemd --user integration)
    ii  dconf-gsettings-backend:amd64           0.30.1-2                     amd64        simple configuration storage system - GSettings back-end
    ii  dconf-service                           0.30.1-2                     amd64        simple configuration storage system - D-Bus service
    ii  debconf                                 1.5.71                       all          Debian configuration management system
    ii  debian-archive-keyring                  2019.1                       all          GnuPG archive keys of the Debian archive
    ii  debianutils                             4.8.6.1                      amd64        Miscellaneous utilities specific to Debian
    ii  di                                      4.47-1                       amd64        advanced df like disk information utility
    ii  diffutils                               1:3.7-3                      amd64        File comparison utilities
    ii  dirmngr                                 2.2.12-1+deb10u1             amd64        GNU privacy guard - network certificate management service
    ii  dmsetup                                 2:1.02.155-3                 amd64        Linux Kernel Device Mapper userspace library
    ii  dpkg                                    1.19.7                       amd64        Debian package management system
    ii  dpkg-dev                                1.19.7                       all          Debian package development tools
    ii  e2fsprogs                               1.44.5-1+deb10u1             amd64        ext2/ext3/ext4 file system utilities
    ii  etckeeper                               1.18.10-1                    all          store /etc in git, mercurial, bzr or darcs
    ii  fakeroot                                1.23-1                       amd64        tool for simulating superuser privileges
    ii  fdisk                                   2.33.1-0.1                   amd64        collection of partitioning utilities
    ii  findutils                               4.6.0+git+20190209-2         amd64        utilities for finding files--find, xargs
    ii  fontconfig                              2.13.1-2                     amd64        generic font configuration library - support binaries
    ii  fontconfig-config                       2.13.1-2                     all          generic font configuration library - configuration
    ii  fonts-dejavu-core                       2.37-1                       all          Vera font family derivate with additional characters
    ii  g++                                     4:8.3.0-1                    amd64        GNU C++ compiler
    ii  g++-8                                   8.3.0-6                      amd64        GNU C++ compiler
    ii  gcc                                     4:8.3.0-1                    amd64        GNU C compiler
    ii  gcc-8                                   8.3.0-6                      amd64        GNU C compiler
    ii  gcc-8-base:amd64                        8.3.0-6                      amd64        GCC, the GNU Compiler Collection (base package)
    ii  gdb                                     8.2.1-2+b1                   amd64        GNU Debugger
    ii  geoclue-2.0                             2.5.2-1                      amd64        geoinformation service
    ii  geoip-database                          20181108-1                   all          IP lookup command line tools that use the GeoIP library (country database)
    ii  git                                     1:2.20.1-2                   amd64        fast, scalable, distributed revision control system
    ii  git-man                                 1:2.20.1-2                   all          fast, scalable, distributed revision control system (manual pages)
    ii  glib-networking:amd64                   2.58.0-2                     amd64        network-related giomodules for GLib
    ii  glib-networking-common                  2.58.0-2                     all          network-related giomodules for GLib - data files
    ii  glib-networking-services                2.58.0-2                     amd64        network-related giomodules for GLib - D-Bus services
    ii  gnupg                                   2.2.12-1+deb10u1             all          GNU privacy guard - a free PGP replacement
    ii  gnupg-l10n                              2.2.12-1+deb10u1             all          GNU privacy guard - localization files
    ii  gnupg-utils                             2.2.12-1+deb10u1             amd64        GNU privacy guard - utility programs
    ii  gpg                                     2.2.12-1+deb10u1             amd64        GNU Privacy Guard -- minimalist public key operations
    ii  gpg-agent                               2.2.12-1+deb10u1             amd64        GNU privacy guard - cryptographic agent
    ii  gpg-wks-client                          2.2.12-1+deb10u1             amd64        GNU privacy guard - Web Key Service client
    ii  gpg-wks-server                          2.2.12-1+deb10u1             amd64        GNU privacy guard - Web Key Service server
    ii  gpgconf                                 2.2.12-1+deb10u1             amd64        GNU privacy guard - core configuration utilities
    ii  gpgsm                                   2.2.12-1+deb10u1             amd64        GNU privacy guard - S/MIME version
    ii  gpgv                                    2.2.12-1+deb10u1             amd64        GNU privacy guard - signature verification tool
    ii  grep                                    3.3-1                        amd64        GNU grep, egrep and fgrep
    ii  gsettings-desktop-schemas               3.28.1-1                     all          GSettings desktop-wide schemas
    ii  gstreamer1.0-plugins-base:amd64         1.14.4-2                     amd64        GStreamer plugins from the "base" set
    ii  gtk-update-icon-cache                   3.24.5-1                     amd64        icon theme caching utility
    ii  gzip                                    1.9-3                        amd64        GNU compression utilities
    ii  hicolor-icon-theme                      0.17-2                       all          default fallback theme for FreeDesktop.org icon themes
    ii  hostname                                3.21                         amd64        utility to set/show the host name or domain name
    ii  i965-va-driver:amd64                    2.3.0+dfsg1-1                amd64        VAAPI driver for Intel G45 & HD Graphics family
    ii  iio-sensor-proxy                        2.4-2                        amd64        IIO sensors to D-Bus proxy
    ii  init-system-helpers                     1.56+nmu1                    all          helper tools for all init systems
    ii  intel-media-va-driver:amd64             18.4.1+dfsg1-1               amd64        VAAPI driver for the Intel GEN8+ Graphics family
    ii  iso-codes                               4.2-1                        all          ISO language, territory, currency, script codes and their translations
    ii  joe                                     4.6-1+b1                     amd64        user friendly full screen text editor
    ii  less                                    487-0.1+b1                   amd64        pager program similar to more
    ii  lib32gcc1                               1:8.3.0-6                    amd64        GCC support library (32 bit Version)
    ii  lib32stdc++6                            8.3.0-6                      amd64        GNU Standard C++ Library v3 (32 bit Version)
    ii  libaacs0:amd64                          0.9.0-2                      amd64        free-and-libre implementation of AACS
    ii  libacl1:amd64                           2.2.53-4                     amd64        access control list - shared library
    ii  libalgorithm-diff-perl                  1.19.03-2                    all          module to find differences between files
    ii  libalgorithm-diff-xs-perl               0.04-5+b1                    amd64        module to find differences between files (XS accelerated)
    ii  libalgorithm-merge-perl                 0.08-3                       all          Perl module for three-way merge of textual data
    ii  libaom0:amd64                           1.0.0-3                      amd64        AV1 Video Codec Library
    ii  libapparmor1:amd64                      2.13.2-10                    amd64        changehat AppArmor library
    ii  libapt-inst2.0:amd64                    1.8.2                        amd64        deb package format runtime library
    ii  libapt-pkg5.0:amd64                     1.8.2                        amd64        package management runtime library
    ii  libarchive13:amd64                      3.3.3-4                      amd64        Multi-format archive and compression library (shared library)
    ii  libargon2-1:amd64                       0~20171227-0.2               amd64        memory-hard hashing function - runtime library
    ii  libasan5:amd64                          8.3.0-6                      amd64        AddressSanitizer -- a fast memory error detector
    ii  libasound2:amd64                        1.1.8-1                      amd64        shared library for ALSA applications
    ii  libasound2-data                         1.1.8-1                      all          Configuration files and profiles for ALSA drivers
    ii  libassuan0:amd64                        2.5.2-1                      amd64        IPC library for the GnuPG components
    ii  libasyncns0:amd64                       0.8-6                        amd64        Asynchronous name service query library
    ii  libatk-bridge2.0-0:amd64                2.30.0-5                     amd64        AT-SPI 2 toolkit bridge - shared library
    ii  libatk1.0-0:amd64                       2.30.0-2                     amd64        ATK accessibility toolkit
    ii  libatk1.0-data                          2.30.0-2                     all          Common files for the ATK accessibility toolkit
    ii  libatomic1:amd64                        8.3.0-6                      amd64        support library providing __atomic built-in functions
    ii  libatspi2.0-0:amd64                     2.30.0-7                     amd64        Assistive Technology Service Provider Interface - shared library
    ii  libattr1:amd64                          1:2.4.48-4                   amd64        extended attribute handling - shared library
    ii  libaudit-common                         1:2.8.4-3                    all          Dynamic library for security auditing - common files
    ii  libaudit1:amd64                         1:2.8.4-3                    amd64        Dynamic library for security auditing
    ii  libavahi-client3:amd64                  0.7-4+b1                     amd64        Avahi client library
    ii  libavahi-common-data:amd64              0.7-4+b1                     amd64        Avahi common data files
    ii  libavahi-common3:amd64                  0.7-4+b1                     amd64        Avahi common library
    ii  libavahi-core7:amd64                    0.7-4+b1                     amd64        Avahi's embeddable mDNS/DNS-SD library
    ii  libavahi-glib1:amd64                    0.7-4+b1                     amd64        Avahi GLib integration library
    ii  libavcodec58:amd64                      7:4.1.4-1~deb10u1            amd64        FFmpeg library with de/encoders for audio/video codecs - runtime files
    ii  libavformat58:amd64                     7:4.1.4-1~deb10u1            amd64        FFmpeg library with (de)muxers for multimedia containers - runtime files
    ii  libavutil56:amd64                       7:4.1.4-1~deb10u1            amd64        FFmpeg library with functions for simplifying programming - runtime files
    ii  libbabeltrace1:amd64                    1.5.6-2+deb10u1              amd64        Babeltrace conversion libraries
    ii  libbdplus0:amd64                        0.1.2-3                      amd64        implementation of BD+ for reading Blu-ray Discs
    ii  libbind9-161:amd64                      1:9.11.5.P4+dfsg-5.1         amd64        BIND9 Shared Library used by BIND
    ii  libbinutils:amd64                       2.31.1-16                    amd64        GNU binary utilities (private shared library)
    ii  libblkid1:amd64                         2.33.1-0.1                   amd64        block device ID library
    ii  libbluray2:amd64                        1:1.1.0-1                    amd64        Blu-ray disc playback support library (shared library)
    ii  libbotan-2-9                            2.9.0-2                      amd64        multiplatform crypto library (2.x version)
    ii  libbrotli1:amd64                        1.0.7-2                      amd64        library implementing brotli encoder and decoder (shared libraries)
    ii  libbsd0:amd64                           0.9.1-2                      amd64        utility functions from BSD systems - shared library
    ii  libbz2-1.0:amd64                        1.0.6-9.2~deb10u1            amd64        high-quality block-sorting file compressor library - runtime
    ii  libc-bin                                2.28-10                      amd64        GNU C Library: Binaries
    ii  libc-dev-bin                            2.28-10                      amd64        GNU C Library: Development binaries
    ii  libc-l10n                               2.28-10                      all          GNU C Library: localization files
    ii  libc6:amd64                             2.28-10                      amd64        GNU C Library: Shared libraries
    ii  libc6-dbg:amd64                         2.28-10                      amd64        GNU C Library: detached debugging symbols
    ii  libc6-dev:amd64                         2.28-10                      amd64        GNU C Library: Development Libraries and Header Files
    ii  libc6-i386                              2.28-10                      amd64        GNU C Library: 32-bit shared libraries for AMD64
    ii  libcairo-gobject2:amd64                 1.16.0-4                     amd64        Cairo 2D vector graphics library (GObject library)
    ii  libcairo2:amd64                         1.16.0-4                     amd64        Cairo 2D vector graphics library
    ii  libcap-ng0:amd64                        0.7.9-2                      amd64        An alternate POSIX capabilities library
    ii  libcap2:amd64                           1:2.25-2                     amd64        POSIX 1003.1e capabilities (library)
    ii  libcap2-bin                             1:2.25-2                     amd64        POSIX 1003.1e capabilities (utilities)
    ii  libcc1-0:amd64                          8.3.0-6                      amd64        GCC cc1 plugin for GDB
    ii  libcdparanoia0:amd64                    3.10.2+debian-13             amd64        audio extraction tool for sampling CDs (library)
    ii  libchromaprint1:amd64                   1.4.3-3                      amd64        audio fingerprint library
    ii  libclang-common-7-dev                   1:7.0.1-8                    amd64        Clang library - Common development package
    ii  libclang1-7                             1:7.0.1-8                    amd64        C interface to the Clang library
    ii  libcodec2-0.8.1:amd64                   0.8.1-2                      amd64        Codec2 runtime library
    ii  libcolord2:amd64                        1.4.3-4                      amd64        system service to manage device colour profiles -- runtime
    ii  libcom-err2:amd64                       1.44.5-1+deb10u1             amd64        common error description library
    ii  libcroco3:amd64                         0.6.12-3                     amd64        Cascading Style Sheet (CSS) parsing and manipulation toolkit
    ii  libcryptsetup12:amd64                   2:2.1.0-5+deb10u2            amd64        disk encryption support - shared library
    ii  libcrystalhd3:amd64                     1:0.0~git20110715.fdd2f19-13 amd64        Crystal HD Video Decoder (shared library)
    ii  libcups2:amd64                          2.2.10-6+deb10u1             amd64        Common UNIX Printing System(tm) - Core library
    ii  libcurl3-gnutls:amd64                   7.64.0-4                     amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
    ii  libcurl4:amd64                          7.64.0-4                     amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
    ii  libdaemon0:amd64                        0.14-7                       amd64        lightweight C library for daemons - runtime library
    ii  libdatrie1:amd64                        0.2.12-2                     amd64        Double-array trie library
    ii  libdb5.3:amd64                          5.3.28+dfsg1-0.5             amd64        Berkeley v5.3 Database Libraries [runtime]
    ii  libdbus-1-3:amd64                       1.12.16-1                    amd64        simple interprocess messaging system (library)
    ii  libdconf1:amd64                         0.30.1-2                     amd64        simple configuration storage system - runtime library
    ii  libdebconfclient0:amd64                 0.249                        amd64        Debian Configuration Management System (C-implementation library)
    ii  libdevmapper1.02.1:amd64                2:1.02.155-3                 amd64        Linux Kernel Device Mapper userspace library
    ii  libdns1104:amd64                        1:9.11.5.P4+dfsg-5.1         amd64        DNS Shared Library used by BIND
    ii  libdouble-conversion1:amd64             3.1.0-3                      amd64        routines to convert IEEE floats to and from strings
    ii  libdpkg-perl                            1.19.7                       all          Dpkg perl modules
    ii  libdrm-amdgpu1:amd64                    2.4.97-1                     amd64        Userspace interface to amdgpu-specific kernel DRM services -- runtime
    ii  libdrm-common                           2.4.97-1                     all          Userspace interface to kernel DRM services -- common files
    ii  libdrm-dev:amd64                        2.4.97-1                     amd64        Userspace interface to kernel DRM services -- development files
    ii  libdrm-intel1:amd64                     2.4.97-1                     amd64        Userspace interface to intel-specific kernel DRM services -- runtime
    ii  libdrm-nouveau2:amd64                   2.4.97-1                     amd64        Userspace interface to nouveau-specific kernel DRM services -- runtime
    ii  libdrm-radeon1:amd64                    2.4.97-1                     amd64        Userspace interface to radeon-specific kernel DRM services -- runtime
    ii  libdrm2:amd64                           2.4.97-1                     amd64        Userspace interface to kernel DRM services -- runtime
    ii  libdw1:amd64                            0.176-1.1                    amd64        library that provides access to the DWARF debug information
    ii  libedit2:amd64                          3.1-20181209-1               amd64        BSD editline and history libraries
    ii  libegl-mesa0:amd64                      18.3.6-2                     amd64        free implementation of the EGL API -- Mesa vendor library
    ii  libegl1:amd64                           1.1.0-1                      amd64        Vendor neutral GL dispatch library -- EGL support
    ii  libelf1:amd64                           0.176-1.1                    amd64        library to read and write ELF files
    ii  libepoxy0:amd64                         1.5.3-0.1                    amd64        OpenGL function pointer management library
    ii  liberror-perl                           0.17027-2                    all          Perl module for error/exception handling in an OO-ish way
    ii  libevdev2:amd64                         1.6.0+dfsg-1                 amd64        wrapper library for evdev devices
    ii  libevent-2.1-6:amd64                    2.1.8-stable-4               amd64        Asynchronous event notification library
    ii  libexpat1:amd64                         2.2.6-2                      amd64        XML parsing C library - runtime library
    ii  libext2fs2:amd64                        1.44.5-1+deb10u1             amd64        ext2/ext3/ext4 file system libraries
    ii  libfakeroot:amd64                       1.23-1                       amd64        tool for simulating superuser privileges - shared libraries
    ii  libfdisk1:amd64                         2.33.1-0.1                   amd64        fdisk partitioning library
    ii  libffi-dev:amd64                        3.2.1-9                      amd64        Foreign Function Interface library (development files)
    ii  libffi6:amd64                           3.2.1-9                      amd64        Foreign Function Interface library runtime
    ii  libfile-fcntllock-perl                  0.22-3+b5                    amd64        Perl module for file locking with fcntl(2)
    ii  libflac8:amd64                          1.3.2-3                      amd64        Free Lossless Audio Codec - runtime C library
    ii  libfontconfig1:amd64                    2.13.1-2                     amd64        generic font configuration library - runtime
    ii  libfontenc1:amd64                       1:1.1.3-1+b2                 amd64        X11 font encoding library
    ii  libfreetype6:amd64                      2.9.1-3                      amd64        FreeType 2 font engine, shared library files
    ii  libfribidi0:amd64                       1.0.5-3.1                    amd64        Free Implementation of the Unicode BiDi algorithm
    ii  libfstrm0:amd64                         0.4.0-1                      amd64        Frame Streams (fstrm) library
    ii  libgbm1:amd64                           18.3.6-2                     amd64        generic buffer management API -- runtime
    ii  libgc1c2:amd64                          1:7.6.4-0.4                  amd64        conservative garbage collector for C and C++
    ii  libgcc-8-dev:amd64                      8.3.0-6                      amd64        GCC support library (development files)
    ii  libgcc1:amd64                           1:8.3.0-6                    amd64        GCC support library
    ii  libgcrypt20:amd64                       1.8.4-5                      amd64        LGPL Crypto library - runtime library
    ii  libgdbm-compat4:amd64                   1.18.1-4                     amd64        GNU dbm database routines (legacy support runtime version) 
    ii  libgdbm6:amd64                          1.18.1-4                     amd64        GNU dbm database routines (runtime version) 
    ii  libgdk-pixbuf2.0-0:amd64                2.38.1+dfsg-1                amd64        GDK Pixbuf library
    ii  libgdk-pixbuf2.0-bin                    2.38.1+dfsg-1                amd64        GDK Pixbuf library (thumbnailer)
    ii  libgdk-pixbuf2.0-common                 2.38.1+dfsg-1                all          GDK Pixbuf library - data files
    ii  libgeoip1:amd64                         1.6.12-1                     amd64        non-DNS IP-to-country resolver library
    ii  libgl1:amd64                            1.1.0-1                      amd64        Vendor neutral GL dispatch library -- legacy GL support
    ii  libgl1-mesa-dev:amd64                   18.3.6-2                     amd64        free implementation of the OpenGL API -- GLX development files
    ii  libgl1-mesa-dri:amd64                   18.3.6-2                     amd64        free implementation of the OpenGL API -- DRI modules
    ii  libglapi-mesa:amd64                     18.3.6-2                     amd64        free implementation of the GL API -- shared library
    ii  libgles1:amd64                          1.1.0-1                      amd64        Vendor neutral GL dispatch library -- GLESv1 support
    ii  libgles2:amd64                          1.1.0-1                      amd64        Vendor neutral GL dispatch library -- GLESv2 support
    ii  libglib2.0-0:amd64                      2.58.3-2+deb10u1             amd64        GLib library of C routines
    ii  libglib2.0-data                         2.58.3-2+deb10u1             all          Common files for GLib library
    ii  libglu1-mesa:amd64                      9.0.0-2.1+b3                 amd64        Mesa OpenGL utility library (GLU)
    ii  libglu1-mesa-dev:amd64                  9.0.0-2.1+b3                 amd64        Mesa OpenGL utility library -- development files
    ii  libglvnd-core-dev:amd64                 1.1.0-1                      amd64        Vendor neutral GL dispatch library -- core development files
    ii  libglvnd-dev:amd64                      1.1.0-1                      amd64        Vendor neutral GL dispatch library -- development files
    ii  libglvnd0:amd64                         1.1.0-1                      amd64        Vendor neutral GL dispatch library
    ii  libglx-mesa0:amd64                      18.3.6-2                     amd64        free implementation of the OpenGL API -- GLX vendor library
    ii  libglx0:amd64                           1.1.0-1                      amd64        Vendor neutral GL dispatch library -- GLX support
    ii  libgme0:amd64                           0.6.2-1                      amd64        Playback library for video game music files - shared library
    ii  libgmp10:amd64                          2:6.1.2+dfsg-4               amd64        Multiprecision arithmetic library
    ii  libgnutls30:amd64                       3.6.7-4                      amd64        GNU TLS library - main runtime library
    ii  libgomp1:amd64                          8.3.0-6                      amd64        GCC OpenMP (GOMP) support library
    ii  libgpg-error0:amd64                     1.35-1                       amd64        GnuPG development runtime library
    ii  libgraphite2-3:amd64                    1.3.13-7                     amd64        Font rendering engine for Complex Scripts -- library
    ii  libgsm1:amd64                           1.0.18-2                     amd64        Shared libraries for GSM speech compressor
    ii  libgssapi-krb5-2:amd64                  1.17-3                       amd64        MIT Kerberos runtime libraries - krb5 GSS-API Mechanism
    ii  libgstreamer-plugins-base1.0-0:amd64    1.14.4-2                     amd64        GStreamer libraries from the "base" set
    ii  libgstreamer1.0-0:amd64                 1.14.4-1                     amd64        Core GStreamer libraries and elements
    ii  libgtk-3-0:amd64                        3.24.5-1                     amd64        GTK+ graphical user interface library
    ii  libgtk-3-bin                            3.24.5-1                     amd64        programs for the GTK+ graphical user interface library
    ii  libgtk-3-common                         3.24.5-1                     all          common files for the GTK+ graphical user interface library
    ii  libgudev-1.0-0:amd64                    232-2                        amd64        GObject-based wrapper library for libudev
    ii  libharfbuzz0b:amd64                     2.3.1-1                      amd64        OpenType text shaping engine (shared library)
    ii  libhogweed4:amd64                       3.4.1-1                      amd64        low level cryptographic library (public-key cryptos)
    ii  libhyphen0:amd64                        2.8.8-7                      amd64        ALTLinux hyphenation library - shared library
    ii  libice6:amd64                           2:1.0.9-2                    amd64        X11 Inter-Client Exchange library
    ii  libicu63:amd64                          63.1-6                       amd64        International Components for Unicode
    ii  libidn11:amd64                          1.33-2.2                     amd64        GNU Libidn library, implementation of IETF IDN specifications
    ii  libidn2-0:amd64                         2.0.5-1                      amd64        Internationalized domain names (IDNA2008/TR46) library
    ii  libigdgmm5:amd64                        18.4.1+ds1-1                 amd64        Intel Graphics Memory Management Library -- shared library
    ii  libinput-bin                            1.12.6-2                     amd64        input device management and event handling library - udev quirks
    ii  libinput10:amd64                        1.12.6-2                     amd64        input device management and event handling library - shared library
    ii  libip4tc0:amd64                         1.8.2-4                      amd64        netfilter libip4tc library
    ii  libipt2                                 2.0-2                        amd64        Intel Processor Trace Decoder Library
    ii  libisc1100:amd64                        1:9.11.5.P4+dfsg-5.1         amd64        ISC Shared Library used by BIND
    ii  libisccc161:amd64                       1:9.11.5.P4+dfsg-5.1         amd64        Command Channel Library used by BIND
    ii  libisccfg163:amd64                      1:9.11.5.P4+dfsg-5.1         amd64        Config File Handling Library used by BIND
    ii  libisl19:amd64                          0.20-2                       amd64        manipulating sets and relations of integer points bounded by linear constraints
    ii  libitm1:amd64                           8.3.0-6                      amd64        GNU Transactional Memory Library
    ii  libjbig0:amd64                          2.1-3.1+b2                   amd64        JBIGkit libraries
    ii  libjim0.77:amd64                        0.77+dfsg0-3                 amd64        small-footprint implementation of Tcl - shared library
    ii  libjpeg62-turbo:amd64                   1:1.5.2-2+b1                 amd64        libjpeg-turbo JPEG runtime library
    ii  libjson-c3:amd64                        0.12.1+ds-2                  amd64        JSON manipulation library - shared library
    ii  libjson-glib-1.0-0:amd64                1.4.4-2                      amd64        GLib JSON manipulation library
    ii  libjson-glib-1.0-common                 1.4.4-2                      all          GLib JSON manipulation library (common files)
    ii  libjsoncpp1:amd64                       1.7.4-3                      amd64        library for reading and writing JSON for C++
    ii  libk5crypto3:amd64                      1.17-3                       amd64        MIT Kerberos runtime libraries - Crypto Library
    ii  libkeyutils1:amd64                      1.6-6                        amd64        Linux Key Management Utilities (library)
    ii  libkmod2:amd64                          26-1                         amd64        libkmod shared library
    ii  libkrb5-3:amd64                         1.17-3                       amd64        MIT Kerberos runtime libraries
    ii  libkrb5support0:amd64                   1.17-3                       amd64        MIT Kerberos runtime libraries - Support library
    ii  libksba8:amd64                          1.3.5-2                      amd64        X.509 and CMS support library
    ii  liblcms2-2:amd64                        2.9-3                        amd64        Little CMS 2 color management library
    ii  libldap-2.4-2:amd64                     2.4.47+dfsg-3+deb10u1        amd64        OpenLDAP libraries
    ii  libldap-common                          2.4.47+dfsg-3+deb10u1        all          OpenLDAP common files for libraries
    ii  libllvm7:amd64                          1:7.0.1-8                    amd64        Modular compiler and toolchain technologies, runtime library
    ii  liblmdb0:amd64                          0.9.22-1                     amd64        Lightning Memory-Mapped Database shared library
    ii  liblocale-gettext-perl                  1.07-3+b4                    amd64        module using libc functions for internationalization in Perl
    ii  liblsan0:amd64                          8.3.0-6                      amd64        LeakSanitizer -- a memory leak detector (runtime)
    ii  liblwres161:amd64                       1:9.11.5.P4+dfsg-5.1         amd64        Lightweight Resolver Library used by BIND
    ii  liblz4-1:amd64                          1.8.3-1                      amd64        Fast LZ compression algorithm library - runtime
    ii  liblzma5:amd64                          5.2.4-1                      amd64        XZ-format compression library
    ii  libmbim-glib4:amd64                     1.18.0-1                     amd64        Support library to use the MBIM protocol
    ii  libmbim-proxy                           1.18.0-1                     amd64        Proxy to communicate with MBIM ports
    ii  libminizip1:amd64                       1.1-8+b1                     amd64        compression library - minizip library
    ii  libmm-glib0:amd64                       1.10.0-1                     amd64        D-Bus service for managing modems - shared libraries
    ii  libmount1:amd64                         2.33.1-0.1                   amd64        device mounting library
    ii  libmp3lame0:amd64                       3.100-2+b1                   amd64        MP3 encoding library
    ii  libmpc3:amd64                           1.1.0-1                      amd64        multiple precision complex floating-point library
    ii  libmpdec2:amd64                         2.4.2-2                      amd64        library for decimal floating point arithmetic (runtime library)
    ii  libmpfr6:amd64                          4.0.2-1                      amd64        multiple precision floating-point computation
    ii  libmpg123-0:amd64                       1.25.10-2                    amd64        MPEG layer 1/2/3 audio decoder (shared library)
    ii  libmpx2:amd64                           8.3.0-6                      amd64        Intel memory protection extensions (runtime)
    ii  libmtdev1:amd64                         1.1.5-1+b1                   amd64        Multitouch Protocol Translation Library - shared library
    ii  libncurses-dev:amd64                    6.1+20181013-2+deb10u1       amd64        developer's libraries for ncurses
    ii  libncurses6:amd64                       6.1+20181013-2+deb10u1       amd64        shared libraries for terminal handling
    ii  libncursesw6:amd64                      6.1+20181013-2+deb10u1       amd64        shared libraries for terminal handling (wide character support)
    ii  libnettle6:amd64                        3.4.1-1                      amd64        low level cryptographic library (symmetric and one-way cryptos)
    ii  libnewt0.52:amd64                       0.52.20-8                    amd64        Not Erik's Windowing Toolkit - text mode windowing with slang
    ii  libnghttp2-14:amd64                     1.36.0-2+deb10u1             amd64        library implementing HTTP/2 protocol (shared library)
    ii  libnl-3-200:amd64                       3.4.0-1                      amd64        library for dealing with netlink sockets
    ii  libnl-genl-3-200:amd64                  3.4.0-1                      amd64        library for dealing with netlink sockets - generic netlink
    ii  libnl-route-3-200:amd64                 3.4.0-1                      amd64        library for dealing with netlink sockets - route interface
    ii  libnotify4:amd64                        0.7.7-4                      amd64        sends desktop notifications to a notification daemon
    ii  libnpth0:amd64                          1.6-1                        amd64        replacement for GNU Pth using system threads
    ii  libnspr4:amd64                          2:4.20-1                     amd64        NetScape Portable Runtime Library
    ii  libnss-mdns:amd64                       0.14.1-1                     amd64        NSS module for Multicast DNS name resolution
    ii  libnss-systemd:amd64                    241-7~deb10u1                amd64        nss module providing dynamic user and group name resolution
    ii  libnss3:amd64                           2:3.42.1-1+deb10u1           amd64        Network Security Service libraries
    ii  libnuma1:amd64                          2.0.12-1                     amd64        Libraries for controlling NUMA policy
    ii  libobjc-8-dev:amd64                     8.3.0-6                      amd64        Runtime library for GNU Objective-C applications (development files)
    ii  libobjc4:amd64                          8.3.0-6                      amd64        Runtime library for GNU Objective-C applications
    ii  libogg0:amd64                           1.3.2-1+b1                   amd64        Ogg bitstream library
    ii  libomp-7-dev                            1:7.0.1-8                    amd64        LLVM OpenMP runtime - dev package
    ii  libomp5-7:amd64                         1:7.0.1-8                    amd64        LLVM OpenMP runtime
    ii  libopengl0:amd64                        1.1.0-1                      amd64        Vendor neutral GL dispatch library -- OpenGL support
    ii  libopenjp2-7:amd64                      2.3.0-2                      amd64        JPEG 2000 image compression/decompression library
    ii  libopenmpt0:amd64                       0.4.3-1                      amd64        module music library based on OpenMPT -- shared library
    ii  libopus0:amd64                          1.3-1                        amd64        Opus codec runtime library
    ii  liborc-0.4-0:amd64                      1:0.4.28-3.1                 amd64        Library of Optimized Inner Loops Runtime Compiler
    ii  libp11-kit0:amd64                       0.23.15-2                    amd64        library for loading and coordinating access to PKCS#11 modules - runtime
    ii  libpam-cap:amd64                        1:2.25-2                     amd64        POSIX 1003.1e capabilities (PAM module)
    ii  libpam-modules:amd64                    1.3.1-5                      amd64        Pluggable Authentication Modules for PAM
    ii  libpam-modules-bin                      1.3.1-5                      amd64        Pluggable Authentication Modules for PAM - helper binaries
    ii  libpam-runtime                          1.3.1-5                      all          Runtime support for the PAM library
    ii  libpam-systemd:amd64                    241-7~deb10u1                amd64        system and service manager - PAM module
    ii  libpam0g:amd64                          1.3.1-5                      amd64        Pluggable Authentication Modules library
    ii  libpango-1.0-0:amd64                    1.42.4-7~deb10u1             amd64        Layout and rendering of internationalized text
    ii  libpangocairo-1.0-0:amd64               1.42.4-7~deb10u1             amd64        Layout and rendering of internationalized text
    ii  libpangoft2-1.0-0:amd64                 1.42.4-7~deb10u1             amd64        Layout and rendering of internationalized text
    ii  libpciaccess0:amd64                     0.14-1                       amd64        Generic PCI access library for X
    ii  libpcre2-16-0:amd64                     10.32-5                      amd64        New Perl Compatible Regular Expression Library - 16 bit runtime files
    ii  libpcre2-8-0:amd64                      10.32-5                      amd64        New Perl Compatible Regular Expression Library- 8 bit runtime files
    ii  libpcre3:amd64                          2:8.39-12                    amd64        Old Perl 5 Compatible Regular Expression Library - runtime files
    ii  libpcsclite1:amd64                      1.8.24-1                     amd64        Middleware to access a smart card using PC/SC (library)
    ii  libperl5.28:amd64                       5.28.1-6                     amd64        shared Perl library
    ii  libpipeline1:amd64                      1.5.1-2                      amd64        pipeline manipulation library
    ii  libpixman-1-0:amd64                     0.36.0-1                     amd64        pixel-manipulation library for X and cairo
    ii  libpng16-16:amd64                       1.6.36-6                     amd64        PNG library - runtime (version 1.6)
    ii  libpolkit-gobject-1-0:amd64             0.105-25                     amd64        PolicyKit Authorization API
    ii  libpopt0:amd64                          1.16-12                      amd64        lib for parsing cmdline parameters
    ii  libprocps7:amd64                        2:3.3.15-2                   amd64        library for accessing process information from /proc
    ii  libprotobuf-c1:amd64                    1.3.1-1+b1                   amd64        Protocol Buffers C shared library (protobuf-c)
    ii  libproxy1v5:amd64                       0.4.15-5                     amd64        automatic proxy configuration management library (shared)
    ii  libpsl5:amd64                           0.20.2-2                     amd64        Library for Public Suffix List (shared libraries)
    ii  libpthread-stubs0-dev:amd64             0.4-1                        amd64        pthread stubs not provided by native libc, development files
    ii  libpulse0:amd64                         12.2-4+deb10u1               amd64        PulseAudio client libraries
    ii  libpython-stdlib:amd64                  2.7.16-1                     amd64        interactive high-level object-oriented language (Python2)
    ii  libpython2-stdlib:amd64                 2.7.16-1                     amd64        interactive high-level object-oriented language (Python2)
    ii  libpython2.7-minimal:amd64              2.7.16-2                     amd64        Minimal subset of the Python language (version 2.7)
    ii  libpython2.7-stdlib:amd64               2.7.16-2                     amd64        Interactive high-level object-oriented language (standard library, version 2.7)
    ii  libpython3.7:amd64                      3.7.3-2                      amd64        Shared Python runtime library (version 3.7)
    ii  libpython3.7-minimal:amd64              3.7.3-2                      amd64        Minimal subset of the Python language (version 3.7)
    ii  libpython3.7-stdlib:amd64               3.7.3-2                      amd64        Interactive high-level object-oriented language (standard library, version 3.7)
    ii  libqbscore1.12:amd64                    1.12.2+dfsg-2                amd64        Qbs core library
    ii  libqbsqtprofilesetup1.12:amd64          1.12.2+dfsg-2                amd64        Qbs profile setup library
    ii  libqmi-glib5:amd64                      1.22.0-1.2                   amd64        Support library to use the Qualcomm MSM Interface (QMI) protocol
    ii  libqmi-proxy                            1.22.0-1.2                   amd64        Proxy to communicate with QMI ports
    ii  libqt5charts5:amd64                     5.11.3-2                     amd64        Qt charts shared library
    ii  libqt5concurrent5:amd64                 5.11.3+dfsg1-1               amd64        Qt 5 concurrent module
    ii  libqt5core5a:amd64                      5.11.3+dfsg1-1               amd64        Qt 5 core module
    ii  libqt5dbus5:amd64                       5.11.3+dfsg1-1               amd64        Qt 5 D-Bus module
    ii  libqt5designer5:amd64                   5.11.3-4                     amd64        Qt 5 designer module
    ii  libqt5designercomponents5:amd64         5.11.3-4                     amd64        Qt 5 Designer components module
    ii  libqt5gui5:amd64                        5.11.3+dfsg1-1               amd64        Qt 5 GUI module
    ii  libqt5help5:amd64                       5.11.3-4                     amd64        Qt 5 help module
    ii  libqt5multimedia5:amd64                 5.11.3-2                     amd64        Qt 5 Multimedia module
    ii  libqt5multimediaquick5:amd64            5.11.3-2                     amd64        Qt 5 Multimedia Quick module
    ii  libqt5network5:amd64                    5.11.3+dfsg1-1               amd64        Qt 5 network module
    ii  libqt5opengl5:amd64                     5.11.3+dfsg1-1               amd64        Qt 5 OpenGL module
    ii  libqt5opengl5-dev:amd64                 5.11.3+dfsg1-1               amd64        Qt 5 OpenGL library development files
    ii  libqt5positioning5:amd64                5.11.3+dfsg-2                amd64        Qt Positioning module
    ii  libqt5printsupport5:amd64               5.11.3+dfsg1-1               amd64        Qt 5 print support module
    ii  libqt5qml5:amd64                        5.11.3-4                     amd64        Qt 5 QML module
    ii  libqt5quick5:amd64                      5.11.3-4                     amd64        Qt 5 Quick library
    ii  libqt5quickcontrols2-5:amd64            5.11.3+dfsg-2                amd64        Qt 5 Quick Controls 2 library
    ii  libqt5quickparticles5:amd64             5.11.3-4                     amd64        Qt 5 Quick particles module
    ii  libqt5quicktemplates2-5:amd64           5.11.3+dfsg-2                amd64        Qt 5 Quick Templates 2 library
    ii  libqt5quicktest5:amd64                  5.11.3-4                     amd64        Qt 5 Quick Test library
    ii  libqt5quickwidgets5:amd64               5.11.3-4                     amd64        Qt 5 Quick Widgets library
    ii  libqt5script5:amd64                     5.11.3+dfsg-3                amd64        Qt 5 script module
    ii  libqt5sensors5:amd64                    5.11.3-2                     amd64        Qt Sensors module
    ii  libqt5serialport5:amd64                 5.11.3-2                     amd64        Qt 5 serial port support
    ii  libqt5sql5:amd64                        5.11.3+dfsg1-1               amd64        Qt 5 SQL module
    ii  libqt5sql5-sqlite:amd64                 5.11.3+dfsg1-1               amd64        Qt 5 SQLite 3 database driver
    ii  libqt5svg5:amd64                        5.11.3-2                     amd64        Qt 5 SVG module
    ii  libqt5test5:amd64                       5.11.3+dfsg1-1               amd64        Qt 5 test module
    ii  libqt5webchannel5:amd64                 5.11.3-2                     amd64        Web communication library for Qt
    ii  libqt5webengine-data                    5.11.3+dfsg-2                all          Web content engine library for Qt - Data
    ii  libqt5webengine5:amd64                  5.11.3+dfsg-2+b1             amd64        Web content engine library for Qt
    ii  libqt5webenginecore5:amd64              5.11.3+dfsg-2+b1             amd64        Web content engine library for Qt - Core
    ii  libqt5webkit5:amd64                     5.212.0~alpha2-21            amd64        Web content engine library for Qt
    ii  libqt5websockets5:amd64                 5.11.3-5                     amd64        Qt 5 Web Sockets module
    ii  libqt5webview5:amd64                    5.11.3-2                     amd64        display web content in a QML application - Library
    ii  libqt5widgets5:amd64                    5.11.3+dfsg1-1               amd64        Qt 5 widgets module
    ii  libqt5xml5:amd64                        5.11.3+dfsg1-1               amd64        Qt 5 XML module
    ii  libqt5xmlpatterns5:amd64                5.11.3-2                     amd64        Qt 5 XML patterns module
    ii  libquadmath0:amd64                      8.3.0-6                      amd64        GCC Quad-Precision Math Library
    ii  libre2-5:amd64                          20190101+dfsg-2              amd64        efficient, principled regular expression library
    ii  libreadline7:amd64                      7.0-5                        amd64        GNU readline and history libraries, run-time libraries
    ii  librest-0.7-0:amd64                     0.8.1-1                      amd64        REST service access library
    ii  librhash0:amd64                         1.3.8-1                      amd64        shared library for hash functions computing
    ii  librsvg2-2:amd64                        2.44.10-2.1                  amd64        SAX-based renderer library for SVG files (runtime)
    ii  librsvg2-common:amd64                   2.44.10-2.1                  amd64        SAX-based renderer library for SVG files (extra runtime)
    ii  librtmp1:amd64                          2.4+20151223.gitfa8646d.1-2  amd64        toolkit for RTMP streams (shared library)
    ii  libsasl2-2:amd64                        2.1.27+dfsg-1                amd64        Cyrus SASL - authentication abstraction library
    ii  libsasl2-modules-db:amd64               2.1.27+dfsg-1                amd64        Cyrus SASL - pluggable authentication modules (DB)
    ii  libseccomp2:amd64                       2.3.3-4                      amd64        high level interface to Linux seccomp filter
    ii  libselinux1:amd64                       2.8-1+b1                     amd64        SELinux runtime shared libraries
    ii  libsemanage-common                      2.8-2                        all          Common files for SELinux policy management libraries
    ii  libsemanage1:amd64                      2.8-2                        amd64        SELinux policy management library
    ii  libsensors-config                       1:3.5.0-3                    all          lm-sensors configuration files
    ii  libsensors5:amd64                       1:3.5.0-3                    amd64        library to read temperature/voltage/fan sensors
    ii  libsepol1:amd64                         2.8-1                        amd64        SELinux library for manipulating binary security policies
    ii  libshine3:amd64                         3.1.1-2                      amd64        Fixed-point MP3 encoding library - runtime files
    ii  libslang2:amd64                         2.3.2-2                      amd64        S-Lang programming library - runtime version
    ii  libsm6:amd64                            2:1.2.3-1                    amd64        X11 Session Management library
    ii  libsmartcols1:amd64                     2.33.1-0.1                   amd64        smart column output alignment library
    ii  libsnappy1v5:amd64                      1.1.7-1                      amd64        fast compression/decompression library
    ii  libsndfile1:amd64                       1.0.28-6                     amd64        Library for reading/writing audio files
    ii  libsoup-gnome2.4-1:amd64                2.64.2-2                     amd64        HTTP library implementation in C -- GNOME support library
    ii  libsoup2.4-1:amd64                      2.64.2-2                     amd64        HTTP library implementation in C -- Shared library
    ii  libsoxr0:amd64                          0.1.2-3                      amd64        High quality 1D sample-rate conversion library
    ii  libspeex1:amd64                         1.2~rc1.2-1+b2               amd64        The Speex codec runtime library
    ii  libsqlite3-0:amd64                      3.27.2-3                     amd64        SQLite 3 shared library
    ii  libss2:amd64                            1.44.5-1+deb10u1             amd64        command-line interface parsing library
    ii  libssh-gcrypt-4:amd64                   0.8.7-1                      amd64        tiny C SSH library (gcrypt flavor)
    ii  libssh2-1:amd64                         1.8.0-2.1                    amd64        SSH2 client-side library
    ii  libssl1.1:amd64                         1.1.1c-1                     amd64        Secure Sockets Layer toolkit - shared libraries
    ii  libstdc++-8-dev:amd64                   8.3.0-6                      amd64        GNU Standard C++ Library v3 (development files)
    ii  libstdc++6:amd64                        8.3.0-6                      amd64        GNU Standard C++ Library v3
    ii  libswresample3:amd64                    7:4.1.4-1~deb10u1            amd64        FFmpeg library for audio resampling, rematrixing etc. - runtime files
    ii  libsystemd0:amd64                       241-7~deb10u1                amd64        systemd utility library
    ii  libtasn1-6:amd64                        4.13-3                       amd64        Manage ASN.1 structures (runtime)
    ii  libthai-data                            0.1.28-2                     all          Data files for Thai language support library
    ii  libthai0:amd64                          0.1.28-2                     amd64        Thai language support library
    ii  libtheora0:amd64                        1.1.1+dfsg.1-15              amd64        Theora Video Compression Codec
    ii  libtiff5:amd64                          4.0.10-4                     amd64        Tag Image File Format (TIFF) library
    ii  libtinfo-dev:amd64                      6.1+20181013-2+deb10u1       amd64        transitional package for libncurses-dev
    ii  libtinfo6:amd64                         6.1+20181013-2+deb10u1       amd64        shared low-level terminfo library for terminal handling
    ii  libtsan0:amd64                          8.3.0-6                      amd64        ThreadSanitizer -- a Valgrind-based detector of data races (runtime)
    ii  libtspi1                                0.3.14+fixed1-1              amd64        open-source TCG Software Stack (library)
    ii  libtwolame0:amd64                       0.3.13-4                     amd64        MPEG Audio Layer 2 encoding library
    ii  libubsan1:amd64                         8.3.0-6                      amd64        UBSan -- undefined behaviour sanitizer (runtime)
    ii  libudev1:amd64                          241-7~deb10u1                amd64        libudev shared library
    ii  libunistring2:amd64                     0.9.10-1                     amd64        Unicode string library for C
    ii  libusb-1.0-0:amd64                      2:1.0.22-2                   amd64        userspace USB programming library
    ii  libutempter0:amd64                      1.1.6-3                      amd64        privileged helper for utmp/wtmp updates (runtime)
    ii  libuuid1:amd64                          2.33.1-0.1                   amd64        Universally Unique ID library
    ii  libuv1:amd64                            1.24.1-1                     amd64        asynchronous event notification library - runtime library
    ii  libva-drm2:amd64                        2.4.0-1                      amd64        Video Acceleration (VA) API for Linux -- DRM runtime
    ii  libva-x11-2:amd64                       2.4.0-1                      amd64        Video Acceleration (VA) API for Linux -- X11 runtime
    ii  libva2:amd64                            2.4.0-1                      amd64        Video Acceleration (VA) API for Linux -- runtime
    ii  libvdpau-va-gl1:amd64                   0.4.2-1+b1                   amd64        VDPAU driver with OpenGL/VAAPI backend
    ii  libvdpau1:amd64                         1.1.1-10                     amd64        Video Decode and Presentation API for Unix (libraries)
    ii  libvisual-0.4-0:amd64                   0.4.0-15                     amd64        audio visualization framework
    ii  libvorbis0a:amd64                       1.3.6-2                      amd64        decoder library for Vorbis General Audio Compression Codec
    ii  libvorbisenc2:amd64                     1.3.6-2                      amd64        encoder library for Vorbis General Audio Compression Codec
    ii  libvorbisfile3:amd64                    1.3.6-2                      amd64        high-level API for Vorbis General Audio Compression Codec
    ii  libvpx5:amd64                           1.7.0-3                      amd64        VP8 and VP9 video codec (shared library)
    ii  libvulkan-dev:amd64                     1.1.97-2                     amd64        Vulkan loader library -- development files
    ii  libvulkan1:amd64                        1.1.97-2                     amd64        Vulkan loader library
    ii  libwacom-bin                            0.32-1                       amd64        Wacom model feature query library -- binaries
    ii  libwacom-common                         0.32-1                       all          Wacom model feature query library (common files)
    ii  libwacom2:amd64                         0.32-1                       amd64        Wacom model feature query library
    ii  libwavpack1:amd64                       5.1.0-6                      amd64        audio codec (lossy and lossless) - library
    ii  libwayland-client0:amd64                1.16.0-1                     amd64        wayland compositor infrastructure - client library
    ii  libwayland-cursor0:amd64                1.16.0-1                     amd64        wayland compositor infrastructure - cursor library
    ii  libwayland-egl1:amd64                   1.16.0-1                     amd64        wayland compositor infrastructure - EGL library
    ii  libwayland-server0:amd64                1.16.0-1                     amd64        wayland compositor infrastructure - server library
    ii  libwebp6:amd64                          0.6.1-2                      amd64        Lossy compression of digital photographic images.
    ii  libwebpdemux2:amd64                     0.6.1-2                      amd64        Lossy compression of digital photographic images.
    ii  libwebpmux3:amd64                       0.6.1-2                      amd64        Lossy compression of digital photographic images.
    ii  libwoff1:amd64                          1.0.2-1                      amd64        library for converting fonts to WOFF 2.0
    ii  libwrap0:amd64                          7.6.q-28                     amd64        Wietse Venema's TCP wrappers library
    ii  libx11-6:amd64                          2:1.6.7-1                    amd64        X11 client-side library
    ii  libx11-data                             2:1.6.7-1                    all          X11 client-side library
    ii  libx11-dev:amd64                        2:1.6.7-1                    amd64        X11 client-side library (development headers)
    ii  libx11-xcb-dev:amd64                    2:1.6.7-1                    amd64        Xlib/XCB interface library (development headers)
    ii  libx11-xcb1:amd64                       2:1.6.7-1                    amd64        Xlib/XCB interface library
    ii  libx264-155:amd64                       2:0.155.2917+git0a84d98-2    amd64        x264 video coding library
    ii  libx265-165:amd64                       2.9-4                        amd64        H.265/HEVC video stream encoder (shared library)
    ii  libxau-dev:amd64                        1:1.0.8-1+b2                 amd64        X11 authorisation library (development headers)
    ii  libxau6:amd64                           1:1.0.8-1+b2                 amd64        X11 authorisation library
    ii  libxaw7:amd64                           2:1.0.13-1+b2                amd64        X11 Athena Widget library
    ii  libxcb-dri2-0:amd64                     1.13.1-2                     amd64        X C Binding, dri2 extension
    ii  libxcb-dri2-0-dev:amd64                 1.13.1-2                     amd64        X C Binding, dri2 extension, development files
    ii  libxcb-dri3-0:amd64                     1.13.1-2                     amd64        X C Binding, dri3 extension
    ii  libxcb-dri3-dev:amd64                   1.13.1-2                     amd64        X C Binding, dri3 extension, development files
    ii  libxcb-glx0:amd64                       1.13.1-2                     amd64        X C Binding, glx extension
    ii  libxcb-glx0-dev:amd64                   1.13.1-2                     amd64        X C Binding, glx extension, development files
    ii  libxcb-icccm4:amd64                     0.4.1-1.1                    amd64        utility libraries for X C Binding -- icccm
    ii  libxcb-image0:amd64                     0.4.0-1+b2                   amd64        utility libraries for X C Binding -- image
    ii  libxcb-keysyms1:amd64                   0.4.0-1+b2                   amd64        utility libraries for X C Binding -- keysyms
    ii  libxcb-present-dev:amd64                1.13.1-2                     amd64        X C Binding, present extension, development files
    ii  libxcb-present0:amd64                   1.13.1-2                     amd64        X C Binding, present extension
    ii  libxcb-randr0:amd64                     1.13.1-2                     amd64        X C Binding, randr extension
    ii  libxcb-randr0-dev:amd64                 1.13.1-2                     amd64        X C Binding, randr extension, development files
    ii  libxcb-render-util0:amd64               0.3.9-1+b1                   amd64        utility libraries for X C Binding -- render-util
    ii  libxcb-render0:amd64                    1.13.1-2                     amd64        X C Binding, render extension
    ii  libxcb-render0-dev:amd64                1.13.1-2                     amd64        X C Binding, render extension, development files
    ii  libxcb-shape0:amd64                     1.13.1-2                     amd64        X C Binding, shape extension
    ii  libxcb-shape0-dev:amd64                 1.13.1-2                     amd64        X C Binding, shape extension, development files
    ii  libxcb-shm0:amd64                       1.13.1-2                     amd64        X C Binding, shm extension
    ii  libxcb-sync-dev:amd64                   1.13.1-2                     amd64        X C Binding, sync extension, development files
    ii  libxcb-sync1:amd64                      1.13.1-2                     amd64        X C Binding, sync extension
    ii  libxcb-util0:amd64                      0.3.8-3+b2                   amd64        utility libraries for X C Binding -- atom, aux and event
    ii  libxcb-xfixes0:amd64                    1.13.1-2                     amd64        X C Binding, xfixes extension
    ii  libxcb-xfixes0-dev:amd64                1.13.1-2                     amd64        X C Binding, xfixes extension, development files
    ii  libxcb-xinerama0:amd64                  1.13.1-2                     amd64        X C Binding, xinerama extension
    ii  libxcb-xkb1:amd64                       1.13.1-2                     amd64        X C Binding, XKEYBOARD extension
    ii  libxcb1:amd64                           1.13.1-2                     amd64        X C Binding
    ii  libxcb1-dev:amd64                       1.13.1-2                     amd64        X C Binding, development files
    ii  libxcomposite1:amd64                    1:0.4.4-2                    amd64        X11 Composite extension library
    ii  libxcursor1:amd64                       1:1.1.15-2                   amd64        X cursor management library
    ii  libxdamage-dev:amd64                    1:1.1.4-3+b3                 amd64        X11 damaged region extension library (development headers)
    ii  libxdamage1:amd64                       1:1.1.4-3+b3                 amd64        X11 damaged region extension library
    ii  libxdmcp-dev:amd64                      1:1.1.2-3                    amd64        X11 authorisation library (development headers)
    ii  libxdmcp6:amd64                         1:1.1.2-3                    amd64        X11 Display Manager Control Protocol library
    ii  libxext-dev:amd64                       2:1.3.3-1+b2                 amd64        X11 miscellaneous extensions library (development headers)
    ii  libxext6:amd64                          2:1.3.3-1+b2                 amd64        X11 miscellaneous extension library
    ii  libxfixes-dev:amd64                     1:5.0.3-1                    amd64        X11 miscellaneous 'fixes' extension library (development headers)
    ii  libxfixes3:amd64                        1:5.0.3-1                    amd64        X11 miscellaneous 'fixes' extension library
    ii  libxft2:amd64                           2.3.2-2                      amd64        FreeType-based font drawing library for X
    ii  libxi6:amd64                            2:1.7.9-1                    amd64        X11 Input extension library
    ii  libxinerama1:amd64                      2:1.1.4-2                    amd64        X11 Xinerama extension library
    ii  libxkbcommon-x11-0:amd64                0.8.2-1                      amd64        library to create keymaps with the XKB X11 protocol
    ii  libxkbcommon0:amd64                     0.8.2-1                      amd64        library interface to the XKB compiler - shared library
    ii  libxml2:amd64                           2.9.4+dfsg1-7+b3             amd64        GNOME XML library
    ii  libxmu6:amd64                           2:1.1.2-2+b3                 amd64        X11 miscellaneous utility library
    ii  libxmuu1:amd64                          2:1.1.2-2+b3                 amd64        X11 miscellaneous micro-utility library
    ii  libxpm4:amd64                           1:3.5.12-1                   amd64        X11 pixmap library
    ii  libxrandr2:amd64                        2:1.5.1-1                    amd64        X11 RandR extension library
    ii  libxrender1:amd64                       1:0.9.10-1                   amd64        X Rendering Extension client library
    ii  libxshmfence-dev:amd64                  1.3-1                        amd64        X shared memory fences - development files
    ii  libxshmfence1:amd64                     1.3-1                        amd64        X shared memory fences - shared library
    ii  libxslt1.1:amd64                        1.1.32-2.1~deb10u1           amd64        XSLT 1.0 processing library - runtime library
    ii  libxss1:amd64                           1:1.2.3-1                    amd64        X11 Screen Saver extension library
    ii  libxt6:amd64                            1:1.1.5-1+b3                 amd64        X11 toolkit intrinsics library
    ii  libxtst6:amd64                          2:1.2.3-1                    amd64        X11 Testing -- Record extension library
    ii  libxv1:amd64                            2:1.0.11-1                   amd64        X11 Video extension library
    ii  libxvidcore4:amd64                      2:1.3.5-1                    amd64        Open source MPEG-4 video codec (library)
    ii  libxxf86dga1:amd64                      2:1.1.4-1+b3                 amd64        X11 Direct Graphics Access extension library
    ii  libxxf86vm-dev:amd64                    1:1.1.4-1+b2                 amd64        X11 XFree86 video mode extension library (development headers)
    ii  libxxf86vm1:amd64                       1:1.1.4-1+b2                 amd64        X11 XFree86 video mode extension library
    ii  libzstd1:amd64                          1.3.8+dfsg-3                 amd64        fast lossless compression algorithm
    ii  libzvbi-common                          0.2.35-16                    all          Vertical Blanking Interval decoder (VBI) - common files
    ii  libzvbi0:amd64                          0.2.35-16                    amd64        Vertical Blanking Interval decoder (VBI) - runtime files
    ii  linux-libc-dev:amd64                    4.19.67-2                    amd64        Linux support headers for userspace development
    ii  llvm-7                                  1:7.0.1-8                    amd64        Modular compiler and toolchain technologies
    ii  llvm-7-dev                              1:7.0.1-8                    amd64        Modular compiler and toolchain technologies, libraries and headers
    ii  llvm-7-runtime                          1:7.0.1-8                    amd64        Modular compiler and toolchain technologies, IR interpreter
    ii  localepurge                             0.7.3.5                      all          reclaim disk space by removing unneeded localizations
    ii  locales                                 2.28-10                      all          GNU C Library: National Language (locale) data [support]
    ii  login                                   1:4.5-1.1                    amd64        system login tools
    ii  lsb-base                                10.2019051400                all          Linux Standard Base init script functionality
    ii  make                                    4.2.1-1.2                    amd64        utility for directing compilation
    ii  manpages                                4.16-2                       all          Manual pages about using a GNU/Linux system
    ii  manpages-dev                            4.16-2                       all          Manual pages about using GNU/Linux for development
    ii  mawk                                    1.3.3-17+b3                  amd64        a pattern scanning and text processing language
    ii  mesa-common-dev:amd64                   18.3.6-2                     amd64        Developer documentation for Mesa
    ii  mesa-va-drivers:amd64                   18.3.6-2                     amd64        Mesa VA-API video acceleration drivers
    ii  mesa-vdpau-drivers:amd64                18.3.6-2                     amd64        Mesa VDPAU video acceleration drivers
    ii  mime-support                            3.62                         all          MIME files 'mime.types' & 'mailcap', and support programs
    ii  modemmanager                            1.10.0-1                     amd64        D-Bus service for managing modems
    ii  mount                                   2.33.1-0.1                   amd64        tools for mounting and manipulating filesystems
    ii  ncurses-base                            6.1+20181013-2+deb10u1       all          basic terminal type definitions
    ii  ncurses-bin                             6.1+20181013-2+deb10u1       amd64        terminal-related programs and man pages
    ii  net-tools                               1.60+git20180626.aebd88e-1   amd64        NET-3 networking toolkit
    ii  notification-daemon                     3.20.0-4                     amd64        daemon for displaying passive pop-up notifications
    ii  openssl                                 1.1.1c-1                     amd64        Secure Sockets Layer toolkit - cryptographic utility
    ii  passwd                                  1:4.5-1.1                    amd64        change and administer password and group data
    ii  patch                                   2.7.6-3+deb10u1              amd64        Apply a diff file to an original
    ii  perl                                    5.28.1-6                     amd64        Larry Wall's Practical Extraction and Report Language
    ii  perl-base                               5.28.1-6                     amd64        minimal Perl system
    ii  perl-modules-5.28                       5.28.1-6                     all          Core Perl modules
    ii  pinentry-curses                         1.1.0-2                      amd64        curses-based PIN or pass-phrase entry dialog for GnuPG
    ii  procps                                  2:3.3.15-2                   amd64        /proc file system utilities
    ii  psmisc                                  23.2-1                       amd64        utilities that use the proc file system
    ii  python                                  2.7.16-1                     amd64        interactive high-level object-oriented language (Python2 version)
    ii  python-minimal                          2.7.16-1                     amd64        minimal subset of the Python2 language
    ii  python2                                 2.7.16-1                     amd64        interactive high-level object-oriented language (Python2 version)
    ii  python2-minimal                         2.7.16-1                     amd64        minimal subset of the Python2 language
    ii  python2.7                               2.7.16-2                     amd64        Interactive high-level object-oriented language (version 2.7)
    ii  python2.7-minimal                       2.7.16-2                     amd64        Minimal subset of the Python language (version 2.7)
    ii  qbs-common                              1.12.2+dfsg-2                all          Qbs static files
    ii  qdoc-qt5                                5.11.3-4                     amd64        Qt 5 qdoc tool
    ii  qml                                     5.11.3-4                     amd64        Qt 5 QML viewer
    ii  qml-module-qtcharts:amd64               5.11.3-2                     amd64        Qt charts QML module
    ii  qml-module-qtgraphicaleffects:amd64     5.11.3-2                     amd64        Qt 5 Graphical Effects module
    ii  qml-module-qtmultimedia:amd64           5.11.3-2                     amd64        Qt 5 Multimedia QML module
    ii  qml-module-qtqml-models2:amd64          5.11.3-4                     amd64        Qt 5 Models2 QML module
    ii  qml-module-qtquick-controls:amd64       5.11.3-2                     amd64        Qt 5 Quick Controls QML module
    ii  qml-module-qtquick-controls2:amd64      5.11.3+dfsg-2                amd64        Qt 5 Qt Quick Controls 2 QML module
    ii  qml-module-qtquick-dialogs:amd64        5.11.3-2                     amd64        Qt 5 Dialogs QML module
    ii  qml-module-qtquick-extras:amd64         5.11.3-2                     amd64        Qt 5 Quick Extras QML module
    ii  qml-module-qtquick-layouts:amd64        5.11.3-4                     amd64        Qt 5 Quick Layouts QML module
    ii  qml-module-qtquick-localstorage:amd64   5.11.3-4                     amd64        Qt 5 localstorage QML module
    ii  qml-module-qtquick-privatewidgets:amd64 5.11.3-2                     amd64        Qt 5 Private Widgets QML module
    ii  qml-module-qtquick-templates2:amd64     5.11.3+dfsg-2                amd64        Qt 5 Qt Quick Templates 2 QML module
    ii  qml-module-qtquick-window2:amd64        5.11.3-4                     amd64        Qt 5 window 2 QML module
    ii  qml-module-qtquick-xmllistmodel:amd64   5.11.3-4                     amd64        Qt 5 xmllistmodel QML module
    ii  qml-module-qtquick2:amd64               5.11.3-4                     amd64        Qt 5 Qt Quick 2 QML module
    ii  qml-module-qttest:amd64                 5.11.3-4                     amd64        Qt 5 test QML module
    ii  qml-module-qtwebengine:amd64            5.11.3+dfsg-2+b1             amd64        Qt WebEngine QML module
    ii  qml-module-qtwebsockets:amd64           5.11.3-5                     amd64        Qt 5 Web Sockets QML module
    ii  qml-module-qtwebview:amd64              5.11.3-2                     amd64        display web content in a QML application
    ii  qmlscene                                5.11.3-4                     amd64        Qt 5 QML scene viewer
    ii  qt3d5-doc                               5.11.3+dfsg-2                all          Qt 3D documentation
    ii  qt5-assistant                           5.11.3-4                     amd64        Qt 5 Assistant
    ii  qt5-default:amd64                       5.11.3+dfsg1-1               amd64        Qt 5 development defaults package
    ii  qt5-doc                                 5.11.3-1                     all          Qt 5 API Documentation
    ii  qt5-gtk-platformtheme:amd64             5.11.3+dfsg1-1               amd64        Qt 5 GTK+ 3 platform theme
    ii  qt5-qmake:amd64                         5.11.3+dfsg1-1               amd64        Qt 5 qmake Makefile generator tool
    ii  qt5-qmake-bin                           5.11.3+dfsg1-1               amd64        Qt 5 qmake Makefile generator tool — binary file
    ii  qt5-qmltooling-plugins:amd64            5.11.3-4                     amd64        Qt 5 qmltooling plugins
    ii  qtbase5-dev:amd64                       5.11.3+dfsg1-1               amd64        Qt 5 base development files
    ii  qtbase5-dev-tools                       5.11.3+dfsg1-1               amd64        Qt 5 base development programs
    ii  qtbase5-doc                             5.11.3+dfsg1-1               all          Qt 5 base documentation
    ii  qtcharts5-doc                           5.11.3-2                     all          Qt charts QCH documentation
    ii  qtchooser                               66-2                         amd64        Wrapper to select between Qt development binary versions
    ii  qtconnectivity5-doc                     5.11.3-2                     all          Qt 5 Connectivity documentation
    ii  qtcreator                               4.8.2-1                      amd64        integrated development environment (IDE) for Qt
    ii  qtcreator-data                          4.8.2-1                      all          application data for Qt Creator IDE
    ii  qtcreator-doc                           4.8.2-1                      all          documentation for Qt Creator IDE
    ii  qtdeclarative5-dev:amd64                5.11.3-4                     amd64        Qt 5 declarative development files
    ii  qtdeclarative5-dev-tools                5.11.3-4                     amd64        Qt 5 declarative development programs
    ii  qtdeclarative5-doc                      5.11.3-4                     all          Qt 5 declarative documentation
    ii  qtgraphicaleffects5-doc                 5.11.3-2                     all          Qt 5 graphical effects documentation
    ii  qtlocation5-doc                         5.11.3+dfsg-2                all          Qt 5 Positioning documentation
    ii  qtmultimedia5-doc                       5.11.3-2                     all          Qt 5 multimedia documentation
    ii  qtquickcontrols2-5-doc                  5.11.3+dfsg-2                all          Qt 5 Quick Controls 2 documentation
    ii  qtquickcontrols5-doc                    5.11.3-2                     all          Qt 5 Quick Controls documentation
    ii  qtscript5-doc                           5.11.3+dfsg-3                all          Qt 5 script documentation
    ii  qtsensors5-doc                          5.11.3-2                     all          Qt 5 Sensors documentation
    ii  qtserialport5-doc                       5.11.3-2                     all          Qt 5 serial port documentation
    ii  qtsvg5-doc                              5.11.3-2                     all          Qt 5 SVG documentation
    ii  qttools5-dev-tools                      5.11.3-4                     amd64        Qt 5 development tools
    ii  qttools5-doc                            5.11.3-4                     all          Qt 5 tools documentation
    ii  qttranslations5-l10n                    5.11.3-2                     all          translations for Qt 5
    ii  qtvirtualkeyboard5-doc                  5.11.3+dfsg-2                all          Qt 5 Virtual Keyboard documentation
    ii  qtwayland5-doc                          5.11.3-2                     all          Qt 5 Wayland Compositor documentation
    ii  qtwebchannel5-doc                       5.11.3-2                     all          Web communication library for Qt - Documentation
    ii  qtwebengine5-doc                        5.11.3+dfsg-2                all          Qt 5 webengine documentation
    ii  qtwebsockets5-doc                       5.11.3-5                     all          Qt 5 Web Sockets documentation
    ii  qtwebview5-doc                          5.11.3-2                     all          display web content in a QML application - Documentation
    ii  qtx11extras5-doc                        5.11.3-2                     all          Qt 5 X11 extras documentation
    ii  qtxmlpatterns5-dev-tools                5.11.3-2                     amd64        Qt 5 XML patterns development programs
    ii  qtxmlpatterns5-doc                      5.11.3-2                     all          Qt 5 XML patterns documentation
    ii  readline-common                         7.0-5                        all          GNU readline and history libraries, common files
    ii  sed                                     4.7-1                        amd64        GNU stream editor for filtering/transforming text
    ii  sensible-utils                          0.0.12                       all          Utilities for sensible alternative selection
    ii  shared-mime-info                        1.10-1                       amd64        FreeDesktop.org shared MIME database and spec
    ii  systemd                                 241-7~deb10u1                amd64        system and service manager
    ii  systemd-sysv                            241-7~deb10u1                amd64        system and service manager - SysV links
    ii  sysvinit-utils                          2.93-8                       amd64        System-V-like utilities
    ii  tar                                     1.30+dfsg-6                  amd64        GNU version of the tar archiving utility
    ii  tzdata                                  2019b-0+deb10u1              all          time zone and daylight-saving time data
    ii  ucf                                     3.0038+nmu1                  all          Update Configuration File(s): preserve user changes to config files
    ii  udev                                    241-7~deb10u1                amd64        /dev/ and hotplug management daemon
    ii  unzip                                   6.0-23+deb10u1               amd64        De-archiver for .zip files
    ii  usb-modeswitch                          2.5.2+repack0-2              amd64        mode switching tool for controlling "flip flop" USB devices
    ii  usb-modeswitch-data                     20170806-2                   all          mode switching data for usb-modeswitch
    ii  util-linux                              2.33.1-0.1                   amd64        miscellaneous system utilities
    ii  va-driver-all:amd64                     2.4.0-1                      amd64        Video Acceleration (VA) API -- driver metapackage
    ii  vdpau-driver-all:amd64                  1.1.1-10                     amd64        Video Decode and Presentation API for Unix (driver metapackage)
    ii  whiptail                                0.52.20-8                    amd64        Displays user-friendly dialog boxes from shell scripts
    ii  wpasupplicant                           2:2.7+git20190128+0c1e29f-6  amd64        client support for WPA and WPA2 (IEEE 802.11i)
    ii  x11-common                              1:7.7+19                     all          X Window System (X.Org) infrastructure
    ii  x11-utils                               7.7+4                        amd64        X11 utilities
    ii  x11proto-core-dev                       2018.4-4                     all          transitional dummy package
    ii  x11proto-damage-dev                     1:2018.4-4                   all          transitional dummy package
    ii  x11proto-dev                            2018.4-4                     all          X11 extension protocols and auxiliary headers
    ii  x11proto-fixes-dev                      1:2018.4-4                   all          transitional dummy package
    ii  x11proto-xext-dev                       2018.4-4                     all          transitional dummy package
    ii  x11proto-xf86vidmode-dev                2018.4-4                     all          transitional dummy package
    ii  xbitmaps                                1.1.1-2                      all          Base X bitmaps
    ii  xdg-user-dirs                           0.17-2                       amd64        tool to manage well known user directories
    ii  xkb-data                                2.26-2                       all          X Keyboard Extension (XKB) configuration data
    ii  xorg-sgml-doctools                      1:1.11-1                     all          Common tools for building X.Org SGML documentation
    ii  xtail                                   2.1-6                        amd64        like "tail -f", but works on truncated files, directories, more
    ii  xterm                                   344-1                        amd64        X terminal emulator
    ii  xtrans-dev                              1.3.5-1                      all          X transport library (development files)
    ii  xz-utils                                5.2.4-1                      amd64        XZ-format compression utilities
    ii  zlib1g:amd64                            1:1.2.11.dfsg-1              amd64        compression library - runtime
