## `clojure:openjdk-11-tools-deps-slim-buster`

```console
$ docker pull clojure@sha256:1a4f12da200026665f478ce35a85c9ae4efe6e8f16d733fd262637a774ad211e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-11-tools-deps-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:ac9bef9b25b1ecba5c248badb3f44493f9e99e153dd0e00b5160b9e85502e91b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271298885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87c14672d94f4dca20f8c8ed093a07218ad55de3c35686a5b66680c1bea7663`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:34:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:34:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 16:37:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 09 Jun 2020 16:37:19 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 16:37:20 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 16:37:20 GMT
ENV JAVA_VERSION=11.0.7
# Tue, 09 Jun 2020 16:37:20 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Tue, 09 Jun 2020 16:37:20 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Tue, 09 Jun 2020 16:37:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Tue, 09 Jun 2020 16:37:45 GMT
CMD ["jshell"]
# Wed, 10 Jun 2020 06:56:32 GMT
ENV CLOJURE_VERSION=1.10.1.536
# Wed, 10 Jun 2020 06:56:32 GMT
WORKDIR /tmp
# Wed, 10 Jun 2020 06:56:52 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "83b824091723afe8e0f4e958bf74a2f7cd4c4caddd34e31af6ef1a4323c45ff1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get remove -y --purge curl wget
# Wed, 10 Jun 2020 06:56:52 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65306eca6b8ea03d29cd8d10a31e9d7a6a1cf8766fe4ca3913e75e00fc47be79`  
		Last Modified: Tue, 09 Jun 2020 16:41:33 GMT  
		Size: 3.2 MB (3248452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbf88050b6e7cbe8b76b77196134f31015ef5cb69123ba6af35da6f5b101459`  
		Last Modified: Tue, 09 Jun 2020 16:44:15 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e07c1589b8c15dc7d4ff58aac0fc18ecd9d5861420dee368caa371e91cace3`  
		Last Modified: Tue, 09 Jun 2020 16:44:46 GMT  
		Size: 196.5 MB (196476202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1771b03af988f29c77464b1628a5ea27905e3725bd2db0461093779e1dbf9ada`  
		Last Modified: Wed, 10 Jun 2020 07:04:59 GMT  
		Size: 44.5 MB (44475756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-11-tools-deps-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5193d45bbca3374cf75a50450c6ff81a9aa5418eab866c16c2a97d1cd4e04dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267058755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f09cfcf6ecd7dde9fc958eddf1d51ac6e18a98dedfdc28277af944cf9c1dc`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:43:09 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 13:45:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 09 Jun 2020 13:45:02 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 13:45:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 09 Jun 2020 13:45:05 GMT
ENV JAVA_VERSION=11.0.7
# Tue, 09 Jun 2020 13:45:06 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Tue, 09 Jun 2020 13:45:07 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Tue, 09 Jun 2020 13:45:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Tue, 09 Jun 2020 13:45:45 GMT
CMD ["jshell"]
# Wed, 10 Jun 2020 03:43:38 GMT
ENV CLOJURE_VERSION=1.10.1.536
# Wed, 10 Jun 2020 03:43:39 GMT
WORKDIR /tmp
# Wed, 10 Jun 2020 03:44:18 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "83b824091723afe8e0f4e958bf74a2f7cd4c4caddd34e31af6ef1a4323c45ff1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get remove -y --purge curl wget
# Wed, 10 Jun 2020 03:44:19 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741745c97e3614499fd6b9013ef0b77c85309673e303a5c5bfa4a09bd38c41a`  
		Last Modified: Tue, 09 Jun 2020 13:48:30 GMT  
		Size: 3.1 MB (3101468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698598a9fb517b9b3237d62973e4ed79d76d111603db0cd65af06b065ef73d36`  
		Last Modified: Tue, 09 Jun 2020 13:49:56 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9291d98da59240745872118189421910a80d5cbf48b12236f352e61816fcac2`  
		Last Modified: Tue, 09 Jun 2020 13:50:30 GMT  
		Size: 194.1 MB (194127086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da0b7a00e6e4580defd1327786d69feb03638c58061998bfd551c4432942dc`  
		Last Modified: Wed, 10 Jun 2020 03:46:48 GMT  
		Size: 44.0 MB (43972288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
