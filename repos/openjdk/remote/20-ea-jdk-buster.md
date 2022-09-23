## `openjdk:20-ea-jdk-buster`

```console
$ docker pull openjdk@sha256:4330bcd686bf9556eeaa0e8aecb524c607dc5231e0331bb8672ed2a0ac24c3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:9eff14c36bbbf49ddf1f25f6159f3c39a1ee5d68908a716ed50c9bcf2b136781
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331008874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019595f00bbff9e77fc74a189e7ce417a660513aa53907fefde2b8505bdb4d9c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:38 GMT
ADD file:4649a893b2859f2ff51182a13c9c8eeaeaea866161b3f4a1c4f0bb48bc01d007 in / 
# Tue, 13 Sep 2022 00:56:38 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:44:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 03:45:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:02:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 07:02:29 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:02:29 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:34:05 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:34:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:34:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86467c57892b6bb48d563cb5940c68b69c431b2e79c3547df60d1c761c21c156`  
		Last Modified: Tue, 13 Sep 2022 01:00:51 GMT  
		Size: 50.4 MB (50440374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34aaa3cba7676359d4f9d29333c92bd9f448969b07f56bb8482398a5dc53c6`  
		Last Modified: Tue, 13 Sep 2022 03:51:20 GMT  
		Size: 7.9 MB (7857266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a443ab54eaa5455912b469fb6d8b621ade658cd0afef9c706b7e37085004b25`  
		Last Modified: Tue, 13 Sep 2022 03:51:20 GMT  
		Size: 10.0 MB (9998148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cacf42b5677aa20eb8fff5102f7482828f27555a167f49da0597869f91002f`  
		Last Modified: Tue, 13 Sep 2022 03:51:39 GMT  
		Size: 51.8 MB (51844022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dadb0d667c93c08e4c43b69152456636f0fbd5838bdf1aa4c0a95b1da6248a9`  
		Last Modified: Tue, 13 Sep 2022 07:10:11 GMT  
		Size: 13.9 MB (13921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b5c94ae2486f94cbdf37338233269f5c9ac265ccd522a99fc26394e80b222`  
		Last Modified: Fri, 23 Sep 2022 00:39:58 GMT  
		Size: 196.9 MB (196947250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d29d476f3cb749824367533b2e4d916903585bbc168ec55290ec50259067b82d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329089277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d230918915aae305089472f146686d965bd8c1895d16ce512c24b0092d31558f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:06 GMT
ADD file:304a544562f139d7ab96511b7f1e059966cf90169117e835072f132468bf91c8 in / 
# Tue, 13 Sep 2022 02:11:07 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 05:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 05:03:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Sep 2022 05:03:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:38:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 14:38:41 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:38:42 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:52:12 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:52:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:52:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2406a452ad23ba9085e0708f5e15309206a618eb828aa307becbb239414392f`  
		Last Modified: Tue, 13 Sep 2022 02:16:42 GMT  
		Size: 49.2 MB (49228261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91678e90eed09f0ef020521348ac09d6816bafc59c40f4fa0d821de2fb50f881`  
		Last Modified: Tue, 13 Sep 2022 05:11:16 GMT  
		Size: 7.7 MB (7722146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9f7a2d689202901c1750505adb5481f0e4499998084e1df70209fa11f8e8b5`  
		Last Modified: Tue, 13 Sep 2022 05:11:16 GMT  
		Size: 9.8 MB (9768786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e42f230da3003e92b349e81764d6c82232541223fa1b17d44222328b0cf201`  
		Last Modified: Tue, 13 Sep 2022 05:11:35 GMT  
		Size: 52.2 MB (52175369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1573794cb1b6b8bc438cfcbac874e10994f6b5687c9e1038cb8a8d9b106b2e9`  
		Last Modified: Tue, 13 Sep 2022 14:51:07 GMT  
		Size: 14.7 MB (14670916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2de447cfa37390b4205a1b42765d602fb213f18ceafd0bb2e0cda4c32662ec`  
		Last Modified: Fri, 23 Sep 2022 01:01:15 GMT  
		Size: 195.5 MB (195523799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
