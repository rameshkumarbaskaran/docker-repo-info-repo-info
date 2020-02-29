## `openjdk:15-ea-12-buster`

```console
$ docker pull openjdk@sha256:9974c012f09bce366068791b7f122f99df78bd23db4ce401d0a562dae4d90fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-12-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:f32607b83742413d25ce073d2a5503157bd10ab42c3507521d4ab998fa1894b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332356132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0ce54c9b79dac3b029d01a9ceb4bcd5bbf494016f0b143ddc2809fcd47bce4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:14:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:14:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:14:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 26 Feb 2020 20:14:50 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:14:51 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 29 Feb 2020 03:18:51 GMT
ENV JAVA_VERSION=15-ea+12
# Sat, 29 Feb 2020 03:18:51 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/12/GPL/openjdk-15-ea+12_linux-x64_bin.tar.gz
# Sat, 29 Feb 2020 03:18:52 GMT
ENV JAVA_SHA256=ff430463b92de38a39224ada330253f9d6381621d99a0822a40e6c6b81d68bb1
# Sat, 29 Feb 2020 03:19:11 GMT
RUN set -eux; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 29 Feb 2020 03:19:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6ff6826f6ff050dac5197a43ec030d0203c4d15e003fd9b61e48635802002`  
		Last Modified: Wed, 26 Feb 2020 20:23:28 GMT  
		Size: 13.9 MB (13920236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748cda98e796f05c106effee9634f06c487a520195d626ec8879cf850e87812f`  
		Last Modified: Wed, 26 Feb 2020 20:23:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1f2c81ec56b2b1a327eb40fd5b0da450aa5e2d9c5f6e827b26d2bc41c2d192`  
		Last Modified: Sat, 29 Feb 2020 03:24:04 GMT  
		Size: 198.5 MB (198454753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
