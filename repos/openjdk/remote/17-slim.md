## `openjdk:17-slim`

```console
$ docker pull openjdk@sha256:e4f89e56fb3039159d07681c648244d208bcad79c768740bf5048b7b6ca2d632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:8e602e7facc8b118d1b69d8453887814418336a792de1f7c6c8185e369f6a3fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216441701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acad165d4e7191578456e9a37e68c3f9fc5972d518b4644f30b65f4bd02acdb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:10:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:10:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 09 Feb 2021 17:10:18 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 17:10:18 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 23:42:25 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:42:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='0ed9bba55c54c5949c2f9116ef5bf936b3c55ec39531f317492bdca43a1c1fa8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='1922fd3e81bec1b42c8660d990ccc7fdb36210792f59cbe307691b7d3fa4c967'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Feb 2021 23:42:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91c0c19c84860aaa974864243509770a5b009f3a88b4a228010a9ade71ac968`  
		Last Modified: Tue, 09 Feb 2021 17:20:14 GMT  
		Size: 3.3 MB (3267910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04325c7a262b3b8aa1b4b60eca64e102c995c38e5c832f9c02d915474cf0e265`  
		Last Modified: Fri, 12 Feb 2021 23:53:51 GMT  
		Size: 186.1 MB (186078649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c62dc9a3a54237f23e6e963623cccbcfa711d5b53fc532075f6d41e71040dd87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209438223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa0670448f58548c7db3aef511be4fe38a42249da5fa011e2509943a5cb539e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 07:12:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 09 Feb 2021 07:12:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 07:12:11 GMT
ENV LANG=C.UTF-8
# Fri, 12 Feb 2021 23:45:00 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:45:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='0ed9bba55c54c5949c2f9116ef5bf936b3c55ec39531f317492bdca43a1c1fa8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='1922fd3e81bec1b42c8660d990ccc7fdb36210792f59cbe307691b7d3fa4c967'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Feb 2021 23:45:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96062c0c15f683e4abb09efb938dfd7ff23002f72a375c75492d44bde3a6c26f`  
		Last Modified: Tue, 09 Feb 2021 07:22:32 GMT  
		Size: 3.1 MB (3118711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d929616f33742e4aa1eb73be0ff15274d10073a3b011923278dfbf2de6fd7054`  
		Last Modified: Fri, 12 Feb 2021 23:52:56 GMT  
		Size: 180.5 MB (180468063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
