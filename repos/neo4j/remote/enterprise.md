## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:792b065c6e2071cdc0dc9a5ed98b5a35c7f8990fed4e20089cf495673c4bc792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c6222e168047b5a3e9c30286452d8e3fb08c5a290a854861e42f6605546afc08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.5 MB (445549098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c95b1462f2a00b605e2a69ceaa5430fa9aa901e4d56f6ae493b5fba105019e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:49:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 11 May 2022 05:49:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 05:49:49 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:49:50 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:49:50 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 11 May 2022 05:50:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 11 May 2022 05:50:24 GMT
CMD ["jshell"]
# Tue, 17 May 2022 22:23:20 GMT
ENV NEO4J_SHA256=b0a0fa18f8285f5860ad79d51f6a343143d31e37c9637f457da53631704a114e NEO4J_TARBALL=neo4j-enterprise-4.4.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 17 May 2022 22:23:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
# Tue, 17 May 2022 22:23:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 17 May 2022 22:23:21 GMT
COPY multi:d7ab6ca18196127ce806534a7144f760972e56cfad82dbb0376dccb34ae89b5c in /startup/ 
# Tue, 17 May 2022 22:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 17 May 2022 22:23:44 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 22:23:44 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 May 2022 22:23:44 GMT
VOLUME [/data /logs]
# Tue, 17 May 2022 22:23:44 GMT
EXPOSE 7473 7474 7687
# Tue, 17 May 2022 22:23:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 May 2022 22:23:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf31789c5c1a5e3676cbd7a34472d61217c52c819552f5b116565c22cb6d2f1`  
		Last Modified: Wed, 11 May 2022 05:58:33 GMT  
		Size: 1.6 MB (1582150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8741521b2ba4d4d676c7a992cb54627c0eb9fdce1b4f68ad17da4f8b2abf103a`  
		Last Modified: Wed, 11 May 2022 06:04:24 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b079b63f250d1049457d0657541b735a1915d4c4a5aa6686d172c3821e3ebc9`  
		Last Modified: Wed, 11 May 2022 06:04:39 GMT  
		Size: 204.2 MB (204236989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc50d798e3a840c4f0caf44e498dc49e2d90f588015b6e1bcc2a335a637a1e9a`  
		Last Modified: Tue, 17 May 2022 22:32:11 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51663ad2cdb52f21eb9215f3a9403fef35131d8d07f1df5afb0b888de991b53`  
		Last Modified: Tue, 17 May 2022 22:32:11 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cda5e960c9a26cf798661b14b6efa480db05e2daec8afdf581f3b0826477ff`  
		Last Modified: Tue, 17 May 2022 22:32:21 GMT  
		Size: 208.3 MB (208338833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:170a7fd6ef5b590b08f4a45bc11fc8a5e8a9be92b7436aef44d5be427c701db7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441481891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cbd412571f739f26708067d4cb6092dad173d7a2b3a7c9ec93c0554821061c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:37:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:40:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 01:40:42 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 01:40:43 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:40:44 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 01:40:45 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 01:41:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 28 May 2022 01:41:16 GMT
CMD ["jshell"]
# Sat, 28 May 2022 19:45:47 GMT
ENV NEO4J_SHA256=b0a0fa18f8285f5860ad79d51f6a343143d31e37c9637f457da53631704a114e NEO4J_TARBALL=neo4j-enterprise-4.4.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 May 2022 19:45:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
# Sat, 28 May 2022 19:45:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 28 May 2022 19:45:50 GMT
COPY multi:d7ab6ca18196127ce806534a7144f760972e56cfad82dbb0376dccb34ae89b5c in /startup/ 
# Sat, 28 May 2022 19:46:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.7-unix.tar.gz
RUN apt update     && apt install -y curl wget gosu jq tini     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:46:03 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 19:46:04 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 May 2022 19:46:05 GMT
VOLUME [/data /logs]
# Sat, 28 May 2022 19:46:06 GMT
EXPOSE 7473 7474 7687
# Sat, 28 May 2022 19:46:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 May 2022 19:46:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c8727eedfb1755681add8fcb3c2c35d3b41f8231849edcec84588c6404f3b3`  
		Last Modified: Sat, 28 May 2022 01:54:41 GMT  
		Size: 1.4 MB (1361240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c4adca2661f00b25f7d41cc4798b8627a367bdb6d2726d9b3d8e8784eec2a`  
		Last Modified: Sat, 28 May 2022 02:00:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d9ea52c9b5091dc68752b4f90b1bf528f6304f15cf49c56adc17afa64cd35b`  
		Last Modified: Sat, 28 May 2022 02:00:31 GMT  
		Size: 202.1 MB (202051353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdf1899f5449c543b4dbb738093a1ef8daaddb740445562a82b4f09f5e157fd`  
		Last Modified: Sat, 28 May 2022 19:55:57 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e97080c1a7bb6d318fc0a6d13532c9d79b00fab424784b985f96959a282ae2`  
		Last Modified: Sat, 28 May 2022 19:55:57 GMT  
		Size: 7.5 KB (7544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84d09de7832f9ee3856287330657013eb2cd729a5aa8e672f4dca20bbcea24c`  
		Last Modified: Sat, 28 May 2022 19:56:10 GMT  
		Size: 208.0 MB (207991972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
