## `clojure:boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:709825b49a70753c0cb4c00db51e156aef79021f704fbd05b0ee31dd0f46132d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:4e86c5ddecec4fa8fb2bc42812ea191f0eea7f3ce84702ea6caf767d9acf250e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277072316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52796034878e550b89083d96aae0ac6bcee7274ad057f22b13f3197a0efe0aea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:27:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 17 Nov 2021 09:27:12 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:27:12 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:27:13 GMT
ENV JAVA_VERSION=17.0.1
# Wed, 17 Nov 2021 09:27:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 17 Nov 2021 09:27:36 GMT
CMD ["jshell"]
# Thu, 18 Nov 2021 13:01:19 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 18 Nov 2021 13:01:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 18 Nov 2021 13:01:19 GMT
WORKDIR /tmp
# Thu, 18 Nov 2021 13:01:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 18 Nov 2021 13:01:24 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 18 Nov 2021 13:01:25 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 18 Nov 2021 13:01:44 GMT
RUN boot
# Thu, 02 Dec 2021 02:33:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 02 Dec 2021 02:33:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 Dec 2021 02:33:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621243a0e6a3f0c137653e666271f422267f0e6648d870513269d843ef863a41`  
		Last Modified: Wed, 17 Nov 2021 09:41:55 GMT  
		Size: 3.3 MB (3269485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eb9614912c4fb9c758624f42469d313443f7da3404b5583a4b6c34673f2bf9`  
		Last Modified: Wed, 17 Nov 2021 09:45:25 GMT  
		Size: 187.5 MB (187548518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2d4a6b54fcbe144f7a8610dc3601d44e4f807930b3dd89eb06f626321e68c`  
		Last Modified: Thu, 18 Nov 2021 13:19:05 GMT  
		Size: 279.8 KB (279752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f00a7d34486cb9307925e9bb5bde15e5f171454357480a3dcd62700108aaf81`  
		Last Modified: Thu, 18 Nov 2021 13:19:08 GMT  
		Size: 58.8 MB (58820482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4623eb409291e0e6b39fd01a45ad5ab117ba4e4a35ef4fb20925fcc3ffa9e8`  
		Last Modified: Thu, 02 Dec 2021 02:39:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ca96c91f952dc385d0fd21f2d55bd57a143fc73d67ff100637d9d9828530cb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274072352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bec1633866f90f0ae98a07f8044030200cdc2c132bc703ef5e49afc490d8113`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:03:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:05:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 02 Dec 2021 11:05:49 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:05:50 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:05:51 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 02 Dec 2021 11:06:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:06:07 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 05:51:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 03 Dec 2021 05:51:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 03 Dec 2021 05:51:46 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 05:51:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 03 Dec 2021 05:51:52 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 03 Dec 2021 05:51:53 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 03 Dec 2021 05:52:07 GMT
RUN boot
# Fri, 03 Dec 2021 05:52:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 05:52:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 05:52:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c7f43e0be8e395071a65cf4a7b754dc421cf18e5de6bde1fab5e7376f8d28`  
		Last Modified: Thu, 02 Dec 2021 11:24:55 GMT  
		Size: 3.1 MB (3118874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6815aa712b20bb12686f01503fc3ed9b4bdd67f889d405bf9a8df50d642f36`  
		Last Modified: Thu, 02 Dec 2021 11:29:45 GMT  
		Size: 186.1 MB (186146483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2369a0f20a470ce5231c3f63e4ce9a4f1aee9047f3016e6759d74aaa7febfb8d`  
		Last Modified: Fri, 03 Dec 2021 06:14:51 GMT  
		Size: 67.5 KB (67528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e8928e40013cfd58be5034c0e3be7dcb7e5ea9b217066b34de3a58e43e231`  
		Last Modified: Fri, 03 Dec 2021 06:14:56 GMT  
		Size: 58.8 MB (58815916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7667048c69f48a4ec5cce60ec829ce77d7fee33d52343b2305b9d94f68b2547`  
		Last Modified: Fri, 03 Dec 2021 06:14:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
