## `openjdk:19-slim-buster`

```console
$ docker pull openjdk@sha256:8712655c54ea8fee829955ea0aa950eef2780cb55d22d52ab34254c45d3d592b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:2d60b78e5207b495066524c01887a47063037c056fbeb9c2c650f834051da05f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220305652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25de664f30677635ce3d45d90a2a78de538c357a6c35046200350046dd4135a2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:30:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Dec 2021 01:42:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 14 Dec 2021 01:42:38 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Dec 2021 01:42:38 GMT
ENV LANG=C.UTF-8
# Sat, 18 Dec 2021 04:09:23 GMT
ENV JAVA_VERSION=19-ea+2
# Sat, 18 Dec 2021 04:09:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='66b20dfbd8d0c7ce80d61fef923fb91721244f6194b191b90f130a3380be459d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='4e19a1ffdaf1f9890ff45d8ff7264b4c4cc968714466abdfe2b47229aa2e4e2f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 18 Dec 2021 04:09:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169731f46e61fb8aef8f7ed809068db98d3feb2466197e9680dbbdbb80d8ed90`  
		Last Modified: Thu, 02 Dec 2021 11:48:59 GMT  
		Size: 3.3 MB (3269625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f3edc19d189e197a6f63620e196a0e555be3c0353ddc6d54e9201b7f3bd871`  
		Last Modified: Sat, 18 Dec 2021 04:21:47 GMT  
		Size: 189.9 MB (189882298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a14aeb9aaa7d71d8d27a932d00ec991e343335c89792e65a5c2c5115ebc921c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217642225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e3bf8115d14b9c8deafff51d0b8aeeea95674e2fb866ec7f99b08b1042ad5c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:54:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 21 Dec 2021 02:54:45 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:54:46 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:54:47 GMT
ENV JAVA_VERSION=19-ea+2
# Tue, 21 Dec 2021 02:55:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='66b20dfbd8d0c7ce80d61fef923fb91721244f6194b191b90f130a3380be459d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='4e19a1ffdaf1f9890ff45d8ff7264b4c4cc968714466abdfe2b47229aa2e4e2f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:55:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c74145b5f237a66007b7c0d55f2ffe3d54c07bf5e09c19bebd4ec94b00005e`  
		Last Modified: Tue, 21 Dec 2021 03:17:41 GMT  
		Size: 3.1 MB (3118854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d482c386d5b2bbcd4a0a46a6eb74b90e39f4f30fcc0af27066ba00c4681f8e58`  
		Last Modified: Tue, 21 Dec 2021 03:17:58 GMT  
		Size: 188.6 MB (188600222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
