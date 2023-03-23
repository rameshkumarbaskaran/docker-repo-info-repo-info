## `openjdk:21-ea-14-bullseye`

```console
$ docker pull openjdk@sha256:cac9aca47c9f1a2fcf1448d4eba566b93137209f302f3db7008e473f4130a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-14-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:cd267bb7ccb8d63ad082a8e6c7d4f89c509c4ef95c5a6713eca7ba339abb7a2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341297783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37952d10ebe344455b4b5c3831f320c57128e86d7f66090cd85eba6ebbe25834`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:42:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 04:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:41:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:41:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 08:41:51 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 08:41:51 GMT
ENV LANG=C.UTF-8
# Mon, 20 Mar 2023 23:53:12 GMT
ENV JAVA_VERSION=21-ea+14
# Mon, 20 Mar 2023 23:53:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 20 Mar 2023 23:53:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167c7feebee855d117e192389484ea8367be1ba84e7ee35f4e5e5663195facbf`  
		Last Modified: Wed, 01 Mar 2023 04:50:15 GMT  
		Size: 5.2 MB (5166586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dfff1f6f3ddd2194ea0775f199572e8b2d75c38713eef0444d6b1fd0ac7604`  
		Last Modified: Wed, 01 Mar 2023 04:50:15 GMT  
		Size: 10.9 MB (10876729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cdcd4942ebc7445d8a70117a83ecbc77dcc5ffc72c4b6f8e24c0c76cfee15d`  
		Last Modified: Wed, 01 Mar 2023 04:50:33 GMT  
		Size: 54.6 MB (54585443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb15dd0f227358da1b0fd4372ab8aff9adfcc4859fbc19c132e15c983aaf188`  
		Last Modified: Wed, 01 Mar 2023 08:46:07 GMT  
		Size: 14.1 MB (14071982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90af9c598da144f4261f920aa8341fa909b0de84d6d09815899bb73ce5cae8`  
		Last Modified: Mon, 20 Mar 2023 23:57:26 GMT  
		Size: 201.6 MB (201551121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-14-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:31a4f65dde35bb95ad8bce76b793b2d166e6b6ae07a67c7bfe6d7352dbfdd65b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339957307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929e39c47f48608a8c7ffb33f995d409f1a7b6d7a71fdb59df7b3074f17ec677`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:11:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:32:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:32:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 23 Mar 2023 09:32:48 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 09:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 09:32:49 GMT
ENV JAVA_VERSION=21-ea+14
# Thu, 23 Mar 2023 09:33:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Mar 2023 09:33:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7971239fe1d69763272ccc0b2527efa95547d37c53630ed0a71db4e00d3ef964`  
		Last Modified: Thu, 23 Mar 2023 07:17:07 GMT  
		Size: 5.2 MB (5152756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c861b53509d61c37240d2f80efb3a351d2f1d7f4f8e8ec2e5004c1d86af89c`  
		Last Modified: Thu, 23 Mar 2023 07:17:07 GMT  
		Size: 10.9 MB (10873620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714880ecc1c021a5f708f4369f91d3c2c53b998a56d563d0a9aa9be2488d794`  
		Last Modified: Thu, 23 Mar 2023 07:17:23 GMT  
		Size: 54.7 MB (54676068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131a790807c32d35d008bb181fd117e5707533f32521e79dc14cbb9702a03c01`  
		Last Modified: Thu, 23 Mar 2023 09:34:39 GMT  
		Size: 15.5 MB (15529075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f842858926b4ca64bef03133ebac8e864016ba66e5c0682c3f7e4745d7559613`  
		Last Modified: Thu, 23 Mar 2023 09:34:49 GMT  
		Size: 200.0 MB (200022689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
