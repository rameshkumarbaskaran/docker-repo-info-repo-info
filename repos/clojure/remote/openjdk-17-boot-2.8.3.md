## `clojure:openjdk-17-boot-2.8.3`

```console
$ docker pull clojure@sha256:cef07ad5ba0b5818b66621fc0ca428edac93706be8f014c6075b7d3d89c5b688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:a5a258d5463bf26b9f4356e36439adb00399ceeb1266bbfd33b76c67e69c4d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (277014489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53532df236a45f87fac9ce68d3bf5de2d217067c78344d7e1dbfeea0c2ef4947`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:01:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 23 Jun 2021 08:01:12 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 08:01:12 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 01:11:51 GMT
ENV JAVA_VERSION=17-ea+28
# Sat, 26 Jun 2021 01:12:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='29f489da387fdabce2ebfbb74f474c424ed9c92380783da511d8ab1ed5dee912'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='60752f6f44e478db934f4dc4b9a7cb715387ae964fb353e469dd986a5aeaf92b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 01:12:04 GMT
CMD ["jshell"]
# Sat, 26 Jun 2021 03:40:45 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 26 Jun 2021 03:40:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 26 Jun 2021 03:40:46 GMT
WORKDIR /tmp
# Sat, 26 Jun 2021 03:40:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 26 Jun 2021 03:40:51 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 26 Jun 2021 03:40:52 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 26 Jun 2021 03:41:13 GMT
RUN boot
# Sat, 26 Jun 2021 03:41:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee45ae9730633057cf9bd12924f9a1bf2b590631d3d085b14c96f4466557794`  
		Last Modified: Wed, 23 Jun 2021 08:12:04 GMT  
		Size: 3.3 MB (3268886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1efdb0509c01ae6078f6acbaf13bddc582a5fe7c6d3c96a17c24840cd08d28`  
		Last Modified: Sat, 26 Jun 2021 01:24:13 GMT  
		Size: 187.5 MB (187499396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8a64a6dddef4c0e6ca5f3a21b17f9164494c5c6391de7c1dc7cd0693b3accc`  
		Last Modified: Sat, 26 Jun 2021 03:49:27 GMT  
		Size: 279.9 KB (279853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe49a38aba147f484faf3825400aad28073ce6e428267e877a7ee922a08009f6`  
		Last Modified: Sat, 26 Jun 2021 03:49:31 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:163486ce1a22415b11ccfb33d94319527ff477b6f0b19eebebb01398d3ad7f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274428260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc7a602cd45cb6028356be8fa275e533b1bd4addc5e7fb385047d148063ccaf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:57:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 23 Jun 2021 04:57:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 04:57:10 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 00:24:58 GMT
ENV JAVA_VERSION=17-ea+28
# Sat, 26 Jun 2021 00:25:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='29f489da387fdabce2ebfbb74f474c424ed9c92380783da511d8ab1ed5dee912'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='60752f6f44e478db934f4dc4b9a7cb715387ae964fb353e469dd986a5aeaf92b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 00:25:11 GMT
CMD ["jshell"]
# Sat, 26 Jun 2021 02:59:03 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 26 Jun 2021 02:59:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 26 Jun 2021 02:59:03 GMT
WORKDIR /tmp
# Sat, 26 Jun 2021 02:59:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 26 Jun 2021 02:59:08 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 26 Jun 2021 02:59:09 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 26 Jun 2021 02:59:28 GMT
RUN boot
# Sat, 26 Jun 2021 02:59:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5c013aa648ff2c30dafc35db9efb2faa7f9fa6f1c98a2f31c1b5fee0334dc`  
		Last Modified: Wed, 23 Jun 2021 05:11:10 GMT  
		Size: 3.1 MB (3118894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1138557721c2d48322abc8e0b51ee2dc8c2e0090f55aeea6aba83f4b8391825`  
		Last Modified: Sat, 26 Jun 2021 00:44:41 GMT  
		Size: 186.3 MB (186294316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab2c962830bdb4c10e9edf553895e6a61454c75b3d432bcbcd5f7b28d6c8270`  
		Last Modified: Sat, 26 Jun 2021 03:07:57 GMT  
		Size: 279.6 KB (279558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db4fed44872fb8c9ac85a7dd053378df545c4325942a22e70b9e99daeb3bc86`  
		Last Modified: Sat, 26 Jun 2021 03:08:02 GMT  
		Size: 58.8 MB (58820499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
