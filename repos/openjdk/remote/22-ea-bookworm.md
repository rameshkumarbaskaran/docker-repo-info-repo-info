## `openjdk:22-ea-bookworm`

```console
$ docker pull openjdk@sha256:3e9acd13ea69193731515822029ad032443060de13953e0952b7bc4a99a9b16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:2e3eabcf71e01fcb19d5cc5cea9417ea7e9eb18c21ce0f85200128f6bfaf4606
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359837770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37ab592f70be6228985718a5ae42386855a9a8248e5bef8321bb27640078432`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:39 GMT
ADD file:8415eb847ca46ed1aa1695965af86f1a0f09e8859a7b3c07b2f719404b665102 in / 
# Thu, 07 Sep 2023 00:20:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:56:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:01:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:01:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 05:01:20 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 05:01:20 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2023 22:40:50 GMT
ENV JAVA_VERSION=22-ea+15
# Thu, 14 Sep 2023 22:41:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 14 Sep 2023 22:41:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:012c0b3e998c1a0c0bedcf712eaaafb188580529dd026a04aa1ce13fdb39e42b`  
		Last Modified: Thu, 07 Sep 2023 00:24:59 GMT  
		Size: 49.6 MB (49557216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00046d1e755ea94fa55a700ca9a10597e4fac7c47be19d970a359b0267a51fbf`  
		Last Modified: Thu, 07 Sep 2023 03:04:41 GMT  
		Size: 24.0 MB (24030451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f13f5a53d118643c1f1ff294867c09f224d00edca21f56caa71c2321f8ca004`  
		Last Modified: Thu, 07 Sep 2023 03:05:02 GMT  
		Size: 64.1 MB (64112250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f59595cfcba1a8417020ad73670346a35f80d9b71835b26df02e0791a1d939`  
		Last Modified: Thu, 07 Sep 2023 05:04:54 GMT  
		Size: 16.9 MB (16947200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2bce13dfd4fca48031126a8f1cce6a7aa6e17bcd09b61e4cfd9672e1843472`  
		Last Modified: Thu, 14 Sep 2023 22:44:56 GMT  
		Size: 205.2 MB (205190653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc0097f981394367e2133951f4cceda3c6f5fe9cb16a1b33a185b2557f1b89a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358386255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98b477e14dc3726bdd18c9504962e4ec0440758a447c93c62020cd2bf23f5e7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:04 GMT
ADD file:7a0adbde6e967e2bcaafa69f04fabdec993025645c8d0d51acc991a31b404eed in / 
# Wed, 20 Sep 2023 02:44:05 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:23:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:57:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:57:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:57:06 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:57:07 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:57:07 GMT
ENV JAVA_VERSION=22-ea+15
# Wed, 20 Sep 2023 17:57:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='86b3ab4e12d302e039dc65fc4700ffd572d072d6d822c983a6d74b569b9186ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/15/GPL/openjdk-22-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='6c680f4dc89b64fbe5cfcf7b12f232e31737112a8801ac594416c21e4b04c892'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Sep 2023 17:57:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:796cc43785ac3cd0081892bd48e545a0615415265b60c794fdf81ac95b034213`  
		Last Modified: Wed, 20 Sep 2023 02:47:15 GMT  
		Size: 49.6 MB (49591881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91290b4a059080b4227746016e1a8f32a290271d8712b213834e9296a38bfea9`  
		Last Modified: Wed, 20 Sep 2023 09:32:11 GMT  
		Size: 23.6 MB (23570121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8d278f2f731ceff5e8c6f5010bef6b1bf18c555a80663ca612e3e42d013779`  
		Last Modified: Wed, 20 Sep 2023 09:32:29 GMT  
		Size: 64.0 MB (63988033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65777dfc089a71320ef895fc4c948c19e71db4805bad312b8d4909f6e631f406`  
		Last Modified: Wed, 20 Sep 2023 18:00:30 GMT  
		Size: 17.7 MB (17729145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f1d0b842792489c83837faf328492f8e581d0d54c9d2dc9c79565cd989e227`  
		Last Modified: Wed, 20 Sep 2023 18:00:40 GMT  
		Size: 203.5 MB (203507075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
