## `openjdk:19-jdk-bullseye`

```console
$ docker pull openjdk@sha256:c92332f17d04e800b54c091e9faedae01077af382f5e717eab3a36155a292448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:87d4e0860ead621ea0b99625ef7480d456906bde95a315aac8dc18168d072807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335945861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dc7f3a17bd5d24fbeb2df6f934d86876d03189c31888b18f2fc60d4ad59026`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:50:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:50:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:55:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 04:55:05 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:55:05 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:30:00 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:30:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:30:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c78fa1b97999d08408734a61040475ade5bd7e33e91c0d5170dba2c7c7a92fd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 5.2 MB (5155961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0d2bd524377dc42d072443c0e5e7cafa14f5df609d39bb1f717f43817a2cd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 10.9 MB (10875087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e5964a957d206950c8c0de99f3c491ecec78887ebe4df0ac5ab9ceb536a4d5`  
		Last Modified: Thu, 23 Jun 2022 00:58:59 GMT  
		Size: 54.6 MB (54577874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0d0c51dfe12c92968626b2b8a2c1cf0affe8b1ab35f4f2e7476b5669505bf6`  
		Last Modified: Thu, 23 Jun 2022 05:06:39 GMT  
		Size: 14.1 MB (14071411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae79058efb0588085e4c1437c8688bed89c6705144052fc94652aafdf508692d`  
		Last Modified: Tue, 28 Jun 2022 00:43:23 GMT  
		Size: 196.3 MB (196255642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c21d6141aeab9b31f4117b9915941d7cdfe08832c4f9ccf871309b6e9b8f9364
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334590613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fa90c08acc954147faf6783590c9d0429c24e421ecb49a933277c4dec8f9dc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:28 GMT
ADD file:64c455af1bb18ff2c202a244e058b6e5ac147b89410ed36edc5e29f4b6f02c5d in / 
# Thu, 23 Jun 2022 00:40:29 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:16:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 15:16:30 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:16:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:44:53 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:45:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:45:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f873dfbc59b181817d5bc2b9fc31d90d8f9139c8cabb2fa7264f9bd7b418b8d2`  
		Last Modified: Thu, 23 Jun 2022 00:46:51 GMT  
		Size: 53.7 MB (53696815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b65e0e9cdc28c8cedaabbc5cbae4652c9b107c47684de49f01a77741a5ded`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 4.9 MB (4938760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43836e7983cba8b758620a218a0ee622daf5513308b6a9e8316f94c271ecafd`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 10.7 MB (10656970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1209d2973c25405a6c092fa82923495c9cbf17ea31b92f3c5f9dc06d85c19a4`  
		Last Modified: Thu, 23 Jun 2022 01:22:14 GMT  
		Size: 54.7 MB (54673319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f8b4f3594f5fb53db003f1176418f363c64bf25cf06591d49dc2bf651e111f`  
		Last Modified: Thu, 23 Jun 2022 15:36:14 GMT  
		Size: 15.5 MB (15526195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bb54c800cb56d22016132b14abb98dfeaffbdbe283fc104f8d2f05c62fcca3`  
		Last Modified: Tue, 28 Jun 2022 01:05:48 GMT  
		Size: 195.1 MB (195098554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
