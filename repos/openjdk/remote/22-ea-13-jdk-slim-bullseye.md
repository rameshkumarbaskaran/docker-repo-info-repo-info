## `openjdk:22-ea-13-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:a7e480fdddd7d14e3f1440fb160622b15b1349360ad9f27d9302dde1e0e159b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-13-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2460432ceb2e836d9dad95a9225e2a8135d522b814eaf1dcfbcf8d80051beb38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238261118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142632166f1740dc2c934fe3b766f65954297860c085cc649e9b7770af531acd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:17:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 16 Aug 2023 15:17:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:17:12 GMT
ENV LANG=C.UTF-8
# Fri, 01 Sep 2023 00:47:20 GMT
ENV JAVA_VERSION=22-ea+13
# Fri, 01 Sep 2023 00:47:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='fb110a662f4aaa988d446d09ec4ad4683cc96ee24d9f4ebf5c96177b441fa1f2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='d8c826ad7c22505872c310eb7651a071dc380ee14401b65b08861ec4ffc6b95d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Sep 2023 00:47:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c001491d10985337074f3c26c09f771a339e441538d4bf8d9c02c011154869a`  
		Last Modified: Wed, 16 Aug 2023 15:21:23 GMT  
		Size: 1.6 MB (1582459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29b646a3df9376ccfec09524bbff72e31af9f61dd75f4e96ee38a4829872d1b`  
		Last Modified: Fri, 01 Sep 2023 00:51:49 GMT  
		Size: 205.3 MB (205260981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-13-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5f3e426fc75d3ea071d46b678664d028b8051b89b778180baa419f1761d3d571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235220765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b0cc249bed3a814a1612207b903fdcffe04db0827f41a5065c24b6cb330ca8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:51:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:51:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 01:51:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 01:51:41 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 01:51:41 GMT
ENV JAVA_VERSION=22-ea+13
# Thu, 07 Sep 2023 01:51:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='fb110a662f4aaa988d446d09ec4ad4683cc96ee24d9f4ebf5c96177b441fa1f2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='d8c826ad7c22505872c310eb7651a071dc380ee14401b65b08861ec4ffc6b95d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Sep 2023 01:51:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04284697cdcc06052ec1cff605b74ea641c90e14dd4b9026a2ebc812c5a5625b`  
		Last Modified: Thu, 07 Sep 2023 01:54:22 GMT  
		Size: 1.6 MB (1566472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc71dd477047e14bafdc6ddc3246ce23b8572a93622a517298df5529fc5cfa`  
		Last Modified: Thu, 07 Sep 2023 01:54:34 GMT  
		Size: 203.6 MB (203591390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
