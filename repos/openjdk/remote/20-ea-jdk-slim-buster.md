## `openjdk:20-ea-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:dda2e282c7589f9f02af482b005ada4a71e104705eea97dee10dcfc2862bb55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:8ba7f5a9213123b778483e2edd7080023c72dd3ec2f06cb9ebda43546d7cb2b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228750107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85e72f4ce480bcfc36de804f4dd6ae6370bbe5ce43ccf5976e3edfad2f75ed`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:38:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 13:38:02 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 13:38:02 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 21:31:43 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:31:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 21:31:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa50eb78de93845177329bacaba9767cb996220ea8583a14fd4c3e67118b1b99`  
		Last Modified: Tue, 15 Nov 2022 13:43:24 GMT  
		Size: 3.3 MB (3275918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d174f9224acb9e511da719e1d1778c7fd73d3b75ae8169e357db107c9df1b50`  
		Last Modified: Wed, 30 Nov 2022 21:37:34 GMT  
		Size: 198.3 MB (198333857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7d6823aa176db82252191199f3b0af5f26662ab12385ff9ba1e635f1c08aa3de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225916788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ef39f8ba292e95479cdc667480446357afae5fca368dd12783a8773245e121`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:34 GMT
ADD file:aaead8e4dd08d41c8d1692bbe76b673119289836428e1f713ca550c2468711ac in / 
# Tue, 15 Nov 2022 01:41:34 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:00:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:00:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 15 Nov 2022 07:00:05 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 07:00:05 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 20:55:40 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 20:55:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 20:56:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc457132e077d684a6cecad3331c35341d814c5d364f3cf24d698a6d8e76d0e7`  
		Last Modified: Tue, 15 Nov 2022 01:45:13 GMT  
		Size: 25.9 MB (25914924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff2698465dffb82732503151fe00374c897aecc02405b716d6a7d3225d9a1e6`  
		Last Modified: Tue, 15 Nov 2022 07:05:37 GMT  
		Size: 3.1 MB (3129446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf18b91ea86c6cffda036fafaf146b0e2ca6ab76c60eb9c1c44b31117ce81864`  
		Last Modified: Wed, 30 Nov 2022 21:01:47 GMT  
		Size: 196.9 MB (196872418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
