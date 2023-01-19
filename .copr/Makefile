srpm:
	dnf install -y rpmdevtools
	spectool -d '_topdir .' -g $(spec)
	sha256sum -c .metadata
	rpmbuild -D '_topdir .' -D "_sourcedir ." -D "_srcrpmdir $(outdir)" -bs $(spec)
