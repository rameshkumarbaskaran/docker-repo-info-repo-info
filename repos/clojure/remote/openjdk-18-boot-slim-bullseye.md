## `clojure:openjdk-18-boot-slim-bullseye`

```console
$ docker pull clojure@sha256:4e855d8b5b6e004eeb177e67e036d3fdd7968737e8f7240470738d21ee41d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8f43b220cf06f58d31732cfdeed3fb29f218d13ec3bbebb6765a6ac9d787970b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281098472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c5a790b72e4499122400ef8492c556b6627f25b7952e9bf47f7c0057f633fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:29 GMT
ENV LANG=C.UTF-8
# Fri, 11 Feb 2022 23:52:48 GMT
ENV JAVA_VERSION=18-ea+35
# Fri, 11 Feb 2022 23:53:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/35/GPL/openjdk-18-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='62a711fdc1a8f7051551113d62f8cc7e3be42e57335d11d605dab060f29a12e2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/35/GPL/openjdk-18-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='cf0298eeac8e0d1d93fb1615916e08c12cd1a0e372a132cec2e66b2a30de6815'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Feb 2022 23:53:16 GMT
CMD ["jshell"]
# Sat, 12 Feb 2022 01:33:24 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 12 Feb 2022 01:33:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 12 Feb 2022 01:33:24 GMT
WORKDIR /tmp
# Sat, 12 Feb 2022 01:33:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 12 Feb 2022 01:33:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 12 Feb 2022 01:33:29 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 12 Feb 2022 01:33:51 GMT
RUN boot
# Sat, 12 Feb 2022 01:33:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 12 Feb 2022 01:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 12 Feb 2022 01:33:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36e89adc1548d864aa7bcd823cc7a96ae82a3e54d06a031358f4975b9081328`  
		Last Modified: Sat, 12 Feb 2022 00:17:01 GMT  
		Size: 189.0 MB (189046158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf9e3a46380f21dc0f4531731bb4a1f736300d91fce093aa234783489eeed47`  
		Last Modified: Sat, 12 Feb 2022 01:43:16 GMT  
		Size: 283.1 KB (283100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d41eed28e605730f1012a1a8487897cfc47f745b3e3f0e1650bc39e37bcac59`  
		Last Modified: Sat, 12 Feb 2022 01:43:20 GMT  
		Size: 58.8 MB (58820500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcb655633ddcb4d70b9fd90a73cc35e7587560175f7df54e9d2a7a3397d4469`  
		Last Modified: Sat, 12 Feb 2022 01:43:16 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a460cf2044e53e2c503acedae1bceb0c637753d754f412da43cf5e1f7ded40c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278271877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfeb77f3352625de57c3033276d15ab3c60c5874eeae758d4e64d52c424d81f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:52:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:52:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:52:15 GMT
ENV LANG=C.UTF-8
# Sat, 12 Feb 2022 00:10:07 GMT
ENV JAVA_VERSION=18-ea+35
# Sat, 12 Feb 2022 00:10:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/35/GPL/openjdk-18-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='62a711fdc1a8f7051551113d62f8cc7e3be42e57335d11d605dab060f29a12e2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/35/GPL/openjdk-18-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='cf0298eeac8e0d1d93fb1615916e08c12cd1a0e372a132cec2e66b2a30de6815'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 12 Feb 2022 00:10:24 GMT
CMD ["jshell"]
# Sat, 12 Feb 2022 03:38:19 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 12 Feb 2022 03:38:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 12 Feb 2022 03:38:20 GMT
WORKDIR /tmp
# Sat, 12 Feb 2022 03:38:25 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 12 Feb 2022 03:38:25 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 12 Feb 2022 03:38:26 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 12 Feb 2022 03:38:39 GMT
RUN boot
# Sat, 12 Feb 2022 03:38:41 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 12 Feb 2022 03:38:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 12 Feb 2022 03:38:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ab1afb4a9bc9fadd36276dc46de77ac914bce63cd1f3af65fd2189850afcb`  
		Last Modified: Sat, 12 Feb 2022 00:35:31 GMT  
		Size: 187.8 MB (187766076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02781479a68f34c059976074ec842f343eb2c974b1f43337459fa7efffd9dbd4`  
		Last Modified: Sat, 12 Feb 2022 03:51:54 GMT  
		Size: 67.2 KB (67208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5516f1ee342320fb67009fac05181cd6fe294241004017ed2b3676907856afd`  
		Last Modified: Sat, 12 Feb 2022 03:52:02 GMT  
		Size: 58.8 MB (58815520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd5f2f8a62ed0749aab536fe1fd493d6104871086583dc31272da6b626e6f56`  
		Last Modified: Sat, 12 Feb 2022 03:51:54 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
