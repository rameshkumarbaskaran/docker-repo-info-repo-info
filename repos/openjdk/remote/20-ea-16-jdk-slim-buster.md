## `openjdk:20-ea-16-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:765893771dc011ab8da767fc4a4e4b9db880b27a4acd401780c3fd0860bf717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-16-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:8c22a14291a13df7d44ca5d6155141d45b56473568ccdf04539125a6325a466c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227616045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec81982489d445b89ebf6a26c18ce2849ce85c3f9e842959486459a28606e42`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:02:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 07:02:54 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:02:54 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:34:19 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:34:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:34:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d52f2655b7c485e515b44593c5e3231a817180881565fc043f92bbbb0af57f`  
		Last Modified: Tue, 13 Sep 2022 07:10:47 GMT  
		Size: 3.3 MB (3273424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3a8eecab48f4c2c2053b014c1ce723acdbee8fb8d8831002f1672bb3db6843`  
		Last Modified: Fri, 23 Sep 2022 00:40:34 GMT  
		Size: 197.2 MB (197212069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-16-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ae0cd5d7758638b1a883f049f3371ff3873f25cfbe9f06161b8910f53b2909e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224610158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8340c1e89e7f770e73f7912b3ac85be1b52e944a65c17acb9e62a3ce4a077f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 14:39:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:39:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 14:39:08 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:39:09 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:52:35 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:52:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a215542ec2c1bdf2d159220f3e405dfdf14e3a6a874ba6b84cfd152bba34a4a8`  
		Last Modified: Tue, 13 Sep 2022 14:51:46 GMT  
		Size: 3.1 MB (3126014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d119f5ce7aa01e42929d98587aa6c62c104527066ffa3a321b7396a46ef83bd9`  
		Last Modified: Fri, 23 Sep 2022 01:01:57 GMT  
		Size: 195.6 MB (195579992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
