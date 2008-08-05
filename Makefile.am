opdir = $(datadir)
bin_SCRIPTS	 =

bin_SCRIPTS	+= scripts/full-upgrade
bin_SCRIPTS	+= scripts/_full-upgrade
bin_SCRIPTS	+= scripts/save-package-report
bin_SCRIPTS	+= scripts/xes
bin_SCRIPTS	+= scripts/check-upgrade
bin_SCRIPTS	+= scripts/download-only
bin_SCRIPTS	+= scripts/install-only
bin_SCRIPTS	+= scripts/remove-packages
bin_SCRIPTS	+= scripts/_remove-packages
bin_SCRIPTS	+= scripts/dont-remove-packages


install-exec-hook:
	find share ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 |  cpio -0pd $(DESTDIR)/$(datadir)/..
	find etc ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 |  cpio -0pd $(DESTDIR)
	mkdir -p $(DESTDIR)/usr/bin
	(cd $(DESTDIR)/usr/bin;ln -s ../../opt/vyatta/bin/full-upgrade .)
