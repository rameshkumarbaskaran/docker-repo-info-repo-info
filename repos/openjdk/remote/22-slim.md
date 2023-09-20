## `openjdk:22-slim`

```console
$ docker pull openjdk@sha256:5aa5e1fe8f31b09adea7ab10c7c6b6e3125163359b1820266e2e683fcb4515de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:4c0928f246bb313e1ebc6281e1bc54eb14f8ae54e6862a0025b0f09a8feafe42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238576748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ef36d16f2c30ced6ab75dc14b42795da5aef5d98221d465bf39593924b5f96`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:40 GMT
ADD file:a1398394375faab8dd9e1e8d584eea96c750fb57ae4ffd2b14624f1cf263561b in / 
# Wed, 20 Sep 2023 04:55:41 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:16:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 06:16:19 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:16:19 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 06:16:19 GMT
ENV JAVA_VERSION=22-ea+15
# Wed, 20 Sep 2023 06:16:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Sep 2023 06:16:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a803e7c4b030119420574a882a52b6431e160fceb7620f61b525d49bc2d58886`  
		Last Modified: Wed, 20 Sep 2023 05:00:22 GMT  
		Size: 29.1 MB (29124705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4972576c83dad66aa1e4f6d08e74f9e551e721a7cb2dc5370fe8da1af5b11e8`  
		Last Modified: Wed, 20 Sep 2023 06:18:48 GMT  
		Size: 4.0 MB (4008047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1388a8655f3d8cad327ce3bdb0fb792820fa6ff897e2d4e7d9b9cfa0e433838a`  
		Last Modified: Wed, 20 Sep 2023 06:19:03 GMT  
		Size: 205.4 MB (205443996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0f71c3e052ee65bf735ba87b30b556b1e3308d8092833d693d148aee64f824f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236737616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9602bfd63be0b8cb63759d298febf0d2e196d5362254b1cb18725cf2fc019d94`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:57:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:57:26 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:57:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:57:26 GMT
ENV JAVA_VERSION=22-ea+15
# Wed, 20 Sep 2023 17:57:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Sep 2023 17:57:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190c8d653feddc1553f480657f5813ecd07f1979c94ef5b5afa2b7c9c278ca4`  
		Last Modified: Wed, 20 Sep 2023 18:00:57 GMT  
		Size: 3.8 MB (3817580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e64fb78db5a7ad02058a4e46bba29d751b3316590f57e85ce9c9a6725bfdd0`  
		Last Modified: Wed, 20 Sep 2023 18:01:09 GMT  
		Size: 203.8 MB (203762815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
