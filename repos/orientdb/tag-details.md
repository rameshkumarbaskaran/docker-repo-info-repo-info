<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `orientdb`

-	[`orientdb:2.0`](#orientdb20)
-	[`orientdb:2.0.18`](#orientdb2018)
-	[`orientdb:2.1`](#orientdb21)
-	[`orientdb:2.1.25`](#orientdb2125)
-	[`orientdb:2.2`](#orientdb22)
-	[`orientdb:2.2.37`](#orientdb2237)
-	[`orientdb:2.2.37-spatial`](#orientdb2237-spatial)
-	[`orientdb:3.0`](#orientdb30)
-	[`orientdb:3.0-tp3`](#orientdb30-tp3)
-	[`orientdb:3.0.42`](#orientdb3042)
-	[`orientdb:3.0.42-tp3`](#orientdb3042-tp3)
-	[`orientdb:3.1`](#orientdb31)
-	[`orientdb:3.1-tp3`](#orientdb31-tp3)
-	[`orientdb:3.1.18`](#orientdb3118)
-	[`orientdb:3.1.18-tp3`](#orientdb3118-tp3)
-	[`orientdb:3.2`](#orientdb32)
-	[`orientdb:3.2-tp3`](#orientdb32-tp3)
-	[`orientdb:3.2.8`](#orientdb328)
-	[`orientdb:3.2.8-tp3`](#orientdb328-tp3)
-	[`orientdb:latest`](#orientdblatest)

## `orientdb:2.0`

```console
$ docker pull orientdb@sha256:b086c4aba8eea0d321c949d4a33b55aefcbe8695a7a1d4d9a48746063646c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0` - linux; amd64

```console
$ docker pull orientdb@sha256:4ee1209b59076484d4f07fce0bb18169fa5a5778301ed5f4ac47baabae061032
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283562081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7265ba7d57efad993e4ab04358f7eaf29038b0424d2ffe560539a0fef3420e40`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:48:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 15:48:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 15:48:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 15:48:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 15:48:07 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 15:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:13:21 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_VERSION=2.0.18
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Tue, 12 Jul 2022 18:13:26 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:26 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:26 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:26 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:26 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:26 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:27 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28818711e1ed38df107014a20127b41491b224d7aed8aa7066b55552d9600d2`  
		Last Modified: Tue, 12 Jul 2022 02:55:23 GMT  
		Size: 54.6 MB (54579006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dec79474efa527dac51b382e80c81f8f9230637bbe5b08b169a099e32c01325`  
		Last Modified: Tue, 12 Jul 2022 15:58:45 GMT  
		Size: 5.4 MB (5420853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65b2dac03048f3c5f53fd83162a4c27140a138fd2e11f538242e3f40c4aaf9d`  
		Last Modified: Tue, 12 Jul 2022 16:00:55 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b37f12466861413be9af59da7fd80fd1c6308b4ab4eec692731369292f2bde`  
		Last Modified: Tue, 12 Jul 2022 16:01:05 GMT  
		Size: 105.9 MB (105943503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97ec57d5dd7c91c0ee518acc68108681a6f8157a930523467e0832740384cdb`  
		Last Modified: Tue, 12 Jul 2022 18:15:59 GMT  
		Size: 46.6 MB (46586575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.0.18`

```console
$ docker pull orientdb@sha256:b086c4aba8eea0d321c949d4a33b55aefcbe8695a7a1d4d9a48746063646c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.0.18` - linux; amd64

```console
$ docker pull orientdb@sha256:4ee1209b59076484d4f07fce0bb18169fa5a5778301ed5f4ac47baabae061032
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283562081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7265ba7d57efad993e4ab04358f7eaf29038b0424d2ffe560539a0fef3420e40`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:57 GMT
ADD file:3451708ab45bc1bcfc1ebb2075d3af16767477cbeb79334959e0d1ff02b0864b in / 
# Tue, 12 Jul 2022 01:19:58 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:48:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:48:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 15:48:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 15:48:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 15:48:07 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 15:48:07 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 15:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:13:21 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_VERSION=2.0.18
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_DOWNLOAD_MD5=9e7b7e7b6d95795b188adb4e5898a1b8
# Tue, 12 Jul 2022 18:13:21 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f562794536bbf8ae2145f96153e58b1e5d9211b3
# Tue, 12 Jul 2022 18:13:26 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:26 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:26 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:26 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:26 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:26 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:27 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:d836772a1c1f9c4b1f280fb2a98ace30a4c4c87370f89aa092b35dfd9556278a`  
		Last Modified: Tue, 12 Jul 2022 01:24:06 GMT  
		Size: 55.0 MB (54999406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9e63c657ad881997f5165c0826be395bfc064415876b9fbaae74bcb5dc721`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 5.2 MB (5156110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1989b6e74cfdda1591b9dd23be47c5caeb002b7a151379361ec0c3f0e6d0e52`  
		Last Modified: Tue, 12 Jul 2022 02:55:03 GMT  
		Size: 10.9 MB (10876416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28818711e1ed38df107014a20127b41491b224d7aed8aa7066b55552d9600d2`  
		Last Modified: Tue, 12 Jul 2022 02:55:23 GMT  
		Size: 54.6 MB (54579006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dec79474efa527dac51b382e80c81f8f9230637bbe5b08b169a099e32c01325`  
		Last Modified: Tue, 12 Jul 2022 15:58:45 GMT  
		Size: 5.4 MB (5420853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65b2dac03048f3c5f53fd83162a4c27140a138fd2e11f538242e3f40c4aaf9d`  
		Last Modified: Tue, 12 Jul 2022 16:00:55 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b37f12466861413be9af59da7fd80fd1c6308b4ab4eec692731369292f2bde`  
		Last Modified: Tue, 12 Jul 2022 16:01:05 GMT  
		Size: 105.9 MB (105943503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97ec57d5dd7c91c0ee518acc68108681a6f8157a930523467e0832740384cdb`  
		Last Modified: Tue, 12 Jul 2022 18:15:59 GMT  
		Size: 46.6 MB (46586575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1`

```console
$ docker pull orientdb@sha256:1ae4b20bd9e96f98d368b39c748901e26d8338fe425539e507496bd9b5823847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1` - linux; amd64

```console
$ docker pull orientdb@sha256:65f45560865ac202737c481e7362c1332029d1b8d4459da9a918a374b5a4904b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172358136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc6dd341930280ccea970c45da7c0ae199354efb4b129f1a5029d99e9496b1`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_VERSION=2.1.25
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Tue, 12 Jul 2022 18:13:12 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:13:16 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:17 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:17 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:17 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:17 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:17 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:17 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d138e149161b7456360dabced412928c52e721c9bad99a4e674f1cf900352f2`  
		Last Modified: Tue, 12 Jul 2022 18:15:43 GMT  
		Size: 2.1 MB (2105683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0883624781b9a1ec8cb1c5d766729d5ff4ce65707c7c88506773669f35464`  
		Last Modified: Tue, 12 Jul 2022 18:15:45 GMT  
		Size: 31.1 MB (31087978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.1.25`

```console
$ docker pull orientdb@sha256:1ae4b20bd9e96f98d368b39c748901e26d8338fe425539e507496bd9b5823847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.1.25` - linux; amd64

```console
$ docker pull orientdb@sha256:65f45560865ac202737c481e7362c1332029d1b8d4459da9a918a374b5a4904b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172358136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc6dd341930280ccea970c45da7c0ae199354efb4b129f1a5029d99e9496b1`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_VERSION=2.1.25
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_DOWNLOAD_MD5=054da3fb7c56e7822b2af116966576ce
# Tue, 12 Jul 2022 18:13:07 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=b7b08242b40117ac8eb9a201f8704bde839dfcb8
# Tue, 12 Jul 2022 18:13:12 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:13:16 GMT
RUN mkdir /orientdb &&   wget  "https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/$ORIENTDB_VERSION/orientdb-community-$ORIENTDB_VERSION.tar.gz"   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1  && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:17 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:17 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:17 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:17 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:17 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:17 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d138e149161b7456360dabced412928c52e721c9bad99a4e674f1cf900352f2`  
		Last Modified: Tue, 12 Jul 2022 18:15:43 GMT  
		Size: 2.1 MB (2105683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0883624781b9a1ec8cb1c5d766729d5ff4ce65707c7c88506773669f35464`  
		Last Modified: Tue, 12 Jul 2022 18:15:45 GMT  
		Size: 31.1 MB (31087978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2`

```console
$ docker pull orientdb@sha256:4ee1bcdd28f1fa89f7e27d0d47606133249bdf0e2f708280049ff734fccff007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2` - linux; amd64

```console
$ docker pull orientdb@sha256:986d85863816a9214d9330701ef88147c2cf03543679f79005bc7f2b75424022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187744061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e026b2e97059deb999f857d8574697b40a38c3eadb87bd1cafd6c53a924d8ab`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_VERSION=2.2.37
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Tue, 12 Jul 2022 18:12:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:13:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:00 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:00 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:01 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818d1b314f18d7fbccaf206b8cc64406d8b9c5255275734dbbe2be4fbf2dfcea`  
		Last Modified: Tue, 12 Jul 2022 18:15:22 GMT  
		Size: 2.1 MB (2105683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b16410eb0f15db36a0a4044e6a46ec5e42a8d6b5a66677ea5ce56b5e43aa09`  
		Last Modified: Tue, 12 Jul 2022 18:15:24 GMT  
		Size: 46.5 MB (46473903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37`

```console
$ docker pull orientdb@sha256:4ee1bcdd28f1fa89f7e27d0d47606133249bdf0e2f708280049ff734fccff007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37` - linux; amd64

```console
$ docker pull orientdb@sha256:986d85863816a9214d9330701ef88147c2cf03543679f79005bc7f2b75424022
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187744061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e026b2e97059deb999f857d8574697b40a38c3eadb87bd1cafd6c53a924d8ab`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_VERSION=2.2.37
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Tue, 12 Jul 2022 18:12:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:13:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:00 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:00 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:01 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818d1b314f18d7fbccaf206b8cc64406d8b9c5255275734dbbe2be4fbf2dfcea`  
		Last Modified: Tue, 12 Jul 2022 18:15:22 GMT  
		Size: 2.1 MB (2105683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b16410eb0f15db36a0a4044e6a46ec5e42a8d6b5a66677ea5ce56b5e43aa09`  
		Last Modified: Tue, 12 Jul 2022 18:15:24 GMT  
		Size: 46.5 MB (46473903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:2.2.37-spatial`

```console
$ docker pull orientdb@sha256:e8ba007d884c109ab5acb228c143104d2cfe1f2f6b3ade675f25c58bd5d8d777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:2.2.37-spatial` - linux; amd64

```console
$ docker pull orientdb@sha256:54865d5751203d3169d248f0bb4dbf234ada3e25b54969b95f4d2b029d62b6db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188946651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2f6872f932a895459d7a8e6533005fcac6f1abd9b55abaca9b5edebb0f53fb`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_VERSION=2.2.37
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_MD5=cb80556ef3b0260d0ee5de88ea73fb9d
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=469c402dde029f265fe905de2c08b43960e81f07
# Tue, 12 Jul 2022 18:12:52 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.37/orientdb-community-2.2.37.tar.gz
# Tue, 12 Jul 2022 18:12:57 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:13:00 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:13:00 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:13:00 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:13:01 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:13:01 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:13:01 GMT
CMD ["server.sh"]
# Tue, 12 Jul 2022 18:13:04 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_MD5=9f64ab5e959f5d9ad9ea5195d6d621d2
# Tue, 12 Jul 2022 18:13:04 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_SHA1=1748c9779ea7a8cb8fc068fcabf960e1778e8a19
# Tue, 12 Jul 2022 18:13:04 GMT
ENV ORIENTDB_DOWNLOAD_SPATIAL_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-spatial/2.2.37/orientdb-spatial-2.2.37-dist.jar
# Tue, 12 Jul 2022 18:13:05 GMT
RUN wget $ORIENTDB_DOWNLOAD_SPATIAL_URL     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_MD5 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | md5sum -c -     && echo "$ORIENTDB_DOWNLOAD_SPATIAL_SHA1 *orientdb-spatial-$ORIENTDB_VERSION-dist.jar" | sha1sum -c -     && mv orientdb-spatial-*-dist.jar /orientdb/lib/
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818d1b314f18d7fbccaf206b8cc64406d8b9c5255275734dbbe2be4fbf2dfcea`  
		Last Modified: Tue, 12 Jul 2022 18:15:22 GMT  
		Size: 2.1 MB (2105683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b16410eb0f15db36a0a4044e6a46ec5e42a8d6b5a66677ea5ce56b5e43aa09`  
		Last Modified: Tue, 12 Jul 2022 18:15:24 GMT  
		Size: 46.5 MB (46473903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867520025bdf0d396a586fb6e33cff60e419481ca899ef9bbd903b1498da9d53`  
		Last Modified: Tue, 12 Jul 2022 18:15:35 GMT  
		Size: 1.2 MB (1202590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0`

```console
$ docker pull orientdb@sha256:61a568809cf496c7b473c63ec1eec6659cb0759928d7299d22a0513bb75e881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0` - linux; amd64

```console
$ docker pull orientdb@sha256:9a7a2d09df516b5bd48af57fd319b2c2ea8c65ae875ec2d770df7d4f9c372f29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178338699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98523d33a10bc1f6a27d0617a3ab59c8006ecd54df77a48c7f72adcfc85e5774`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_VERSION=3.0.42
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Tue, 12 Jul 2022 18:12:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:34 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:34 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:35 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:35 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:35 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:35 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:35 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7a2d5342d4d566d8957dc398333ca5dc749ad23dc290509104876e749840fd`  
		Last Modified: Tue, 12 Jul 2022 18:14:55 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9d07289a7ddf536abb1fb74ed8d0a316e391b7b938ea0d1e5ba363189302e`  
		Last Modified: Tue, 12 Jul 2022 18:14:57 GMT  
		Size: 37.1 MB (37068557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0-tp3`

```console
$ docker pull orientdb@sha256:4c7627d6779efaf6aa7aa4698ef49820767dfb68f636eb2c39ece53f148761ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:815adb9e3d0fe7ce709a03a451e0f0a80ee9dbfcf13d81d6617bef44a8f53d75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205359490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e068ab49b924eaa381e0224acc4008b6e5263540a23dbb795dafe0da82d0720`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_VERSION=3.0.42
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Tue, 12 Jul 2022 18:12:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:48 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:48 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:12:48 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:48 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:49 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:12:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce61ce160b38f17a8bfd159319c4b6c7847a9c2f39a66439955ff2b1c6e6a3`  
		Last Modified: Tue, 12 Jul 2022 18:15:07 GMT  
		Size: 2.1 MB (2105687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b836dc122fc09fc3f8937a447485d8ff217473454993667b99007d2eb4ed544`  
		Last Modified: Tue, 12 Jul 2022 18:15:11 GMT  
		Size: 64.1 MB (64087950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6cae3386fe908886fa0eb21a4626f99564997b96984aac891b373618168d27`  
		Last Modified: Tue, 12 Jul 2022 18:15:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42`

```console
$ docker pull orientdb@sha256:61a568809cf496c7b473c63ec1eec6659cb0759928d7299d22a0513bb75e881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42` - linux; amd64

```console
$ docker pull orientdb@sha256:9a7a2d09df516b5bd48af57fd319b2c2ea8c65ae875ec2d770df7d4f9c372f29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178338699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98523d33a10bc1f6a27d0617a3ab59c8006ecd54df77a48c7f72adcfc85e5774`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_VERSION=3.0.42
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=59ed522290668fb400e67503652bb813
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=fe6a510c72983b32a3ffd657be9ae62fab2b61f8
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.0.42/orientdb-community-3.0.42.tar.gz
# Tue, 12 Jul 2022 18:12:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:34 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:34 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:35 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:35 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:35 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:35 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:35 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7a2d5342d4d566d8957dc398333ca5dc749ad23dc290509104876e749840fd`  
		Last Modified: Tue, 12 Jul 2022 18:14:55 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc9d07289a7ddf536abb1fb74ed8d0a316e391b7b938ea0d1e5ba363189302e`  
		Last Modified: Tue, 12 Jul 2022 18:14:57 GMT  
		Size: 37.1 MB (37068557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.0.42-tp3`

```console
$ docker pull orientdb@sha256:4c7627d6779efaf6aa7aa4698ef49820767dfb68f636eb2c39ece53f148761ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.0.42-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:815adb9e3d0fe7ce709a03a451e0f0a80ee9dbfcf13d81d6617bef44a8f53d75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205359490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e068ab49b924eaa381e0224acc4008b6e5263540a23dbb795dafe0da82d0720`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:27 GMT
ENV ORIENTDB_VERSION=3.0.42
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_MD5=20104f313e82db3a2bd88b7501d596aa
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=1abc7a4979ca561d13edd01b1d18b3b869abace9
# Tue, 12 Jul 2022 18:12:38 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.0.42/orientdb-tp3-3.0.42.tar.gz
# Tue, 12 Jul 2022 18:12:43 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:48 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:48 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:12:48 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:48 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:49 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:49 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:12:49 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce61ce160b38f17a8bfd159319c4b6c7847a9c2f39a66439955ff2b1c6e6a3`  
		Last Modified: Tue, 12 Jul 2022 18:15:07 GMT  
		Size: 2.1 MB (2105687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b836dc122fc09fc3f8937a447485d8ff217473454993667b99007d2eb4ed544`  
		Last Modified: Tue, 12 Jul 2022 18:15:11 GMT  
		Size: 64.1 MB (64087950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6cae3386fe908886fa0eb21a4626f99564997b96984aac891b373618168d27`  
		Last Modified: Tue, 12 Jul 2022 18:15:07 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1`

```console
$ docker pull orientdb@sha256:6169e3ccdd20fe9f90de877e58633034389eaa48e6d900f248f8ea601a3195e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1` - linux; amd64

```console
$ docker pull orientdb@sha256:00e51c6e3b4acf7591ae436089c110c8378515c5e7514acbde16be9000505307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194308954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb6bbc818c966c0fc5f598b4feb1faddc31660d57ba66260cc954b3e5c009e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_VERSION=3.1.18
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b5039f79f08eeb5c60817699a650190a
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f3201cec2eb59572fd813168489fe6de0682c698
# Tue, 12 Jul 2022 18:12:02 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.18/orientdb-community-3.1.18.tar.gz
# Tue, 12 Jul 2022 18:12:06 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:10 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:10 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:10 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:10 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f1b4ab09261d5216fa0be9cf75cfe2a448990e94088407b569b84638a881e7`  
		Last Modified: Tue, 12 Jul 2022 18:14:27 GMT  
		Size: 2.1 MB (2105692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cbe6c5de7e417480126befed3bd6f11c794e912882b493c20a6f2717520182`  
		Last Modified: Tue, 12 Jul 2022 18:14:30 GMT  
		Size: 53.0 MB (53038787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1-tp3`

```console
$ docker pull orientdb@sha256:9fc10bbf82a78f7ea242526229665765cce091137f12e1fc9ee1a5a6e7455c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:32471b936549a90414d93c590e3afd7841c68d0bec4e3e8052f60adb767ecc73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217355669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6192f8c68075db14d00748c2cee8c614abba258f79f5cf8f8b3c285b46992e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_VERSION=3.1.18
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bebb872ef46dfce2a2430f27b4a7ffa9
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f5641f1dc198435cb22efeb340b02e35df4ad55c
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.18/orientdb-tp3-3.1.18.tar.gz
# Tue, 12 Jul 2022 18:12:18 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:24 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:12:24 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:24 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:12:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba431c7fcd004349aeb26e714d1555bae442cbe41d834cb624e03e2e9d76bff`  
		Last Modified: Tue, 12 Jul 2022 18:14:40 GMT  
		Size: 2.1 MB (2105647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647d925043699e1755749bc598c8b66cf7e9cf88c379e802e5b788b41c9bc5a9`  
		Last Modified: Tue, 12 Jul 2022 18:14:44 GMT  
		Size: 76.1 MB (76084169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a754e993639e06236d1bb63dd3535951f4abd3e5115c632caf58255fa12f93`  
		Last Modified: Tue, 12 Jul 2022 18:14:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.18`

```console
$ docker pull orientdb@sha256:6169e3ccdd20fe9f90de877e58633034389eaa48e6d900f248f8ea601a3195e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.18` - linux; amd64

```console
$ docker pull orientdb@sha256:00e51c6e3b4acf7591ae436089c110c8378515c5e7514acbde16be9000505307
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194308954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb6bbc818c966c0fc5f598b4feb1faddc31660d57ba66260cc954b3e5c009e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_VERSION=3.1.18
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_DOWNLOAD_MD5=b5039f79f08eeb5c60817699a650190a
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f3201cec2eb59572fd813168489fe6de0682c698
# Tue, 12 Jul 2022 18:12:02 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.18/orientdb-community-3.1.18.tar.gz
# Tue, 12 Jul 2022 18:12:06 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:10 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:10 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:10 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:10 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:10 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:10 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:11 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f1b4ab09261d5216fa0be9cf75cfe2a448990e94088407b569b84638a881e7`  
		Last Modified: Tue, 12 Jul 2022 18:14:27 GMT  
		Size: 2.1 MB (2105692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cbe6c5de7e417480126befed3bd6f11c794e912882b493c20a6f2717520182`  
		Last Modified: Tue, 12 Jul 2022 18:14:30 GMT  
		Size: 53.0 MB (53038787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.1.18-tp3`

```console
$ docker pull orientdb@sha256:9fc10bbf82a78f7ea242526229665765cce091137f12e1fc9ee1a5a6e7455c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.1.18-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:32471b936549a90414d93c590e3afd7841c68d0bec4e3e8052f60adb767ecc73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217355669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6192f8c68075db14d00748c2cee8c614abba258f79f5cf8f8b3c285b46992e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:12:01 GMT
ENV ORIENTDB_VERSION=3.1.18
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_MD5=bebb872ef46dfce2a2430f27b4a7ffa9
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f5641f1dc198435cb22efeb340b02e35df4ad55c
# Tue, 12 Jul 2022 18:12:13 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.1.18/orientdb-tp3-3.1.18.tar.gz
# Tue, 12 Jul 2022 18:12:18 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:12:23 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:12:24 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:12:24 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:12:24 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:12:24 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:12:24 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:12:24 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba431c7fcd004349aeb26e714d1555bae442cbe41d834cb624e03e2e9d76bff`  
		Last Modified: Tue, 12 Jul 2022 18:14:40 GMT  
		Size: 2.1 MB (2105647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647d925043699e1755749bc598c8b66cf7e9cf88c379e802e5b788b41c9bc5a9`  
		Last Modified: Tue, 12 Jul 2022 18:14:44 GMT  
		Size: 76.1 MB (76084169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a754e993639e06236d1bb63dd3535951f4abd3e5115c632caf58255fa12f93`  
		Last Modified: Tue, 12 Jul 2022 18:14:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2`

```console
$ docker pull orientdb@sha256:78fe0f955ad85a6760085139c3a2133200a57e8167d0697ada2bc02ae5e68a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2` - linux; amd64

```console
$ docker pull orientdb@sha256:aa057945b37644e54d57b3b672515f4c0731b04664ea5dc624af8835c252c493
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213810178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c720548f43bd472f80f25f122066534c8fb07b0fc585ae4bf846195793d7b1`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_MD5=42def2b96e5c4c9618baa3b4c001f502
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=0a402f53e910f74af83d25a17e5b968ee92dae46
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.8/orientdb-community-3.2.8.tar.gz
# Tue, 12 Jul 2022 18:11:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:11:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:11:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:11:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:11:43 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:11:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ca3056065fd40fdc2602e42d7e81808eb4acf27033e9fddf1efb9e718d364e`  
		Last Modified: Tue, 12 Jul 2022 18:13:54 GMT  
		Size: 2.1 MB (2105672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d98799006d354e6944fdd01d886d0c4707e98a037382272ac9699fdc9c2d5`  
		Last Modified: Tue, 12 Jul 2022 18:13:58 GMT  
		Size: 72.5 MB (72540031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2-tp3`

```console
$ docker pull orientdb@sha256:6913226e53da7ac495abe52819890ad771a2cd4187aecdda808036f25639672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:fafe4298e5c6db2e37f0bd399b1624bc39499453d501e3121ac535292cb4abec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238126532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8857c034da7757e2d3d09a98cca080df3ffe4f57cd329823b150d4d3a409e7e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0959836e3f0a33109a7e77eedb829ea0
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ee51b2f717bea2b34b2242e66ed3ea20602482e4
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.8/orientdb-tp3-3.2.8.tar.gz
# Tue, 12 Jul 2022 18:11:52 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:11:57 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:11:58 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:11:58 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:11:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:11:58 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:11:58 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:11:59 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:11:59 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:11:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f26807db7f220b56fe2726f94976918c777ce53e61a14f8376544a81aff877`  
		Last Modified: Tue, 12 Jul 2022 18:14:11 GMT  
		Size: 2.1 MB (2105680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8c6e6026d07463acb9a6006ab35fffa0b5c8ce896c0d8c7d0e1a4517250fb3`  
		Last Modified: Tue, 12 Jul 2022 18:14:16 GMT  
		Size: 96.9 MB (96854999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec090e73d11e1617f2143a682cb02ce97a141a8352093d2bd145fbeac4f5b69e`  
		Last Modified: Tue, 12 Jul 2022 18:14:11 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.8`

```console
$ docker pull orientdb@sha256:78fe0f955ad85a6760085139c3a2133200a57e8167d0697ada2bc02ae5e68a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.8` - linux; amd64

```console
$ docker pull orientdb@sha256:aa057945b37644e54d57b3b672515f4c0731b04664ea5dc624af8835c252c493
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213810178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c720548f43bd472f80f25f122066534c8fb07b0fc585ae4bf846195793d7b1`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_MD5=42def2b96e5c4c9618baa3b4c001f502
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=0a402f53e910f74af83d25a17e5b968ee92dae46
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.8/orientdb-community-3.2.8.tar.gz
# Tue, 12 Jul 2022 18:11:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:11:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:11:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:11:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:11:43 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:11:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ca3056065fd40fdc2602e42d7e81808eb4acf27033e9fddf1efb9e718d364e`  
		Last Modified: Tue, 12 Jul 2022 18:13:54 GMT  
		Size: 2.1 MB (2105672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d98799006d354e6944fdd01d886d0c4707e98a037382272ac9699fdc9c2d5`  
		Last Modified: Tue, 12 Jul 2022 18:13:58 GMT  
		Size: 72.5 MB (72540031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:3.2.8-tp3`

```console
$ docker pull orientdb@sha256:6913226e53da7ac495abe52819890ad771a2cd4187aecdda808036f25639672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:3.2.8-tp3` - linux; amd64

```console
$ docker pull orientdb@sha256:fafe4298e5c6db2e37f0bd399b1624bc39499453d501e3121ac535292cb4abec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238126532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8857c034da7757e2d3d09a98cca080df3ffe4f57cd329823b150d4d3a409e7e`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0959836e3f0a33109a7e77eedb829ea0
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ee51b2f717bea2b34b2242e66ed3ea20602482e4
# Tue, 12 Jul 2022 18:11:47 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-tp3/3.2.8/orientdb-tp3-3.2.8.tar.gz
# Tue, 12 Jul 2022 18:11:52 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:11:57 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-tp3-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-tp3-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-tp3-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:11:58 GMT
ADD file:5bcd10827429355383b443914a6e6c163692cb388c7594e6e8d3d4625653a011 in /orientdb/config 
# Tue, 12 Jul 2022 18:11:58 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:11:58 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:11:58 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:11:58 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:11:59 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:11:59 GMT
EXPOSE 8182
# Tue, 12 Jul 2022 18:11:59 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f26807db7f220b56fe2726f94976918c777ce53e61a14f8376544a81aff877`  
		Last Modified: Tue, 12 Jul 2022 18:14:11 GMT  
		Size: 2.1 MB (2105680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8c6e6026d07463acb9a6006ab35fffa0b5c8ce896c0d8c7d0e1a4517250fb3`  
		Last Modified: Tue, 12 Jul 2022 18:14:16 GMT  
		Size: 96.9 MB (96854999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec090e73d11e1617f2143a682cb02ce97a141a8352093d2bd145fbeac4f5b69e`  
		Last Modified: Tue, 12 Jul 2022 18:14:11 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `orientdb:latest`

```console
$ docker pull orientdb@sha256:78fe0f955ad85a6760085139c3a2133200a57e8167d0697ada2bc02ae5e68a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:aa057945b37644e54d57b3b672515f4c0731b04664ea5dc624af8835c252c493
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213810178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c720548f43bd472f80f25f122066534c8fb07b0fc585ae4bf846195793d7b1`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Tue, 12 Jul 2022 18:11:33 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 12 Jul 2022 18:11:33 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_MD5=42def2b96e5c4c9618baa3b4c001f502
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=0a402f53e910f74af83d25a17e5b968ee92dae46
# Tue, 12 Jul 2022 18:11:34 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.8/orientdb-community-3.2.8.tar.gz
# Tue, 12 Jul 2022 18:11:39 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:11:43 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 12 Jul 2022 18:11:43 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:11:43 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 12 Jul 2022 18:11:43 GMT
WORKDIR /orientdb
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2424
# Tue, 12 Jul 2022 18:11:43 GMT
EXPOSE 2480
# Tue, 12 Jul 2022 18:11:43 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb6d406ee56d2ec0f242c91a97c204cfb6307fd3e547798c13ebeeebf197e3`  
		Last Modified: Tue, 12 Jul 2022 02:20:01 GMT  
		Size: 106.2 MB (106215380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ca3056065fd40fdc2602e42d7e81808eb4acf27033e9fddf1efb9e718d364e`  
		Last Modified: Tue, 12 Jul 2022 18:13:54 GMT  
		Size: 2.1 MB (2105672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d98799006d354e6944fdd01d886d0c4707e98a037382272ac9699fdc9c2d5`  
		Last Modified: Tue, 12 Jul 2022 18:13:58 GMT  
		Size: 72.5 MB (72540031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
