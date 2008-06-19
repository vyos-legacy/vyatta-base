opdir = $(datadir)
bin_SCRIPTS	 =

bin_SCRIPTS	+= scripts/full-upgrade
bin_SCRIPTS	+= scripts/save-package-report

VYATTA_CONFIG_VERSION_DIR=/opt/vyatta/etc/config-migrate/current

install-exec-hook:
	find share ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 |  cpio -0pd $(DESTDIR)/$(datadir)/..
	find etc ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 |  cpio -0pd $(DESTDIR)
	mkdir -p $(DESTDIR)/usr/bin
	(cd $(DESTDIR)/usr/bin;ln -s ../../opt/vyatta/bin/full-upgrade .)
