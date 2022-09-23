## `openjdk:20-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:f59d06d43435c0cd5a7e6db77175eaaeb25721cefe964e3b4515d53087dc8e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:ac4ed8ecaf25d190fa6fd07a9b6b47a919b03ac3330db9e3e78c1bf39059efe0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230197806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deffaf033b0d2d090ab89d25e23ec1f207d6a8335d32963bae3adcabb0a4dc52`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:01:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 07:01:59 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:01:59 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:33:46 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:34:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:34:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e69b53e7b682e7dd85bc12ebde7a4734ebd6cf1c24c9932ed6d0f5ad309612`  
		Last Modified: Tue, 13 Sep 2022 07:09:16 GMT  
		Size: 1.6 MB (1582302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a36dae14c19609810dc7847976edfc194b5ca56e53b31bdc850e5e88387758`  
		Last Modified: Fri, 23 Sep 2022 00:39:11 GMT  
		Size: 197.2 MB (197211383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7fccec485f09310c5075a4be2cc1f2d12c82448ec9c51389c3fc6da42cda2852
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227195068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a7435132aa75dd612245df1dae2cd31a9bc60b20a3c6a6a376d83bf507336a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 14:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:38:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 14:38:03 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:38:04 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:51:48 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:52:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:52:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dff4c2315c7ba5819fcc75c0bf4e213049019660b96d9d0fa49d7361693e85`  
		Last Modified: Tue, 13 Sep 2022 14:50:08 GMT  
		Size: 1.6 MB (1565978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9ff0c7bfe9d35776770e3eb1f0c01752b3aafba7b2af3a6a5835ff36a0e331`  
		Last Modified: Fri, 23 Sep 2022 01:00:18 GMT  
		Size: 195.6 MB (195574851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
