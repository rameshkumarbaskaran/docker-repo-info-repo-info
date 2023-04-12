## `openjdk:21-ea-slim-buster`

```console
$ docker pull openjdk@sha256:ef93b24da2933d9b816ac0936f9c5c588212493cb587adf76443b64e19505f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:eef0d7cfeb5de46dfb9b2d8ce18f4a58862211be95c0ae70b32f6dd25c489678
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232229383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02adaea18e4a33c3ce4f6cb170d8c84582745b3b199b47bd73e65808cf59da6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:39:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:39:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 09:39:08 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 09:39:08 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 09:39:08 GMT
ENV JAVA_VERSION=21-ea+17
# Wed, 12 Apr 2023 09:39:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Apr 2023 09:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e35bb669fa393f13e7b4c100af1023e9c2da16c731aff14e3fd9e83c7cfe2a8`  
		Last Modified: Wed, 12 Apr 2023 09:41:34 GMT  
		Size: 3.3 MB (3278764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82782e66b0c34c162d908dd6b219bb85b6713a2a2c1653e52c1ac3e6a2377790`  
		Last Modified: Wed, 12 Apr 2023 09:41:47 GMT  
		Size: 201.8 MB (201811699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6843bb1ebbd985111f941736ad0ef6b01567f560ebb48ebcf6c624c969d0d7bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229229229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bba77ecd237f3e5776ca9bc6feb3479c127746eeaa4003b4109bd11921c3c44`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:02 GMT
ADD file:39d4ef5cc48487567b857a8527ab3c106b5099eafffbeaa8b70df450fb8409e3 in / 
# Wed, 12 Apr 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:11:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 05:11:47 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 05:11:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 05:11:47 GMT
ENV JAVA_VERSION=21-ea+17
# Wed, 12 Apr 2023 05:11:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Apr 2023 05:12:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:27bec964ec41cf69bd5df2ffd45c27623ae4bb0eb6f9f366179f7ac9b47d9840`  
		Last Modified: Wed, 12 Apr 2023 00:43:11 GMT  
		Size: 25.9 MB (25922011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe87b3c027f2b1952babc2b86de6d9f2011dfb0410c3f340d15409fba01477`  
		Last Modified: Wed, 12 Apr 2023 05:14:03 GMT  
		Size: 3.1 MB (3131734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e415eb43cf8e7d3cf7376bb524d58bf0fce0043988a73da34b0545a115e8ea5`  
		Last Modified: Wed, 12 Apr 2023 05:14:15 GMT  
		Size: 200.2 MB (200175484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
