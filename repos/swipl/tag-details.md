<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `swipl`

-	[`swipl:8.2.4`](#swipl824)
-	[`swipl:8.3.18`](#swipl8318)
-	[`swipl:latest`](#swipllatest)
-	[`swipl:stable`](#swiplstable)

## `swipl:8.2.4`

```console
$ docker pull swipl@sha256:1a83dd77830dca193e5b41afac05503fb05f09f51412355632b53ccf3f441113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:8.2.4` - linux; amd64

```console
$ docker pull swipl@sha256:1bda21db0fbcd1eaa963ffb4fc7b74fb335f3e52c6db8c788c79e5d1d518fa7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56283312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e144f3ba68c748012e7ff8d03064e2ef5533da676e19452a6cb0160389d44a`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:34:21 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 09:34:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:34:34 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 10:11:05 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 10:11:05 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14b1ce8a5d2cb646e4d8c93661fcbf253fcf2cd31e9a537674f98515c1fd23`  
		Last Modified: Sat, 27 Mar 2021 10:11:22 GMT  
		Size: 24.9 MB (24920300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb8dc3b4457d6a8210b1c1b5b6222f727990ac1a01216d06105fd63324d938f`  
		Last Modified: Sat, 27 Mar 2021 10:11:34 GMT  
		Size: 8.8 MB (8834610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.2.4` - linux; arm variant v7

```console
$ docker pull swipl@sha256:63fc5c0b0f71cac7ef63d25f35c40d02de1d974372bc6deef577ca9a972ff1d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1e7026940e4d0cd779015e44ab586bbefff0975325095e06a9b2a25fa4fc37`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:49:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 05:50:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:50:07 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:00:00 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 06:00:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290b7112bb87d99f5fecca2dc9edf7da9d6372a795f514c30df1175422ab848`  
		Last Modified: Sat, 27 Mar 2021 06:00:34 GMT  
		Size: 22.9 MB (22880971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080a8e8a3e779ad4bf8be545e70b3c7d8ef20819ead1c7e3baf79d3fc6c25645`  
		Last Modified: Sat, 27 Mar 2021 06:00:44 GMT  
		Size: 6.2 MB (6192823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.2.4` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:573a5bf2b3097b171592a6aec44375f5815d184946236b722805a2e5fe85f740
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52696678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf232d1b8b65e221e1b89f55d33fffe224d13ac3237b811c6d437a6712b7e03`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:42 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Mar 2021 08:47:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 08:47:32 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 09:55:00 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Wed, 31 Mar 2021 09:55:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e886c04bbfe8fe1b0f6b5b9ceb8b149b6bfea57210608333caec8229c21c2f8`  
		Last Modified: Wed, 31 Mar 2021 09:55:33 GMT  
		Size: 23.7 MB (23741969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547e7feb7e3e1f33c14d3e956af585b3ea1113409e4a729ff8a867f1b0dc904d`  
		Last Modified: Wed, 31 Mar 2021 09:55:44 GMT  
		Size: 8.6 MB (8565399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:8.3.18`

```console
$ docker pull swipl@sha256:e4bd9b2b7f00622ac0f7c1e0ef1d6cac5dfd54e7ecbf6095ce451c3a65b4be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:8.3.18` - linux; amd64

```console
$ docker pull swipl@sha256:4e38644bde9652f92a343138b16a00bd7a19484da24e691facc3663392e4686a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56391661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf74db4e0f376171c6183ea37780c42b133fe94949cf8b452e34aaa486246c7`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:34:21 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 09:34:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:34:34 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:50:40 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 09:50:40 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14b1ce8a5d2cb646e4d8c93661fcbf253fcf2cd31e9a537674f98515c1fd23`  
		Last Modified: Sat, 27 Mar 2021 10:11:22 GMT  
		Size: 24.9 MB (24920300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e67d299ad2ee56cd46a2ab3a67caaff4be6e3c5b09c0421533937e15cd81a`  
		Last Modified: Sat, 27 Mar 2021 10:11:19 GMT  
		Size: 8.9 MB (8942959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.3.18` - linux; arm variant v7

```console
$ docker pull swipl@sha256:7185fb785817a90623f09b55d21e7fcdfea0aaa2eb8d0b4f4fa12b8994b651aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48496020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a337c762daf2508089582f27fa4a8783862fe733e3381a5b196c2a4b87072e`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:49:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 05:50:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:50:07 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 05:54:54 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 05:54:57 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290b7112bb87d99f5fecca2dc9edf7da9d6372a795f514c30df1175422ab848`  
		Last Modified: Sat, 27 Mar 2021 06:00:34 GMT  
		Size: 22.9 MB (22880971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f809a2cc44c732a320cb5056303c2578578b71bbfc89ce1d506a26230af14`  
		Last Modified: Sat, 27 Mar 2021 06:00:30 GMT  
		Size: 6.3 MB (6299425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:8.3.18` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:d1dff3b3d4d46181e0d5626a75a588dc897f8c05d443a57fb226e83bdceab624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52805023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f6e7192e8cbbed516c0f6e5e203d62a8a041f531ede1f2c36fa8682e382a22`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:42 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Mar 2021 08:47:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 08:47:32 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 09:21:31 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Wed, 31 Mar 2021 09:21:33 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e886c04bbfe8fe1b0f6b5b9ceb8b149b6bfea57210608333caec8229c21c2f8`  
		Last Modified: Wed, 31 Mar 2021 09:55:33 GMT  
		Size: 23.7 MB (23741969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b20651b823bbb3ffa0a5bc7e307b0fcb68cda88e62e4eecef06242e121dacdd`  
		Last Modified: Wed, 31 Mar 2021 09:55:28 GMT  
		Size: 8.7 MB (8673744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:latest`

```console
$ docker pull swipl@sha256:e4bd9b2b7f00622ac0f7c1e0ef1d6cac5dfd54e7ecbf6095ce451c3a65b4be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:latest` - linux; amd64

```console
$ docker pull swipl@sha256:4e38644bde9652f92a343138b16a00bd7a19484da24e691facc3663392e4686a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56391661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf74db4e0f376171c6183ea37780c42b133fe94949cf8b452e34aaa486246c7`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:34:21 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 09:34:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:34:34 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 09:50:40 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 09:50:40 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14b1ce8a5d2cb646e4d8c93661fcbf253fcf2cd31e9a537674f98515c1fd23`  
		Last Modified: Sat, 27 Mar 2021 10:11:22 GMT  
		Size: 24.9 MB (24920300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e67d299ad2ee56cd46a2ab3a67caaff4be6e3c5b09c0421533937e15cd81a`  
		Last Modified: Sat, 27 Mar 2021 10:11:19 GMT  
		Size: 8.9 MB (8942959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm variant v7

```console
$ docker pull swipl@sha256:7185fb785817a90623f09b55d21e7fcdfea0aaa2eb8d0b4f4fa12b8994b651aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48496020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a337c762daf2508089582f27fa4a8783862fe733e3381a5b196c2a4b87072e`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:49:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 05:50:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:50:07 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 05:54:54 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 05:54:57 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290b7112bb87d99f5fecca2dc9edf7da9d6372a795f514c30df1175422ab848`  
		Last Modified: Sat, 27 Mar 2021 06:00:34 GMT  
		Size: 22.9 MB (22880971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f809a2cc44c732a320cb5056303c2578578b71bbfc89ce1d506a26230af14`  
		Last Modified: Sat, 27 Mar 2021 06:00:30 GMT  
		Size: 6.3 MB (6299425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:latest` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:d1dff3b3d4d46181e0d5626a75a588dc897f8c05d443a57fb226e83bdceab624
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52805023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f6e7192e8cbbed516c0f6e5e203d62a8a041f531ede1f2c36fa8682e382a22`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:42 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Mar 2021 08:47:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 08:47:32 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 09:21:31 GMT
RUN set -eux;     SWIPL_VER=8.3.18;     SWIPL_CHECKSUM=528349b353b36dde3d57d1de366a45e4fbbb89d4a96de907b9a0497e601be768;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/devel/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Wed, 31 Mar 2021 09:21:33 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e886c04bbfe8fe1b0f6b5b9ceb8b149b6bfea57210608333caec8229c21c2f8`  
		Last Modified: Wed, 31 Mar 2021 09:55:33 GMT  
		Size: 23.7 MB (23741969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b20651b823bbb3ffa0a5bc7e307b0fcb68cda88e62e4eecef06242e121dacdd`  
		Last Modified: Wed, 31 Mar 2021 09:55:28 GMT  
		Size: 8.7 MB (8673744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `swipl:stable`

```console
$ docker pull swipl@sha256:1a83dd77830dca193e5b41afac05503fb05f09f51412355632b53ccf3f441113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `swipl:stable` - linux; amd64

```console
$ docker pull swipl@sha256:1bda21db0fbcd1eaa963ffb4fc7b74fb335f3e52c6db8c788c79e5d1d518fa7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56283312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e144f3ba68c748012e7ff8d03064e2ef5533da676e19452a6cb0160389d44a`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:34:21 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 09:34:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:34:34 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 10:11:05 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 10:11:05 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14b1ce8a5d2cb646e4d8c93661fcbf253fcf2cd31e9a537674f98515c1fd23`  
		Last Modified: Sat, 27 Mar 2021 10:11:22 GMT  
		Size: 24.9 MB (24920300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb8dc3b4457d6a8210b1c1b5b6222f727990ac1a01216d06105fd63324d938f`  
		Last Modified: Sat, 27 Mar 2021 10:11:34 GMT  
		Size: 8.8 MB (8834610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:stable` - linux; arm variant v7

```console
$ docker pull swipl@sha256:63fc5c0b0f71cac7ef63d25f35c40d02de1d974372bc6deef577ca9a972ff1d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1e7026940e4d0cd779015e44ab586bbefff0975325095e06a9b2a25fa4fc37`
-	Default Command: `["swipl"]`

```dockerfile
# Fri, 26 Mar 2021 11:22:47 GMT
ADD file:b1a5bfd28534bad7b8c5855866772582382ed83f0066f18ee2a8641adfd9ba0c in / 
# Fri, 26 Mar 2021 11:22:49 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:49:32 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Sat, 27 Mar 2021 05:50:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:50:07 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:00:00 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Sat, 27 Mar 2021 06:00:02 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:f45436284e34e941cb0711d5901be5a1fd36d7b444c793225978d28caa2fe50c`  
		Last Modified: Fri, 26 Mar 2021 11:31:36 GMT  
		Size: 19.3 MB (19315624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290b7112bb87d99f5fecca2dc9edf7da9d6372a795f514c30df1175422ab848`  
		Last Modified: Sat, 27 Mar 2021 06:00:34 GMT  
		Size: 22.9 MB (22880971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080a8e8a3e779ad4bf8be545e70b3c7d8ef20819ead1c7e3baf79d3fc6c25645`  
		Last Modified: Sat, 27 Mar 2021 06:00:44 GMT  
		Size: 6.2 MB (6192823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swipl:stable` - linux; arm64 variant v8

```console
$ docker pull swipl@sha256:573a5bf2b3097b171592a6aec44375f5815d184946236b722805a2e5fe85f740
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52696678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf232d1b8b65e221e1b89f55d33fffe224d13ac3237b811c6d437a6712b7e03`
-	Default Command: `["swipl"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 08:46:42 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Michael Hendricks <michael@ndrix.org>
# Wed, 31 Mar 2021 08:47:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends     libtcmalloc-minimal4     libarchive13     libyaml-dev     libgmp10     libossp-uuid16     libssl1.1     ca-certificates     libdb5.3     libpcre3     libedit2     libgeos-c1v5     libspatialindex4v5     unixodbc     odbc-postgresql     tdsodbc     libmariadbclient18     libsqlite3-0     libserd-0-0     libraptor2-0 &&     dpkgArch="$(dpkg --print-architecture)" &&     rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 08:47:32 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 09:55:00 GMT
RUN set -eux;     SWIPL_VER=8.2.4;     SWIPL_CHECKSUM=f4bcc78437f9080ab089762e9e6afa7071df7f584c14999b92b9a90a4efbd7d8;     BUILD_DEPS='make cmake ninja-build gcc g++ wget git autoconf libarchive-dev libgmp-dev libossp-uuid-dev libpcre3-dev libreadline-dev libedit-dev libssl-dev zlib1g-dev libdb-dev unixodbc-dev libsqlite3-dev libserd-dev libraptor2-dev libgeos++-dev libspatialindex-dev libgoogle-perftools-dev';     dpkgArch="$(dpkg --print-architecture)";     apt-get update; apt-get install -y --no-install-recommends $BUILD_DEPS; rm -rf /var/lib/apt/lists/*;     mkdir /tmp/src;     cd /tmp/src;     wget -q https://www.swi-prolog.org/download/stable/src/swipl-$SWIPL_VER.tar.gz;     echo "$SWIPL_CHECKSUM  swipl-$SWIPL_VER.tar.gz" >> swipl-$SWIPL_VER.tar.gz-CHECKSUM;     sha256sum -c swipl-$SWIPL_VER.tar.gz-CHECKSUM;     tar -xzf swipl-$SWIPL_VER.tar.gz;     mkdir swipl-$SWIPL_VER/build;     cd swipl-$SWIPL_VER/build;     cmake -DCMAKE_BUILD_TYPE=Release           -DSWIPL_PACKAGES_X=OFF 	  -DSWIPL_PACKAGES_JAVA=OFF 	  -DCMAKE_INSTALL_PREFIX=/usr 	  -G Ninja           ..;     ../scripts/pgo-compile.sh;     ninja;     ninja install;     rm -rf /tmp/src;     mkdir -p /usr/share/swi-prolog/pack;     cd /usr/share/swi-prolog/pack;     install_addin () {         git clone "$2" "$1";         git -C "$1" checkout -q "$3";         if [ "$1" = 'prosqlite' ]; then rm -rf "$1/lib"; fi;         swipl -g "pack_rebuild($1)" -t halt;         find "$1" -mindepth 1 -maxdepth 1 ! -name lib ! -name prolog ! -name pack.pl -exec rm -rf {} +;         find "$1" -name .git -exec rm -rf {} +;         find "$1" -name '*.so' -exec strip {} +;     };     dpkgArch="$(dpkg --print-architecture)";     install_addin space https://github.com/JanWielemaker/space.git cd6fefa63317a7a6effb61a1c5aee634ebe2ca05;     install_addin prosqlite https://github.com/nicos-angelopoulos/prosqlite.git cfd2f68709f5fb61833c0e2f8e9c6546e542009c;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] || install_addin rocksdb https://github.com/JanWielemaker/rocksdb.git f110766ee97cfbc6fddd4c33b7238f00e76ecc18;     [ "$dpkgArch" = 'armhf' ] || [ "$dpkgArch" = 'armel' ] ||  install_addin hdt https://github.com/JanWielemaker/hdt.git e0a0eff87fc3318434cb493690c570e1255ed30e;     install_addin rserve_client https://github.com/JanWielemaker/rserve_client.git f8e83a4e1e4600baef4222dc4c2904a41a79a5ad;     apt-get purge -y --auto-remove $BUILD_DEPS
# Wed, 31 Mar 2021 09:55:01 GMT
CMD ["swipl"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e886c04bbfe8fe1b0f6b5b9ceb8b149b6bfea57210608333caec8229c21c2f8`  
		Last Modified: Wed, 31 Mar 2021 09:55:33 GMT  
		Size: 23.7 MB (23741969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:547e7feb7e3e1f33c14d3e956af585b3ea1113409e4a729ff8a867f1b0dc904d`  
		Last Modified: Wed, 31 Mar 2021 09:55:44 GMT  
		Size: 8.6 MB (8565399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
