## `openjdk:20-ea-3-slim-buster`

```console
$ docker pull openjdk@sha256:5adc8946cba6ba8343686b24f39aa1c4328ab0b6baa418ee60ceb0ca1294cf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-3-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:0310e58b4c5256a2bbcf6fe2e1541cb56159e53ef50f5729fc02d06c2d72ea2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227947803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e656cf95a636bd126615eb582627bb8112f36a79e044ca6649ee63d012f7cf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:54:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Thu, 23 Jun 2022 04:54:40 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:54:40 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:28:49 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:29:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='8f930cbbf2c85c0cfe87eef8646d1e038fe51d19132613e868e96118b1e0f8d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7b270b059fe08487492d38760e0e821b3a7be20864205d7ab0b5e5206109bda'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:29:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fab7e4cce528d853465a0775f91b15783a53a42b906820fb3f70f0f731667`  
		Last Modified: Thu, 23 Jun 2022 05:08:38 GMT  
		Size: 3.3 MB (3273402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe5aeb8b162dbd03b00b162ffbce36d7e8a9b3a2e795d5bca486dc0c302294c`  
		Last Modified: Tue, 28 Jun 2022 00:41:26 GMT  
		Size: 197.5 MB (197534358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:46e3aeb21a976abdf21f07d3f4e97d4c10e5e1cdca0ac38c3d47e2d61dd99002
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225199771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9acd4cee825f3ef5e5016b28af9dfe18eecbddd92f1a0fe0b49c4677c0a305`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:15:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:15:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Thu, 23 Jun 2022 15:15:48 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:15:49 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:43:38 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:43:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='8f930cbbf2c85c0cfe87eef8646d1e038fe51d19132613e868e96118b1e0f8d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7b270b059fe08487492d38760e0e821b3a7be20864205d7ab0b5e5206109bda'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:43:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f637b7908849640db5a85b9e9242a3aae4e71783948b20c9f1e0bab2cdb5039`  
		Last Modified: Thu, 23 Jun 2022 15:38:45 GMT  
		Size: 3.1 MB (3125979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9307c6d0f11b04da93342c5204db63529f0fdc9a57aa3512aca3cd5aa0edc13f`  
		Last Modified: Tue, 28 Jun 2022 01:03:20 GMT  
		Size: 196.2 MB (196159763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
