<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:8.0.3`](#swipl803)
-	[`swipl:8.1.12`](#swipl8112)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:8.0.3`

```console
$ docker pull swipl@sha256:9cbb1ae42a16607ca7a5ca0d05f5c80697b95b80b26b8dc54754585ae83cd0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:8.0.3` - linux; amd64

```console
$ docker pull swipl@sha256:82b9883c6ce05f5ef24a11e81adcf234c2614eb6bc57057da152433a0791efdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55560931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d7d9b6698d6f8399475a0dd0022c799c9755a32eac6f59ceeb2bb80d4d226e`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 17:55:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 31 Mar 2020 17:55:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:08:38 GMT
RUN set -eux;     SWIPL_VER=8.0.3;     SWIPL_CHECKSUM=cee59c0a477c8166d722703f6e52f962028f3ac43a5f41240ecb45dbdbe2d6ae;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 31 Mar 2020 18:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 18:08:39 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68d9dc7b6a81338a5f92e020a766e2a92508716cb4de9b3b11b85347ae5682`  
		Last Modified: Tue, 31 Mar 2020 18:08:54 GMT  
		Size: 26.2 MB (26243125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc6ce5d7da93b7c86d143f9d238203eead0633ad611f20f7c0d5de7e20b7122`  
		Last Modified: Tue, 31 Mar 2020 18:08:59 GMT  
		Size: 6.8 MB (6804432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:8.1.12`

```console
$ docker pull swipl@sha256:673881ca48019f4b6517e774f31e07bd14babf5b68751675a0ee2e0c7113ed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:8.1.12` - linux; amd64

```console
$ docker pull swipl@sha256:2d513c6a956b58493207e9d3a337d413f7f6fa98315c4dbb4bd46e7c8c3dbb43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55676053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130bd61edbebe87c4de080fa408ff9474579e87ee4d6f232d814c78879cddba`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 17:55:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 31 Mar 2020 17:55:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:02:15 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 31 Mar 2020 18:02:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 18:02:16 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68d9dc7b6a81338a5f92e020a766e2a92508716cb4de9b3b11b85347ae5682`  
		Last Modified: Tue, 31 Mar 2020 18:08:54 GMT  
		Size: 26.2 MB (26243125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4419dd519b3dc99eda5b4b16c836a35e420d967e0f7f3b625b41f5b73559d`  
		Last Modified: Tue, 31 Mar 2020 18:08:51 GMT  
		Size: 6.9 MB (6919554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.1.12` - linux; arm variant v7

```console
$ docker pull swipl@sha256:573b28b7baa866d9e7c40cdd320b95e467c38ff49c0bfd350e1e87edf7925360
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48128940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9facd478ff786d34d31cb8a11a3f8c2eeacf1672b5b1a43eed611fd2f4493e2`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:31:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 16 Apr 2020 04:31:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 04:39:41 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 16 Apr 2020 04:39:43 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 04:39:43 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c98703c39cced81578c9aa0b99383701700807d60c98ba74603bf3c14b5000c`  
		Last Modified: Thu, 16 Apr 2020 04:40:13 GMT  
		Size: 22.7 MB (22666474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1df3de2cdd8fa3e398873c70e42175bf962ff7eab75137ed6e837f1fbec3bb`  
		Last Modified: Thu, 16 Apr 2020 04:40:09 GMT  
		Size: 6.2 MB (6163920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.1.12` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6e2db36121e99907783aba92f6035eebf4d2b6e339345fa575e78fe1124ee563
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52143686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6237f8f363d3d7653b504adda94d3ffd913fb17db3268fbae954c679bbac006a`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:42:55 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 16 Apr 2020 05:43:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:53:42 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 16 Apr 2020 05:53:44 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 05:53:45 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67c80d85c1da95a08e6b000ab939ad070c371b0e4f47bad9ddc181637a6d950`  
		Last Modified: Thu, 16 Apr 2020 05:54:07 GMT  
		Size: 25.0 MB (25047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14d6cd97c99d769e2637ac641d7c9d48781e75b35e679a2993513ee802f225c`  
		Last Modified: Thu, 16 Apr 2020 05:54:02 GMT  
		Size: 6.7 MB (6726497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:latest`

```console
$ docker pull swipl@sha256:673881ca48019f4b6517e774f31e07bd14babf5b68751675a0ee2e0c7113ed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:2d513c6a956b58493207e9d3a337d413f7f6fa98315c4dbb4bd46e7c8c3dbb43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55676053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c130bd61edbebe87c4de080fa408ff9474579e87ee4d6f232d814c78879cddba`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 17:55:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 31 Mar 2020 17:55:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:02:15 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 31 Mar 2020 18:02:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 18:02:16 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68d9dc7b6a81338a5f92e020a766e2a92508716cb4de9b3b11b85347ae5682`  
		Last Modified: Tue, 31 Mar 2020 18:08:54 GMT  
		Size: 26.2 MB (26243125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4419dd519b3dc99eda5b4b16c836a35e420d967e0f7f3b625b41f5b73559d`  
		Last Modified: Tue, 31 Mar 2020 18:08:51 GMT  
		Size: 6.9 MB (6919554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:573b28b7baa866d9e7c40cdd320b95e467c38ff49c0bfd350e1e87edf7925360
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48128940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9facd478ff786d34d31cb8a11a3f8c2eeacf1672b5b1a43eed611fd2f4493e2`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 16 Apr 2020 01:05:08 GMT
ADD file:e37c4728c0c89ac126542ac35e7e493425c021bfac751079c9b266821a1b4e99 in / 
# Thu, 16 Apr 2020 01:05:10 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:31:06 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 16 Apr 2020 04:31:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 04:39:41 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 16 Apr 2020 04:39:43 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 04:39:43 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f78d9963dfddc4747d6200353b50f6093a6e37ca82e1612fa397d64ff13e7299`  
		Last Modified: Thu, 16 Apr 2020 01:12:33 GMT  
		Size: 19.3 MB (19298546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c98703c39cced81578c9aa0b99383701700807d60c98ba74603bf3c14b5000c`  
		Last Modified: Thu, 16 Apr 2020 04:40:13 GMT  
		Size: 22.7 MB (22666474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1df3de2cdd8fa3e398873c70e42175bf962ff7eab75137ed6e837f1fbec3bb`  
		Last Modified: Thu, 16 Apr 2020 04:40:09 GMT  
		Size: 6.2 MB (6163920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:6e2db36121e99907783aba92f6035eebf4d2b6e339345fa575e78fe1124ee563
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52143686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6237f8f363d3d7653b504adda94d3ffd913fb17db3268fbae954c679bbac006a`
-	Default Command: `["swipl"]`

```dockerfile
# Thu, 16 Apr 2020 02:45:19 GMT
ADD file:1588320d1c43714ec0353b7471f2ffd649045ca0f5f70dcb1eb064875fff9578 in / 
# Thu, 16 Apr 2020 02:45:21 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:42:55 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Thu, 16 Apr 2020 05:43:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:53:42 GMT
RUN set -eux;     SWIPL_VER=8.1.12;     SWIPL_CHECKSUM=1c8f62a2dd6b279972c77b8b817bd93bb7bc54b11f852868eff79e82be0655e9;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Thu, 16 Apr 2020 05:53:44 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 05:53:45 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:8978c87ff45d64d1663a585dcf1ed66d9e711c2e4048d83ef561da9514ef46e6`  
		Last Modified: Thu, 16 Apr 2020 02:51:32 GMT  
		Size: 20.4 MB (20370106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67c80d85c1da95a08e6b000ab939ad070c371b0e4f47bad9ddc181637a6d950`  
		Last Modified: Thu, 16 Apr 2020 05:54:07 GMT  
		Size: 25.0 MB (25047083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14d6cd97c99d769e2637ac641d7c9d48781e75b35e679a2993513ee802f225c`  
		Last Modified: Thu, 16 Apr 2020 05:54:02 GMT  
		Size: 6.7 MB (6726497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:stable`

```console
$ docker pull swipl@sha256:9cbb1ae42a16607ca7a5ca0d05f5c80697b95b80b26b8dc54754585ae83cd0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swipl:stable` - linux; amd64

```console
$ docker pull swipl@sha256:82b9883c6ce05f5ef24a11e81adcf234c2614eb6bc57057da152433a0791efdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55560931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d7d9b6698d6f8399475a0dd0022c799c9755a32eac6f59ceeb2bb80d4d226e`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 17:55:25 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Tue, 31 Mar 2020 17:55:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libarchive13     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     { [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || apt-get install -y --no-install-recommends librocksdb4.5; } &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:08:38 GMT
RUN set -eux;     SWIPL_VER=8.0.3;     SWIPL_CHECKSUM=cee59c0a477c8166d722703f6e52f962028f3ac43a5f41240ecb45dbdbe2d6ae;     BUILD_DEPS='make cmake gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev';     dpkgArch="$(dpkg --print-architecture)";     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || BUILD_DEPS="$BUILD_DEPS librocksdb-dev";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget http://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr           ..;     LANG=C.UTF8 make;     LANG=C.UTF8 make install;     rm -rf /tmp/src;     mkdir -p /usr/lib/swipl/pack;     cd /usr/lib/swipl/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git 816cb2e45a5fb53290a763a3306e430b72c40794;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git 93f29d8f298d73de5719b93516acc73e00610eed;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git befdfab843d71bdabbe9574348697a6fe5be4fc3;     apt-get purge -y --auto-remove $BUILD_DEPS
# Tue, 31 Mar 2020 18:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 18:08:39 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c68d9dc7b6a81338a5f92e020a766e2a92508716cb4de9b3b11b85347ae5682`  
		Last Modified: Tue, 31 Mar 2020 18:08:54 GMT  
		Size: 26.2 MB (26243125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc6ce5d7da93b7c86d143f9d238203eead0633ad611f20f7c0d5de7e20b7122`  
		Last Modified: Tue, 31 Mar 2020 18:08:59 GMT  
		Size: 6.8 MB (6804432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
