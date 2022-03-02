## `clojure:openjdk-18-boot-slim-buster`

```console
$ docker pull clojure@sha256:b9140a0b7e4bb8e51a5be5fc03ae4e201694ee0be2542dc37e9d19e2cc779917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:f023bce952a24dc2b7ec1f9572614fc25d27789ebae75e25a648d11792ea8433
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278575699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6570492a8332bf767cef657e6ae2c77c5854d670c08810b46f1ca60cef95651d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:21:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:21:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:21:11 GMT
ENV LANG=C.UTF-8
# Mon, 21 Feb 2022 18:28:08 GMT
ENV JAVA_VERSION=18
# Mon, 21 Feb 2022 18:28:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 21 Feb 2022 18:28:25 GMT
CMD ["jshell"]
# Mon, 21 Feb 2022 19:31:02 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 21 Feb 2022 19:31:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 21 Feb 2022 19:31:03 GMT
WORKDIR /tmp
# Mon, 21 Feb 2022 19:31:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 21 Feb 2022 19:31:08 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 21 Feb 2022 19:31:08 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 21 Feb 2022 19:31:42 GMT
RUN boot
# Mon, 21 Feb 2022 19:31:42 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 21 Feb 2022 19:31:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 21 Feb 2022 19:31:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8d0f5eb646a53df0b867301afa43404e868c540fdf170240578844dfd0d6b`  
		Last Modified: Wed, 26 Jan 2022 09:43:10 GMT  
		Size: 3.3 MB (3269688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05415153b9adccd8e14809843d9c1258c30019b83b6051851b80ba688df96e0d`  
		Last Modified: Mon, 21 Feb 2022 18:40:20 GMT  
		Size: 189.1 MB (189051219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264b8db9b3e583c097ca68f41c182e9903f03f57a1e8909cface958412297ecb`  
		Last Modified: Mon, 21 Feb 2022 19:39:10 GMT  
		Size: 279.8 KB (279810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fd44c4c3801177b326987546e31c81e3fca9524c36cf295278cca273253179`  
		Last Modified: Mon, 21 Feb 2022 19:39:13 GMT  
		Size: 58.8 MB (58820845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d6dcf29310a64ee6b815a8a367826e27c9b14f487affcd019b14c52ad8b3c0`  
		Last Modified: Mon, 21 Feb 2022 19:39:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0cdb1dfd0055d9c31593677461698590754b2b666eafc8ad0c016eb57bc8ac10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275687624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211898dc70fd8dce5292900aff5608624aae738a3b4cca9cf5b2f4d4e4ee6d54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:57 GMT
ADD file:7d35162eea06441e7115c6fd9508802eafee00f64b11a7529a8f125bc67fa95e in / 
# Tue, 01 Mar 2022 02:11:57 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:51:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 01 Mar 2022 13:51:19 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:51:20 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 13:51:21 GMT
ENV JAVA_VERSION=18
# Tue, 01 Mar 2022 13:51:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:51:37 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:36:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Mar 2022 08:36:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Mar 2022 08:36:27 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:36:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Mar 2022 08:36:33 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Mar 2022 08:36:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Mar 2022 08:36:47 GMT
RUN boot
# Wed, 02 Mar 2022 08:36:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:36:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:36:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:69bf0018a85cc0775a59a4dbda1b2f2e71086a2d817473f72336bf4d0a83b9d0`  
		Last Modified: Tue, 01 Mar 2022 02:19:15 GMT  
		Size: 25.9 MB (25923140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1598aa0249d59bdc58f96c0187ae665625594bf9f256f5bca2c1b941fc493be2`  
		Last Modified: Tue, 01 Mar 2022 14:14:40 GMT  
		Size: 3.1 MB (3118853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28511f1fd4d703e3fa640844904e6871741e362cb09766784ce56573dbfa0a01`  
		Last Modified: Tue, 01 Mar 2022 14:17:15 GMT  
		Size: 187.8 MB (187762055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9143a0630ebaf9424ed634cfa224003051fa7c710d6b5fdc2fcadd3812bec7ef`  
		Last Modified: Wed, 02 Mar 2022 09:04:52 GMT  
		Size: 67.5 KB (67492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8b1e77c4077a9cd196da9e1b8e6cf5eb63fab97a7bd7a57e5db0dd8f477db0`  
		Last Modified: Wed, 02 Mar 2022 09:04:58 GMT  
		Size: 58.8 MB (58815679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0bb1c1be83bb35ecf01ad54d752fc033abfbf1087d0257dffc9d642a7d4990`  
		Last Modified: Wed, 02 Mar 2022 09:04:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
