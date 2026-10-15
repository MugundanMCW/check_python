# check_python
mcw@DESKTOP-JO12IN5 CLANGARM64 ~
$ bash build-filezilla-clangarm64.sh

==> Toolchain
clang version 23.1.3 (https://github.com/msys2/MINGW-packages 067886dba977a6b4c97dfedfb25286b5eda55620)
MINGW_PREFIX=/clangarm64  PREFIX=/home/mcw/prefix  JOBS=12

==> Installing build tools and dependencies
warning: base-devel-2026.08-3 is up to date -- skipping
warning: git-2.56.0-1 is up to date -- skipping
warning: subversion-1.14.5-3 is up to date -- skipping
warning: autoconf-wrapper-20260320-2 is up to date -- skipping
warning: automake-wrapper-20260320-2 is up to date -- skipping
warning: libtool-2.6.2-1 is up to date -- skipping
warning: make-4.4.1-3 is up to date -- skipping
warning: patch-2.8-2 is up to date -- skipping
warning: perl-5.42.3-3 is up to date -- skipping
warning: pkgconf-3.0.8-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-clang-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-clang-analyzer-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-clang-libs-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-clang-tools-extra-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-compiler-rt-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-crt-14.0.0.r426.g4564ee4b5-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-headers-14.0.0.r426.g4564ee4b5-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-libc++-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-libunwind-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-libwinpthread-14.0.0.r426.g4564ee4b5-2 is up to date -- skipping
warning: mingw-w64-clang-aarch64-lld-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-lldb-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-llvm-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-llvm-libs-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-llvm-openmp-23.1.3-2 is up to date -- skipping
warning: mingw-w64-clang-aarch64-llvm-tools-23.1.3-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-make-4.4.1-5 is up to date -- skipping
warning: mingw-w64-clang-aarch64-pkgconf-1~3.0.8-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-winpthreads-14.0.0.r426.g4564ee4b5-2 is up to date -- skipping
warning: mingw-w64-clang-aarch64-cmake-4.4.4-3 is up to date -- skipping
warning: mingw-w64-clang-aarch64-meson-1.12.1-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-ninja-1.13.2-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-pkgconf-1~3.0.8-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-gmp-6.3.0-2 is up to date -- skipping
warning: mingw-w64-clang-aarch64-nettle-4.0-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-gnutls-3.8.13-3 is up to date -- skipping
warning: mingw-w64-clang-aarch64-zlib-1.3.2-2 is up to date -- skipping
warning: mingw-w64-clang-aarch64-sqlite3-3.54.0-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-libidn2-2.3.8-4 is up to date -- skipping
warning: mingw-w64-clang-aarch64-pugixml-1.16-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-gettext-tools-1.0-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-wxwidgets3.2-msw-3.2.11-1 is up to date -- skipping
warning: mingw-w64-clang-aarch64-wxwidgets3.2-common-3.2.11-1 is up to date -- skipping
 there is nothing to do

==> Dependency check
  gnutls     3.8.13
  nettle     4.0
  sqlite3    3.54.0
  zlib       1.3.2
  libidn2    2.3.8
  wxWidgets  3.2.11 (/clangarm64/bin/wx-config-3.2)

==> libfilezilla trunk
Updating 'libfilezilla':
At revision 11585.
URL: https://svn.filezilla-project.org/svn/libfilezilla/trunk
Revision: 11585

==> Pre-emptive libc++ include fixes
  patched lib/libfilezilla/nonowning_buffer.hpp: +#include <cstdlib>
  patched lib/nonowning_buffer.cpp: +#include <cstdlib>
locales/Makefile.am:34: warning: '%'-style pattern rules are a GNU make extension
locales/Makefile.am:38: warning: '%'-style pattern rules are a GNU make extension
configure: loading site script /etc/config.site
checking for a BSD-compatible install... /usr/bin/install -c
checking whether sleep supports fractional seconds... yes
checking filesystem timestamp resolution... 0.01
checking whether build environment is sane... yes
checking for a race-free mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking xargs -n works... yes
checking whether UID '197609' is supported by ustar format... yes
checking whether GID '197121' is supported by ustar format... yes
checking how to create a ustar tar archive... gnutar
checking build system type... aarch64-w64-mingw32
checking host system type... aarch64-w64-mingw32
checking whether the C++ compiler works... yes
checking for C++ compiler default output file name... a.exe
checking for suffix of executables... .exe
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether the compiler supports GNU C++... yes
checking whether clang++ accepts -g... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of clang++... gcc3
checking for aarch64-w64-mingw32-gcc... clang
checking whether the compiler supports GNU C... yes
checking whether clang accepts -g... yes
checking for clang option to enable C23 features... -std=gnu23
checking whether clang -std=gnu23 understands -c and -o together... yes
checking dependency style of clang -std=gnu23... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by clang -std=gnu23... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /clangarm64/bin/nm -B
checking the name lister (/clangarm64/bin/nm -B) interface... BSD nm
checking whether ln -s works... no, using cp -pR
checking the maximum length of command line arguments... 8192
checking how to convert aarch64-w64-mingw32 file names to aarch64-w64-mingw32 format... func_convert_file_msys_to_w32
checking how to convert aarch64-w64-mingw32 file names to toolchain format... func_convert_file_msys_to_w32
checking whether cygpath is installed... yes
checking for C:/msys64/clangarm64/bin/ld option to reload object files... -r
checking for file... file
checking for aarch64-w64-mingw32-objdump... no
checking for objdump... objdump
checking how to recognize dependent libraries... file_magic ^x86 archive import|^x86 DLL
checking for aarch64-w64-mingw32-dlltool... no
checking for dlltool... dlltool
checking how to associate runtime and link libraries... func_cygming_dll_for_implib
checking for aarch64-w64-mingw32-ranlib... no
checking for ranlib... ranlib
checking for aarch64-w64-mingw32-ar... no
checking for ar... ar
checking for archiver @FILE support... @
checking for aarch64-w64-mingw32-strip... no
checking for strip... strip
checking command to parse /clangarm64/bin/nm -B output from clang -std=gnu23 object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for aarch64-w64-mingw32-mt... no
checking for mt... no
checking if : is a manifest tool... no
checking for stdio.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for strings.h... yes
checking for sys/stat.h... yes
checking for sys/types.h... yes
checking for unistd.h... yes
checking for dlfcn.h... no
checking for aarch64-w64-mingw32-as... no
checking for as... as
checking for aarch64-w64-mingw32-dlltool... dlltool
checking for aarch64-w64-mingw32-objdump... objdump
checking which variant of shared library versioning to provide... (default) aix
checking for objdir... .libs
checking if clang -std=gnu23 supports -fno-rtti -fno-exceptions... yes
checking for clang -std=gnu23 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang -std=gnu23 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang -std=gnu23 static flag -static works... yes
checking if clang -std=gnu23 supports -c -o file.o... yes
checking if clang -std=gnu23 supports -c -o file.o... (cached) yes
checking whether the clang -std=gnu23 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking whether -lc should be explicitly linked in... yes
checking dynamic linker characteristics... Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... no
checking how to run the C++ preprocessor... clang++ -E
checking for ld used by clang++... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking whether the clang++ linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking for clang++ option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang++ PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang++ static flag -static works... yes
checking if clang++ supports -c -o file.o... yes
checking if clang++ supports -c -o file.o... (cached) yes
checking whether the clang++ linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking dynamic linker characteristics... Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether C compiler accepts -Werror=partial-availability... yes
checking whether the linker accepts -Wl,-no_weak_imports... no
checking whether clang++ supports C++17 features with -std=c++17... yes
checking for whether we need -stdlib=libc++... no
checking for clang -std=gnu23 option to support large files... -D_FILE_OFFSET_BITS=64
checking whether std::chrono::steady_clock is steady... yes
checking for clang -std=gnu23 options to detect undeclared functions... none needed
checking for clang -std=gnu23 options to ignore future-version functions... none needed
checking whether CLOCK_MONOTONIC is declared... yes
checking for d_type member in directory struct... no
checking for timegm... no
checking for clock_gettime... yes
checking for st_mtim member in stat struct... no
checking whether pthread_condattr_setclock is declared... yes
checking for aarch64-w64-mingw32-pkg-config... /clangarm64/bin/aarch64-w64-mingw32-pkg-config
checking pkg-config is at least version 0.9.0... yes
checking for gmp >= 6.2... yes
checking for nettle >= 3.3... yes
checking for hogweed >= 3.3... yes
checking for gnutls >= 3.7.0... yes
checking whether to use windres... yes
checking for aarch64-w64-mingw32-windres... no
checking for windres... windres
checking whether the linker accepts -Wl,--dynamicbase... yes
checking whether the linker accepts -Wl,--nxcompat... yes
checking whether the linker accepts -Wl,--major-subsystem-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-subsystem-version -Wl,0... yes
checking whether the linker accepts -Wl,--major-os-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-os-version -Wl,0... yes
checking whether the linker accepts -Wl,--large-address-aware... yes
checking for cppunit >= 1.13.0... no
checking for aarch64-w64-mingw32-doxygen... no
checking for doxygen... no
configure: WARNING: doxygen not found - will not generate any doxygen documentation
checking for aarch64-w64-mingw32-perl... no
checking for perl... /usr/bin/perl
checking for xgettext... /clangarm64/bin/xgettext
checking for msgfmt... /clangarm64/bin/msgfmt
checking for msgmerge... /clangarm64/bin/msgmerge
checking whether msgmerge version >= 0.11.0... yes, 1.0
checking available libfilezilla message catalogs... an ar az bg_BG ca ca_ES@valencia co cs_CZ cy da de el es et eu fa_IR fi_FI fr gl_ES he_IL hr hu_HU hy id_ID is it ja_JP kab ko_KR ky lo_LA lt_LT lv_LV mk_MK nb_NO ne nl nn_NO oc pl_PL pt_BR pt_PT ro_RO ru sk_SK sl_SI sr sv th_TH tr uk_UA vi_VN zh_CN zh_TW
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating lib/Makefile
config.status: creating lib/libfilezilla.pc
config.status: creating lib/libfilezilla/version.hpp
config.status: creating lib/windows/version.rc
config.status: creating demos/Makefile
config.status: creating doc/Doxyfile
config.status: creating doc/Makefile
config.status: creating locales/Makefile
config.status: creating tests/Makefile
config.status: creating config/config.hpp
config.status: config/config.hpp is unchanged
config.status: executing depfiles commands
config.status: executing libtool commands

==> Building libfilezilla (with missing-#include auto-repair)
































make[1]: Entering directory '/home/mcw/libfilezilla/doc'
make[1]: Nothing to be done for 'all'.
make[1]: Leaving directory '/home/mcw/libfilezilla/doc'
Making install in .
make[1]: Entering directory '/home/mcw/libfilezilla'
make[2]: Entering directory '/home/mcw/libfilezilla'
make[2]: Nothing to be done for 'install-exec-am'.
make[2]: Nothing to be done for 'install-data-am'.
make[2]: Leaving directory '/home/mcw/libfilezilla'
make[1]: Leaving directory '/home/mcw/libfilezilla'
Making install in lib
make[1]: Entering directory '/home/mcw/libfilezilla/lib'
make[2]: Entering directory '/home/mcw/libfilezilla/lib'
 /usr/bin/mkdir -p '/home/mcw/prefix/lib'
 /bin/sh ../libtool   --mode=install /usr/bin/install -c   libfilezilla.la '/home/mcw/prefix/lib'
libtool: install: /usr/bin/install -c .libs/libfilezilla.dll.a /home/mcw/prefix/lib/libfilezilla.dll.a
libtool: install: base_file=`basename libfilezilla.la`
libtool: install:  dlpath=`/bin/sh 2>&1 -c '. .libs/'libfilezilla.la'i; echo libfilezilla-59.dll'`
libtool: install:  dldir=/home/mcw/prefix/lib/`dirname ../bin/libfilezilla-59.dll`
libtool: install:  test -d /home/mcw/prefix/lib/../bin || mkdir -p /home/mcw/prefix/lib/../bin
libtool: install:  /usr/bin/install -c .libs/libfilezilla-59.dll /home/mcw/prefix/lib/../bin/libfilezilla-59.dll
libtool: install:  chmod a+x /home/mcw/prefix/lib/../bin/libfilezilla-59.dll
libtool: install:  if test -n '' && test -n 'strip --strip-unneeded'; then eval 'strip --strip-unneeded /home/mcw/prefix/lib/../bin/libfilezilla-59.dll' || exit 0; fi
libtool: install: /usr/bin/install -c .libs/libfilezilla.lai /home/mcw/prefix/lib/libfilezilla.la
 /usr/bin/mkdir -p '/home/mcw/prefix/include'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/install -c -m 644  libfilezilla/basic_tls_params.hpp libfilezilla/ascii_layer.hpp libfilezilla/apply.hpp libfilezilla/buffer.hpp libfilezilla/encode.hpp libfilezilla/encryption.hpp libfilezilla/event.hpp libfilezilla/event_handler.hpp libfilezilla/event_loop.hpp libfilezilla/file.hpp libfilezilla/format.hpp libfilezilla/forward_like.hpp libfilezilla/fsresult.hpp libfilezilla/hash.hpp libfilezilla/hostname_lookup.hpp libfilezilla/impersonation.hpp libfilezilla/invoker.hpp libfilezilla/iputils.hpp libfilezilla/json.hpp libfilezilla/jws.hpp libfilezilla/libfilezilla.hpp libfilezilla/local_filesys.hpp libfilezilla/logger.hpp libfilezilla/mutex.hpp libfilezilla/nonowning_buffer.hpp libfilezilla/optional.hpp libfilezilla/process.hpp libfilezilla/rate_limiter.hpp libfilezilla/rate_limited_layer.hpp libfilezilla/recursive_remove.hpp libfilezilla/rwmutex.hpp libfilezilla/shared.hpp libfilezilla/signature.hpp libfilezilla/socket.hpp libfilezilla/string.hpp libfilezilla/thread.hpp libfilezilla/thread_pool.hpp libfilezilla/time.hpp libfilezilla/tls_info.hpp libfilezilla/tls_layer.hpp '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla/aio'
 /usr/bin/install -c -m 644  libfilezilla/aio/aio.hpp libfilezilla/aio/reader.hpp libfilezilla/aio/writer.hpp libfilezilla/aio/xml_writer.hpp '/home/mcw/prefix/include/libfilezilla/aio'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/install -c -m 644  libfilezilla/tls_params.hpp libfilezilla/tls_system_trust_store.hpp libfilezilla/translate.hpp libfilezilla/uri.hpp libfilezilla/util.hpp libfilezilla/visibility_helper.hpp libfilezilla/xml.hpp '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla/private'
 /usr/bin/install -c -m 644  libfilezilla/private/defs.hpp libfilezilla/private/visibility.hpp '/home/mcw/prefix/include/libfilezilla/private'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla/glue'
 /usr/bin/install -c -m 644  libfilezilla/glue/wx.hpp libfilezilla/glue/wxinvoker.hpp libfilezilla/glue/async_pipe.hpp libfilezilla/glue/dll.hpp libfilezilla/glue/registry.hpp libfilezilla/glue/windows.hpp '/home/mcw/prefix/include/libfilezilla/glue'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla/http'
 /usr/bin/install -c -m 644  libfilezilla/http/client.hpp libfilezilla/http/client_request.hpp libfilezilla/http/client_response.hpp libfilezilla/http/digest.hpp libfilezilla/http/headers.hpp '/home/mcw/prefix/include/libfilezilla/http'
 /usr/bin/mkdir -p '/home/mcw/prefix/include'
 /usr/bin/mkdir -p '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/install -c -m 644  libfilezilla/version.hpp '/home/mcw/prefix/include/libfilezilla'
 /usr/bin/mkdir -p '/home/mcw/prefix/lib/pkgconfig'
 /usr/bin/install -c -m 644 libfilezilla.pc '/home/mcw/prefix/lib/pkgconfig'
make[2]: Leaving directory '/home/mcw/libfilezilla/lib'
make[1]: Leaving directory '/home/mcw/libfilezilla/lib'
Making install in demos
make[1]: Entering directory '/home/mcw/libfilezilla/demos'
make[2]: Entering directory '/home/mcw/libfilezilla/demos'
make[2]: Nothing to be done for 'install-exec-am'.
make[2]: Nothing to be done for 'install-data-am'.
make[2]: Leaving directory '/home/mcw/libfilezilla/demos'
make[1]: Leaving directory '/home/mcw/libfilezilla/demos'
Making install in locales
make[1]: Entering directory '/home/mcw/libfilezilla/locales'
make[2]: Entering directory '/home/mcw/libfilezilla/locales'
make[2]: Nothing to be done for 'install-exec-am'.
for i in an ar az bg_BG ca ca_ES@valencia co cs_CZ cy da de el es et eu fa_IR fi_FI fr gl_ES he_IL hr hu_HU hy id_ID is it ja_JP kab ko_KR ky lo_LA lt_LT lv_LV mk_MK nb_NO ne nl nn_NO oc pl_PL pt_BR pt_PT ro_RO ru sk_SK sl_SI sr sv th_TH tr uk_UA vi_VN zh_CN zh_TW ; do \
  /bin/sh /home/mcw/libfilezilla/config/install-sh -d /home/mcw/prefix/share/locale/$i/LC_MESSAGES ; \
  /usr/bin/install -c -m 644 $i.mo /home/mcw/prefix/share/locale/$i/LC_MESSAGES/libfilezilla.mo ; \
done
make[2]: Leaving directory '/home/mcw/libfilezilla/locales'
make[1]: Leaving directory '/home/mcw/libfilezilla/locales'
Making install in doc
make[1]: Entering directory '/home/mcw/libfilezilla/doc'
make[2]: Entering directory '/home/mcw/libfilezilla/doc'
make[2]: Nothing to be done for 'install-exec-am'.
make[2]: Nothing to be done for 'install-data-am'.
make[2]: Leaving directory '/home/mcw/libfilezilla/doc'
make[1]: Leaving directory '/home/mcw/libfilezilla/doc'




  libfilezilla 0.57.0 installed to /home/mcw/prefix
  local patches saved to /home/mcw/libfilezilla-clangarm64-includes.patch

==> FileZilla trunk source
A    /home/mcw/filezilla/data
A    /home/mcw/filezilla/docs
A    /home/mcw/filezilla/locales
A    /home/mcw/filezilla/AUTHORS
A    /home/mcw/filezilla/docs/filezilla.man
A    /home/mcw/filezilla/docs/fzdefaults.xml.man
A    /home/mcw/filezilla/locales/Makefile.am
A    /home/mcw/filezilla/COPYING
A    /home/mcw/filezilla/ChangeLog
A    /home/mcw/filezilla/GPL.html
A    /home/mcw/filezilla/INSTALL
A    /home/mcw/filezilla/Makefile.am
A    /home/mcw/filezilla/NEWS
A    /home/mcw/filezilla/README
A    /home/mcw/filezilla/configure.ac
A    /home/mcw/filezilla/locales/ca.po
A    /home/mcw/filezilla/locales/ar.po
A    /home/mcw/filezilla/data/INetC.dll
A    /home/mcw/filezilla/data/Makefile.am
A    /home/mcw/filezilla/locales/cs_CZ.po
A    /home/mcw/filezilla/locales/bg_BG.po
A    /home/mcw/filezilla/locales/fi_FI.po
A    /home/mcw/filezilla/locales/co.po
A    /home/mcw/filezilla/locales/da.po
A    /home/mcw/filezilla/locales/en.po
A    /home/mcw/filezilla/locales/de.po
A    /home/mcw/filezilla/locales/es.po
A    /home/mcw/filezilla/locales/fa_IR.po
A    /home/mcw/filezilla/locales/gl_ES.po
A    /home/mcw/filezilla/locales/eu.po
A    /home/mcw/filezilla/locales/he_IL.po
A    /home/mcw/filezilla/locales/ga.po
A    /home/mcw/filezilla/locales/hu_HU.po
A    /home/mcw/filezilla/locales/hy.po
A    /home/mcw/filezilla/locales/ja_JP.po
A    /home/mcw/filezilla/locales/id_ID.po
A    /home/mcw/filezilla/locales/ka.po
A    /home/mcw/filezilla/locales/ku.po
A    /home/mcw/filezilla/locales/ko_KR.po
A    /home/mcw/filezilla/locales/lt_LT.po
A    /home/mcw/filezilla/locales/ne.po
A    /home/mcw/filezilla/data/UAC.dll
A    /home/mcw/filezilla/data/UAC.nsh
A    /home/mcw/filezilla/data/UAC_unicode.dll.txt
A    /home/mcw/filezilla/data/dllcopy.sh
A    /home/mcw/filezilla/data/dylibcopy.sh
A    /home/mcw/filezilla/data/filezilla.appdata.xml
A    /home/mcw/filezilla/data/filezilla.desktop
A    /home/mcw/filezilla/data/install.nsi.in
A    /home/mcw/filezilla/data/makezip.sh.in
A    /home/mcw/filezilla/data/nsis_appid.dll
A    /home/mcw/filezilla/data/nsis_appid.txt
A    /home/mcw/filezilla/m4
A    /home/mcw/filezilla/locales/lv_LV.po
A    /home/mcw/filezilla/locales/it.po
A    /home/mcw/filezilla/locales/km_KH.po
A    /home/mcw/filezilla/locales/lo_LA.po
A    /home/mcw/filezilla/locales/nb_NO.po
A    /home/mcw/filezilla/locales/nl.po
A    /home/mcw/filezilla/locales/pt_BR.po
A    /home/mcw/filezilla/data/offer.nsh
A    /home/mcw/filezilla/data/process_running.nsh
A    /home/mcw/filezilla/locales/pl_PL.po
A    /home/mcw/filezilla/locales/oc.po
A    /home/mcw/filezilla/locales/ro_RO.po
A    /home/mcw/filezilla/locales/sr.po
A    /home/mcw/filezilla/locales/tr.po
A    /home/mcw/filezilla/locales/sk_SK.po
A    /home/mcw/filezilla/locales/ta.po
A    /home/mcw/filezilla/src
A    /home/mcw/filezilla/locales/vi_VN.po
A    /home/mcw/filezilla/m4/ax_check_compile_flag.m4
A    /home/mcw/filezilla/m4/ax_cxx_compile_stdcxx_17.m4
A    /home/mcw/filezilla/data/uninstall.ico
A    /home/mcw/filezilla/docs/fzdefaults.xml.example
A    /home/mcw/filezilla/docs/iconspecs.htm
A    /home/mcw/filezilla/locales/an.po
A    /home/mcw/filezilla/src/commonui
A    /home/mcw/filezilla/locales/ru.po
A    /home/mcw/filezilla/locales/sv.po
A    /home/mcw/filezilla/locales/uk_UA.po
A    /home/mcw/filezilla/m4/ax_append_flag.m4
A    /home/mcw/filezilla/m4/ax_cxx_compile_stdcxx.m4
A    /home/mcw/filezilla/m4/check_libc++.m4
A    /home/mcw/filezilla/m4/check_time.m4
A    /home/mcw/filezilla/m4/map_emplace.m4
A    /home/mcw/filezilla/locales/az.po
A    /home/mcw/filezilla/locales/ca_ES@valencia.po
A    /home/mcw/filezilla/m4/check_regex.m4
A    /home/mcw/filezilla/m4/fz_check_pugixml.m4
A    /home/mcw/filezilla/m4/pkg.m4
A    /home/mcw/filezilla/locales/zh_TW.po
A    /home/mcw/filezilla/m4/ax_check_link_flag.m4
A    /home/mcw/filezilla/m4/check_clock_gettime.m4
A    /home/mcw/filezilla/src/commonui/Makefile.am
A    /home/mcw/filezilla/src/commonui/buildinfo.h
A    /home/mcw/filezilla/locales/cy.po
A    /home/mcw/filezilla/locales/el.po
A    /home/mcw/filezilla/locales/et.po
A    /home/mcw/filezilla/src/commonui/auto_ascii_files.cpp
A    /home/mcw/filezilla/src/commonui/cert_store.cpp
A    /home/mcw/filezilla/src/commonui/file_utils.cpp
A    /home/mcw/filezilla/m4/check_thread_local.m4
A    /home/mcw/filezilla/m4/icopyhookw.m4
A    /home/mcw/filezilla/src/Makefile.am
A    /home/mcw/filezilla/src/commonui/buildinfo.cpp
A    /home/mcw/filezilla/src/commonui/chmod_data.cpp
A    /home/mcw/filezilla/src/commonui/chmod_data.h
A    /home/mcw/filezilla/src/commonui/filter.h
A    /home/mcw/filezilla/src/commonui/hostkey_store.cpp
A    /home/mcw/filezilla/src/commonui/local_recursive_operation.cpp
A    /home/mcw/filezilla/src/commonui/fz_paths.cpp
A    /home/mcw/filezilla/src/commonui/hostkey_store.h
A    /home/mcw/filezilla/src/commonui/local_recursive_operation.h
A    /home/mcw/filezilla/src/commonui/misc.h
A    /home/mcw/filezilla/src/commonui/protect.h
A    /home/mcw/filezilla/src/commonui/filter.cpp
A    /home/mcw/filezilla/src/commonui/fz_paths_osx.mm
A    /home/mcw/filezilla/src/commonui/ipcmutex.h
A    /home/mcw/filezilla/src/commonui/login_manager.h
A    /home/mcw/filezilla/src/commonui/options.h
A    /home/mcw/filezilla/src/dbus
A    /home/mcw/filezilla/src/commonui/remote_recursive_operation.cpp
A    /home/mcw/filezilla/src/commonui/site.cpp
A    /home/mcw/filezilla/src/commonui/misc.cpp
A    /home/mcw/filezilla/src/commonui/protect.cpp
A    /home/mcw/filezilla/src/commonui/remote_recursive_operation.h
A    /home/mcw/filezilla/src/commonui/site_manager.h
A    /home/mcw/filezilla/src/commonui/updater_cert.h
A    /home/mcw/filezilla/src/commonui/site_manager.cpp
A    /home/mcw/filezilla/src/commonui/updater_cert.cpp
A    /home/mcw/filezilla/src/commonui/xml_cert_store.h
A    /home/mcw/filezilla/src/commonui/xmlfunctions.h
A    /home/mcw/filezilla/locales/fr.po
A    /home/mcw/filezilla/locales/hr.po
A    /home/mcw/filezilla/locales/is.po
A    /home/mcw/filezilla/src/commonui/site_color.h
A    /home/mcw/filezilla/src/commonui/updater.h
A    /home/mcw/filezilla/src/commonui/xml_cert_store.cpp
A    /home/mcw/filezilla/src/commonui/xmlfunctions.cpp
A    /home/mcw/filezilla/src/dbus/dbushandler.h
A    /home/mcw/filezilla/src/engine
A    /home/mcw/filezilla/locales/kab.po
A    /home/mcw/filezilla/locales/ky.po
A    /home/mcw/filezilla/locales/mk_MK.po
A    /home/mcw/filezilla/locales/nn_NO.po
A    /home/mcw/filezilla/locales/pt_PT.po
A    /home/mcw/filezilla/src/dbus/desktop_notification.cpp
A    /home/mcw/filezilla/src/dbus/session_manager.cpp
A    /home/mcw/filezilla/src/dbus/wxdbusmessage.cpp
A    /home/mcw/filezilla/src/commonui/xml_file.cpp
A    /home/mcw/filezilla/src/dbus/Makefile.am
A    /home/mcw/filezilla/src/dbus/desktop_notification.h
A    /home/mcw/filezilla/src/dbus/session_manager.h
A    /home/mcw/filezilla/src/dbus/power_management_inhibitor.h
A    /home/mcw/filezilla/src/dbus/wxdbusconnection.h
A    /home/mcw/filezilla/src/engine/ftp
A    /home/mcw/filezilla/locales/sl_SI.po
A    /home/mcw/filezilla/locales/th_TH.po
A    /home/mcw/filezilla/src/engine/activity_logger.cpp
A    /home/mcw/filezilla/src/engine/Makefile.am
A    /home/mcw/filezilla/locales/zh_CN.po
A    /home/mcw/filezilla/src/dbus/wxdbusmessage.h
A    /home/mcw/filezilla/src/engine/activity_logger_layer.cpp
A    /home/mcw/filezilla/src/engine/controlsocket.h
A    /home/mcw/filezilla/src/engine/directorylistingparser.cpp
A    /home/mcw/filezilla/src/engine/engineprivate.cpp
A    /home/mcw/filezilla/src/engine/ftp/chmod.cpp
A    /home/mcw/filezilla/src/engine/commands.cpp
A    /home/mcw/filezilla/src/engine/directorycache.h
A    /home/mcw/filezilla/src/engine/engine_context.cpp
A    /home/mcw/filezilla/src/engine/controlsocket.cpp
A    /home/mcw/filezilla/src/engine/directorylisting.cpp
A    /home/mcw/filezilla/src/engine/engine_options.cpp
A    /home/mcw/filezilla/src/engine/filezilla.h
A    /home/mcw/filezilla/src/engine/ftp/delete.cpp
A    /home/mcw/filezilla/src/engine/ftp/cwd.h
A    /home/mcw/filezilla/src/engine/ftp/filetransfer.h
A    /home/mcw/filezilla/src/engine/ftp/list.h
A    /home/mcw/filezilla/m4/ax_check_define.m4
A    /home/mcw/filezilla/m4/check_atomic.m4
A    /home/mcw/filezilla/m4/check_steady_clock.m4
A    /home/mcw/filezilla/m4/fz_checkversion.m4
A    /home/mcw/filezilla/src/engine/http
A    /home/mcw/filezilla/src/engine/externalipresolver.cpp
A    /home/mcw/filezilla/src/engine/ftp/cwd.cpp
A    /home/mcw/filezilla/src/engine/ftp/filetransfer.cpp
A    /home/mcw/filezilla/m4/wxwin.m4
A    /home/mcw/filezilla/src/commonui/auto_ascii_files.h
A    /home/mcw/filezilla/src/commonui/cert_store.h
A    /home/mcw/filezilla/src/commonui/file_utils.h
A    /home/mcw/filezilla/src/commonui/fz_paths.h
A    /home/mcw/filezilla/src/commonui/ipcmutex.cpp
A    /home/mcw/filezilla/src/commonui/login_manager.cpp
A    /home/mcw/filezilla/src/engine/ftp/mkd.h
A    /home/mcw/filezilla/src/engine/ftp/rawtransfer.h
A    /home/mcw/filezilla/src/engine/ftp/rmd.h
A    /home/mcw/filezilla/src/engine/ftp/list.cpp
A    /home/mcw/filezilla/src/engine/ftp/mkd.cpp
A    /home/mcw/filezilla/src/engine/ftp/rawtransfer.cpp
A    /home/mcw/filezilla/src/engine/ftp/rmd.cpp
A    /home/mcw/filezilla/src/engine/http/filetransfer.h
A    /home/mcw/filezilla/src/engine/http/request.h
A    /home/mcw/filezilla/src/engine/logging_private.h
A    /home/mcw/filezilla/src/engine/notification.cpp
A    /home/mcw/filezilla/src/engine/ftp/ftpcontrolsocket.cpp
A    /home/mcw/filezilla/src/engine/http/filetransfer.cpp
A    /home/mcw/filezilla/src/engine/http/request.cpp
A    /home/mcw/filezilla/src/engine/logging.cpp
A    /home/mcw/filezilla/src/engine/misc.cpp
A    /home/mcw/filezilla/src/engine/sftp
A    /home/mcw/filezilla/src/engine/pathcache.cpp
A    /home/mcw/filezilla/src/engine/proxy.h
A    /home/mcw/filezilla/src/engine/ftp/logon.cpp
A    /home/mcw/filezilla/src/engine/ftp/rawcommand.cpp
A    /home/mcw/filezilla/src/engine/ftp/rename.cpp
A    /home/mcw/filezilla/src/engine/ftp/transfersocket.cpp
A    /home/mcw/filezilla/src/engine/http/httpcontrolsocket.cpp
A    /home/mcw/filezilla/src/engine/local_path.cpp
A    /home/mcw/filezilla/src/engine/lookup.cpp
A    /home/mcw/filezilla/src/engine/oplock_manager.cpp
A    /home/mcw/filezilla/src/engine/pathcache.h
A    /home/mcw/filezilla/src/engine/servercapabilities.cpp
A    /home/mcw/filezilla/src/commonui/options.cpp
A    /home/mcw/filezilla/src/commonui/recursive_operation.h
A    /home/mcw/filezilla/src/commonui/site.h
A    /home/mcw/filezilla/src/engine/rtt.cpp
A    /home/mcw/filezilla/src/engine/sftp/chmod.h
A    /home/mcw/filezilla/src/commonui/updater.cpp
A    /home/mcw/filezilla/src/commonui/visibility.h
A    /home/mcw/filezilla/src/commonui/xml_file.h
A    /home/mcw/filezilla/src/dbus/dbushandler.cpp
A    /home/mcw/filezilla/src/dbus/power_management_inhibitor.cpp
A    /home/mcw/filezilla/src/dbus/wxdbusconnection.cpp
A    /home/mcw/filezilla/src/engine/FileZillaEngine.cpp
A    /home/mcw/filezilla/src/engine/activity_logger_layer.h
A    /home/mcw/filezilla/src/engine/storj
A    /home/mcw/filezilla/src/engine/optionsbase.cpp
A    /home/mcw/filezilla/src/engine/proxy.cpp
A    /home/mcw/filezilla/src/engine/server.cpp
A    /home/mcw/filezilla/src/engine/sftp/chmod.cpp
A    /home/mcw/filezilla/src/engine/sftp/delete.cpp
A    /home/mcw/filezilla/src/engine/sftp/list.cpp
A    /home/mcw/filezilla/src/engine/sftp/rename.cpp
A    /home/mcw/filezilla/src/engine/sftp/sftpcontrolsocket.cpp
A    /home/mcw/filezilla/src/engine/storj/connect.h
A    /home/mcw/filezilla/src/engine/sftp/delete.h
A    /home/mcw/filezilla/src/engine/sftp/list.h
A    /home/mcw/filezilla/src/engine/sftp/rename.h
A    /home/mcw/filezilla/src/engine/sftp/sftpcontrolsocket.h
A    /home/mcw/filezilla/src/engine/storj/delete.cpp
A    /home/mcw/filezilla/src/engine/servercapabilities.h
A    /home/mcw/filezilla/src/engine/sftp/connect.cpp
A    /home/mcw/filezilla/src/engine/sftp/filetransfer.cpp
A    /home/mcw/filezilla/src/engine/sftp/mkd.cpp
A    /home/mcw/filezilla/src/engine/sftp/rmd.cpp
A    /home/mcw/filezilla/src/engine/sizeformatting.cpp
A    /home/mcw/filezilla/src/engine/storj/delete.h
A    /home/mcw/filezilla/src/fzshellext
A    /home/mcw/filezilla/src/fzshellext/32
A    /home/mcw/filezilla/src/fzshellext/64
A    /home/mcw/filezilla/src/engine/storj/file_transfer.h
A    /home/mcw/filezilla/src/engine/storj/list.h
A    /home/mcw/filezilla/src/engine/storj/rmd.h
A    /home/mcw/filezilla/src/engine/storj/file_transfer.cpp
A    /home/mcw/filezilla/src/engine/storj/list.cpp
A    /home/mcw/filezilla/src/engine/directorycache.cpp
A    /home/mcw/filezilla/src/engine/directorylistingparser.h
A    /home/mcw/filezilla/src/engine/engineprivate.h
A    /home/mcw/filezilla/src/engine/ftp/chmod.h
A    /home/mcw/filezilla/src/engine/ftp/delete.h
A    /home/mcw/filezilla/src/engine/ftp/ftpcontrolsocket.h
A    /home/mcw/filezilla/src/engine/ftp/logon.h
A    /home/mcw/filezilla/src/engine/ftp/rawcommand.h
A    /home/mcw/filezilla/src/engine/ftp/rename.h
A    /home/mcw/filezilla/src/engine/ftp/transfersocket.h
A    /home/mcw/filezilla/src/engine/http/httpcontrolsocket.h
A    /home/mcw/filezilla/src/engine/storj/input_thread.cpp
A    /home/mcw/filezilla/src/engine/storj/mkd.cpp
A    /home/mcw/filezilla/src/engine/storj/storjcontrolsocket.cpp
A    /home/mcw/filezilla/src/include
A    /home/mcw/filezilla/src/engine/tls.h
A    /home/mcw/filezilla/src/fzshellext/configure.ac
A    /home/mcw/filezilla/src/engine/version.cpp
A    /home/mcw/filezilla/src/fzshellext/shellext.h
A    /home/mcw/filezilla/src/engine/storj/rmd.cpp
A    /home/mcw/filezilla/src/engine/tls.cpp
A    /home/mcw/filezilla/src/fzshellext/Makefile.am
A    /home/mcw/filezilla/src/fzshellext/shellext.cpp
A    /home/mcw/filezilla/src/engine/logfile_writer.cpp
A    /home/mcw/filezilla/src/engine/lookup.h
A    /home/mcw/filezilla/src/engine/oplock_manager.h
A    /home/mcw/filezilla/src/engine/posix_chmod.cpp
A    /home/mcw/filezilla/src/engine/rtt.h
A    /home/mcw/filezilla/src/interface
A    /home/mcw/filezilla/src/include/Makefile.am
A    /home/mcw/filezilla/src/include/engine_context.h
A    /home/mcw/filezilla/src/include/local_path.h
A    /home/mcw/filezilla/src/include/notification.h
A    /home/mcw/filezilla/src/include/server.h
A    /home/mcw/filezilla/src/fzshellext/fzshellext.rc
A    /home/mcw/filezilla/src/fzshellext/version.rc.in
A    /home/mcw/filezilla/src/include/commands.h
A    /home/mcw/filezilla/src/include/externalipresolver.h
A    /home/mcw/filezilla/src/include/logging.h
A    /home/mcw/filezilla/src/include/posix_chmod.h
A    /home/mcw/filezilla/src/include/activity_logger.h
A    /home/mcw/filezilla/src/include/engine_options.h
A    /home/mcw/filezilla/src/include/logfile_writer.h
A    /home/mcw/filezilla/src/include/optionsbase.h
A    /home/mcw/filezilla/src/include/serverpath.h
A    /home/mcw/filezilla/src/include/visibility.h
A    /home/mcw/filezilla/src/interface/LocalListView.cpp
A    /home/mcw/filezilla/src/include/version.h
A    /home/mcw/filezilla/src/interface/FileZilla.cpp
A    /home/mcw/filezilla/src/engine/serverpath.cpp
A    /home/mcw/filezilla/src/engine/sftp/connect.h
A    /home/mcw/filezilla/src/engine/sftp/filetransfer.h
A    /home/mcw/filezilla/src/engine/sftp/mkd.h
A    /home/mcw/filezilla/src/engine/sftp/rmd.h
A    /home/mcw/filezilla/src/engine/storj/connect.cpp
A    /home/mcw/filezilla/src/include/setup.h
A    /home/mcw/filezilla/src/include/xml_string_writer.h
A    /home/mcw/filezilla/src/interface/LocalListView.h
A    /home/mcw/filezilla/src/interface/Mainfrm.h
A    /home/mcw/filezilla/src/interface/QueueView.cpp
A    /home/mcw/filezilla/src/interface/Mainfrm.cpp
A    /home/mcw/filezilla/src/interface/Options.h
A    /home/mcw/filezilla/src/interface/RemoteListView.h
A    /home/mcw/filezilla/src/interface/StatusView.h
A    /home/mcw/filezilla/src/interface/LocalTreeView.h
A    /home/mcw/filezilla/src/interface/Options.cpp
A    /home/mcw/filezilla/src/engine/storj/event.h
A    /home/mcw/filezilla/src/engine/storj/input_thread.h
A    /home/mcw/filezilla/src/engine/storj/mkd.h
A    /home/mcw/filezilla/src/engine/storj/storjcontrolsocket.h
A    /home/mcw/filezilla/src/engine/xmlutils.cpp
A    /home/mcw/filezilla/src/fzshellext/resource.h
A    /home/mcw/filezilla/src/include/FileZillaEngine.h
A    /home/mcw/filezilla/src/include/directorylisting.h
A    /home/mcw/filezilla/src/include/libfilezilla_engine.h
A    /home/mcw/filezilla/src/include/misc.h
A    /home/mcw/filezilla/src/include/s3sse.h
A    /home/mcw/filezilla/src/interface/asksavepassworddialog.h
A    /home/mcw/filezilla/src/interface/aui_notebook_ex.h
A    /home/mcw/filezilla/src/interface/buildinfo.h
A    /home/mcw/filezilla/src/interface/clearprivatedata.h
A    /home/mcw/filezilla/src/interface/RemoteListView.cpp
A    /home/mcw/filezilla/src/interface/StatusView.cpp
A    /home/mcw/filezilla/src/interface/asksavepassworddialog.cpp
A    /home/mcw/filezilla/src/interface/aui_notebook_ex.cpp
A    /home/mcw/filezilla/src/interface/buildinfo.cpp
A    /home/mcw/filezilla/src/interface/clearprivatedata.cpp
A    /home/mcw/filezilla/src/interface/RemoteTreeView.cpp
A    /home/mcw/filezilla/src/interface/aboutdialog.cpp
A    /home/mcw/filezilla/src/interface/asyncrequestqueue.cpp
A    /home/mcw/filezilla/src/interface/bookmarks_dialog.cpp
A    /home/mcw/filezilla/src/interface/chmoddialog.cpp
A    /home/mcw/filezilla/src/interface/cmdline.cpp
A    /home/mcw/filezilla/src/interface/commandqueue.h
A    /home/mcw/filezilla/src/interface/context_control.h
A    /home/mcw/filezilla/src/interface/defaultfileexistsdlg.h
A    /home/mcw/filezilla/src/interface/dndobjects.cpp
A    /home/mcw/filezilla/src/interface/drop_target_ex.cpp
A    /home/mcw/filezilla/src/interface/dropsource_mac.mm
A    /home/mcw/filezilla/src/interface/commandqueue.cpp
A    /home/mcw/filezilla/src/interface/context_control.cpp
A    /home/mcw/filezilla/src/interface/defaultfileexistsdlg.cpp
A    /home/mcw/filezilla/src/interface/conditionaldialog.cpp
A    /home/mcw/filezilla/src/interface/customheightlistctrl.cpp
A    /home/mcw/filezilla/src/interface/dialogex.cpp
A    /home/mcw/filezilla/src/interface/dndobjects.h
A    /home/mcw/filezilla/src/interface/drop_target_ex.h
A    /home/mcw/filezilla/src/interface/encoding_converter.h
A    /home/mcw/filezilla/src/include/sizeformatting.h
A    /home/mcw/filezilla/src/include/xmlutils.h
A    /home/mcw/filezilla/src/interface/LocalTreeView.cpp
A    /home/mcw/filezilla/src/interface/Makefile.am
A    /home/mcw/filezilla/src/interface/QueueView.h
A    /home/mcw/filezilla/src/interface/RemoteTreeView.h
A    /home/mcw/filezilla/src/interface/aboutdialog.h
A    /home/mcw/filezilla/src/interface/asyncrequestqueue.h
A    /home/mcw/filezilla/src/interface/bookmarks_dialog.h
A    /home/mcw/filezilla/src/interface/chmoddialog.h
A    /home/mcw/filezilla/src/interface/cmdline.h
A    /home/mcw/filezilla/src/interface/dialogex_mac.mm
A    /home/mcw/filezilla/src/interface/dragdropmanager.h
A    /home/mcw/filezilla/src/interface/dropsource.h
A    /home/mcw/filezilla/src/interface/encoding_converter.cpp
A    /home/mcw/filezilla/src/interface/file_utils.cpp
A    /home/mcw/filezilla/src/interface/file_utils.h
A    /home/mcw/filezilla/src/interface/filelist_statusbar.h
A    /home/mcw/filezilla/src/interface/filezillaapp.h
A    /home/mcw/filezilla/src/interface/filter_manager.h
A    /home/mcw/filezilla/src/interface/graphics.h
A    /home/mcw/filezilla/src/interface/infotext.h
A    /home/mcw/filezilla/src/interface/led.h
A    /home/mcw/filezilla/src/interface/filelist_statusbar.cpp
A    /home/mcw/filezilla/src/interface/filezilla.h
A    /home/mcw/filezilla/src/interface/filter_manager.cpp
A    /home/mcw/filezilla/src/interface/graphics.cpp
A    /home/mcw/filezilla/src/interface/infotext.cpp
A    /home/mcw/filezilla/src/interface/led.cpp
A    /home/mcw/filezilla/src/interface/listctrlex.h
A    /home/mcw/filezilla/src/interface/local_recursive_operation.h
A    /home/mcw/filezilla/src/interface/loginmanager.h
A    /home/mcw/filezilla/src/interface/menu_bar.h
A    /home/mcw/filezilla/src/interface/conditionaldialog.h
A    /home/mcw/filezilla/src/interface/customheightlistctrl.h
A    /home/mcw/filezilla/src/interface/dialogex.h
A    /home/mcw/filezilla/src/interface/dragdropmanager.cpp
A    /home/mcw/filezilla/src/interface/dropsource.cpp
A    /home/mcw/filezilla/src/interface/edithandler.h
A    /home/mcw/filezilla/src/interface/edithandler.cpp
A    /home/mcw/filezilla/src/interface/export.cpp
A    /home/mcw/filezilla/src/interface/fileexistsdlg.cpp
A    /home/mcw/filezilla/src/interface/filelistctrl.cpp
A    /home/mcw/filezilla/src/interface/filter_conditions_dialog.cpp
A    /home/mcw/filezilla/src/interface/filteredit.cpp
A    /home/mcw/filezilla/src/interface/import.cpp
A    /home/mcw/filezilla/src/interface/inputdialog.cpp
A    /home/mcw/filezilla/src/interface/list_search_panel.cpp
A    /home/mcw/filezilla/src/interface/listingcomparison.cpp
A    /home/mcw/filezilla/src/interface/locale_initializer.cpp
A    /home/mcw/filezilla/src/interface/export.h
A    /home/mcw/filezilla/src/interface/fileexistsdlg.h
A    /home/mcw/filezilla/src/interface/filelistctrl.h
A    /home/mcw/filezilla/src/interface/filter_conditions_dialog.h
A    /home/mcw/filezilla/src/interface/filteredit.h
A    /home/mcw/filezilla/src/interface/resources
A    /home/mcw/filezilla/src/interface/resources/16x16
A    /home/mcw/filezilla/src/interface/netconfwizard.h
A    /home/mcw/filezilla/src/interface/osx_sandbox_userdirs.h
A    /home/mcw/filezilla/src/interface/power_management.h
A    /home/mcw/filezilla/src/interface/listctrlex.cpp
A    /home/mcw/filezilla/src/interface/local_recursive_operation.cpp
A    /home/mcw/filezilla/src/interface/resources/20x20
A    /home/mcw/filezilla/src/interface/resources/24x24
A    /home/mcw/filezilla/src/interface/manual_transfer.cpp
A    /home/mcw/filezilla/src/interface/msgbox.cpp
A    /home/mcw/filezilla/src/interface/option_change_event_handler.cpp
A    /home/mcw/filezilla/src/interface/overlay.cpp
A    /home/mcw/filezilla/src/interface/power_management_osx.mm
A    /home/mcw/filezilla/src/interface/queue_storage.h
A    /home/mcw/filezilla/src/interface/resources/32x32
A    /home/mcw/filezilla/src/interface/resources/480x480
A    /home/mcw/filezilla/src/interface/resources/48x48
A    /home/mcw/filezilla/src/interface/resources/blukis
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16
A    /home/mcw/filezilla/src/interface/queue_storage.cpp
A    /home/mcw/filezilla/src/interface/queueview_successful.cpp
A    /home/mcw/filezilla/src/interface/recentserverlist.cpp
A    /home/mcw/filezilla/src/interface/remote_recursive_operation.cpp
A    /home/mcw/filezilla/src/interface/resources/16x16/filezilla.png
A    /home/mcw/filezilla/src/interface/loginmanager.cpp
A    /home/mcw/filezilla/src/interface/menu_bar.cpp
A    /home/mcw/filezilla/src/interface/netconfwizard.cpp
A    /home/mcw/filezilla/src/interface/osx_sandbox_userdirs.cpp
A    /home/mcw/filezilla/src/interface/power_management.cpp
A    /home/mcw/filezilla/src/interface/queue.h
A    /home/mcw/filezilla/src/interface/queueview_failed.h
A    /home/mcw/filezilla/src/interface/quickconnectbar.h
A    /home/mcw/filezilla/src/interface/recursive_operation_status.h
A    /home/mcw/filezilla/src/interface/import.h
A    /home/mcw/filezilla/src/interface/inputdialog.h
A    /home/mcw/filezilla/src/interface/list_search_panel.h
A    /home/mcw/filezilla/src/interface/listingcomparison.h
A    /home/mcw/filezilla/src/interface/locale_initializer.h
A    /home/mcw/filezilla/src/interface/manual_transfer.h
A    /home/mcw/filezilla/src/interface/msgbox.h
A    /home/mcw/filezilla/src/interface/option_change_event_handler.h
A    /home/mcw/filezilla/src/interface/queueview_successful.h
A    /home/mcw/filezilla/src/interface/recentserverlist.h
A    /home/mcw/filezilla/src/interface/remote_recursive_operation.h
A    /home/mcw/filezilla/src/interface/resources/16x16/throbber.gif
A    /home/mcw/filezilla/src/interface/resources/24x24/unknown.png
A    /home/mcw/filezilla/src/interface/overlay.h
A    /home/mcw/filezilla/src/interface/queue.cpp
A    /home/mcw/filezilla/src/interface/queueview_failed.cpp
A    /home/mcw/filezilla/src/interface/resources/32x32/filezilla.png
A    /home/mcw/filezilla/src/interface/resources/FileZilla.icns
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/renderer.h
A    /home/mcw/filezilla/src/interface/resources/20x20/unknown.png
A    /home/mcw/filezilla/src/interface/resources/48x48/filezilla.png
A    /home/mcw/filezilla/src/interface/resources/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/showhidden.png
A    /home/mcw/filezilla/src/interface/quickconnectbar.cpp
A    /home/mcw/filezilla/src/interface/recursive_operation_status.cpp
A    /home/mcw/filezilla/src/interface/renderer.cpp
A    /home/mcw/filezilla/src/interface/resources/16x16/unknown.png
A    /home/mcw/filezilla/src/interface/resources/480x480/filezilla.png
A    /home/mcw/filezilla/src/interface/resources/MacInfo.plist.in
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/folderback.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/FileZilla.ico
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/bookmarks.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/folderup.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/binary.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/compare.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/auto.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/cancel.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/folder.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/help.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/blukis/16x16/symlink.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/ascii.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/bookmarks.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/download.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/find.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/folderup.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/logview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/refresh.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/filter.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/lock.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/auto.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/classic
A    /home/mcw/filezilla/src/interface/resources/classic/16x16
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/folderback.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/queueview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/server.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/symlink.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/bookmarks.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/find.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/folderup.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/blukis/32x32/upload.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/folderback.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/server.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/symlink.png
A    /home/mcw/filezilla/src/interface/resources/blukis/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/cyril
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/blukis/theme.xml
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/help.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/blukis/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/folderback.png
A    /home/mcw/filezilla/src/interface/resources/default
A    /home/mcw/filezilla/src/interface/resources/default/480x480
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/classic/theme.xml
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/classic/16x16/symlink.png
A    /home/mcw/filezilla/src/interface/resources/classic/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/folderup.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/cyril/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/default/480x480/binary.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/auto.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/cancel.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/download.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/ascii.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/cyril/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/cyril/theme.xml
A    /home/mcw/filezilla/src/interface/resources/default/480x480/close.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/bookmarks.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/file.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/folderback.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/compare.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/dropdown.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/folder.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/help.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/filter.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16
A    /home/mcw/filezilla/src/interface/resources/default/480x480/find.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/folderup.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/lock.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/logview.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/refresh.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/queueview.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/server.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/sort_down_light.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/symlink.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/treeitem_collapsed_light.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/filezilla.entitlements
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/sort_up_dark.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/treeitem_expanded_dark.png
A    /home/mcw/filezilla/src/interface/resources/default/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/default/480x480/leds.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/sort_down_dark.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24
A    /home/mcw/filezilla/src/interface/resources/default/480x480/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/sort_up_light.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/binary.png
A    /home/mcw/filezilla/src/interface/resources/filezilla.rc
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/treeitem_collapsed_dark.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/upload.png
A    /home/mcw/filezilla/src/interface/resources/defaultfilters.xml
A    /home/mcw/filezilla/src/interface/resources/default/480x480/synctransfer.png
A    /home/mcw/filezilla/src/interface/resources/default/480x480/treeitem_expanded_light.png
A    /home/mcw/filezilla/src/interface/resources/default/theme.xml
A    /home/mcw/filezilla/src/interface/resources/filezilla.svg
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/filter.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/help.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/download.png
A    /home/mcw/filezilla/src/interface/resources/finished.wav
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/leds.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/ascii.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/cancel.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/folder.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/queueview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/logview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/refresh.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/ascii.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/cancel.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/folder.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/server.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/upload.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/binary.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/find.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/leds.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/auto.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/compare.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/queueview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/server.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/upload.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/auto.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/compare.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/file.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/lock.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/lock.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/24x24/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/download.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/find.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/filter.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/help.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/logview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/refresh.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/lone
A    /home/mcw/filezilla/src/interface/resources/lone/16x16
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/help.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/find.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/leds.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/32x32/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/auto.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/leds.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/theme.xml
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/server.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/helper.entitlements
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/binary.png
A    /home/mcw/filezilla/src/interface/resources/flatzilla/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/folderback.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/auto.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/compare.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/folderup.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/download.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/folder.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/filter.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/folderup.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/logview.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/refresh.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/help.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/lock.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/ascii.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/cancel.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/folderback.png
A    /home/mcw/filezilla/src/interface/resources/minimal
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/help.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/queueview.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/upload.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/32x32/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/auto.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/folderback.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/bookmarks.png
A    /home/mcw/filezilla/src/interface/resources/minimal/32x32
A    /home/mcw/filezilla/src/interface/resources/opencrystal
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/lone/theme.xml
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/folderup.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/folderup.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/lone/48x48/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/lone/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/folderback.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/minimal/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/20x20
A    /home/mcw/filezilla/src/interface/resources/opencrystal/24x24
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/minimal/theme.xml
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/folderup.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/minimal/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/minimal/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/folderback.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/24x24/server.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/download.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/find.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/folderup.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/help.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/20x20/server.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/binary.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/filter.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/auto.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/compare.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/lock.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/logview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/refresh.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/folderback.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/queueview.png
A    /home/mcw/filezilla/src/interface/resources/sun
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/ascii.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/cancel.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/folder.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/help.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/upload.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/help.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/32x32/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/auto.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/find.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/folderup.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/tango
A    /home/mcw/filezilla/src/interface/resources/tango/16x16
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/folderback.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/theme.xml
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/find.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/folderup.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/auto.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/folderback.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/auto.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/showhidden.png
A    /home/mcw/filezilla/src/interface/resources/opencrystal/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/help.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/speedlimits.png
A    /home/mcw/filezilla/src/interface/resources/sun/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/binary.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/compare.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/file.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/ascii.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/cancel.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/folder.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/logview.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/refresh.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/ascii.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/sun/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/sun/theme.xml
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/download.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/find.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/lock.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/unknown.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/auto.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/compare.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/file.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/unknown.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/cancel.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/folder.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/filter.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/queueview.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/server.png
A    /home/mcw/filezilla/src/interface/resources/tango/16x16/upload.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/binary.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/filter.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/queueview.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/server.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/auto.png
A    /home/mcw/filezilla/src/interface/settings
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/download.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/find.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/lock.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/upload.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/binary.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/disconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/logview.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/refresh.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/ascii.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/tango/32x32/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/bookmark.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/download.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/find.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/lock.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/reconnect.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/compare.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/file.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/folderclosed.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/processqueue.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/remotetreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/unknown.png
A    /home/mcw/filezilla/src/interface/resources/tango/theme.xml
A    /home/mcw/filezilla/src/interface/search.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_ftp.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_sftp.h
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/cancel.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/downloadadd.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/folder.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/logview.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/refresh.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/synchronize.png
A    /home/mcw/filezilla/src/interface/resources/tango/Makefile.am
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/filter.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/localtreeview.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/queueview.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/server.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/upload.png
A    /home/mcw/filezilla/src/interface/resources/version.rc.in
A    /home/mcw/filezilla/src/interface/settings/optionspage.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_active.cpp
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/sitemanager.png
A    /home/mcw/filezilla/src/interface/resources/tango/48x48/uploadadd.png
A    /home/mcw/filezilla/src/interface/resources/windows_manifest.xml
A    /home/mcw/filezilla/src/interface/settings/optionspage.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_debug.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_edit_associations.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_filelists.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_ftpproxy.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_language.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_passwords.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_sizeformatting.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_passive.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_dateformatting.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_edit.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_fileexists.cpp
A    /home/mcw/filezilla/src/interface/search.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_ftp.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_sftp.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_debug.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_edit_associations.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_filelists.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_ftpproxy.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_language.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_passwords.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_sizeformatting.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_filetype.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_interface.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_logging.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_proxy.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_themes.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_updatecheck.cpp
A    /home/mcw/filezilla/src/interface/sftp_crypt_info_dlg.cpp
A    /home/mcw/filezilla/src/interface/settings/optionspage_transfer.h
A    /home/mcw/filezilla/src/interface/settings/settingsdialog.h
A    /home/mcw/filezilla/src/interface/sitemanager.h
A    /home/mcw/filezilla/src/interface/sitemanager_dialog.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_active.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_connection_passive.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_dateformatting.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_edit.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_fileexists.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_filetype.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_interface.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_transfer.cpp
A    /home/mcw/filezilla/src/interface/settings/settingsdialog.cpp
A    /home/mcw/filezilla/src/interface/sitemanager.cpp
A    /home/mcw/filezilla/src/interface/sitemanager_dialog.cpp
A    /home/mcw/filezilla/src/interface/speedlimits_dialog.cpp
A    /home/mcw/filezilla/src/interface/state.cpp
A    /home/mcw/filezilla/src/interface/statuslinectrl.cpp
A    /home/mcw/filezilla/src/interface/speedlimits_dialog.h
A    /home/mcw/filezilla/src/interface/state.h
A    /home/mcw/filezilla/src/interface/statuslinectrl.h
A    /home/mcw/filezilla/src/interface/systemimagelist.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_logging.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_proxy.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_themes.h
A    /home/mcw/filezilla/src/interface/settings/optionspage_updatecheck.h
A    /home/mcw/filezilla/src/interface/sftp_crypt_info_dlg.h
A    /home/mcw/filezilla/src/interface/sitemanager_controls.h
A    /home/mcw/filezilla/src/interface/sitemanager_site.h
A    /home/mcw/filezilla/src/interface/splitter.h
A    /home/mcw/filezilla/src/interface/statusbar.h
A    /home/mcw/filezilla/src/interface/storj_key_interface.h
A    /home/mcw/filezilla/src/interface/textctrlex.h
A    /home/mcw/filezilla/src/interface/wxext
A    /home/mcw/filezilla/src/pugixml
A    /home/mcw/filezilla/src/interface/themeprovider.h
A    /home/mcw/filezilla/src/interface/toolbar.h
A    /home/mcw/filezilla/src/interface/update_dialog.cpp
A    /home/mcw/filezilla/src/interface/verifyhostkeydialog.cpp
A    /home/mcw/filezilla/src/interface/viewheader.cpp
A    /home/mcw/filezilla/src/interface/systemimagelist.cpp
A    /home/mcw/filezilla/src/interface/themeprovider.cpp
A    /home/mcw/filezilla/src/interface/toolbar.cpp
A    /home/mcw/filezilla/src/interface/treectrlex.h
A    /home/mcw/filezilla/src/interface/sitemanager_controls.cpp
A    /home/mcw/filezilla/src/interface/sitemanager_site.cpp
A    /home/mcw/filezilla/src/interface/splitter.cpp
A    /home/mcw/filezilla/src/interface/statusbar.cpp
A    /home/mcw/filezilla/src/interface/storj_key_interface.cpp
A    /home/mcw/filezilla/src/interface/textctrlex.cpp
A    /home/mcw/filezilla/src/interface/timeformatting.cpp
A    /home/mcw/filezilla/src/interface/toolbar.mm
A    /home/mcw/filezilla/src/interface/update_dialog.h
A    /home/mcw/filezilla/src/interface/verifyhostkeydialog.h
A    /home/mcw/filezilla/src/interface/viewheader.h
A    /home/mcw/filezilla/src/storj
A    /home/mcw/filezilla/tests
A    /home/mcw/filezilla/src/interface/welcome_dialog.cpp
A    /home/mcw/filezilla/src/interface/wrapengine.cpp
A    /home/mcw/filezilla/src/interface/timeformatting.h
A    /home/mcw/filezilla/src/interface/treectrlex.cpp
A    /home/mcw/filezilla/src/interface/verifycertdialog.cpp
A    /home/mcw/filezilla/src/interface/verifycertdialog.h
A    /home/mcw/filezilla/src/interface/view.h
A    /home/mcw/filezilla/src/interface/volume_enumerator.h
A    /home/mcw/filezilla/src/interface/window_state_manager.h
A    /home/mcw/filezilla/src/interface/wxext/spinctrlex.h
A    /home/mcw/filezilla/src/interface/xh_text_ex.h
A    /home/mcw/filezilla/src/interface/xrc_helper.h
A    /home/mcw/filezilla/src/interface/welcome_dialog.h
A    /home/mcw/filezilla/src/interface/wrapengine.h
A    /home/mcw/filezilla/src/interface/wxfilesystem_blob_handler.h
A    /home/mcw/filezilla/src/interface/xmlfunctions.h
A    /home/mcw/filezilla/src/pugixml/pugiconfig.hpp
A    /home/mcw/filezilla/src/storj/events.hpp
A    /home/mcw/filezilla/src/interface/view.cpp
A    /home/mcw/filezilla/src/interface/volume_enumerator.cpp
A    /home/mcw/filezilla/src/interface/window_state_manager.cpp
A    /home/mcw/filezilla/src/interface/wxext/spinctrlex.cpp
A    /home/mcw/filezilla/src/interface/xh_text_ex.cpp
A    /home/mcw/filezilla/src/interface/xrc_helper.cpp
A    /home/mcw/filezilla/src/pugixml/pugixml.cpp
A    /home/mcw/filezilla/src/storj/fzstorj.cpp
A    /home/mcw/filezilla/src/interface/wxfilesystem_blob_handler.cpp
A    /home/mcw/filezilla/src/interface/xmlfunctions.cpp
A    /home/mcw/filezilla/src/pugixml/Makefile.am
A    /home/mcw/filezilla/src/storj/Makefile.am
A    /home/mcw/filezilla/tests/cmpnatural.cpp
A    /home/mcw/filezilla/tests/serverpathtest.cpp
A    /home/mcw/filezilla/src/pugixml/pugixml.hpp
A    /home/mcw/filezilla/tests/Makefile.am
A    /home/mcw/filezilla/tests/localpathtest.cpp
A    /home/mcw/filezilla/tests/dirparsertest.cpp
A    /home/mcw/filezilla/tests/test.cpp
A    /home/mcw/filezilla/tests/gui_test.cpp
 U   /home/mcw/filezilla
Checked out revision 11585.
URL: https://svn.filezilla-project.org/svn/FileZilla3/trunk
Revision: 11585
Last Changed Date: 2026-10-08 08:49:54 -0400 (Thu, 08 Oct 2026)

==> autoreconf
libtoolize: putting auxiliary files in AC_CONFIG_AUX_DIR, '../../config'.
libtoolize: copying file '../../config/ltmain.sh'
libtoolize: putting macros in AC_CONFIG_MACRO_DIRS, '../../m4'.
libtoolize: copying file '../../m4/libtool.m4'
libtoolize: copying file '../../m4/ltoptions.m4'
libtoolize: copying file '../../m4/ltsugar.m4'
libtoolize: copying file '../../m4/ltversion.m4'
libtoolize: copying file '../../m4/lt~obsolete.m4'
configure.ac:13: installing '../../config/compile'
configure.ac:10: installing '../../config/config.guess'
configure.ac:10: installing '../../config/config.sub'
configure.ac:5: installing '../../config/install-sh'
configure.ac:5: installing '../../config/missing'
Makefile.am: installing '../../config/depcomp'
locales/Makefile.am:46: warning: '%'-style pattern rules are a GNU make extension
locales/Makefile.am:50: warning: '%'-style pattern rules are a GNU make extension
parallel-tests: installing 'config/test-driver'

==> configure --build=aarch64-w64-mingw32 --host=aarch64-w64-mingw32 --prefix=/home/mcw/prefix --with-pugixml=builtin --enable-shared --disable-static --with-wx-config=/clangarm64/bin/wx-config-3.2 --disable-autoupdatecheck
configure: loading site script /etc/config.site
checking for a BSD-compatible install... /usr/bin/install -c
checking whether sleep supports fractional seconds... yes
checking filesystem timestamp resolution... 0.01
checking whether build environment is sane... yes
checking for a race-free mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking xargs -n works... yes
checking whether UID '197609' is supported by ustar format... yes
checking whether GID '197121' is supported by ustar format... yes
checking how to create a ustar tar archive... gnutar
checking build system type... aarch64-w64-mingw32
checking host system type... aarch64-w64-mingw32
checking whether the C++ compiler works... yes
checking for C++ compiler default output file name... a.exe
checking for suffix of executables... .exe
checking whether we are cross compiling...

no
checking for suffix of object files... o
checking whether the compiler supports GNU C++... yes
checking whether clang++ accepts -g... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of clang++... gcc3
checking for aarch64-w64-mingw32-g++... no
checking for aarch64-w64-mingw32-objc++... no
checking for aarch64-w64-mingw32-objcxx... no
checking for aarch64-w64-mingw32-c++... aarch64-w64-mingw32-c++
checking whether the compiler supports GNU Objective C++... yes
checking whether aarch64-w64-mingw32-c++ accepts -g... yes
checking dependency style of aarch64-w64-mingw32-c++... gcc3
checking for aarch64-w64-mingw32-gcc... clang
checking whether the compiler supports GNU C... yes
checking whether clang accepts -g... yes
checking for clang option to enable C23 features... -std=gnu23
checking whether clang -std=gnu23 understands -c and -o together... yes
checking dependency style of clang -std=gnu23... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by clang -std=gnu23... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /clangarm64/bin/nm -B
checking the name lister (/clangarm64/bin/nm -B) interface... BSD nm
checking whether ln -s works... no, using cp -pR
checking the maximum length of command line arguments... 8192
checking how to convert aarch64-w64-mingw32 file names to aarch64-w64-mingw32 format... func_convert_file_msys_to_w32
checking how to convert aarch64-w64-mingw32 file names to toolchain format... func_convert_file_msys_to_w32
checking whether cygpath is installed... yes
checking for C:/msys64/clangarm64/bin/ld option to reload object files... -r
checking for file... file
checking for aarch64-w64-mingw32-objdump... no
checking for objdump... objdump
checking how to recognize dependent libraries... file_magic ^x86 archive import|^x86 DLL
checking for aarch64-w64-mingw32-dlltool... no
checking for dlltool... dlltool
checking how to associate runtime and link libraries... func_cygming_dll_for_implib
checking for aarch64-w64-mingw32-ranlib... no
checking for ranlib... ranlib
checking for aarch64-w64-mingw32-ar... no
checking for ar... ar
checking for archiver @FILE support... @
checking for aarch64-w64-mingw32-strip... no
checking for strip... strip
checking command to parse /clangarm64/bin/nm -B output from clang -std=gnu23 object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for aarch64-w64-mingw32-mt... no
checking for mt... no
checking if : is a manifest tool... no
checking for stdio.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for strings.h... yes
checking for sys/stat.h... yes
checking for sys/types.h... yes
checking for unistd.h... yes
checking for dlfcn.h... no
checking for aarch64-w64-mingw32-g++... (cached) aarch64-w64-mingw32-c++
checking for aarch64-w64-mingw32-gnustep-config... no
checking for gnustep-config... no
checking which variant of shared library versioning to provide... (default) aix
checking for objdir... .libs
checking if clang -std=gnu23 supports -fno-rtti -fno-exceptions... yes
checking for clang -std=gnu23 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang -std=gnu23 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang -std=gnu23 static flag -static works... yes
checking if clang -std=gnu23 supports -c -o file.o... yes
checking if clang -std=gnu23 supports -c -o file.o... (cached) yes
checking whether the clang -std=gnu23 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries...

yes
checking whether -lc should be explicitly linked in... yes
checking dynamic linker characteristics...

Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... no
checking how to run the C++ preprocessor... clang++ -E
checking for ld used by clang++... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking whether the clang++ linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking for clang++ option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang++ PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang++ static flag -static works... yes
checking if clang++ supports -c -o file.o... yes
checking if clang++ supports -c -o file.o... (cached) yes
checking whether the clang++ linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking dynamic linker characteristics... Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking for Objective C++ compilation... no
checking if aarch64-w64-mingw32-c++ supports -fno-rtti -fno-exceptions... (cached) yes
checking for aarch64-w64-mingw32-c++ option to produce PIC... -DDLL_EXPORT
checking if aarch64-w64-mingw32-c++ PIC flag -DDLL_EXPORT works... yes
checking if aarch64-w64-mingw32-c++ static flag -static works... yes
checking if aarch64-w64-mingw32-c++ supports -c -o file.o... yes
checking if aarch64-w64-mingw32-c++ supports -c -o file.o... (cached) yes
checking whether the aarch64-w64-mingw32-c++ linker (C:/msys64/clangarm64/bin/ld) supports shared libraries...

yes
checking whether -lc should be explicitly linked in... yes
checking how to hardcode library paths into programs... immediate
checking whether C compiler accepts -Werror=partial-availability... yes
checking whether the linker accepts -Wl,-no_weak_imports... no
checking whether clang++ supports C++17 features with -std=c++17... yes
checking for whether we need -stdlib=libc++... no
checking whether std::map has emplace... yes
checking whether std::chrono::steady_clock is steady... yes
checking for thread_local... yes
checking whether std::atomic can be used without link library... yes
checking for whether we need to use Boost Regex due GCC bug 86164... no


configure: Running sub-configure for shell extension
configure: loading site script /etc/config.site
checking for a BSD-compatible install... /usr/bin/install -c
checking whether sleep supports fractional seconds... yes
checking filesystem timestamp resolution... 0.01
checking whether build environment is sane... yes
checking for i686-w64-mingw32-strip... no
checking for strip... strip
checking for a race-free mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking xargs -n works... yes
checking whether UID '197609' is supported by ustar format... yes
checking whether GID '197121' is supported by ustar format... yes
checking how to create a ustar tar archive... gnutar
checking build system type... aarch64-w64-mingw32
checking host system type... i686-w64-mingw32
checking for i686-w64-mingw32-gcc... clang -std=gnu23
checking whether the C compiler works... yes
checking for C compiler default output file name... a.exe
checking for suffix of executables... .exe
checking whether we are cross compiling...

no
checking for suffix of object files... o
checking whether the compiler supports GNU C... yes
checking whether clang -std=gnu23 accepts -g... yes
checking for clang -std=gnu23 option to enable C23 features... none needed
checking whether clang -std=gnu23 understands -c and -o together... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of clang -std=gnu23... gcc3
checking whether the compiler supports GNU C++... yes
checking whether clang++ -std=c++17 accepts -g... yes
checking dependency style of clang++ -std=c++17... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by clang -std=gnu23... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... no
checking for i686-w64-mingw32-dumpbin... no
checking for i686-w64-mingw32-link... no
checking for dumpbin... no
checking for link... link -dump
checking the name lister (nm) interface... BSD nm
checking whether ln -s works... no, using cp -pR
checking the maximum length of command line arguments... 8192
checking how to convert aarch64-w64-mingw32 file names to i686-w64-mingw32 format... func_convert_file_msys_to_w32
checking how to convert aarch64-w64-mingw32 file names to toolchain format... func_convert_file_msys_to_w32
checking whether cygpath is installed... yes
checking for C:/msys64/clangarm64/bin/ld option to reload object files... -r
checking for file... file
checking for i686-w64-mingw32-objdump... no
checking for objdump... objdump
checking how to recognize dependent libraries... file_magic ^x86 archive import|^x86 DLL
checking for i686-w64-mingw32-dlltool... no
checking for dlltool... dlltool
checking how to associate runtime and link libraries... func_cygming_dll_for_implib
checking for i686-w64-mingw32-ranlib... no
checking for ranlib... ranlib
checking for i686-w64-mingw32-ar... no
checking for ar... ar
checking for archiver @FILE support... @
checking for i686-w64-mingw32-strip... strip
checking command to parse nm output from clang -std=gnu23 object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for i686-w64-mingw32-mt... no
checking for mt... no
checking if : is a manifest tool... no
checking for stdio.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for strings.h... yes
checking for sys/stat.h... yes
checking for sys/types.h... yes
checking for unistd.h... yes
checking for dlfcn.h... no
checking which variant of shared library versioning to provide... (default) aix
checking for objdir... .libs
checking if clang -std=gnu23 supports -fno-rtti -fno-exceptions... yes
checking for clang -std=gnu23 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang -std=gnu23 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang -std=gnu23 static flag -static works... yes
checking if clang -std=gnu23 supports -c -o file.o... yes
checking if clang -std=gnu23 supports -c -o file.o... (cached) yes
checking whether the clang -std=gnu23 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries...

yes
checking whether -lc should be explicitly linked in... yes
checking dynamic linker characteristics...

Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking how to run the C++ preprocessor... clang++ -std=c++17 -E
checking for ld used by clang++ -std=c++17... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking whether the clang++ -std=c++17 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking for clang++ -std=c++17 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang++ -std=c++17 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang++ -std=c++17 static flag -static works... yes
checking if clang++ -std=c++17 supports -c -o file.o... yes
checking if clang++ -std=c++17 supports -c -o file.o... (cached) yes
checking whether the clang++ -std=c++17 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking dynamic linker characteristics... Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether the compiler actually targets MinGW... yes
checking whether clang++ -std=c++17 supports C++17 features with -std=c++17... yes
checking for whether we need -stdlib=libc++... no
checking for shlobj.h... yes
checking whether to use windres... yes
checking for i686-w64-mingw32-windres... no
checking for windres... windres
checking whether MinGW headers declare ICopyHookW... yes
checking whether the linker accepts -Wl,--dynamicbase... yes
checking whether the linker accepts -Wl,--nxcompat... yes
checking whether the linker accepts -Wl,--major-subsystem-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-subsystem-version -Wl,1... yes
checking whether the linker accepts -Wl,--major-os-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-os-version -Wl,1... yes
checking whether the linker accepts -Wl,--large-address-aware... yes
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands
configure: loading site script /etc/config.site
checking for a BSD-compatible install... /usr/bin/install -c
checking whether sleep supports fractional seconds... yes
checking filesystem timestamp resolution... 0.01
checking whether build environment is sane... yes
checking for x86_64-w64-mingw32-strip... no
checking for strip... strip
checking for a race-free mkdir -p... /usr/bin/mkdir -p
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking xargs -n works... yes
checking whether UID '197609' is supported by ustar format... yes
checking whether GID '197121' is supported by ustar format... yes
checking how to create a ustar tar archive... gnutar
checking build system type... aarch64-w64-mingw32
checking host system type... x86_64-w64-mingw32
checking for x86_64-w64-mingw32-gcc... clang -std=gnu23
checking whether the C compiler works... yes
checking for C compiler default output file name... a.exe
checking for suffix of executables... .exe
checking whether we are cross compiling...

no
checking for suffix of object files... o
checking whether the compiler supports GNU C... yes
checking whether clang -std=gnu23 accepts -g... yes
checking for clang -std=gnu23 option to enable C23 features... none needed
checking whether clang -std=gnu23 understands -c and -o together... yes
checking whether make supports the include directive... yes (GNU style)
checking dependency style of clang -std=gnu23... gcc3
checking whether the compiler supports GNU C++... yes
checking whether clang++ -std=c++17 accepts -g... yes
checking dependency style of clang++ -std=c++17... gcc3
checking how to print strings... printf
checking for a sed that does not truncate output... /usr/bin/sed
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking for fgrep... /usr/bin/grep -F
checking for ld used by clang -std=gnu23... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... no
checking for x86_64-w64-mingw32-dumpbin... no
checking for x86_64-w64-mingw32-link... no
checking for dumpbin... no
checking for link... link -dump
checking the name lister (nm) interface... BSD nm
checking whether ln -s works... no, using cp -pR
checking the maximum length of command line arguments... 8192
checking how to convert aarch64-w64-mingw32 file names to x86_64-w64-mingw32 format... func_convert_file_msys_to_w32
checking how to convert aarch64-w64-mingw32 file names to toolchain format... func_convert_file_msys_to_w32
checking whether cygpath is installed... yes
checking for C:/msys64/clangarm64/bin/ld option to reload object files... -r
checking for file... file
checking for x86_64-w64-mingw32-objdump... no
checking for objdump... objdump
checking how to recognize dependent libraries... file_magic ^x86 archive import|^x86 DLL
checking for x86_64-w64-mingw32-dlltool... no
checking for dlltool... dlltool
checking how to associate runtime and link libraries... func_cygming_dll_for_implib
checking for x86_64-w64-mingw32-ranlib... no
checking for ranlib... ranlib
checking for x86_64-w64-mingw32-ar... no
checking for ar... ar
checking for archiver @FILE support... @
checking for x86_64-w64-mingw32-strip... strip
checking command to parse nm output from clang -std=gnu23 object... ok
checking for sysroot... no
checking for a working dd... /usr/bin/dd
checking how to truncate binary pipes... /usr/bin/dd bs=4096 count=1
checking for x86_64-w64-mingw32-mt... no
checking for mt... no
checking if : is a manifest tool... no
checking for stdio.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for strings.h... yes
checking for sys/stat.h... yes
checking for sys/types.h... yes
checking for unistd.h... yes
checking for dlfcn.h... no
checking which variant of shared library versioning to provide... (default) aix
checking for objdir... .libs
checking if clang -std=gnu23 supports -fno-rtti -fno-exceptions... yes
checking for clang -std=gnu23 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang -std=gnu23 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang -std=gnu23 static flag -static works... yes
checking if clang -std=gnu23 supports -c -o file.o... yes
checking if clang -std=gnu23 supports -c -o file.o... (cached) yes
checking whether the clang -std=gnu23 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries...

yes
checking whether -lc should be explicitly linked in... yes
checking dynamic linker characteristics...

Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking how to run the C++ preprocessor... clang++ -std=c++17 -E
checking for ld used by clang++ -std=c++17... C:/msys64/clangarm64/bin/ld
checking if the linker (C:/msys64/clangarm64/bin/ld) is GNU ld... yes
checking whether the clang++ -std=c++17 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking for clang++ -std=c++17 option to produce PIC... -DDLL_EXPORT -DPIC
checking if clang++ -std=c++17 PIC flag -DDLL_EXPORT -DPIC works... yes
checking if clang++ -std=c++17 static flag -static works... yes
checking if clang++ -std=c++17 supports -c -o file.o... yes
checking if clang++ -std=c++17 supports -c -o file.o... (cached) yes
checking whether the clang++ -std=c++17 linker (C:/msys64/clangarm64/bin/ld) supports shared libraries... yes
checking dynamic linker characteristics... Win32 ld.exe
checking how to hardcode library paths into programs... immediate
checking whether the compiler actually targets MinGW... yes
checking whether clang++ -std=c++17 supports C++17 features with -std=c++17... yes
checking for whether we need -stdlib=libc++... no
checking for shlobj.h... yes
checking whether to use windres... yes
checking for x86_64-w64-mingw32-windres... no
checking for windres... windres
checking whether MinGW headers declare ICopyHookW... yes
checking whether the linker accepts -Wl,--dynamicbase... yes
checking whether the linker accepts -Wl,--nxcompat... yes
checking whether the linker accepts -Wl,--major-subsystem-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-subsystem-version -Wl,1... yes
checking whether the linker accepts -Wl,--major-os-version -Wl,6... yes
checking whether the linker accepts -Wl,--minor-os-version -Wl,1... yes
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating Makefile
config.status: creating config.h
config.status: executing depfiles commands
config.status: executing libtool commands
checking for aarch64-w64-mingw32-pkg-config... /clangarm64/bin/aarch64-w64-mingw32-pkg-config
checking pkg-config is at least version 0.9.0...

yes
checking for libfilezilla >= 0.57.0...



yes
checking for libfzssh-client >= 1.4.0...



no


configure: error: libfzssh-client not found: Package 'libfzssh-client' not found. You can download it from https://fzssh.filezilla-project.org/

mcw@DESKTOP-JO12IN5 CLANGARM64 ~
$
