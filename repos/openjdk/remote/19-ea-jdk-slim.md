## `openjdk:19-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:3222590c4c8c7a4f295d909841fe0334a725bb151063186a4dcf54bb1b0d90fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:2f15c3577ca7f2abd0022ec12265453453bbb8b26673154c1171fb8c052ad617
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229488358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc54ea829fcdd5ab043f229366ca5a0f9b8f15e38e03bd4e6396cb03f6108e5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:55:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 04:55:18 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:55:18 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:30:23 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:30:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:30:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4dc029a36926590a5070a9a58443942497e3b2d48cff116b8b15004d386a40`  
		Last Modified: Thu, 23 Jun 2022 05:07:14 GMT  
		Size: 1.6 MB (1582249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927624db10c04c8f8166248697f27de82283e318766a936781eaf0cf8be46f1e`  
		Last Modified: Tue, 28 Jun 2022 00:43:58 GMT  
		Size: 196.5 MB (196526701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:92e361440ecc1a54fe8de3e6a0418c81d430d16a2d2e084dd2bba4f5fc56b035
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226575508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ff45a8c55e1808105fec2c3af5befc55db330f227db7edad1dcfdcbab2176c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:14:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:16:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 15:16:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:16:53 GMT
ENV LANG=C.UTF-8
# Tue, 28 Jun 2022 00:45:12 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:45:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:45:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b1362d29199a34271f94fac2115a6940998ae50f16fd5de481ae77825beed`  
		Last Modified: Thu, 23 Jun 2022 15:36:55 GMT  
		Size: 1.4 MB (1361261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d636fedf06d53af31664274906b2837f2b5c506d79905fca5c434843cde1c329`  
		Last Modified: Tue, 28 Jun 2022 01:06:33 GMT  
		Size: 195.1 MB (195148527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
