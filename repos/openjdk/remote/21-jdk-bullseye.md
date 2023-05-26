## `openjdk:21-jdk-bullseye`

```console
$ docker pull openjdk@sha256:4c9a98c1349d5fab14004bc412987f749f09d3864e586a3d613ffc58bdb459bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:780b8c878789ac15ffa5c9d67a127865f654181ba6a0e5dffa74b509fdc6d14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342476724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0a7bfe7df5a78ecb6b433716838baf4cf5c092ea1d5cfdad6fd0022ee07979`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:48:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:48:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:48:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 23 May 2023 07:48:06 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:48:06 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 07:48:06 GMT
ENV JAVA_VERSION=21-ea+23
# Tue, 23 May 2023 07:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 23 May 2023 07:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6710592d62aa1338ac1c1c363dedc255659f666cc41441c7e0f735c484db10ff`  
		Last Modified: Tue, 23 May 2023 01:56:06 GMT  
		Size: 15.8 MB (15760489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75256935197ed1bb3b994a77c01efa00349b901014448a260fafd9c3719a741d`  
		Last Modified: Tue, 23 May 2023 01:56:23 GMT  
		Size: 54.6 MB (54584391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d67ece42c80b3348f67d4cd549463747207c58c70f770e205fa9fd1902bdb9a`  
		Last Modified: Tue, 23 May 2023 07:50:00 GMT  
		Size: 14.1 MB (14072098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00d301cba037ad50ad2f27dda2adae8febba14ea356e099ac0b8a034587f5bf`  
		Last Modified: Tue, 23 May 2023 07:50:12 GMT  
		Size: 203.0 MB (203010719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:58708c050e6dad557545e888d113c85ad881f734b974962c95aae2e09a736b24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341232381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e449fa853365329bb3c0eebb2511efd7f0b7f4e4a9f7ff4d8b1bfc7a4c8cffc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:54:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:55:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 18:14:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 18:14:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 23 May 2023 18:14:34 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 18:14:34 GMT
ENV LANG=C.UTF-8
# Thu, 25 May 2023 23:40:19 GMT
ENV JAVA_VERSION=21-ea+24
# Thu, 25 May 2023 23:40:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='437e740a3ee795a3cf08d6cf5006d03668023151200d5e09ada16d94ef30db22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='ecabd8a50340461d04d06b8f587bf06c614aed9cb441ee3ff9577e1b10e53035'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 25 May 2023 23:40:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cef00b9ad96bea3be667b285f4b22763747912cc8e4f2c3f145facb418d71d`  
		Last Modified: Tue, 23 May 2023 06:02:56 GMT  
		Size: 15.7 MB (15746706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db91b65282bc9aae941329f294e69b2671a6429827e8b357b950a2c112ef783`  
		Last Modified: Tue, 23 May 2023 06:03:12 GMT  
		Size: 54.7 MB (54675888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609082541036b6cde2396564c5b8f3b539e2ee96f4e023757b2603b5f2222cac`  
		Last Modified: Tue, 23 May 2023 18:15:41 GMT  
		Size: 15.5 MB (15528917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c714fc5968e17e7d442812b643e3488f773548b68fa1827dab8233a83f0b2d38`  
		Last Modified: Thu, 25 May 2023 23:43:05 GMT  
		Size: 201.6 MB (201588258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
