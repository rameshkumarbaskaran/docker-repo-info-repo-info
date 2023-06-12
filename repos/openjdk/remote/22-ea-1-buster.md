## `openjdk:22-ea-1-buster`

```console
$ docker pull openjdk@sha256:423f12310b581e79fc3e1bd2187b3d61bf7a1d847180bf42d99442177fc2995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-1-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8252320f07e70b30120f25310a75529ff4b65f115b39d6091e57c573e4213272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336727030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dcb0b9f4672c55f6898b552aa3680169d888a7460f799c6c8b44f4d9e418b5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 00:43:21 GMT
ADD file:a5100e7ed3c2665c1b4dfbb32eb2b47b85783f2a6800e0ae9004db0ce021dfa5 in / 
# Tue, 23 May 2023 00:43:22 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:56:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 18:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Jun 2023 21:46:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Mon, 12 Jun 2023 21:46:50 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 21:46:50 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 21:46:50 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 21:46:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 21:47:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ea482247e9a0d1ae4ed218fb0828063b9cce53822e64fd4621f587ab85a7e6d`  
		Last Modified: Tue, 23 May 2023 00:46:24 GMT  
		Size: 49.2 MB (49238292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b9a832fb21afaa962a9cab69bf1b4044aa29ef4bd4684505838c4c7cabb76f`  
		Last Modified: Tue, 23 May 2023 06:03:52 GMT  
		Size: 17.5 MB (17450452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49fbb768597d28581cacecb6d008fd42c9ce8fe13fb045d488db3f8ac1b8ac9`  
		Last Modified: Tue, 23 May 2023 06:04:06 GMT  
		Size: 52.2 MB (52190742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fea950bba30f7aa91b4a4e02a998515a06a6391f7482fc0996de1647669518`  
		Last Modified: Tue, 23 May 2023 18:16:13 GMT  
		Size: 14.7 MB (14672966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937cfb288971add1c3c90ea17ea69b8a9c08f0020fe713933b52b604da47ff48`  
		Last Modified: Mon, 12 Jun 2023 21:51:27 GMT  
		Size: 203.2 MB (203174578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
