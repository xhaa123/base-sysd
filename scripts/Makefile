#
#  nutyx
#
#  Copyright (c) 2016 by NuTyX team (http://nutyx.org)
#
#  This program is free software; you can redistribute it and/or modify
#  it under the terms of the GNU General Public License as published by
#  the Free Software Foundation; either version 2 of the License, or
#  (at your option) any later version.
#
#  This program is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#  GNU General Public License for more details.
#
#  You should have received a copy of the GNU General Public License
#  along with this program; if not, write to the Free Software
#  Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307,
#  USA.
#

include ../Makefile.inc

all: install-nutyx setup-nutyx flushmem which mkinitramfs

%: %.in
	sed -e "s/#VERSION#/$(VERSION)/" $< > $@


.PHONY:	install clean distclean dist

install: all
	install -D -m0755 install-nutyx $(SBINDIR)/install-nutyx
	install -D -m0755 setup-nutyx $(SBINDIR)/setup-nutyx
	install -D -m0755 flushmem $(SBINDIR)/flushmem
	install -D -m0755 mkinitramfs $(SBINDIR)/mkinitramfs
	install -D -m0755 which $(BINDIR)/which

clean:
	rm -f install-nutyx
	rm -f setup-nutyx
	rm -f flushmem
	rm -f which
	rm -f mkinitramfs

distclean: clean

# End of file
