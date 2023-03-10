## `openjdk:21-ea-13-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:5d350eb74b5cc8dcecf64fd4d7e9c8a9d382681e01a71148a965b9aaac2768e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-13-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:be305a46c66334ed60794891ba00d9606946bdc942539b8bd9a67f3d4318958b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230331937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7f1fa85e61c0ccd520f818d714b165d0fa4688d2213a1782609d0ee02762d1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:43:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:43:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 08:43:15 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 08:43:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 Mar 2023 23:27:55 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:28:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 23:28:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be15480d750c54bb843b324de2c368873a4a37cca927bddbc98058e7ca2127c`  
		Last Modified: Wed, 01 Mar 2023 08:47:51 GMT  
		Size: 3.3 MB (3278792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4492d4c620e8838a78df59e9fe20dc1178e31b0a1f7602f4694e55a177fb6f63`  
		Last Modified: Thu, 09 Mar 2023 23:33:00 GMT  
		Size: 199.9 MB (199913263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-13-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:022e9f9ebb258819fd6f3f78f3bde0226672474349ea2269fe8274338adf30fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227471831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eae3476c9a79ad788700bce2734aa1b0c147a8ef5c499dc1f8bd1c79186b561`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:25:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:25:13 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:25:13 GMT
ENV LANG=C.UTF-8
# Thu, 09 Mar 2023 22:48:29 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 22:48:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 22:48:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d097c08e52f9ff771689670d39bd09c2779339cc38112e4f75380522d71e9cf`  
		Last Modified: Wed, 01 Mar 2023 05:29:40 GMT  
		Size: 3.1 MB (3131731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d221ad52320f34ac5a53bb82f8969e833080adb7c223f53ad26e18fcc96d387`  
		Last Modified: Thu, 09 Mar 2023 22:53:17 GMT  
		Size: 198.4 MB (198417401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
