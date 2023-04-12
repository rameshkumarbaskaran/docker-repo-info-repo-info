## `openjdk:21-ea-17-jdk-bullseye`

```console
$ docker pull openjdk@sha256:49483645934b0a0a7bf8c3106f90f36460ddfbd23543e20268bd283d0121c89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-17-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:fd36014e5950f24e6d3ad27d1a147636af2f871f9582c2fa8b717cf570792a5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341282985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2830b620cf4ed811d8ddcbf00b0b75e2b759784f4d76787838e9e28e2505fc9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:01:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:01:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 06:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 16:43:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 16:43:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 23 Mar 2023 16:43:58 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 16:43:58 GMT
ENV LANG=C.UTF-8
# Tue, 11 Apr 2023 23:33:13 GMT
ENV JAVA_VERSION=21-ea+17
# Tue, 11 Apr 2023 23:33:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 Apr 2023 23:33:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a71c865a2c34678c6dea55e4b0928f751ee3c0ca91cace6e4e0578c534d6cf`  
		Last Modified: Thu, 23 Mar 2023 06:08:01 GMT  
		Size: 5.2 MB (5166592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670730c27c2eacf07897a6e94fe55423ea50b884d9c28161a283bbbf064d1124`  
		Last Modified: Thu, 23 Mar 2023 06:08:02 GMT  
		Size: 10.9 MB (10876735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7a2c95f0f8b221d776ccf35911b68eec2cf9414a44d216205a6f03e381d3d7`  
		Last Modified: Thu, 23 Mar 2023 06:08:19 GMT  
		Size: 54.6 MB (54583510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8dcb5102ca902e2a58b698b899fa3cd3444bd088c2c8b6cc0dd23b6e89edfc`  
		Last Modified: Thu, 23 Mar 2023 16:45:55 GMT  
		Size: 14.1 MB (14071945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2456ad4bb63378be11f5b2c868f9a0af1dda1709173a765231f01a4c0ddf2b6e`  
		Last Modified: Tue, 11 Apr 2023 23:36:10 GMT  
		Size: 201.5 MB (201538595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-17-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8f2c3f1c85e4561bc9224884c49306f29a94e9dd9e3f63953a77779e19e5fd84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339836771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6197492bc4a33e668c122540bfecb0fffd3f7d0c5db53c4e0ed3ecda078f164b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:06:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:10:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 05:10:41 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 05:10:41 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 05:10:41 GMT
ENV JAVA_VERSION=21-ea+17
# Wed, 12 Apr 2023 05:10:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Apr 2023 05:10:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5884e7f2c8c61aa845de4902fc29639b58861ae6c2d80bafe82082c0456c0740`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 5.2 MB (5152752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b792b01ed3c8dc1488cd8aac41ab7d49bb17f3fa22b2e6c846078cec81a1c00`  
		Last Modified: Wed, 12 Apr 2023 01:13:17 GMT  
		Size: 10.9 MB (10873655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f993d5b17f32f4b8a535c25e182e5d8412625beee450e513ca57036e8fdd6dc`  
		Last Modified: Wed, 12 Apr 2023 01:13:34 GMT  
		Size: 54.7 MB (54676038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09cb5578d3115a65cc6337102cf310454aa8eef83438795a15e17d95122657d`  
		Last Modified: Wed, 12 Apr 2023 05:12:33 GMT  
		Size: 15.5 MB (15529043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7183215120730a76a51e982063ad1739186ac840f95f25a5b8e060c8dc86de26`  
		Last Modified: Wed, 12 Apr 2023 05:12:43 GMT  
		Size: 199.9 MB (199899754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
