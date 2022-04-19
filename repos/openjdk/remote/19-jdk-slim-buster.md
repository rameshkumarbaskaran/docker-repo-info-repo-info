## `openjdk:19-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:0059fd5c8debf620e757e319d69e35992b020fd25700bc605b4cb7abf9462598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:e832504531233c2e323a971a4408cd5784d188af9e6c40d10b51cf51d01c7cf9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225346013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c83c72ecc61a570f5a571793dfc173d05b61467c9d111975375d1a58d7598`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:52:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 00:52:53 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:52:54 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 02:54:38 GMT
ENV JAVA_VERSION=19-ea+18
# Tue, 19 Apr 2022 02:54:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='c79b13e466464b0054cad0301cf53bcd4b083d591f5fe61e932f39d34063f93b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='eeec6bd83fea107d1c6de91d7eb2936b7829e8315e81458beb4e401a9f51f006'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 19 Apr 2022 02:54:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a93b586a56127b277f2e371624af9ed70508966a2ca124e827d47b841391445`  
		Last Modified: Tue, 29 Mar 2022 01:05:57 GMT  
		Size: 3.3 MB (3273249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07161d1958afdfcbb399a7d8887dae6dfce23be213874c46e6016deb0ceab3dc`  
		Last Modified: Tue, 19 Apr 2022 03:03:58 GMT  
		Size: 194.9 MB (194920794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b9fbbd2796be55affa2b341857745707fc79645010445bd9dec888862a6eb208
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222606908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fff147ba0a746665b3e21aa337a6c04cc58eff99d407901d0996ad29c4f86eb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:19:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:19:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 01:19:12 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:19:13 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 03:33:01 GMT
ENV JAVA_VERSION=19-ea+18
# Tue, 19 Apr 2022 03:33:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='c79b13e466464b0054cad0301cf53bcd4b083d591f5fe61e932f39d34063f93b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='eeec6bd83fea107d1c6de91d7eb2936b7829e8315e81458beb4e401a9f51f006'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 19 Apr 2022 03:33:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b464c2cba1daef8144ee6cab94db7ab3e6c663c917369550b9b29d8cac37b`  
		Last Modified: Tue, 29 Mar 2022 01:39:33 GMT  
		Size: 3.1 MB (3125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab75d549fde83af255acd8df1fd5a14d9004f0ceeaf87d5e97519d7c115abe7`  
		Last Modified: Tue, 19 Apr 2022 03:49:14 GMT  
		Size: 193.6 MB (193561346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
