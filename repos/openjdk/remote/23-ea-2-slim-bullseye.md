## `openjdk:23-ea-2-slim-bullseye`

```console
$ docker pull openjdk@sha256:a22013cfb3db81e247dfd9d7016caaa7e5b6cf5fd3127500b70f1030627ed1a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-2-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8b12cc1637ea3ce6fde727be0258c205c30b99a8c15804ce69479613687e35c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235915160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564be4883e0ce58a7e7cb7a1b6accfbbfb1432d6a972e7a8e1a8fec50ccd4864`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fa47b82816d3e25d4334e72298655b11ec4c22766cc5812164bf205cc5115`  
		Last Modified: Sat, 16 Dec 2023 01:51:56 GMT  
		Size: 1.4 MB (1378184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48830290dd879553ef6a0e429516954556b8972323880a6f94400a6b04f5481`  
		Last Modified: Sat, 16 Dec 2023 01:52:00 GMT  
		Size: 203.1 MB (203119152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ae5f8679757eaf442c0d0bbe43e910af3ecc882a879e3dc74aca2c9257c0239e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fe4d688c1f8b36d0d7f11111be2d9ee6e3dda5951df537f684db3e93bb3ad7`

```dockerfile
```

-	Layers:
	-	`sha256:47b588ee057c8d9c10dee60db06bc39a3114b77eb0da8230a63e28311cf82ce8`  
		Last Modified: Sat, 16 Dec 2023 01:51:56 GMT  
		Size: 2.2 MB (2190179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf032172ccbbbecf3c466083b485ab40536f25e5e58c905332408bb33758bcc`  
		Last Modified: Sat, 16 Dec 2023 01:51:56 GMT  
		Size: 17.5 KB (17459 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c22aad714419bd1c702f8ddb1ab2f1e9fa9eb1bc1bb14772fe57b699180a16a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232452268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3497567519e7c4dc4aaf41835a2f59c341fd71e2705069025839074fe7f9175`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:53:43 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2023 19:53:43 GMT
ENV JAVA_VERSION=23-ea+2
# Fri, 15 Dec 2023 19:53:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='c10168b0639ae5a316fb20444202e82fabe5908be7241f1cd42e34ed9d1eca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/2/GPL/openjdk-23-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='84b416aba4f3578138dd0d27f570dbaee9123528c4d45d13a338278c3d7136c1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Dec 2023 19:53:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b44bd09e3f229b14cf1e2425e653e0398d79b3eb82f0a7052b42ecf74ba27`  
		Last Modified: Fri, 15 Dec 2023 23:26:07 GMT  
		Size: 1.4 MB (1362043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7a290530a7f515be0ba172c0a371d7ce95c503846e65ef098438e1c513e798`  
		Last Modified: Sat, 16 Dec 2023 18:38:14 GMT  
		Size: 201.0 MB (201026102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-2-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d23a908130ab5c3f2dc969f87e4d1cddffc6c5173023d6564e3a84c970d2565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49172eba36d8879a3fe270a194df418c979aee2bca8f7bd86c7d9fd873c21cd2`

```dockerfile
```

-	Layers:
	-	`sha256:191bf3f8acb1a13de05265b41246b6faf6ddda9a11679b30b2430729c4564fab`  
		Last Modified: Sat, 16 Dec 2023 18:38:09 GMT  
		Size: 2.2 MB (2189543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e2c55b73a73ce74d9baee7962bd82beb84e9f1b56960dcd2b19ec840d58313`  
		Last Modified: Sat, 16 Dec 2023 18:38:09 GMT  
		Size: 17.3 KB (17306 bytes)  
		MIME: application/vnd.in-toto+json
