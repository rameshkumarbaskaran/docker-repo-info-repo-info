## `clojure:openjdk-18-boot-slim-buster`

```console
$ docker pull clojure@sha256:7961566b99a8624e716b62462138ab29f85b75999fe65178f214ce2f4ae0bc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:4706ebe22d164bed805102c7102638967c65bb64365dee9f4559cc8ac8a949ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278473912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2640544af5f4f2d7ee245edfb7c52f6cc513c1d952f9abe0f5abbcf182c126`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:30:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:30:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:30:51 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:30:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 23:47:49 GMT
ENV JAVA_VERSION=18-ea+26
# Fri, 03 Dec 2021 23:48:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='fdf145c2819ef28edee67b7a6605bee89aefc505a1abea1686bec03fcba87c70'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='14e35be6e99a093bd4d5666bd4d557ebb94ab9e03eab9e9ae0eb69fc7b3e662b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 03 Dec 2021 23:48:04 GMT
CMD ["jshell"]
# Sat, 04 Dec 2021 00:15:07 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Dec 2021 00:15:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Dec 2021 00:15:07 GMT
WORKDIR /tmp
# Sat, 04 Dec 2021 00:15:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Dec 2021 00:15:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Dec 2021 00:15:13 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Dec 2021 00:15:39 GMT
RUN boot
# Sat, 04 Dec 2021 00:15:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Dec 2021 00:15:40 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Dec 2021 00:15:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169731f46e61fb8aef8f7ed809068db98d3feb2466197e9680dbbdbb80d8ed90`  
		Last Modified: Thu, 02 Dec 2021 11:48:59 GMT  
		Size: 3.3 MB (3269625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c329ac79158d2f8bfe8d1b79b967750cad4674dcf5cc36fc8c7c3935a9c920b4`  
		Last Modified: Fri, 03 Dec 2021 23:56:38 GMT  
		Size: 188.9 MB (188949897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc07ccdab8c439f0503146d0c479759ca674e7aad869dde65a6bb6995b765d`  
		Last Modified: Sat, 04 Dec 2021 00:23:05 GMT  
		Size: 279.8 KB (279779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7448042935a81e49ae080d0ea12f13e708e656e04e87b9fbe0d6f183bd56f6d4`  
		Last Modified: Sat, 04 Dec 2021 00:23:09 GMT  
		Size: 58.8 MB (58820477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1b348b50e04017f2bb15a7907f759464f3691fb33dead348360738f65e430`  
		Last Modified: Sat, 04 Dec 2021 00:23:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2fad5b3abb0b5b14b3258597899b3d56f15b93a3547a2531e8fb09d95894b091
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275601285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194cd4277403c5de603d36f14460a5d403621f4ca74f55f436cb0019afe8c6f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:03:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:03:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:03:24 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:03:25 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 23:09:59 GMT
ENV JAVA_VERSION=18-ea+26
# Fri, 03 Dec 2021 23:10:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='fdf145c2819ef28edee67b7a6605bee89aefc505a1abea1686bec03fcba87c70'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='14e35be6e99a093bd4d5666bd4d557ebb94ab9e03eab9e9ae0eb69fc7b3e662b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 03 Dec 2021 23:10:15 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 23:56:25 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 03 Dec 2021 23:56:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 03 Dec 2021 23:56:27 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 23:56:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 03 Dec 2021 23:56:33 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 03 Dec 2021 23:56:34 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 03 Dec 2021 23:56:55 GMT
RUN boot
# Fri, 03 Dec 2021 23:56:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 23:56:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 23:56:57 GMT
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
	-	`sha256:fd8fc63955d0686401dc5da65adbf58f5483f69248b6f115c6436cfb726074ee`  
		Last Modified: Fri, 03 Dec 2021 23:23:51 GMT  
		Size: 187.7 MB (187674877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e68b214339e1b72bd06b2f5fa52dc467baacf8f271d3095141d7e6d42ba32ae`  
		Last Modified: Sat, 04 Dec 2021 00:08:11 GMT  
		Size: 67.5 KB (67538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43175b564d46e796327445edfcfa87220c817eda275b719c5c00092ab6e8360a`  
		Last Modified: Sat, 04 Dec 2021 00:08:17 GMT  
		Size: 58.8 MB (58816448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e2a86c741acb820922054fa162d2c255bf36a2a6e4745a8826491462f7c52`  
		Last Modified: Sat, 04 Dec 2021 00:08:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
