## `openjdk:22-ea-18-bookworm`

```console
$ docker pull openjdk@sha256:d4af77adca247aeb905f51d17b83acfe8c0d6a16c2f57294bb8eae9cbdb54f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-18-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b9de45922f1bc129733351fbd9cc4e0feac40a82669d045aea3a74e5d53c5a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359935628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19d3e94df7f419d7d2cc9e0b95fdfb8b12093f0119421b09f5b01a0e0500486`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:19:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 13:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 13:58:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 12 Oct 2023 13:58:42 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 13:58:42 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 13:58:42 GMT
ENV JAVA_VERSION=22-ea+18
# Thu, 12 Oct 2023 13:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 12 Oct 2023 13:58:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800d84653581fc119cd75cd572fa190d3b813d49221b9e5ee463e3560e2cb342`  
		Last Modified: Thu, 12 Oct 2023 03:29:04 GMT  
		Size: 64.1 MB (64130287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc5a642a701433b4f9473abb5932a8cb41a3b21a8ecb44308c2bd1937f64696`  
		Last Modified: Thu, 12 Oct 2023 14:00:13 GMT  
		Size: 17.0 MB (16951780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0cb5d5b66dadb95d60668ede0fd29aa1a12e0633c84519a5a5f69a54f72abb`  
		Last Modified: Thu, 12 Oct 2023 14:00:32 GMT  
		Size: 205.2 MB (205220078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-18-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4e9917047ae7769b7ee929043c864d38ab37fab6cd1a6e232ad0b15cdb717ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358438062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c85c5c7f83efd96b6b3f2f7a94042a42d16cc9871fe90de3597ed2332adf7b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:45:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:49:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 11 Oct 2023 22:49:44 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:49:44 GMT
ENV LANG=C.UTF-8
# Wed, 11 Oct 2023 22:49:44 GMT
ENV JAVA_VERSION=22-ea+18
# Wed, 11 Oct 2023 22:50:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='07830a4cc21745464a68057e8c441e98d4cd673cd02348e9791d9eafe9f3d0df'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='03432a54970a3005c521d34b44a2438ac28f8fe150bf686e28cea6ea9b2a002e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 11 Oct 2023 22:50:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a653d69b7b96df6835b157d043d7b926f776531e96c9263f4c7dae0033514d`  
		Last Modified: Wed, 11 Oct 2023 19:54:07 GMT  
		Size: 64.0 MB (63994319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de154cc53d72c8ff61e89ed76922abeb9188c1820dc7d0257c0459d92f3bd1a`  
		Last Modified: Wed, 11 Oct 2023 22:51:51 GMT  
		Size: 17.7 MB (17733456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54fd5d289bbb39352812608cc2be9216b957df62239c42958517edd15abf15f`  
		Last Modified: Wed, 11 Oct 2023 22:52:02 GMT  
		Size: 203.5 MB (203509623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
