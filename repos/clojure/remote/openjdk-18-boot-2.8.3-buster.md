## `clojure:openjdk-18-boot-2.8.3-buster`

```console
$ docker pull clojure@sha256:f1aaf144f4cb6ea4737477bbf4e36f0778bd4179b56a2405b267d7341c22fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-buster` - linux; amd64

```console
$ docker pull clojure@sha256:30cec0650fc551ae93042c8f9913e90c303dd6ded7e8aa8dda1f2b2d4eea5164
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382568801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b740bf83adb6b403eb84ee8e2b1777ff347bd8368f89378608b1c8a12a643c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:31:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:08:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 23:08:54 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:08:54 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:08:54 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 23:09:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:09:04 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:42:37 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:42:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:42:37 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:42:41 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 29 Mar 2022 23:42:41 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:42:42 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:43:02 GMT
RUN boot
# Tue, 29 Mar 2022 23:43:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:43:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:43:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98d6bb51c7ccadb2f72a1498db713088ec7c3f449b3c810d95dbca6ba7511ba`  
		Last Modified: Tue, 29 Mar 2022 17:39:41 GMT  
		Size: 51.8 MB (51843446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355592f16f1c7af5aaf7bf2b59b429fc6d54e6a9d493142700d424847989c58`  
		Last Modified: Tue, 29 Mar 2022 23:20:09 GMT  
		Size: 13.9 MB (13921230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da2c15b3a26cf50e1f2ba899e3b89c1414e379b23eed1fe114f1d2919fb72a9`  
		Last Modified: Tue, 29 Mar 2022 23:22:23 GMT  
		Size: 188.8 MB (188787724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392b55d53fa49c3711ec9cb30c95f71cf3467eee8db91bf45e2949e210791081`  
		Last Modified: Wed, 30 Mar 2022 00:03:15 GMT  
		Size: 903.9 KB (903860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d49d2808da30290dd7ca09028874c4fcc04c754b71461c0c1d08ae3fcaf90e9`  
		Last Modified: Wed, 30 Mar 2022 00:03:18 GMT  
		Size: 58.8 MB (58820632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36896544ce776274a3e0aa67c5f3038bbffc6d8e149919c4c3d0554ccb8f184b`  
		Last Modified: Wed, 30 Mar 2022 00:03:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:153fb8b5c5dce70462bbb3dc863b027074b6b7e7c4559aee70724d27d7bc384a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380749408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff6bdefc7dbcc871719b0be0ef7b6f5bcba92d2ef34794a064291b5ca2300b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 09:01:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 30 Mar 2022 09:01:38 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 09:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 09:01:40 GMT
ENV JAVA_VERSION=18
# Wed, 30 Mar 2022 09:01:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 09:01:53 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 09:50:15 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 30 Mar 2022 09:50:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 09:50:16 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:50:27 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 30 Mar 2022 09:50:27 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 30 Mar 2022 09:50:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 30 Mar 2022 09:50:46 GMT
RUN boot
# Wed, 30 Mar 2022 09:50:47 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 09:50:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 09:50:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bff08cf9734159a77ecf001874bfd910561517c9c87811003564d4a2f00421`  
		Last Modified: Wed, 30 Mar 2022 02:25:51 GMT  
		Size: 52.2 MB (52174968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b271ee6d3652db1e127606e48dbdddd1d0197d93f24fe910a41298350932c02d`  
		Last Modified: Wed, 30 Mar 2022 09:20:58 GMT  
		Size: 14.7 MB (14671177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea71f16da2d66db91f1e7c288f5015cae0a94c0483076e4667b58d94e31e5e37`  
		Last Modified: Wed, 30 Mar 2022 09:23:38 GMT  
		Size: 187.7 MB (187710651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9cee8d79492316f881bbcf7c001c2d9891275784047607007e0f61c7275345`  
		Last Modified: Wed, 30 Mar 2022 10:18:46 GMT  
		Size: 663.9 KB (663867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c9a974b573644cf9497dcdcd94755aa5dfe5ce56ae80d465f0291fa11f87f0`  
		Last Modified: Wed, 30 Mar 2022 10:18:50 GMT  
		Size: 58.8 MB (58815668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28941f8da739fe3def0a4934860c44a1e0e80ad4ef5e2c9fbae19978887bd25a`  
		Last Modified: Wed, 30 Mar 2022 10:18:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
