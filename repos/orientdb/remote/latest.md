## `orientdb:latest`

```console
$ docker pull orientdb@sha256:04985b5a8f930c6240c212a7a4b532f0b465aeece3407a1bd2f143e51c2c41ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:c1d88663ec47c390cecf0c3dbb607d60b949a2519626599f6831607534a65588
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211529827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47088d5d4e002d260cb9634601b46681df0c589fdb9002fb85a26cac1106858`
-	Default Command: `["server.sh"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:40 GMT
ADD file:5e8343ab9a73edc27c2889634896e792ab289b85c206de0fc31183fdc0a32ac7 in / 
# Tue, 17 Aug 2021 01:23:41 GMT
CMD ["bash"]
# Thu, 26 Aug 2021 00:33:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 00:38:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 26 Aug 2021 00:38:13 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 26 Aug 2021 00:38:13 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 00:38:13 GMT
ENV LANG=C.UTF-8
# Thu, 26 Aug 2021 00:38:13 GMT
ENV JAVA_VERSION=8u302
# Thu, 26 Aug 2021 00:38:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 26 Aug 2021 03:15:44 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 26 Aug 2021 03:15:44 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 26 Aug 2021 03:15:44 GMT
ENV ORIENTDB_VERSION=3.2.0
# Thu, 26 Aug 2021 03:15:45 GMT
ENV ORIENTDB_DOWNLOAD_MD5=7bff911bea6b02d2f1d9ddff5e4ba8ea
# Thu, 26 Aug 2021 03:15:45 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f424731e3d078de692fab97d6aa3b3e8395d7d01
# Thu, 26 Aug 2021 03:15:45 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.0/orientdb-community-3.2.0.tar.gz
# Thu, 26 Aug 2021 03:15:50 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 03:15:54 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 26 Aug 2021 03:15:54 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 03:15:54 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 26 Aug 2021 03:15:55 GMT
WORKDIR /orientdb
# Thu, 26 Aug 2021 03:15:55 GMT
EXPOSE 2424
# Thu, 26 Aug 2021 03:15:55 GMT
EXPOSE 2480
# Thu, 26 Aug 2021 03:15:55 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:99046ad9247f8a1cbd1048d9099d026191ad9cda63c08aadeb704b7000a51717`  
		Last Modified: Tue, 17 Aug 2021 01:29:35 GMT  
		Size: 31.4 MB (31361314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97c10298fea9915576e7ff72c6eca3d7c589aaafd6bc6481a5814c4271d2251`  
		Last Modified: Thu, 26 Aug 2021 00:43:26 GMT  
		Size: 1.6 MB (1581998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12127b9e959d71cc3433b3b0fadff2350394a628f731a4573086dab33730b236`  
		Last Modified: Thu, 26 Aug 2021 00:50:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c054f505cfb5b06d099ec513057f0f6b2754978050debfc4f3b7cc523d46c78`  
		Last Modified: Thu, 26 Aug 2021 00:50:23 GMT  
		Size: 106.3 MB (106261763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc19ea3261c6b0da0ff5fa0feb35c834d2efcad2eb86b6ef2390f27cf223c07`  
		Last Modified: Thu, 26 Aug 2021 03:18:24 GMT  
		Size: 2.1 MB (2102066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df524f097b8932a6a6d05dfbfeb79331cf54a059ee34ff468d70ed09c39418b5`  
		Last Modified: Thu, 26 Aug 2021 03:18:28 GMT  
		Size: 70.2 MB (70222472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
