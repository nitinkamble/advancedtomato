# Copyright (C) 2000-2002, 2005-2006 MySQL AB
# 
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA

MYSQLDATAdir =          $(localstatedir)
MYSQLSHAREdir =         $(pkgdatadir)
MYSQLBASEdir=           $(prefix)
MYSQLLIBdir=            $(pkglibdir)
INCLUDES =              -I$(top_srcdir)/include -I$(top_builddir)/include \
			-I$(top_srcdir)/regex \
			-I$(top_srcdir)/sql \
                        -I$(srcdir)
WRAPLIBS=

LDADD =

DEFS =                  @DEFS@
pkglib_LIBRARIES =	libheap.a
noinst_PROGRAMS	=	hp_test1 hp_test2
noinst_LIBRARIES =	libheap.a
hp_test1_LDFLAGS = @NOINST_LDFLAGS@
hp_test1_LDADD =	libheap.a \
			$(top_builddir)/mysys/libmysys.a \
			$(top_builddir)/dbug/libdbug.a \
			$(top_builddir)/strings/libmystrings.a
hp_test2_LDFLAGS = @NOINST_LDFLAGS@
hp_test2_LDADD =	libheap.a \
			$(top_builddir)/mysys/libmysys.a \
			$(top_builddir)/dbug/libdbug.a \
			$(top_builddir)/strings/libmystrings.a
noinst_HEADERS =	heapdef.h ha_heap.h
libheap_a_SOURCES =	hp_open.c hp_extra.c hp_close.c hp_panic.c hp_info.c \
			hp_rrnd.c hp_scan.c hp_update.c hp_write.c hp_delete.c \
			hp_rsame.c hp_create.c hp_rename.c hp_rfirst.c \
			hp_rnext.c hp_rlast.c hp_rprev.c hp_clear.c \
			hp_rkey.c hp_block.c \
			ha_heap.cc \
			hp_hash.c _check.c _rectest.c hp_static.c


EXTRA_DIST =		CMakeLists.txt plug.in

# Don't update the files from bitkeeper
%::SCCS/s.%
