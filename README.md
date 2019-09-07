# buster-qml

![Pulls](https://img.shields.io/docker/pulls/mkovac/buster-qml.svg)
![Stars](https://img.shields.io/docker/stars/mkovac/buster-qml.svg)

My QML/Qt5 development environment with QtCreator,
a [container image](https://hub.docker.com/r/mkovac/buster-qml/) 
based on [Debian](https://debian.org/) [Buster](https://wiki.debian.org/DebianBuster).

This image is built daily and in case of any security update, the list of
packages is updated, commited and this triggers update of docker-hub image
and all dependant images.

## Quick Usage

Run prebuilt:

    $ docker run --rm -ti --env DISPLAY=$DISPLAY \
        --volume /tmp/.X11-unix:/tmp/.X11-unix:ro mkovac/buster-qml qtcreator

    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name                                 Version                        Architecture Description
    +++-====================================-==============================-============-===============================================================================
    ii  adduser                              3.115                          all          add and remove users and groups
    ii  adwaita-icon-theme                   3.22.0-1+deb9u1                all          default icon theme of GNOME
    ii  apt                                  1.4.9                          amd64        commandline package manager
    ii  apt-utils                            1.4.9                          amd64        package management related utility programs
    ii  at-spi2-core                         2.22.0-6+deb9u1                amd64        Assistive Technology Service Provider Interface (dbus core)
    ii  base-files                           9.9+deb9u10                    amd64        Debian base system miscellaneous files
    ii  base-passwd                          3.5.43                         amd64        Debian base system master password and group files
    ii  bash                                 4.4-5                          amd64        GNU Bourne Again SHell
    ii  binfmt-support                       2.1.6-2                        amd64        Support for extra binary formats
    ii  binutils                             2.28-5                         amd64        GNU assembler, linker and binary utilities
    ii  bsdutils                             1:2.29.2-1+deb9u1              amd64        basic utilities from 4.4BSD-Lite
    ii  build-essential                      12.3                           amd64        Informational list of build-essential packages
    ii  bzip2                                1.0.6-8.1                      amd64        high-quality block-sorting file compressor - utilities
    ii  ca-certificates                      20161130+nmu1+deb9u1           all          Common CA certificates
    ii  chromium                             73.0.3683.75-1~deb9u1          amd64        web browser
    ii  clang                                1:3.8-36                       amd64        C, C++ and Objective-C compiler (LLVM based)
    ii  clang-3.8                            1:3.8.1-24                     amd64        C, C++ and Objective-C compiler (LLVM based)
    ii  cmake                                3.7.2-1                        amd64        cross-platform, open-source make system
    ii  cmake-data                           3.7.2-1                        all          CMake data files (modules, templates and documentation)
    ii  coreutils                            8.26-3                         amd64        GNU core utilities
    ii  cpp                                  4:6.3.0-4                      amd64        GNU C preprocessor (cpp)
    ii  cpp-6                                6.3.0-18+deb9u1                amd64        GNU C preprocessor
    ii  curl                                 7.52.1-5+deb9u9                amd64        command line tool for transferring data with URL syntax
    ii  dash                                 0.5.8-2.4                      amd64        POSIX-compliant shell
    ii  dbus                                 1.10.28-0+deb9u1               amd64        simple interprocess messaging system (daemon and utilities)
    ii  dconf-gsettings-backend:amd64        0.26.0-2+b1                    amd64        simple configuration storage system - GSettings back-end
    ii  dconf-service                        0.26.0-2+b1                    amd64        simple configuration storage system - D-Bus service
    ii  debconf                              1.5.61                         all          Debian configuration management system
    ii  debian-archive-keyring               2017.5+deb9u1                  all          GnuPG archive keys of the Debian archive
    ii  debianutils                          4.8.1.1                        amd64        Miscellaneous utilities specific to Debian
    ii  di                                   4.34-2+b1                      amd64        advanced df like disk information utility
    ii  diffutils                            1:3.5-3                        amd64        File comparison utilities
    ii  dirmngr                              2.1.18-8~deb9u4                amd64        GNU privacy guard - network certificate management service
    ii  dpkg                                 1.18.25                        amd64        Debian package management system
    ii  dpkg-dev                             1.18.25                        all          Debian package development tools
    ii  e2fslibs:amd64                       1.43.4-2                       amd64        ext2/ext3/ext4 file system libraries
    ii  e2fsprogs                            1.43.4-2                       amd64        ext2/ext3/ext4 file system utilities
    ii  etckeeper                            1.18.5-1                       all          store /etc in git, mercurial, bzr or darcs
    ii  fakeroot                             1.21-3.1                       amd64        tool for simulating superuser privileges
    ii  findutils                            4.6.0+git+20161106-2           amd64        utilities for finding files--find, xargs
    ii  fontconfig                           2.11.0-6.7+b1                  amd64        generic font configuration library - support binaries
    ii  fontconfig-config                    2.11.0-6.7                     all          generic font configuration library - configuration
    ii  fonts-dejavu-core                    2.37-1                         all          Vera font family derivate with additional characters
    ii  fonts-liberation                     1:1.07.4-2                     all          Fonts with the same metrics as Times, Arial and Courier
    ii  g++                                  4:6.3.0-4                      amd64        GNU C++ compiler
    ii  g++-6                                6.3.0-18+deb9u1                amd64        GNU C++ compiler
    ii  gcc                                  4:6.3.0-4                      amd64        GNU C compiler
    ii  gcc-6                                6.3.0-18+deb9u1                amd64        GNU C compiler
    ii  gcc-6-base:amd64                     6.3.0-18+deb9u1                amd64        GCC, the GNU Compiler Collection (base package)
    ii  gdb                                  7.12-6                         amd64        GNU Debugger
    ii  git                                  1:2.11.0-3+deb9u4              amd64        fast, scalable, distributed revision control system
    ii  git-man                              1:2.11.0-3+deb9u4              all          fast, scalable, distributed revision control system (manual pages)
    ii  glib-networking:amd64                2.50.0-1+b1                    amd64        network-related giomodules for GLib
    ii  glib-networking-common               2.50.0-1                       all          network-related giomodules for GLib - data files
    ii  glib-networking-services             2.50.0-1+b1                    amd64        network-related giomodules for GLib - D-Bus services
    ii  gnome-icon-theme                     3.12.0-2                       all          GNOME Desktop icon theme
    ii  gnupg                                2.1.18-8~deb9u4                amd64        GNU privacy guard - a free PGP replacement
    ii  gnupg-agent                          2.1.18-8~deb9u4                amd64        GNU privacy guard - cryptographic agent
    ii  gnupg-l10n                           2.1.18-8~deb9u4                all          GNU privacy guard - localization files
    ii  gpgv                                 2.1.18-8~deb9u4                amd64        GNU privacy guard - signature verification tool
    ii  grep                                 2.27-2                         amd64        GNU grep, egrep and fgrep
    ii  gsettings-desktop-schemas            3.22.0-1                       all          GSettings desktop-wide schemas
    ii  gstreamer1.0-plugins-base:amd64      1.10.4-1+deb9u1                amd64        GStreamer plugins from the "base" set
    ii  gtk-update-icon-cache                3.22.11-1                      amd64        icon theme caching utility
    ii  gzip                                 1.6-5+b1                       amd64        GNU compression utilities
    ii  hicolor-icon-theme                   0.15-1                         all          default fallback theme for FreeDesktop.org icon themes
    ii  hostname                             3.18+b1                        amd64        utility to set/show the host name or domain name
    ii  i965-va-driver:amd64                 1.7.3-1                        amd64        VAAPI driver for Intel G45 & HD Graphics family
    ii  init-system-helpers                  1.48                           all          helper tools for all init systems
    ii  iso-codes                            3.75-1                         all          ISO language, territory, currency, script codes and their translations
    ii  joe                                  4.4-1                          amd64        user friendly full screen text editor
    ii  less                                 481-2.1                        amd64        pager program similar to more
    ii  libaacs0:amd64                       0.8.1-2                        amd64        free-and-libre implementation of AACS
    ii  libacl1:amd64                        2.2.52-3+b1                    amd64        Access control list shared library
    ii  libalgorithm-diff-perl               1.19.03-1                      all          module to find differences between files
    ii  libalgorithm-diff-xs-perl            0.04-4+b2                      amd64        module to find differences between files (XS accelerated)
    ii  libalgorithm-merge-perl              0.08-3                         all          Perl module for three-way merge of textual data
    ii  libapparmor1:amd64                   2.11.0-3+deb9u2                amd64        changehat AppArmor library
    ii  libapt-inst2.0:amd64                 1.4.9                          amd64        deb package format runtime library
    ii  libapt-pkg5.0:amd64                  1.4.9                          amd64        package management runtime library
    ii  libarchive13:amd64                   3.2.2-2+deb9u1                 amd64        Multi-format archive and compression library (shared library)
    ii  libasan3:amd64                       6.3.0-18+deb9u1                amd64        AddressSanitizer -- a fast memory error detector
    ii  libasound2:amd64                     1.1.3-5                        amd64        shared library for ALSA applications
    ii  libasound2-data                      1.1.3-5                        all          Configuration files and profiles for ALSA drivers
    ii  libassuan0:amd64                     2.4.3-2                        amd64        IPC library for the GnuPG components
    ii  libasyncns0:amd64                    0.8-6                          amd64        Asynchronous name service query library
    ii  libatk-bridge2.0-0:amd64             2.22.0-2                       amd64        AT-SPI 2 toolkit bridge - shared library
    ii  libatk1.0-0:amd64                    2.22.0-1                       amd64        ATK accessibility toolkit
    ii  libatk1.0-data                       2.22.0-1                       all          Common files for the ATK accessibility toolkit
    ii  libatomic1:amd64                     6.3.0-18+deb9u1                amd64        support library providing __atomic built-in functions
    ii  libatspi2.0-0:amd64                  2.22.0-6+deb9u1                amd64        Assistive Technology Service Provider Interface - shared library
    ii  libattr1:amd64                       1:2.4.47-2+b2                  amd64        Extended attribute shared library
    ii  libaudit-common                      1:2.6.7-2                      all          Dynamic library for security auditing - common files
    ii  libaudit1:amd64                      1:2.6.7-2                      amd64        Dynamic library for security auditing
    ii  libauthen-sasl-perl                  2.1600-1                       all          Authen::SASL - SASL Authentication framework
    ii  libavahi-client3:amd64               0.6.32-2                       amd64        Avahi client library
    ii  libavahi-common-data:amd64           0.6.32-2                       amd64        Avahi common data files
    ii  libavahi-common3:amd64               0.6.32-2                       amd64        Avahi common library
    ii  libavcodec57:amd64                   7:3.2.14-1~deb9u1              amd64        FFmpeg library with de/encoders for audio/video codecs - runtime files
    ii  libavformat57:amd64                  7:3.2.14-1~deb9u1              amd64        FFmpeg library with (de)muxers for multimedia containers - runtime files
    ii  libavutil55:amd64                    7:3.2.14-1~deb9u1              amd64        FFmpeg library with functions for simplifying programming - runtime files
    ii  libbabeltrace-ctf1:amd64             1.5.1-1                        amd64        Common Trace Format (CTF) library
    ii  libbabeltrace1:amd64                 1.5.1-1                        amd64        Babeltrace conversion libraries
    ii  libbdplus0:amd64                     0.1.2-2                        amd64        implementation of BD+ for reading Blu-ray Discs
    ii  libblkid1:amd64                      2.29.2-1+deb9u1                amd64        block device ID library
    ii  libbluray1:amd64                     1:0.9.3-3                      amd64        Blu-ray disc playback support library (shared library)
    ii  libbotan-1.10-1                      1.10.16-1                      amd64        multiplatform crypto library
    ii  libbsd0:amd64                        0.8.3-1                        amd64        utility functions from BSD systems - shared library
    ii  libbz2-1.0:amd64                     1.0.6-8.1                      amd64        high-quality block-sorting file compressor library - runtime
    ii  libc-bin                             2.24-11+deb9u4                 amd64        GNU C Library: Binaries
    ii  libc-dev-bin                         2.24-11+deb9u4                 amd64        GNU C Library: Development binaries
    ii  libc-l10n                            2.24-11+deb9u4                 all          GNU C Library: localization files
    ii  libc6:amd64                          2.24-11+deb9u4                 amd64        GNU C Library: Shared libraries
    ii  libc6-dbg:amd64                      2.24-11+deb9u4                 amd64        GNU C Library: detached debugging symbols
    ii  libc6-dev:amd64                      2.24-11+deb9u4                 amd64        GNU C Library: Development Libraries and Header Files
    ii  libcairo-gobject2:amd64              1.14.8-1                       amd64        Cairo 2D vector graphics library (GObject library)
    ii  libcairo2:amd64                      1.14.8-1                       amd64        Cairo 2D vector graphics library
    ii  libcap-ng0:amd64                     0.7.7-3+b1                     amd64        An alternate POSIX capabilities library
    ii  libcap2:amd64                        1:2.25-1                       amd64        POSIX 1003.1e capabilities (library)
    ii  libcap2-bin                          1:2.25-1                       amd64        POSIX 1003.1e capabilities (utilities)
    ii  libcc1-0:amd64                       6.3.0-18+deb9u1                amd64        GCC cc1 plugin for GDB
    ii  libcdparanoia0:amd64                 3.10.2+debian-11               amd64        audio extraction tool for sampling CDs (library)
    ii  libchromaprint1:amd64                1.4.2-1                        amd64        audio fingerprint library
    ii  libcilkrts5:amd64                    6.3.0-18+deb9u1                amd64        Intel Cilk Plus language extensions (runtime)
    ii  libclang-common-3.8-dev              1:3.8.1-24                     amd64        clang library - Common development package
    ii  libclang1-3.8:amd64                  1:3.8.1-24                     amd64        C interface to the clang library
    ii  libclang1-3.9:amd64                  1:3.9.1-9                      amd64        C interface to the clang library
    ii  libcolord2:amd64                     1.3.3-2                        amd64        system service to manage device colour profiles -- runtime
    ii  libcomerr2:amd64                     1.43.4-2                       amd64        common error description library
    ii  libcroco3:amd64                      0.6.11-3                       amd64        Cascading Style Sheet (CSS) parsing and manipulation toolkit
    ii  libcrystalhd3:amd64                  1:0.0~git20110715.fdd2f19-12   amd64        Crystal HD Video Decoder (shared library)
    ii  libcups2:amd64                       2.2.1-8+deb9u4                 amd64        Common UNIX Printing System(tm) - Core library
    ii  libcurl3:amd64                       7.52.1-5+deb9u9                amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
    ii  libcurl3-gnutls:amd64                7.52.1-5+deb9u9                amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
    ii  libdatrie1:amd64                     0.2.10-4+b1                    amd64        Double-array trie library
    ii  libdb5.3:amd64                       5.3.28-12+deb9u1               amd64        Berkeley v5.3 Database Libraries [runtime]
    ii  libdbus-1-3:amd64                    1.10.28-0+deb9u1               amd64        simple interprocess messaging system (library)
    ii  libdconf1:amd64                      0.26.0-2+b1                    amd64        simple configuration storage system - runtime library
    ii  libdebconfclient0:amd64              0.227                          amd64        Debian Configuration Management System (C-implementation library)
    ii  libdouble-conversion1:amd64          2.0.1-4                        amd64        routines to convert IEEE floats to and from strings
    ii  libdpkg-perl                         1.18.25                        all          Dpkg perl modules
    ii  libdrm-amdgpu1:amd64                 2.4.74-1                       amd64        Userspace interface to amdgpu-specific kernel DRM services -- runtime
    ii  libdrm-dev:amd64                     2.4.74-1                       amd64        Userspace interface to kernel DRM services -- development files
    ii  libdrm-intel1:amd64                  2.4.74-1                       amd64        Userspace interface to intel-specific kernel DRM services -- runtime
    ii  libdrm-nouveau2:amd64                2.4.74-1                       amd64        Userspace interface to nouveau-specific kernel DRM services -- runtime
    ii  libdrm-radeon1:amd64                 2.4.74-1                       amd64        Userspace interface to radeon-specific kernel DRM services -- runtime
    ii  libdrm2:amd64                        2.4.74-1                       amd64        Userspace interface to kernel DRM services -- runtime
    ii  libdw1:amd64                         0.168-1                        amd64        library that provides access to the DWARF debug information
    ii  libedit2:amd64                       3.1-20160903-3                 amd64        BSD editline and history libraries
    ii  libegl1-mesa:amd64                   13.0.6-1+b2                    amd64        free implementation of the EGL API -- runtime
    ii  libelf1:amd64                        0.168-1                        amd64        library to read and write ELF files
    ii  libencode-locale-perl                1.05-1                         all          utility to determine the locale encoding
    ii  libepoxy0:amd64                      1.3.1-2                        amd64        OpenGL function pointer management library
    ii  liberror-perl                        0.17024-1                      all          Perl module for error/exception handling in an OO-ish way
    ii  libevdev2:amd64                      1.5.6+dfsg-1                   amd64        wrapper library for evdev devices
    ii  libevent-2.0-5:amd64                 2.0.21-stable-3                amd64        Asynchronous event notification library
    ii  libexpat1:amd64                      2.2.0-2+deb9u2                 amd64        XML parsing C library - runtime library
    ii  libfakeroot:amd64                    1.21-3.1                       amd64        tool for simulating superuser privileges - shared libraries
    ii  libfdisk1:amd64                      2.29.2-1+deb9u1                amd64        fdisk partitioning library
    ii  libffi-dev:amd64                     3.2.1-6                        amd64        Foreign Function Interface library (development files)
    ii  libffi6:amd64                        3.2.1-6                        amd64        Foreign Function Interface library runtime
    ii  libfile-basedir-perl                 0.07-1                         all          Perl module to use the freedesktop basedir specification
    ii  libfile-desktopentry-perl            0.22-1                         all          Perl module to handle freedesktop .desktop files
    ii  libfile-fcntllock-perl               0.22-3+b2                      amd64        Perl module for file locking with fcntl(2)
    ii  libfile-listing-perl                 6.04-1                         all          module to parse directory listings
    ii  libfile-mimeinfo-perl                0.27-1                         all          Perl module to determine file types
    ii  libflac8:amd64                       1.3.2-1                        amd64        Free Lossless Audio Codec - runtime C library
    ii  libfont-afm-perl                     1.20-2                         all          Font::AFM - Interface to Adobe Font Metrics files
    ii  libfontconfig1:amd64                 2.11.0-6.7+b1                  amd64        generic font configuration library - runtime
    ii  libfontenc1:amd64                    1:1.1.3-1+b2                   amd64        X11 font encoding library
    ii  libfreetype6:amd64                   2.6.3-3.2                      amd64        FreeType 2 font engine, shared library files
    ii  libgail-common:amd64                 2.24.31-2                      amd64        GNOME Accessibility Implementation Library -- common modules
    ii  libgail18:amd64                      2.24.31-2                      amd64        GNOME Accessibility Implementation Library -- shared libraries
    ii  libgbm1:amd64                        13.0.6-1+b2                    amd64        generic buffer management API -- runtime
    ii  libgc1c2:amd64                       1:7.4.2-8                      amd64        conservative garbage collector for C and C++
    ii  libgcc-6-dev:amd64                   6.3.0-18+deb9u1                amd64        GCC support library (development files)
    ii  libgcc1:amd64                        1:6.3.0-18+deb9u1              amd64        GCC support library
    ii  libgcrypt20:amd64                    1.7.6-2+deb9u3                 amd64        LGPL Crypto library - runtime library
    ii  libgdbm3:amd64                       1.8.3-14                       amd64        GNU dbm database routines (runtime version)
    ii  libgdk-pixbuf2.0-0:amd64             2.36.5-2+deb9u2                amd64        GDK Pixbuf library
    ii  libgdk-pixbuf2.0-common              2.36.5-2+deb9u2                all          GDK Pixbuf library - data files
    ii  libgl1-mesa-dev:amd64                13.0.6-1+b2                    amd64        free implementation of the OpenGL API -- GLX development files
    ii  libgl1-mesa-dri:amd64                13.0.6-1+b2                    amd64        free implementation of the OpenGL API -- DRI modules
    ii  libgl1-mesa-glx:amd64                13.0.6-1+b2                    amd64        free implementation of the OpenGL API -- GLX runtime
    ii  libglapi-mesa:amd64                  13.0.6-1+b2                    amd64        free implementation of the GL API -- shared library
    ii  libglew2.0:amd64                     2.0.0-3+b1                     amd64        OpenGL Extension Wrangler - runtime environment
    ii  libglib2.0-0:amd64                   2.50.3-2+deb9u1                amd64        GLib library of C routines
    ii  libglib2.0-data                      2.50.3-2+deb9u1                all          Common files for GLib library
    ii  libglu1-mesa:amd64                   9.0.0-2.1                      amd64        Mesa OpenGL utility library (GLU)
    ii  libglu1-mesa-dev:amd64               9.0.0-2.1                      amd64        Mesa OpenGL utility library -- development files
    ii  libgme0:amd64                        0.6.0-4                        amd64        Playback library for video game music files - shared library
    ii  libgmp10:amd64                       2:6.1.2+dfsg-1                 amd64        Multiprecision arithmetic library
    ii  libgnutls30:amd64                    3.5.8-5+deb9u4                 amd64        GNU TLS library - main runtime library
    ii  libgomp1:amd64                       6.3.0-18+deb9u1                amd64        GCC OpenMP (GOMP) support library
    ii  libgpg-error0:amd64                  1.26-2                         amd64        library for common error values and messages in GnuPG components
    ii  libgraphite2-3:amd64                 1.3.10-1                       amd64        Font rendering engine for Complex Scripts -- library
    ii  libgsm1:amd64                        1.0.13-4+b2                    amd64        Shared libraries for GSM speech compressor
    ii  libgssapi-krb5-2:amd64               1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - krb5 GSS-API Mechanism
    ii  libgstreamer-plugins-base1.0-0:amd64 1.10.4-1+deb9u1                amd64        GStreamer libraries from the "base" set
    ii  libgstreamer1.0-0:amd64              1.10.4-1                       amd64        Core GStreamer libraries and elements
    ii  libgtk-3-0:amd64                     3.22.11-1                      amd64        GTK+ graphical user interface library
    ii  libgtk-3-bin                         3.22.11-1                      amd64        programs for the GTK+ graphical user interface library
    ii  libgtk-3-common                      3.22.11-1                      all          common files for the GTK+ graphical user interface library
    ii  libgtk2.0-0:amd64                    2.24.31-2                      amd64        GTK+ graphical user interface library
    ii  libgtk2.0-bin                        2.24.31-2                      amd64        programs for the GTK+ graphical user interface library
    ii  libgtk2.0-common                     2.24.31-2                      all          common files for the GTK+ graphical user interface library
    ii  libgudev-1.0-0:amd64                 230-3                          amd64        GObject-based wrapper library for libudev
    ii  libharfbuzz0b:amd64                  1.4.2-1                        amd64        OpenType text shaping engine (shared library)
    ii  libhogweed4:amd64                    3.3-1+b2                       amd64        low level cryptographic library (public-key cryptos)
    ii  libhtml-form-perl                    6.03-1                         all          module that represents an HTML form element
    ii  libhtml-format-perl                  2.12-1                         all          module for transforming HTML into various formats
    ii  libhtml-parser-perl                  3.72-3                         amd64        collection of modules that parse HTML text documents
    ii  libhtml-tagset-perl                  3.20-3                         all          Data tables pertaining to HTML
    ii  libhtml-tree-perl                    5.03-2                         all          Perl module to represent and create HTML syntax trees
    ii  libhttp-cookies-perl                 6.01-1                         all          HTTP cookie jars
    ii  libhttp-daemon-perl                  6.01-1                         all          simple http server class
    ii  libhttp-date-perl                    6.02-1                         all          module of date conversion routines
    ii  libhttp-message-perl                 6.11-1                         all          perl interface to HTTP style messages
    ii  libhttp-negotiate-perl               6.00-2                         all          implementation of content negotiation
    ii  libice6:amd64                        2:1.0.9-2                      amd64        X11 Inter-Client Exchange library
    ii  libicu57:amd64                       57.1-6+deb9u3                  amd64        International Components for Unicode
    ii  libidn11:amd64                       1.33-1                         amd64        GNU Libidn library, implementation of IETF IDN specifications
    ii  libidn2-0:amd64                      0.16-1+deb9u1                  amd64        Internationalized domain names (IDNA2008) library
    ii  libinput-bin                         1.6.3-1                        amd64        input device management and event handling library - udev quirks
    ii  libinput10:amd64                     1.6.3-1                        amd64        input device management and event handling library - shared library
    ii  libio-html-perl                      1.001-1                        all          open an HTML file with automatic charset detection
    ii  libio-socket-ssl-perl                2.044-1                        all          Perl module implementing object oriented interface to SSL sockets
    ii  libipc-system-simple-perl            1.25-3                         all          Perl module to run commands simply, with detailed diagnostics
    ii  libisl15:amd64                       0.18-1                         amd64        manipulating sets and relations of integer points bounded by linear constraints
    ii  libitm1:amd64                        6.3.0-18+deb9u1                amd64        GNU Transactional Memory Library
    ii  libjbig0:amd64                       2.1-3.1+b2                     amd64        JBIGkit libraries
    ii  libjpeg62-turbo:amd64                1:1.5.1-2                      amd64        libjpeg-turbo JPEG runtime library
    ii  libjson-glib-1.0-0:amd64             1.2.6-1                        amd64        GLib JSON manipulation library
    ii  libjson-glib-1.0-common              1.2.6-1                        all          GLib JSON manipulation library (common files)
    ii  libjsoncpp1:amd64                    1.7.4-3                        amd64        library for reading and writing JSON for C++
    ii  libk5crypto3:amd64                   1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - Crypto Library
    ii  libkeyutils1:amd64                   1.5.9-9                        amd64        Linux Key Management Utilities (library)
    ii  libkrb5-3:amd64                      1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries
    ii  libkrb5support0:amd64                1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - Support library
    ii  libksba8:amd64                       1.3.5-2                        amd64        X.509 and CMS support library
    ii  liblcms2-2:amd64                     2.8-4+deb9u1                   amd64        Little CMS 2 color management library
    ii  libldap-2.4-2:amd64                  2.4.44+dfsg-5+deb9u3           amd64        OpenLDAP libraries
    ii  libldap-common                       2.4.44+dfsg-5+deb9u3           all          OpenLDAP common files for libraries
    ii  libllvm3.8:amd64                     1:3.8.1-24                     amd64        Modular compiler and toolchain technologies, runtime library
    ii  libllvm3.9:amd64                     1:3.9.1-9                      amd64        Modular compiler and toolchain technologies, runtime library
    ii  liblocale-gettext-perl               1.07-3+b1                      amd64        module using libc functions for internationalization in Perl
    ii  liblsan0:amd64                       6.3.0-18+deb9u1                amd64        LeakSanitizer -- a memory leak detector (runtime)
    ii  liblwp-mediatypes-perl               6.02-1                         all          module to guess media type for a file or a URL
    ii  liblwp-protocol-https-perl           6.06-2                         all          HTTPS driver for LWP::UserAgent
    ii  liblz4-1:amd64                       0.0~r131-2+b1                  amd64        Fast LZ compression algorithm library - runtime
    ii  liblzma5:amd64                       5.2.2-1.2+b1                   amd64        XZ-format compression library
    ii  liblzo2-2:amd64                      2.08-1.2+b2                    amd64        data compression library
    ii  libmailtools-perl                    2.18-1                         all          Manipulate email in perl programs
    ii  libminizip1:amd64                    1.1-8+b1                       amd64        compression library - minizip library
    ii  libmount1:amd64                      2.29.2-1+deb9u1                amd64        device mounting library
    ii  libmp3lame0:amd64                    3.99.5+repack1-9+b2            amd64        MP3 encoding library
    ii  libmpc3:amd64                        1.0.3-1+b2                     amd64        multiple precision complex floating-point library
    ii  libmpdec2:amd64                      2.4.2-1                        amd64        library for decimal floating point arithmetic (runtime library)
    ii  libmpfr4:amd64                       3.1.5-1                        amd64        multiple precision floating-point computation
    ii  libmpg123-0:amd64                    1.23.8-1+b1                    amd64        MPEG layer 1/2/3 audio decoder (shared library)
    ii  libmpx2:amd64                        6.3.0-18+deb9u1                amd64        Intel memory protection extensions (runtime)
    ii  libmtdev1:amd64                      1.1.5-1+b1                     amd64        Multitouch Protocol Translation Library - shared library
    ii  libncurses5:amd64                    6.0+20161126-1+deb9u2          amd64        shared libraries for terminal handling
    ii  libncursesw5:amd64                   6.0+20161126-1+deb9u2          amd64        shared libraries for terminal handling (wide character support)
    ii  libnet-dbus-perl                     1.1.0-4+b1                     amd64        Perl extension for the DBus bindings
    ii  libnet-http-perl                     6.12-1                         all          module providing low-level HTTP connection client
    ii  libnet-smtp-ssl-perl                 1.04-1                         all          Perl module providing SSL support to Net::SMTP
    ii  libnet-ssleay-perl                   1.80-1                         amd64        Perl module for Secure Sockets Layer (SSL)
    ii  libnettle6:amd64                     3.3-1+b2                       amd64        low level cryptographic library (symmetric and one-way cryptos)
    ii  libnewt0.52:amd64                    0.52.19-1+b1                   amd64        Not Erik's Windowing Toolkit - text mode windowing with slang
    ii  libnghttp2-14:amd64                  1.18.1-1+deb9u1                amd64        library implementing HTTP/2 protocol (shared library)
    ii  libnpth0:amd64                       1.3-1                          amd64        replacement for GNU Pth using system threads
    ii  libnspr4:amd64                       2:4.12-6                       amd64        NetScape Portable Runtime Library
    ii  libnss3:amd64                        2:3.26.2-1.1+deb9u1            amd64        Network Security Service libraries
    ii  libnuma1:amd64                       2.0.11-2.1                     amd64        Libraries for controlling NUMA policy
    ii  libobjc-6-dev:amd64                  6.3.0-18+deb9u1                amd64        Runtime library for GNU Objective-C applications (development files)
    ii  libobjc4:amd64                       6.3.0-18+deb9u1                amd64        Runtime library for GNU Objective-C applications
    ii  libogg0:amd64                        1.3.2-1                        amd64        Ogg bitstream library
    ii  libopenjp2-7:amd64                   2.1.2-1.1+deb9u3               amd64        JPEG 2000 image compression/decompression library
    ii  libopenmpt0:amd64                    0.2.7386~beta20.3-3+deb9u3     amd64        module music library based on OpenMPT -- shared library
    ii  libopus0:amd64                       1.2~alpha2-1                   amd64        Opus codec runtime library
    ii  liborc-0.4-0:amd64                   1:0.4.26-2                     amd64        Library of Optimized Inner Loops Runtime Compiler
    ii  libp11-kit0:amd64                    0.23.3-2                       amd64        library for loading and coordinating access to PKCS#11 modules - runtime
    ii  libpam-cap:amd64                     1:2.25-1                       amd64        POSIX 1003.1e capabilities (PAM module)
    ii  libpam-modules:amd64                 1.1.8-3.6                      amd64        Pluggable Authentication Modules for PAM
    ii  libpam-modules-bin                   1.1.8-3.6                      amd64        Pluggable Authentication Modules for PAM - helper binaries
    ii  libpam-runtime                       1.1.8-3.6                      all          Runtime support for the PAM library
    ii  libpam0g:amd64                       1.1.8-3.6                      amd64        Pluggable Authentication Modules library
    ii  libpango-1.0-0:amd64                 1.40.5-1                       amd64        Layout and rendering of internationalized text
    ii  libpangocairo-1.0-0:amd64            1.40.5-1                       amd64        Layout and rendering of internationalized text
    ii  libpangoft2-1.0-0:amd64              1.40.5-1                       amd64        Layout and rendering of internationalized text
    ii  libpci3:amd64                        1:3.5.2-1                      amd64        Linux PCI Utilities (shared library)
    ii  libpciaccess0:amd64                  0.13.4-1+b2                    amd64        Generic PCI access library for X
    ii  libpcre16-3:amd64                    2:8.39-3                       amd64        Old Perl 5 Compatible Regular Expression Library - 16 bit runtime files
    ii  libpcre3:amd64                       2:8.39-3                       amd64        Old Perl 5 Compatible Regular Expression Library - runtime files
    ii  libperl5.24:amd64                    5.24.1-3+deb9u5                amd64        shared Perl library
    ii  libpipeline1:amd64                   1.4.1-2                        amd64        pipeline manipulation library
    ii  libpixman-1-0:amd64                  0.34.0-1                       amd64        pixel-manipulation library for X and cairo
    ii  libpng16-16:amd64                    1.6.28-1+deb9u1                amd64        PNG library - runtime (version 1.6)
    ii  libpopt0:amd64                       1.16-10+b2                     amd64        lib for parsing cmdline parameters
    ii  libprocps6:amd64                     2:3.3.12-3+deb9u1              amd64        library for accessing process information from /proc
    ii  libproxy1v5:amd64                    0.4.14-2                       amd64        automatic proxy configuration management library (shared)
    ii  libpsl5:amd64                        0.17.0-3                       amd64        Library for Public Suffix List (shared libraries)
    ii  libpthread-stubs0-dev:amd64          0.3-4                          amd64        pthread stubs not provided by native libc, development files
    ii  libpulse0:amd64                      10.0-1+deb9u1                  amd64        PulseAudio client libraries
    ii  libpython-stdlib:amd64               2.7.13-2                       amd64        interactive high-level object-oriented language (default python version)
    ii  libpython2.7-minimal:amd64           2.7.13-2+deb9u3                amd64        Minimal subset of the Python language (version 2.7)
    ii  libpython2.7-stdlib:amd64            2.7.13-2+deb9u3                amd64        Interactive high-level object-oriented language (standard library, version 2.7)
    ii  libpython3.5:amd64                   3.5.3-1+deb9u1                 amd64        Shared Python runtime library (version 3.5)
    ii  libpython3.5-minimal:amd64           3.5.3-1+deb9u1                 amd64        Minimal subset of the Python language (version 3.5)
    ii  libpython3.5-stdlib:amd64            3.5.3-1+deb9u1                 amd64        Interactive high-level object-oriented language (standard library, version 3.5)
    ii  libqbscore1.7                        1.7.0+dfsg-4                   amd64        Qbs core library
    ii  libqbsqtprofilesetup1.7              1.7.0+dfsg-4                   amd64        Qbs profile setup library
    ii  libqt5clucene5:amd64                 5.7.1-1                        amd64        Qt 5 CLucene module
    ii  libqt5concurrent5:amd64              5.7.1+dfsg-3+deb9u1            amd64        Qt 5 concurrent module
    ii  libqt5core5a:amd64                   5.7.1+dfsg-3+deb9u1            amd64        Qt 5 core module
    ii  libqt5dbus5:amd64                    5.7.1+dfsg-3+deb9u1            amd64        Qt 5 D-Bus module
    ii  libqt5designer5:amd64                5.7.1-1                        amd64        Qt 5 designer module
    ii  libqt5designercomponents5:amd64      5.7.1-1                        amd64        Qt 5 Designer components module
    ii  libqt5gui5:amd64                     5.7.1+dfsg-3+deb9u1            amd64        Qt 5 GUI module
    ii  libqt5help5:amd64                    5.7.1-1                        amd64        Qt 5 help module
    ii  libqt5network5:amd64                 5.7.1+dfsg-3+deb9u1            amd64        Qt 5 network module
    ii  libqt5opengl5:amd64                  5.7.1+dfsg-3+deb9u1            amd64        Qt 5 OpenGL module
    ii  libqt5opengl5-dev:amd64              5.7.1+dfsg-3+deb9u1            amd64        Qt 5 OpenGL library development files
    ii  libqt5printsupport5:amd64            5.7.1+dfsg-3+deb9u1            amd64        Qt 5 print support module
    ii  libqt5qml5:amd64                     5.7.1-2+b2                     amd64        Qt 5 QML module
    ii  libqt5quick5:amd64                   5.7.1-2+b2                     amd64        Qt 5 Quick library
    ii  libqt5quickparticles5:amd64          5.7.1-2+b2                     amd64        Qt 5 Quick particles module
    ii  libqt5quicktest5:amd64               5.7.1-2+b2                     amd64        Qt 5 Quick Test library
    ii  libqt5quickwidgets5:amd64            5.7.1-2+b2                     amd64        Qt 5 Quick Widgets library
    ii  libqt5script5:amd64                  5.7.1~20161021+dfsg-2          amd64        Qt 5 script module
    ii  libqt5sql5:amd64                     5.7.1+dfsg-3+deb9u1            amd64        Qt 5 SQL module
    ii  libqt5sql5-sqlite:amd64              5.7.1+dfsg-3+deb9u1            amd64        Qt 5 SQLite 3 database driver
    ii  libqt5svg5:amd64                     5.7.1~20161021-2+b2            amd64        Qt 5 SVG module
    ii  libqt5test5:amd64                    5.7.1+dfsg-3+deb9u1            amd64        Qt 5 test module
    ii  libqt5webkit5:amd64                  5.7.1+dfsg-1                   amd64        Web content engine library for Qt
    ii  libqt5widgets5:amd64                 5.7.1+dfsg-3+deb9u1            amd64        Qt 5 widgets module
    ii  libqt5xml5:amd64                     5.7.1+dfsg-3+deb9u1            amd64        Qt 5 XML module
    ii  libqt5xmlpatterns5:amd64             5.7.1~20161021-3               amd64        Qt 5 XML patterns module
    ii  libquadmath0:amd64                   6.3.0-18+deb9u1                amd64        GCC Quad-Precision Math Library
    ii  libre2-3:amd64                       20170101+dfsg-1                amd64        efficient, principled regular expression library
    ii  libreadline7:amd64                   7.0-3                          amd64        GNU readline and history libraries, run-time libraries
    ii  librest-0.7-0:amd64                  0.8.0-2                        amd64        REST service access library
    ii  librsvg2-2:amd64                     2.40.16-1+b1                   amd64        SAX-based renderer library for SVG files (runtime)
    ii  librsvg2-common:amd64                2.40.16-1+b1                   amd64        SAX-based renderer library for SVG files (extra runtime)
    ii  librtmp1:amd64                       2.4+20151223.gitfa8646d.1-1+b1 amd64        toolkit for RTMP streams (shared library)
    ii  libsasl2-2:amd64                     2.1.27~101-g0780600+dfsg-3     amd64        Cyrus SASL - authentication abstraction library
    ii  libsasl2-modules-db:amd64            2.1.27~101-g0780600+dfsg-3     amd64        Cyrus SASL - pluggable authentication modules (DB)
    ii  libselinux1:amd64                    2.6-3+b3                       amd64        SELinux runtime shared libraries
    ii  libsemanage-common                   2.6-2                          all          Common files for SELinux policy management libraries
    ii  libsemanage1:amd64                   2.6-2                          amd64        SELinux policy management library
    ii  libsensors4:amd64                    1:3.4.0-4                      amd64        library to read temperature/voltage/fan sensors
    ii  libsepol1:amd64                      2.6-2                          amd64        SELinux library for manipulating binary security policies
    ii  libshine3:amd64                      3.1.0-5                        amd64        Fixed-point MP3 encoding library - runtime files
    ii  libslang2:amd64                      2.3.1-5                        amd64        S-Lang programming library - runtime version
    ii  libsm6:amd64                         2:1.2.2-1+b3                   amd64        X11 Session Management library
    ii  libsmartcols1:amd64                  2.29.2-1+deb9u1                amd64        smart column output alignment library
    ii  libsnappy1v5:amd64                   1.1.3-3                        amd64        fast compression/decompression library
    ii  libsndfile1:amd64                    1.0.27-3                       amd64        Library for reading/writing audio files
    ii  libsoup-gnome2.4-1:amd64             2.56.0-2+deb9u2                amd64        HTTP library implementation in C -- GNOME support library
    ii  libsoup2.4-1:amd64                   2.56.0-2+deb9u2                amd64        HTTP library implementation in C -- Shared library
    ii  libsoxr0:amd64                       0.1.2-2                        amd64        High quality 1D sample-rate conversion library
    ii  libspeex1:amd64                      1.2~rc1.2-1+b2                 amd64        The Speex codec runtime library
    ii  libsqlite3-0:amd64                   3.16.2-5+deb9u1                amd64        SQLite 3 shared library
    ii  libss2:amd64                         1.43.4-2                       amd64        command-line interface parsing library
    ii  libssh-gcrypt-4:amd64                0.7.3-2+deb9u2                 amd64        tiny C SSH library (gcrypt flavor)
    ii  libssh2-1:amd64                      1.7.0-1+deb9u1                 amd64        SSH2 client-side library
    ii  libssl1.0.2:amd64                    1.0.2s-1~deb9u1                amd64        Secure Sockets Layer toolkit - shared libraries
    ii  libssl1.1:amd64                      1.1.0k-1~deb9u1                amd64        Secure Sockets Layer toolkit - shared libraries
    ii  libstdc++-6-dev:amd64                6.3.0-18+deb9u1                amd64        GNU Standard C++ Library v3 (development files)
    ii  libstdc++6:amd64                     6.3.0-18+deb9u1                amd64        GNU Standard C++ Library v3
    ii  libswresample2:amd64                 7:3.2.14-1~deb9u1              amd64        FFmpeg library for audio resampling, rematrixing etc. - runtime files
    ii  libsystemd0:amd64                    232-25+deb9u12                 amd64        systemd utility library
    ii  libtasn1-6:amd64                     4.10-1.1+deb9u1                amd64        Manage ASN.1 structures (runtime)
    ii  libtext-iconv-perl                   1.7-5+b4                       amd64        converts between character sets in Perl
    ii  libthai-data                         0.1.26-1                       all          Data files for Thai language support library
    ii  libthai0:amd64                       0.1.26-1                       amd64        Thai language support library
    ii  libtheora0:amd64                     1.1.1+dfsg.1-14+b1             amd64        Theora Video Compression Codec
    ii  libtie-ixhash-perl                   1.23-2                         all          Perl module to order associative arrays
    ii  libtiff5:amd64                       4.0.8-2+deb9u4                 amd64        Tag Image File Format (TIFF) library
    ii  libtimedate-perl                     2.3000-2                       all          collection of modules to manipulate date/time information
    ii  libtinfo-dev:amd64                   6.0+20161126-1+deb9u2          amd64        developer's library for the low-level terminfo library
    ii  libtinfo5:amd64                      6.0+20161126-1+deb9u2          amd64        shared low-level terminfo library for terminal handling
    ii  libtsan0:amd64                       6.3.0-18+deb9u1                amd64        ThreadSanitizer -- a Valgrind-based detector of data races (runtime)
    ii  libtwolame0:amd64                    0.3.13-2                       amd64        MPEG Audio Layer 2 encoding library
    ii  libtxc-dxtn-s2tc:amd64               1.0+git20151227-2              amd64        Texture compression library for Mesa
    ii  libubsan0:amd64                      6.3.0-18+deb9u1                amd64        UBSan -- undefined behaviour sanitizer (runtime)
    ii  libudev1:amd64                       232-25+deb9u12                 amd64        libudev shared library
    ii  libunistring0:amd64                  0.9.6+really0.9.3-0.1          amd64        Unicode string library for C
    ii  liburi-perl                          1.71-1                         all          module to manipulate and access URI strings
    ii  libustr-1.0-1:amd64                  1.0.4-6                        amd64        Micro string library: shared library
    ii  libutempter0:amd64                   1.1.6-3                        amd64        privileged helper for utmp/wtmp updates (runtime)
    ii  libuuid1:amd64                       2.29.2-1+deb9u1                amd64        Universally Unique ID library
    ii  libuv1:amd64                         1.9.1-3                        amd64        asynchronous event notification library - runtime library
    ii  libva-drm1:amd64                     1.7.3-2                        amd64        Video Acceleration (VA) API for Linux -- DRM runtime
    ii  libva-x11-1:amd64                    1.7.3-2                        amd64        Video Acceleration (VA) API for Linux -- X11 runtime
    ii  libva1:amd64                         1.7.3-2                        amd64        Video Acceleration (VA) API for Linux -- runtime
    ii  libvdpau-va-gl1:amd64                0.4.2-1                        amd64        VDPAU driver with OpenGL/VAAPI backend
    ii  libvdpau1:amd64                      1.1.1-6                        amd64        Video Decode and Presentation API for Unix (libraries)
    ii  libvisual-0.4-0:amd64                0.4.0-10                       amd64        audio visualization framework
    ii  libvorbis0a:amd64                    1.3.5-4+deb9u2                 amd64        decoder library for Vorbis General Audio Compression Codec
    ii  libvorbisenc2:amd64                  1.3.5-4+deb9u2                 amd64        encoder library for Vorbis General Audio Compression Codec
    ii  libvorbisfile3:amd64                 1.3.5-4+deb9u2                 amd64        high-level API for Vorbis General Audio Compression Codec
    ii  libvpx4:amd64                        1.6.1-3+deb9u1                 amd64        VP8 and VP9 video codec (shared library)
    ii  libwacom-bin                         0.22-1+b1                      amd64        Wacom model feature query library -- binaries
    ii  libwacom-common                      0.22-1                         all          Wacom model feature query library (common files)
    ii  libwacom2:amd64                      0.22-1+b1                      amd64        Wacom model feature query library
    ii  libwavpack1:amd64                    5.0.0-2+deb9u2                 amd64        audio codec (lossy and lossless) - library
    ii  libwayland-client0:amd64             1.12.0-1+deb9u1                amd64        wayland compositor infrastructure - client library
    ii  libwayland-cursor0:amd64             1.12.0-1+deb9u1                amd64        wayland compositor infrastructure - cursor library
    ii  libwayland-egl1-mesa:amd64           13.0.6-1+b2                    amd64        implementation of the Wayland EGL platform -- runtime
    ii  libwayland-server0:amd64             1.12.0-1+deb9u1                amd64        wayland compositor infrastructure - server library
    ii  libwebp6:amd64                       0.5.2-1                        amd64        Lossy compression of digital photographic images.
    ii  libwebpdemux2:amd64                  0.5.2-1                        amd64        Lossy compression of digital photographic images.
    ii  libwebpmux2:amd64                    0.5.2-1                        amd64        Lossy compression of digital photographic images.
    ii  libwrap0:amd64                       7.6.q-26                       amd64        Wietse Venema's TCP wrappers library
    ii  libwww-perl                          6.15-1                         all          simple and consistent interface to the world-wide web
    ii  libwww-robotrules-perl               6.01-1                         all          database of robots.txt-derived permissions
    ii  libx11-6:amd64                       2:1.6.4-3+deb9u1               amd64        X11 client-side library
    ii  libx11-data                          2:1.6.4-3+deb9u1               all          X11 client-side library
    ii  libx11-dev:amd64                     2:1.6.4-3+deb9u1               amd64        X11 client-side library (development headers)
    ii  libx11-doc                           2:1.6.4-3+deb9u1               all          X11 client-side library (development documentation)
    ii  libx11-protocol-perl                 0.56-7                         all          Perl module for the X Window System Protocol, version 11
    ii  libx11-xcb-dev:amd64                 2:1.6.4-3+deb9u1               amd64        Xlib/XCB interface library (development headers)
    ii  libx11-xcb1:amd64                    2:1.6.4-3+deb9u1               amd64        Xlib/XCB interface library
    ii  libx264-148:amd64                    2:0.148.2748+git97eaef2-1      amd64        x264 video coding library
    ii  libx265-95:amd64                     2.1-2+b2                       amd64        H.265/HEVC video stream encoder (shared library)
    ii  libxau-dev:amd64                     1:1.0.8-1                      amd64        X11 authorisation library (development headers)
    ii  libxau6:amd64                        1:1.0.8-1                      amd64        X11 authorisation library
    ii  libxaw7:amd64                        2:1.0.13-1+b2                  amd64        X11 Athena Widget library
    ii  libxcb-dri2-0:amd64                  1.12-1                         amd64        X C Binding, dri2 extension
    ii  libxcb-dri2-0-dev:amd64              1.12-1                         amd64        X C Binding, dri2 extension, development files
    ii  libxcb-dri3-0:amd64                  1.12-1                         amd64        X C Binding, dri3 extension
    ii  libxcb-dri3-dev:amd64                1.12-1                         amd64        X C Binding, dri3 extension, development files
    ii  libxcb-glx0:amd64                    1.12-1                         amd64        X C Binding, glx extension
    ii  libxcb-glx0-dev:amd64                1.12-1                         amd64        X C Binding, glx extension, development files
    ii  libxcb-icccm4:amd64                  0.4.1-1                        amd64        utility libraries for X C Binding -- icccm
    ii  libxcb-image0:amd64                  0.4.0-1+b2                     amd64        utility libraries for X C Binding -- image
    ii  libxcb-keysyms1:amd64                0.4.0-1+b2                     amd64        utility libraries for X C Binding -- keysyms
    ii  libxcb-present-dev:amd64             1.12-1                         amd64        X C Binding, present extension, development files
    ii  libxcb-present0:amd64                1.12-1                         amd64        X C Binding, present extension
    ii  libxcb-randr0:amd64                  1.12-1                         amd64        X C Binding, randr extension
    ii  libxcb-randr0-dev:amd64              1.12-1                         amd64        X C Binding, randr extension, development files
    ii  libxcb-render-util0:amd64            0.3.9-1                        amd64        utility libraries for X C Binding -- render-util
    ii  libxcb-render0:amd64                 1.12-1                         amd64        X C Binding, render extension
    ii  libxcb-render0-dev:amd64             1.12-1                         amd64        X C Binding, render extension, development files
    ii  libxcb-shape0:amd64                  1.12-1                         amd64        X C Binding, shape extension
    ii  libxcb-shape0-dev:amd64              1.12-1                         amd64        X C Binding, shape extension, development files
    ii  libxcb-shm0:amd64                    1.12-1                         amd64        X C Binding, shm extension
    ii  libxcb-sync-dev:amd64                1.12-1                         amd64        X C Binding, sync extension, development files
    ii  libxcb-sync1:amd64                   1.12-1                         amd64        X C Binding, sync extension
    ii  libxcb-util0:amd64                   0.3.8-3+b2                     amd64        utility libraries for X C Binding -- atom, aux and event
    ii  libxcb-xfixes0:amd64                 1.12-1                         amd64        X C Binding, xfixes extension
    ii  libxcb-xfixes0-dev:amd64             1.12-1                         amd64        X C Binding, xfixes extension, development files
    ii  libxcb-xinerama0:amd64               1.12-1                         amd64        X C Binding, xinerama extension
    ii  libxcb-xkb1:amd64                    1.12-1                         amd64        X C Binding, XKEYBOARD extension
    ii  libxcb1:amd64                        1.12-1                         amd64        X C Binding
    ii  libxcb1-dev:amd64                    1.12-1                         amd64        X C Binding, development files
    ii  libxcomposite1:amd64                 1:0.4.4-2                      amd64        X11 Composite extension library
    ii  libxcursor1:amd64                    1:1.1.14-1+deb9u2              amd64        X cursor management library
    ii  libxdamage-dev:amd64                 1:1.1.4-2+b3                   amd64        X11 damaged region extension library (development headers)
    ii  libxdamage1:amd64                    1:1.1.4-2+b3                   amd64        X11 damaged region extension library
    ii  libxdmcp-dev:amd64                   1:1.1.2-3                      amd64        X11 authorisation library (development headers)
    ii  libxdmcp6:amd64                      1:1.1.2-3                      amd64        X11 Display Manager Control Protocol library
    ii  libxext-dev:amd64                    2:1.3.3-1+b2                   amd64        X11 miscellaneous extensions library (development headers)
    ii  libxext6:amd64                       2:1.3.3-1+b2                   amd64        X11 miscellaneous extension library
    ii  libxfixes-dev:amd64                  1:5.0.3-1                      amd64        X11 miscellaneous 'fixes' extension library (development headers)
    ii  libxfixes3:amd64                     1:5.0.3-1                      amd64        X11 miscellaneous 'fixes' extension library
    ii  libxft2:amd64                        2.3.2-1+b2                     amd64        FreeType-based font drawing library for X
    ii  libxi6:amd64                         2:1.7.9-1                      amd64        X11 Input extension library
    ii  libxinerama1:amd64                   2:1.1.3-1+b3                   amd64        X11 Xinerama extension library
    ii  libxkbcommon-x11-0:amd64             0.7.1-2~deb9u1                 amd64        library to create keymaps with the XKB X11 protocol
    ii  libxkbcommon0:amd64                  0.7.1-2~deb9u1                 amd64        library interface to the XKB compiler - shared library
    ii  libxml-parser-perl                   2.44-2+b1                      amd64        Perl module for parsing XML files
    ii  libxml-twig-perl                     1:3.50-1                       all          Perl module for processing huge XML documents in tree mode
    ii  libxml-xpathengine-perl              0.13-1                         all          re-usable XPath engine for DOM-like trees
    ii  libxml2:amd64                        2.9.4+dfsg1-2.2+deb9u2         amd64        GNOME XML library
    ii  libxmu6:amd64                        2:1.1.2-2                      amd64        X11 miscellaneous utility library
    ii  libxmuu1:amd64                       2:1.1.2-2                      amd64        X11 miscellaneous micro-utility library
    ii  libxpm4:amd64                        1:3.5.12-1                     amd64        X11 pixmap library
    ii  libxrandr2:amd64                     2:1.5.1-1                      amd64        X11 RandR extension library
    ii  libxrender1:amd64                    1:0.9.10-1                     amd64        X Rendering Extension client library
    ii  libxshmfence-dev:amd64               1.2-1+b2                       amd64        X shared memory fences - development files
    ii  libxshmfence1:amd64                  1.2-1+b2                       amd64        X shared memory fences - shared library
    ii  libxslt1.1:amd64                     1.1.29-2.1+deb9u1              amd64        XSLT 1.0 processing library - runtime library
    ii  libxss1:amd64                        1:1.2.2-1                      amd64        X11 Screen Saver extension library
    ii  libxt6:amd64                         1:1.1.5-1                      amd64        X11 toolkit intrinsics library
    ii  libxtst6:amd64                       2:1.2.3-1                      amd64        X11 Testing -- Record extension library
    ii  libxv1:amd64                         2:1.0.11-1                     amd64        X11 Video extension library
    ii  libxvidcore4:amd64                   2:1.3.4-1+b2                   amd64        Open source MPEG-4 video codec (library)
    ii  libxxf86dga1:amd64                   2:1.1.4-1+b3                   amd64        X11 Direct Graphics Access extension library
    ii  libxxf86vm-dev:amd64                 1:1.1.4-1+b2                   amd64        X11 XFree86 video mode extension library (development headers)
    ii  libxxf86vm1:amd64                    1:1.1.4-1+b2                   amd64        X11 XFree86 video mode extension library
    ii  libzvbi-common                       0.2.35-13                      all          Vertical Blanking Interval decoder (VBI) - common files
    ii  libzvbi0:amd64                       0.2.35-13                      amd64        Vertical Blanking Interval decoder (VBI) - runtime files
    ii  linux-libc-dev:amd64                 4.9.189-3                      amd64        Linux support headers for userspace development
    ii  llvm-3.8                             1:3.8.1-24                     amd64        Modular compiler and toolchain technologies
    ii  llvm-3.8-dev                         1:3.8.1-24                     amd64        Modular compiler and toolchain technologies, libraries and headers
    ii  llvm-3.8-runtime                     1:3.8.1-24                     amd64        Modular compiler and toolchain technologies, IR interpreter
    ii  localepurge                          0.7.3.4                        all          reclaim disk space by removing unneeded localizations
    ii  locales                              2.24-11+deb9u4                 all          GNU C Library: National Language (locale) data [support]
    ii  login                                1:4.4-4.1                      amd64        system login tools
    ii  lsb-base                             9.20161125                     all          Linux Standard Base init script functionality
    ii  make                                 4.1-9.1                        amd64        utility for directing compilation
    ii  manpages                             4.10-2                         all          Manual pages about using a GNU/Linux system
    ii  manpages-dev                         4.10-2                         all          Manual pages about using GNU/Linux for development
    ii  mawk                                 1.3.3-17+b3                    amd64        a pattern scanning and text processing language
    ii  mesa-common-dev:amd64                13.0.6-1+b2                    amd64        Developer documentation for Mesa
    ii  mesa-utils                           8.3.0-3                        amd64        Miscellaneous Mesa GL utilities
    ii  mesa-va-drivers:amd64                13.0.6-1+b2                    amd64        Mesa VA-API video acceleration drivers
    ii  mesa-vdpau-drivers:amd64             13.0.6-1+b2                    amd64        Mesa VDPAU video acceleration drivers
    ii  mime-support                         3.60                           all          MIME files 'mime.types' & 'mailcap', and support programs
    ii  mount                                2.29.2-1+deb9u1                amd64        tools for mounting and manipulating filesystems
    ii  multiarch-support                    2.24-11+deb9u4                 amd64        Transitional package to ensure multiarch compatibility
    ii  ncurses-base                         6.0+20161126-1+deb9u2          all          basic terminal type definitions
    ii  ncurses-bin                          6.0+20161126-1+deb9u2          amd64        terminal-related programs and man pages
    ii  net-tools                            1.60+git20161116.90da8a0-1     amd64        NET-3 networking toolkit
    ii  netbase                              5.4                            all          Basic TCP/IP networking system
    ii  openssl                              1.1.0k-1~deb9u1                amd64        Secure Sockets Layer toolkit - cryptographic utility
    ii  passwd                               1:4.4-4.1                      amd64        change and administer password and group data
    ii  patch                                2.7.5-1+deb9u2                 amd64        Apply a diff file to an original
    ii  perl                                 5.24.1-3+deb9u5                amd64        Larry Wall's Practical Extraction and Report Language
    ii  perl-base                            5.24.1-3+deb9u5                amd64        minimal Perl system
    ii  perl-modules-5.24                    5.24.1-3+deb9u5                all          Core Perl modules
    ii  perl-openssl-defaults:amd64          3                              amd64        version compatibility baseline for Perl OpenSSL packages
    ii  pinentry-curses                      1.0.0-2                        amd64        curses-based PIN or pass-phrase entry dialog for GnuPG
    ii  procps                               2:3.3.12-3+deb9u1              amd64        /proc file system utilities
    ii  psmisc                               22.21-2.1+b2                   amd64        utilities that use the proc file system
    ii  python                               2.7.13-2                       amd64        interactive high-level object-oriented language (default version)
    ii  python-minimal                       2.7.13-2                       amd64        minimal subset of the Python language (default version)
    ii  python2.7                            2.7.13-2+deb9u3                amd64        Interactive high-level object-oriented language (version 2.7)
    ii  python2.7-minimal                    2.7.13-2+deb9u3                amd64        Minimal subset of the Python language (version 2.7)
    ii  qml                                  5.7.1-2+b2                     amd64        Qt 5 QML viewer
    ii  qml-module-qtgraphicaleffects:amd64  5.7.1~20161021-3               amd64        Qt 5 Graphical Effects module
    ii  qml-module-qtqml-models2:amd64       5.7.1-2+b2                     amd64        Qt 5 Models2 QML module
    ii  qml-module-qtquick-controls:amd64    5.7.1~20161021-2               amd64        Qt 5 Quick Controls QML module
    ii  qml-module-qtquick-layouts:amd64     5.7.1-2+b2                     amd64        Qt 5 Quick Layouts QML module
    ii  qml-module-qtquick-window2:amd64     5.7.1-2+b2                     amd64        Qt 5 window 2 QML module
    ii  qml-module-qtquick2:amd64            5.7.1-2+b2                     amd64        Qt 5 Qt Quick 2 QML module
    ii  qmlscene                             5.7.1-2+b2                     amd64        Qt 5 QML scene viewer
    ii  qt3d5-doc                            5.7.1+dfsg-2                   all          Qt 3D documentation
    ii  qt5-default                          5.7.1+dfsg-3+deb9u1            amd64        Qt 5 development defaults package
    ii  qt5-doc                              5.7.1-2                        all          Qt 5 API Documentation
    ii  qt5-gtk-platformtheme:amd64          5.7.1+dfsg-3+deb9u1            amd64        Qt 5 GTK+ 3 platform theme
    ii  qt5-qmake:amd64                      5.7.1+dfsg-3+deb9u1            amd64        Qt 5 qmake Makefile generator tool
    ii  qt5-qmltooling-plugins:amd64         5.7.1-2+b2                     amd64        Qt 5 qmltooling plugins
    ii  qtbase5-dev:amd64                    5.7.1+dfsg-3+deb9u1            amd64        Qt 5 base development files
    ii  qtbase5-dev-tools                    5.7.1+dfsg-3+deb9u1            amd64        Qt 5 base development programs
    ii  qtbase5-doc                          5.7.1+dfsg-3+deb9u1            all          Qt 5 base documentation
    ii  qtchooser                            63-g13a3d08-1                  amd64        Wrapper to select between Qt development binary versions
    ii  qtconnectivity5-doc                  5.7.1~20161021-2               all          Qt 5 Sensors documentation
    ii  qtcreator                            4.2.0-1+b1                     amd64        integrated development environment (IDE) for Qt
    ii  qtcreator-data                       4.2.0-1                        all          application data for Qt Creator IDE
    ii  qtcreator-doc                        4.2.0-1                        all          documentation for Qt Creator IDE
    ii  qtdeclarative5-dev:amd64             5.7.1-2+b2                     amd64        Qt 5 declarative development files
    ii  qtdeclarative5-dev-tools             5.7.1-2+b2                     amd64        Qt 5 declarative development programs
    ii  qtdeclarative5-doc                   5.7.1-2                        all          Qt 5 declarative documentation
    ii  qtgraphicaleffects5-doc              5.7.1~20161021-3               all          Qt 5 graphical effects documentation
    ii  qtlocation5-doc                      5.7.1-1                        all          Qt 5 Positioning documentation
    ii  qtmultimedia5-doc                    5.7.1~20161021-2               all          Qt 5 multimedia documentation
    ii  qtquickcontrols2-5-doc               5.7.1-1                        all          Qt 5 Quick Controls 2 documentation
    ii  qtquickcontrols5-doc                 5.7.1~20161021-2               all          Qt 5 Quick Controls documentation
    ii  qtscript5-doc                        5.7.1~20161021+dfsg-2          all          Qt 5 script documentation
    ii  qtsensors5-doc                       5.7.1~20161021-2               all          Qt 5 Sensors documentation
    ii  qtserialport5-doc                    5.7.1~20161021-2               all          Qt 5 serial port documentation
    ii  qtsvg5-doc                           5.7.1~20161021-2               all          Qt 5 SVG documentation
    ii  qttools5-dev-tools:amd64             5.7.1-1                        amd64        Qt 5 development tools
    ii  qttools5-doc                         5.7.1-1                        all          Qt 5 tools documentation
    ii  qttranslations5-l10n                 5.7.1~20161021-1               all          translations for Qt 5
    ii  qtwayland5-doc                       5.7.1~20161021-2               all          Qt 5 Wayland Compositor documentation
    ii  qtwebchannel5-doc                    5.7.1-2                        all          Web communication library for Qt - Documentation
    ii  qtwebengine5-doc                     5.7.1+dfsg-6.1                 all          Qt 5 webengine documentation
    ii  qtwebkit5-doc                        5.7.1+dfsg-1                   all          Qt 5 webkit documentation
    ii  qtwebkit5-examples-doc               5.7.1+dfsg-1                   all          Qt 5 webkit examples documentation
    ii  qtwebsockets5-doc                    5.7.1~20161021-4               all          Qt 5 Web Sockets documentation
    ii  qtx11extras5-doc                     5.7.1~20161021-2               all          Qt 5 X11 extras documentation
    ii  qtxmlpatterns5-dev-tools             5.7.1~20161021-3               amd64        Qt 5 XML patterns development programs
    ii  qtxmlpatterns5-doc                   5.7.1~20161021-3               all          Qt 5 XML patterns documentation
    ii  readline-common                      7.0-3                          all          GNU readline and history libraries, common files
    ii  sed                                  4.4-1                          amd64        GNU stream editor for filtering/transforming text
    ii  sensible-utils                       0.0.9+deb9u1                   all          Utilities for sensible alternative selection
    ii  sgml-base                            1.29                           all          SGML infrastructure and SGML catalog file support
    ii  shared-mime-info                     1.8-1+deb9u1                   amd64        FreeDesktop.org shared MIME database and spec
    ii  sysvinit-utils                       2.88dsf-59.9                   amd64        System-V-like utilities
    ii  tar                                  1.29b-1.1                      amd64        GNU version of the tar archiving utility
    ii  tcpd                                 7.6.q-26                       amd64        Wietse Venema's TCP wrapper utilities
    ii  tzdata                               2019b-0+deb9u1                 all          time zone and daylight-saving time data
    ii  ucf                                  3.0036                         all          Update Configuration File(s): preserve user changes to config files
    ii  unzip                                6.0-21+deb9u2                  amd64        De-archiver for .zip files
    ii  util-linux                           2.29.2-1+deb9u1                amd64        miscellaneous system utilities
    ii  va-driver-all:amd64                  1.7.3-2                        amd64        Video Acceleration (VA) API -- driver metapackage
    ii  vdpau-driver-all:amd64               1.1.1-6                        amd64        Video Decode and Presentation API for Unix (driver metapackage)
    ii  whiptail                             0.52.19-1+b1                   amd64        Displays user-friendly dialog boxes from shell scripts
    ii  x11-common                           1:7.7+19                       all          X Window System (X.Org) infrastructure
    ii  x11-utils                            7.7+3+b1                       amd64        X11 utilities
    ii  x11-xserver-utils                    7.7+7+b1                       amd64        X server utilities
    ii  x11proto-core-dev                    7.0.31-1                       all          X11 core wire protocol and auxiliary headers
    ii  x11proto-damage-dev                  1:1.2.1-2                      all          X11 Damage extension wire protocol
    ii  x11proto-dri2-dev                    2.8-2                          all          X11 DRI2 extension wire protocol
    ii  x11proto-fixes-dev                   1:5.0-2                        all          X11 Fixes extension wire protocol
    ii  x11proto-gl-dev                      1.4.17-1                       all          X11 OpenGL extension wire protocol
    ii  x11proto-input-dev                   2.3.2-1                        all          X11 Input extension wire protocol
    ii  x11proto-kb-dev                      1.0.7-1                        all          X11 XKB extension wire protocol
    ii  x11proto-xext-dev                    7.3.0-1                        all          X11 various extension wire protocol
    ii  x11proto-xf86vidmode-dev             2.3.1-2                        all          X11 Video Mode extension wire protocol
    ii  xbitmaps                             1.1.1-2                        all          Base X bitmaps
    ii  xdg-user-dirs                        0.15-2+b1                      amd64        tool to manage well known user directories
    ii  xdg-utils                            1.1.1-1+deb9u1                 all          desktop integration utilities from freedesktop.org
    ii  xkb-data                             2.19-1+deb9u1                  all          X Keyboard Extension (XKB) configuration data
    ii  xml-core                             0.17                           all          XML infrastructure and XML catalog file support
    ii  xorg-sgml-doctools                   1:1.11-1                       all          Common tools for building X.Org SGML documentation
    ii  xtail                                2.1-5.1+b1                     amd64        like "tail -f", but works on truncated files, directories, more
    ii  xterm                                327-2                          amd64        X terminal emulator
    ii  xtrans-dev                           1.3.5-1                        all          X transport library (development files)
    ii  xz-utils                             5.2.2-1.2+b1                   amd64        XZ-format compression utilities
    ii  zlib1g:amd64                         1:1.2.8.dfsg-5                 amd64        compression library - runtime
