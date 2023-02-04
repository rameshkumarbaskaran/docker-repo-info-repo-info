## `openjdk:21-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:308fd258d63e5141216084ebaa41d06543abf574dc8b7b8614b50d5b6de3c134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:633dd73726173f5cebb28a04e96f8ddb48b1314dce0b2545b703f2a993cbcfb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232599864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee4b6bdc4d97fa2803e26bcea77ab154f43a2944b34d380e7c6ca164ed782d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 15:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 15:05:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Sat, 04 Feb 2023 15:05:37 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 15:05:37 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 15:05:38 GMT
ENV JAVA_VERSION=21-ea+8
# Sat, 04 Feb 2023 15:05:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/8/GPL/openjdk-21-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ce77e229b2dc811e1231ab1197f851d3234e56cb9e9a26e9f1d7c0294eb09af8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/8/GPL/openjdk-21-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='c52c76023ce2b7202744161d92772f5bc21c6ada643b926c92d5a56b0d1c4664'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Feb 2023 15:05:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e36e14cb842a12521a286b21470cc280fa5ccd5e1fba1f05426e0f5e281e50a`  
		Last Modified: Sat, 04 Feb 2023 15:12:25 GMT  
		Size: 1.6 MB (1582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55d79aeba57e41dc76ef7b3840ce8055cb44a8ac2f62a28076e4fdb9f9feae1`  
		Last Modified: Sat, 04 Feb 2023 15:12:40 GMT  
		Size: 199.6 MB (199620634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4f3879ac2f454849ba1415c68d76e832f717d45891d099692fae82743be3fa68
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229694930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8732a7d164b80b52a2424674de1ee5e797c72b996629e116ba3cf2f4104ee32e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:13:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:13:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Sat, 04 Feb 2023 09:13:05 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 09:13:06 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 09:13:06 GMT
ENV JAVA_VERSION=21-ea+8
# Sat, 04 Feb 2023 09:13:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/8/GPL/openjdk-21-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='ce77e229b2dc811e1231ab1197f851d3234e56cb9e9a26e9f1d7c0294eb09af8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/8/GPL/openjdk-21-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='c52c76023ce2b7202744161d92772f5bc21c6ada643b926c92d5a56b0d1c4664'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Feb 2023 09:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ee2e58ebf78c483b4dba276ed5ef2fd462c4471bf7dfef4daffe6b2595c09`  
		Last Modified: Sat, 04 Feb 2023 09:20:28 GMT  
		Size: 1.6 MB (1566232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507541258b3a7338138b6d9f2aadce6408692513e60d7e964d794fbccd7db923`  
		Last Modified: Sat, 04 Feb 2023 09:20:40 GMT  
		Size: 198.1 MB (198083906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
