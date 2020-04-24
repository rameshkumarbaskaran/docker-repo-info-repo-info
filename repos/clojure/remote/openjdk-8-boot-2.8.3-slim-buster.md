## `clojure:openjdk-8-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:a977fb3d2d14f5500c993e3ace18ef37253fad085870c4cdf066cbf32c007253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-8-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:7a88d8a9ec5c653c089fd9198f8447cb7a63ae7f545b8c555dea285c3be97c8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194167263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa14538d8d4f393309846ead75fc116ceae9b61e9ece1abfa7dac36a2924f39`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:59:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 04:04:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Apr 2020 04:04:24 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 04:04:26 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 23 Apr 2020 04:04:26 GMT
ENV JAVA_VERSION=8u252
# Thu, 23 Apr 2020 04:04:26 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jdk_
# Thu, 23 Apr 2020 04:04:27 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 23 Apr 2020 04:04:47 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Thu, 23 Apr 2020 22:24:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Apr 2020 22:24:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Apr 2020 22:24:44 GMT
WORKDIR /tmp
# Thu, 23 Apr 2020 22:24:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Thu, 23 Apr 2020 22:24:53 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Apr 2020 22:24:54 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Apr 2020 22:25:30 GMT
RUN boot
# Thu, 23 Apr 2020 22:25:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd01647a92dedec9093f4872d18b5a91e98a48731a7c9bc733d288be336017`  
		Last Modified: Thu, 23 Apr 2020 04:07:47 GMT  
		Size: 3.2 MB (3249064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb931af9b241b70d07321c65d1cb8a1416d548e86ca8e6933e2734adf039d68e`  
		Last Modified: Thu, 23 Apr 2020 04:12:48 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b8cbae8041edd4d8c351fce0041a1a5e42ff391f481d3686ae1cf98fb0418b`  
		Last Modified: Thu, 23 Apr 2020 04:13:00 GMT  
		Size: 104.7 MB (104718134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b846c55ab6fb7d4b1d2f9cb89fbe7fecead3ddf7debb1bf3d4ab4ec6adcc364`  
		Last Modified: Thu, 23 Apr 2020 22:34:46 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148bf6f4ad39ecdf076fdb98aa4edac004a3b558e7fdb00d27d8ccd917178634`  
		Last Modified: Thu, 23 Apr 2020 22:34:50 GMT  
		Size: 58.8 MB (58820331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
