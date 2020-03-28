## `zookeeper:latest`

```console
$ docker pull zookeeper@sha256:836ac084ec13494f9d1db0f415144d11c975c6f8b969e1aead3ce812889bb65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `zookeeper:latest` - linux; amd64

```console
$ docker pull zookeeper@sha256:6a3e704c8fda3944a6f45010688d964dbf6d12d03a3e2b92cbb2ef8a12eb7f05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90195216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329e4b7227e5bdc37476eaa6ba6205e0a34371bd002822dfb1ad05be141cf891`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["zkServer.sh","start-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:24 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:21:10 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jre_
# Wed, 26 Feb 2020 20:21:11 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:21:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Sat, 28 Mar 2020 00:32:49 GMT
ENV ZOO_CONF_DIR=/conf ZOO_DATA_DIR=/data ZOO_DATA_LOG_DIR=/datalog ZOO_LOG_DIR=/logs ZOO_TICK_TIME=2000 ZOO_INIT_LIMIT=5 ZOO_SYNC_LIMIT=2 ZOO_AUTOPURGE_PURGEINTERVAL=0 ZOO_AUTOPURGE_SNAPRETAINCOUNT=3 ZOO_MAX_CLIENT_CNXNS=60 ZOO_STANDALONE_ENABLED=true ZOO_ADMINSERVER_ENABLED=true
# Sat, 28 Mar 2020 00:32:50 GMT
RUN set -eux;     groupadd -r zookeeper --gid=1000;     useradd -r -g zookeeper --uid=1000 zookeeper;     mkdir -p "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR";     chown zookeeper:zookeeper "$ZOO_DATA_LOG_DIR" "$ZOO_DATA_DIR" "$ZOO_CONF_DIR" "$ZOO_LOG_DIR"
# Sat, 28 Mar 2020 00:32:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         dirmngr         gosu         gnupg         netcat         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Sat, 28 Mar 2020 00:32:56 GMT
ARG GPG_KEY=BBE7232D7991050B54C8EA0ADC08637CA615D22C
# Sat, 28 Mar 2020 00:32:57 GMT
ARG SHORT_DISTRO_NAME=zookeeper-3.6.0
# Sat, 28 Mar 2020 00:32:57 GMT
ARG DISTRO_NAME=apache-zookeeper-3.6.0-bin
# Sat, 28 Mar 2020 00:33:12 GMT
# ARGS: DISTRO_NAME=apache-zookeeper-3.6.0-bin GPG_KEY=BBE7232D7991050B54C8EA0ADC08637CA615D22C SHORT_DISTRO_NAME=zookeeper-3.6.0
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "zookeeper/$SHORT_DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -zxf "$DISTRO_NAME.tar.gz";     mv "$DISTRO_NAME/conf/"* "$ZOO_CONF_DIR";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R zookeeper:zookeeper "/$DISTRO_NAME"
# Sat, 28 Mar 2020 00:33:12 GMT
WORKDIR /apache-zookeeper-3.6.0-bin
# Sat, 28 Mar 2020 00:33:12 GMT
VOLUME [/data /datalog /logs]
# Sat, 28 Mar 2020 00:33:12 GMT
EXPOSE 2181 2888 3888 8080
# Sat, 28 Mar 2020 00:33:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-zookeeper-3.6.0-bin/bin ZOOCFGDIR=/conf
# Sat, 28 Mar 2020 00:33:13 GMT
COPY file:f0630bae0b70ba4c7943399d14326ac5df07510b2ff215bef5e47c2c60005d63 in / 
# Sat, 28 Mar 2020 00:33:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 28 Mar 2020 00:33:13 GMT
CMD ["zkServer.sh" "start-foreground"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa8e973e226cdc57cde0ef199d85ee1aa93b5f6a04abf68dc4952cdab931d5`  
		Last Modified: Wed, 26 Feb 2020 20:26:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c28bc4eb5532356cd06f142ed9cd6cee0811be74e992fdd2190fee8cbcf710`  
		Last Modified: Wed, 26 Feb 2020 20:27:41 GMT  
		Size: 42.2 MB (42172601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e507ab0703e6b08c102703b1acf9bfa13b68662c8414a788d392b71ba96c0`  
		Last Modified: Sat, 28 Mar 2020 00:33:21 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfb5d9f11b91fbfe91dae61e38ba35ba4ad4547add04ab94e5143a3a18aed31`  
		Last Modified: Sat, 28 Mar 2020 00:33:22 GMT  
		Size: 5.4 MB (5382321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f07583e09c249c5e75cba6ef9981b0df252cf682b842437c187479dbf39eea`  
		Last Modified: Sat, 28 Mar 2020 00:33:24 GMT  
		Size: 12.3 MB (12296612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980711aec96a6fbb89d5c51f13e7877bc1bfd7da943a119aa0bc122ec92c4279`  
		Last Modified: Sat, 28 Mar 2020 00:33:21 GMT  
		Size: 750.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
