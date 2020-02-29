## `openjdk:15-ea-12-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:ab0865ed6d3ae6e07cbe3f3ce2e89f43bcba07be0e4de5365e620b6c1610e369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-12-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:c0538f87c4c50df6142a1c5eb1b2a3469a4d521f3f559ffae8cef9ddac47abaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229061063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c703fd9c545e81fc95eaf8130d9ec12c30e3b9ed60b33ae45159f59db9ea8a66`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:15:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 26 Feb 2020 20:15:16 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:15:17 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 29 Feb 2020 03:19:20 GMT
ENV JAVA_VERSION=15-ea+12
# Sat, 29 Feb 2020 03:19:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/12/GPL/openjdk-15-ea+12_linux-x64_bin.tar.gz
# Sat, 29 Feb 2020 03:19:20 GMT
ENV JAVA_SHA256=ff430463b92de38a39224ada330253f9d6381621d99a0822a40e6c6b81d68bb1
# Sat, 29 Feb 2020 03:19:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 29 Feb 2020 03:19:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ef4ede9eafa0c8417206226414d724d42c5b8368c21dbb197bbcc15b62107`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537467111761672cd7f1b4071ebd0993be8e5302d601ca9167fdc4aa58c469f`  
		Last Modified: Sat, 29 Feb 2020 03:24:38 GMT  
		Size: 198.7 MB (198719937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
