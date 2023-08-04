## `openjdk:21-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:22a9405b36c92de0b904f80991ac5b035efbb4f2b3b4b525e1a699fee18c5595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:9e02d1014ae6299c60bbde30a15ce082403b3e7680a6a1e21d11590aa263d6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237309857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ddc013dac08248ef7217ecd63e6c8a17746773ea1ea53020b035c2c3896ab4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:10:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Fri, 28 Jul 2023 04:10:52 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 04:10:52 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:31:10 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 00:31:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d16356385a726320077563c6180f2eabf72ded64b5695f24f3e7a2d3980b1f11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='cb862b1f34e15c99aacab2c9e6ed259ad056eaa3dfc547ebc6026630db64af94'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:31:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb66e7ec1c7a7454751d006538099f5227c45bf60b9bca6714a1f3df49c9637`  
		Last Modified: Fri, 28 Jul 2023 04:13:59 GMT  
		Size: 1.6 MB (1582416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836b067eb9ca5b761db743ea7c9eccce50737ef9700fdfa8c7a5ae0362c8ec90`  
		Last Modified: Fri, 04 Aug 2023 00:39:28 GMT  
		Size: 204.3 MB (204309839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:915b71325cfed4bf24feec8d493e166611b5e0c74496a7615e38cebed7cb7e07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa770e18f1a717d5133f99fe1960d6a28afa62d6a57840436763b81cda0bc6c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 10:41:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:43:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Fri, 28 Jul 2023 10:43:01 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 10:43:01 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 01:00:32 GMT
ENV JAVA_VERSION=21-ea+34
# Fri, 04 Aug 2023 01:00:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='d16356385a726320077563c6180f2eabf72ded64b5695f24f3e7a2d3980b1f11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='cb862b1f34e15c99aacab2c9e6ed259ad056eaa3dfc547ebc6026630db64af94'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 01:00:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfcd6c33d9e0f4dee755272a69686a8c3c0c86e69318d611216eda7d52d6aaa`  
		Last Modified: Fri, 28 Jul 2023 10:45:56 GMT  
		Size: 1.6 MB (1566457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76598b65bfd8120e6d3ffc3d6d273f55e97a4b6b2707c292f73c7457925d479`  
		Last Modified: Fri, 04 Aug 2023 01:08:37 GMT  
		Size: 202.6 MB (202649397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
