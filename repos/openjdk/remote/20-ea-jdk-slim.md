## `openjdk:20-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:fc53a0cfed9e5886385567792e002360c4c39de0f21fa60727a769972b837e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:2a267ed6d072ca2532d2228dfa9557e22d80810ab3249dbb882423e476d0b041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231327627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda705ab02097a6902752e852dd2a4a858aefe2e6189686b34b44ff257d717ea`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:37:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:37:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 13:37:09 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:37:09 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 21:31:10 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:31:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 21:31:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54e66bc569588bf6945416d9455248d373e1db9ffe9428a75b3963b798662d6`  
		Last Modified: Tue, 15 Nov 2022 13:42:10 GMT  
		Size: 1.6 MB (1583981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0677561d749da40d300f83eb97ef2d59424a1703d3bbc53467b2aaa997ed5f98`  
		Last Modified: Wed, 30 Nov 2022 21:36:20 GMT  
		Size: 198.3 MB (198331016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6d041cbf7b6203e0fa7e4843897f815874fcc04f851f0b3f4ec3c09a097089d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228496206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2c52c6cd8818ed7ddb69fd09c8e203b58c16ad7130880f6ac6dcccf425735d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:59:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 06:59:21 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 06:59:21 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 20:55:09 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 20:55:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 20:55:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bb8ead4542ac0732ce51843584ff03141aa14c30f7161cc4856f3caa5d7a95`  
		Last Modified: Tue, 15 Nov 2022 07:04:17 GMT  
		Size: 1.6 MB (1567467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59db5dc89950d8ddcb0e8765a30627f0b7a8073770008cafcbbce8fd104ed319`  
		Last Modified: Wed, 30 Nov 2022 21:00:36 GMT  
		Size: 196.9 MB (196868134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
