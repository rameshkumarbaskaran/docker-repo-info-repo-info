## `clojure:openjdk-15-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:bae60652e677d581ef3d2ab601d8cad372e95645e5fed31b13413a4f47bc720f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:d7a47aa941394d9f7d88b13ec5634854c9b26d461908d59f5c548793a7e0557a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285192662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a837113ff63bf60dbb4303311bbca30d6d64f83237042f4e8cb434962e85180`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 21:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:00:03 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 21:00:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 15 May 2020 21:00:04 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:00:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 30 May 2020 00:33:47 GMT
ENV JAVA_VERSION=15-ea+25
# Sat, 30 May 2020 00:34:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-aarch64_bin.tar.gz; 			downloadSha256=32bd13e6fc92dba80d7eb504435a7bd9cbdb0aec2246476eb893b3ef5c5e8f66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-x64_bin.tar.gz; 			downloadSha256=6380fb115db35eea50760346cb4828d7e4054481f025acd84e3b39a3bc2d61eb; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 30 May 2020 00:34:04 GMT
CMD ["jshell"]
# Tue, 02 Jun 2020 00:26:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 02 Jun 2020 00:26:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 02 Jun 2020 00:26:59 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:27:04 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Tue, 02 Jun 2020 00:27:04 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 02 Jun 2020 00:27:04 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 02 Jun 2020 00:27:22 GMT
RUN boot
# Tue, 02 Jun 2020 00:27:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee19e84e8bd1140527176689c9c1a75f28c0462c0c714e549536452708cbfb64`  
		Last Modified: Fri, 15 May 2020 21:07:16 GMT  
		Size: 3.2 MB (3249166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e2ad6cc28f75db2e56f69cadbd0229b730550706f322b80ca8ad45ce205dd`  
		Last Modified: Fri, 15 May 2020 21:07:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3348212e55a455bf2cc7d9dc79c034be1e26a6d15e1baf8ef57fb22e4ef992a`  
		Last Modified: Sat, 30 May 2020 00:36:58 GMT  
		Size: 195.7 MB (195744850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7c939b653d1717d1e773d2cc6b28165f69e1f8430c8c4cbed8e2e3cd942f9`  
		Last Modified: Tue, 02 Jun 2020 00:33:52 GMT  
		Size: 279.6 KB (279636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3453235a7e9ef9897d292a88ee21adbd13ca72ee020a61f9712655872c633b01`  
		Last Modified: Tue, 02 Jun 2020 00:33:56 GMT  
		Size: 58.8 MB (58820043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
