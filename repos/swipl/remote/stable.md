## `swipl:stable`

```console
$ docker pull swipl@sha256:13f37f321e738e5a31c68189548fbd751e5b3768b21db6797584c62127167892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:stable` - linux; amd64

```console
$ docker pull swipl@sha256:a39f25788bb069fc6cd1ba7c139b28106d0786fcfec59ec132bec8ef92def7a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55572428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c39a399dad03f81dd3440445a80e49bc9e23d7081f7033c2d8a12231b99474`
-	Default Command: `["swipl"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:32:15 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 01 Feb 2020 18:32:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:47:54 GMT
RUN set -eux;     SWIPL_VER=8.0.3;     SWIPL_CHECKSUM=cee59c0a477c8166d722703f6e52f962028f3ac43a5f41240ecb45dbdbe2d6ae;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 01 Feb 2020 18:47:55 GMT
ENV LANG=C.UTF-8
# Sat, 01 Feb 2020 18:47:55 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3c075ec43c0a754796f8237bb589e3a907b1feca2536f802e44d279bd8ccb4`  
		Last Modified: Sat, 01 Feb 2020 18:48:23 GMT  
		Size: 26.2 MB (26243087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218847d5deeccf5ce473c315fa1cbb39a10aa41d0257a89f4efc49eecb8e46b5`  
		Last Modified: Sat, 01 Feb 2020 18:48:28 GMT  
		Size: 6.8 MB (6804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
