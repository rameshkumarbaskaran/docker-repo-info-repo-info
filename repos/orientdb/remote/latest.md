## `orientdb:latest`

```console
$ docker pull orientdb@sha256:aabd4e6b676513c69bf6e4378622e0236ddc3226a8bba37e069952c0be3da9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:bfd8728d6a15f73e05c5449e0451ae82a14c14846fd862d90db131a0a6648e8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213822932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09484c88c7b923c4e1ce6f05c9de2e3358c110dcb7371ca29fbc90505574c7d7`
-	Default Command: `["server.sh"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:00:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:00:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:00:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:00:37 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:00:37 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:00:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Jun 2022 22:25:58 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Thu, 23 Jun 2022 22:25:58 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Tue, 28 Jun 2022 18:10:27 GMT
ENV ORIENTDB_VERSION=3.2.8
# Tue, 28 Jun 2022 18:10:27 GMT
ENV ORIENTDB_DOWNLOAD_MD5=42def2b96e5c4c9618baa3b4c001f502
# Tue, 28 Jun 2022 18:10:28 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=0a402f53e910f74af83d25a17e5b968ee92dae46
# Tue, 28 Jun 2022 18:10:28 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.8/orientdb-community-3.2.8.tar.gz
# Tue, 28 Jun 2022 18:10:32 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 18:10:36 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Tue, 28 Jun 2022 18:10:36 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 18:10:36 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Tue, 28 Jun 2022 18:10:37 GMT
WORKDIR /orientdb
# Tue, 28 Jun 2022 18:10:37 GMT
EXPOSE 2424
# Tue, 28 Jun 2022 18:10:37 GMT
EXPOSE 2480
# Tue, 28 Jun 2022 18:10:37 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4dc029a36926590a5070a9a58443942497e3b2d48cff116b8b15004d386a40`  
		Last Modified: Thu, 23 Jun 2022 05:07:14 GMT  
		Size: 1.6 MB (1582249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e04eeb91a4371c25329796317d1b09a60bacf789ea0952f690c5680fc3cf4`  
		Last Modified: Thu, 23 Jun 2022 05:20:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64f23aac47f8460fedec2cb2bb72974613568fb4d3cc50e94e19b38b15b2f53`  
		Last Modified: Thu, 23 Jun 2022 05:20:21 GMT  
		Size: 106.2 MB (106215317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcdbb908fc0561b6d3bd98152ff0bd94fc2dad1ac4bfff131c2985e8f0d9ea9`  
		Last Modified: Tue, 28 Jun 2022 18:11:30 GMT  
		Size: 2.1 MB (2105713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38148a869d2231084023051774877be433fbc2814f720c9c5e789dd967063dde`  
		Last Modified: Tue, 28 Jun 2022 18:11:35 GMT  
		Size: 72.5 MB (72540036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
