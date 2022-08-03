## `tomcat:9-jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:de3496f3c8819781a8768b1de092f41c326fb569dd5808eaddcda6cbb1c77b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:5eabd15e8f7e84ad3eacf33a9327da906e6be971cb65575a4904104a5d72ddfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132284663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681dd345665fcc025e38c2e1481fc0af98f00f7f39ab9cbb4b8cdb8e4f1cf2d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:20 GMT
ADD file:d738977543f4afc4c3040c6fca3e3f15388ec3b7263a29a6aa83f9a4bf05fed1 in / 
# Tue, 12 Jul 2022 01:20:21 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:49:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:49:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 15:47:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 15:47:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 15:47:51 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 15:47:51 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 15:47:51 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:28:34 GMT
ENV JAVA_VERSION=11.0.16
# Mon, 25 Jul 2022 20:28:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Jul 2022 23:10:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 23:10:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 23:10:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 23:10:21 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 23:10:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:10:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:16:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Jul 2022 23:16:56 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Jul 2022 23:16:56 GMT
ENV TOMCAT_VERSION=9.0.65
# Mon, 25 Jul 2022 23:16:56 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Mon, 25 Jul 2022 23:16:57 GMT
COPY dir:9df3f7591ebcd4b2a6e097ec259e64aaf7cc5cec7623c941cf73b2961bc7cfe6 in /usr/local/tomcat 
# Mon, 25 Jul 2022 23:17:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Jul 2022 23:17:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Jul 2022 23:17:02 GMT
EXPOSE 8080
# Mon, 25 Jul 2022 23:17:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80b89a2b88b24e7be7c8038e2cbff99ad4fd2f07ad914da4bab80dabaadf8a99`  
		Last Modified: Tue, 12 Jul 2022 01:24:55 GMT  
		Size: 50.4 MB (50440555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0405f798f5b335d83b02371187f3be0ce2092aa0c6b6178ff11290ee6a14c9`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 7.9 MB (7856888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab80b2b0494ab26b41941fb73a028292e2e5d2070c56b3488e890eda20e04641`  
		Last Modified: Tue, 12 Jul 2022 02:56:14 GMT  
		Size: 10.0 MB (9998095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ab3530dc99d3cf181a3d34282de25b735acb04b544360d89d0763cdb43bb6d`  
		Last Modified: Tue, 12 Jul 2022 16:00:30 GMT  
		Size: 5.5 MB (5532631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23384506b8e1fd81247edb796013ffa416a105a20801ffa6b802f538ff38ad79`  
		Last Modified: Tue, 12 Jul 2022 16:00:29 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a19206765c41a469962459009310b8b896402d6729bdee8166ad1d4dceff2`  
		Last Modified: Mon, 25 Jul 2022 20:43:46 GMT  
		Size: 45.8 MB (45773012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77f0be36f178ee161ffc24ac033a69f10b9ef899d2ee772e94e271aad383c3d`  
		Last Modified: Mon, 25 Jul 2022 23:38:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc97c81791a2bed7124916a2d65fb660f98284145dfe58e06b5a0f7c715b708`  
		Last Modified: Mon, 25 Jul 2022 23:44:58 GMT  
		Size: 12.2 MB (12222011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10871f37b929d00b9ced6b75c563f789e06e0d7f18fbb9ab70a7b8f96fcfda`  
		Last Modified: Mon, 25 Jul 2022 23:44:57 GMT  
		Size: 461.0 KB (460957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b6b18abcfc830202fc8644e31bcaca92179193bc26729caef394ec240d42c`  
		Last Modified: Mon, 25 Jul 2022 23:44:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:2be54dd9b24764d817e2552f10737986c4c2daab679762a6fecef101545ef105
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129750596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45c8f642417b9e0b400eb0c0933f1f7dc8b226bc32e6e1d32cdfabc41b9189`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:25:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 02 Aug 2022 04:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:50:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 02 Aug 2022 04:50:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 02 Aug 2022 04:50:49 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:50:50 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 04:50:51 GMT
ENV JAVA_VERSION=11.0.16
# Tue, 02 Aug 2022 04:50:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 03 Aug 2022 01:53:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:53:53 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:53:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:53:55 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:53:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:53:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:12:08 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 03 Aug 2022 02:12:08 GMT
ENV TOMCAT_MAJOR=9
# Wed, 03 Aug 2022 02:12:09 GMT
ENV TOMCAT_VERSION=9.0.65
# Wed, 03 Aug 2022 02:12:10 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Wed, 03 Aug 2022 02:12:12 GMT
COPY dir:9f1f64b42e1b033aaacdb8ac6741c5671ddf94b0a6366701b0153ad50eec1605 in /usr/local/tomcat 
# Wed, 03 Aug 2022 02:12:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:12:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 02:12:18 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 02:12:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ca5ccee8fca6610f14b5ed35ac33bb5f545532b6583e1461037a083c3d87b`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 7.7 MB (7719992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32de8e1f96ccb825d3be85704be7218044a19ff05ea1eea0222e8c942fbf6f8f`  
		Last Modified: Tue, 02 Aug 2022 01:45:50 GMT  
		Size: 9.8 MB (9768645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55122ede21178db0d7b4344f167dcbda7d103c4b77dfa15b37411fc005e009c8`  
		Last Modified: Tue, 02 Aug 2022 05:17:16 GMT  
		Size: 5.5 MB (5506788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da056785d1770185dc9c78ca7d278ef3051b0651306f888fc1f8d0129dbef6`  
		Last Modified: Tue, 02 Aug 2022 05:17:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc66ba0403fd0d18ced4a3b1b068ff3a161d6acb9b8e4327f007e1e448cb7b8`  
		Last Modified: Tue, 02 Aug 2022 05:17:22 GMT  
		Size: 45.1 MB (45073109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6340891dfc47c1932872d887ecd85aa353c7496e84cc74ccbdc2107fc2f12e44`  
		Last Modified: Wed, 03 Aug 2022 03:03:23 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7319e66fe5441995497232a6d2577dbd75e7ac0f010851649d99e49951b24e6f`  
		Last Modified: Wed, 03 Aug 2022 03:15:58 GMT  
		Size: 12.2 MB (12234407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f888f3622cd53033d276cd13be5aa202486e2c2d16c492511ed5d64d34d61c`  
		Last Modified: Wed, 03 Aug 2022 03:15:57 GMT  
		Size: 218.3 KB (218251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
