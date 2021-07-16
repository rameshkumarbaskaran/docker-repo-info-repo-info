## `openjdk:18-ea-slim`

```console
$ docker pull openjdk@sha256:8f11f632453149a57c93912d4c92aa349c7ca4b02a15bbe2e56c1c184037ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:69de4fa58305d634d79351145286417ba418310983cadfd7c5f9fd1bdba1c6b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218369011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c103b9d47184ccf4dede6d8b86cb78801b264f4da4ad95b07404a0f065d843`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:00:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 23 Jun 2021 08:00:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 08:00:10 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jul 2021 22:21:30 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:21:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:21:44 GMT
CMD ["jshell"]
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
	-	`sha256:a1d382aafedc59101561cceb41c4f450883fe99e0be208f363a9956357ad89bd`  
		Last Modified: Thu, 15 Jul 2021 22:29:57 GMT  
		Size: 188.0 MB (187954274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8657b72d8fc3aef8dcbaba70ea8e06bf5fceead7fb009d6475f82e806c9c5801
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215729774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03440f805a117da0780b27b1d993adad7337cbccf4a0d271bdbdccf8515c1121`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:56:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 23 Jun 2021 04:56:08 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 04:56:08 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jul 2021 22:41:52 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:42:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:42:05 GMT
CMD ["jshell"]
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
	-	`sha256:e6aaa80fd5989cc2bb1734f39dbc7529c72b4345e5c2249f835c6b4ca6e26d0b`  
		Last Modified: Thu, 15 Jul 2021 22:56:49 GMT  
		Size: 186.7 MB (186695887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
