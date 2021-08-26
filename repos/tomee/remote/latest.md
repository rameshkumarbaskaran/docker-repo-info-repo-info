## `tomee:latest`

```console
$ docker pull tomee@sha256:7f672477d2f91eaec4d7097839b3e5b65f43f94f23f5872f32d766856be43206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:latest` - linux; amd64

```console
$ docker pull tomee@sha256:53f72cfc3a2b9c1663b5f088526e7b8da20f6a7a381d3d37230a377c02fc4310
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170452547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2feb76ca2772dee00fe99585f8c10d599d86fc09af2046f4bc8e4d4934b8af2a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:26 GMT
ADD file:a528c112b566e7f129178dadedfa421b0c5b870997c4628327967850e54b915c in / 
# Tue, 17 Aug 2021 01:23:26 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:18:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:19:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 26 Aug 2021 00:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 00:37:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 26 Aug 2021 00:37:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 26 Aug 2021 00:37:05 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 00:37:05 GMT
ENV LANG=C.UTF-8
# Thu, 26 Aug 2021 00:37:05 GMT
ENV JAVA_VERSION=11.0.12
# Thu, 26 Aug 2021 00:37:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 26 Aug 2021 04:14:02 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 04:14:02 GMT
RUN mkdir -p /usr/local/tomee
# Thu, 26 Aug 2021 04:14:03 GMT
WORKDIR /usr/local/tomee
# Thu, 26 Aug 2021 04:14:03 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97     C92604B0DEC5C62CFF5801E73D4683C24EDC64D1     294A395FFDC9FCF25A7E2BFDCF6FC99C2CC77782
# Thu, 26 Aug 2021 04:14:16 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||         gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;     done
# Thu, 26 Aug 2021 04:14:17 GMT
ENV TOMEE_VER=8.0.6
# Thu, 26 Aug 2021 04:14:49 GMT
ENV TOMEE_BUILD=webprofile
# Thu, 26 Aug 2021 04:14:54 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee 	&& rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER} 	&& rm bin/*.bat 	&& rm bin/*.exe 	&& rm tomee.tar.gz*
# Thu, 26 Aug 2021 04:14:55 GMT
EXPOSE 8080
# Thu, 26 Aug 2021 04:14:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4c25b3090c2685271afcffc2a4db73f15ab11a0124bfcde6085c934a4e6f4a51`  
		Last Modified: Tue, 17 Aug 2021 01:29:06 GMT  
		Size: 54.9 MB (54915004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acf565088aae3ef2159885f29853bce88eb16082b0c98fcacd08fc9008c84b9`  
		Last Modified: Tue, 17 Aug 2021 09:29:09 GMT  
		Size: 5.2 MB (5153283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95c0dd0dc0d3d367cc5b85f86d8881afb658e8eb341a86daf3835c2f14159ac`  
		Last Modified: Tue, 17 Aug 2021 09:29:10 GMT  
		Size: 10.9 MB (10871829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25bb2549fe99d4b2f8a93017af8beec80c7aa60bb814b7bc3dcabb511d88c75`  
		Last Modified: Thu, 26 Aug 2021 00:48:56 GMT  
		Size: 5.7 MB (5653933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f590a1c98e3e508a42e09147a7f5d417255a53a9d266bc7714f68c1e20b9d5c`  
		Last Modified: Thu, 26 Aug 2021 00:48:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b799f9bfa86ea1695d7ff98f19c78ab740c116b5eebca5f56d12db737843165b`  
		Last Modified: Thu, 26 Aug 2021 00:49:02 GMT  
		Size: 46.9 MB (46853927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ae1718842735c694159b1ee37f959c30b6283ceee5f56be8767095d8de186`  
		Last Modified: Thu, 26 Aug 2021 04:18:10 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7b45523691e8c51d3c46b325b192c111c6c24d102f6845e28cc7cbc9adfd85`  
		Last Modified: Thu, 26 Aug 2021 04:18:10 GMT  
		Size: 21.0 KB (21040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51afe103d8cc93bd6ec3b47f06f7ab36a053811e3d4473b90b95cdeccb8ef18`  
		Last Modified: Thu, 26 Aug 2021 04:18:58 GMT  
		Size: 47.0 MB (46983148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
