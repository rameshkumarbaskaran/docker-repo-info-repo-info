## `tomcat:9-jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:5230f8f1ebe733493f3619ab88495087a16d2724a6b638c1d2be3f36a91ecd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:035e54ef354469327392bbfa0e9271fd0fb43d5c7d3a16bfcfd556ea701d8a47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133713038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76954e66047570d1c58d5cb053bde953e0c4ebd3c341160f4499a410731f91e2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:59:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Jun 2022 04:59:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 04:59:49 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:59:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:59:50 GMT
ENV JAVA_VERSION=11.0.15
# Thu, 23 Jun 2022 04:59:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 23 Jun 2022 22:39:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:39:21 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:39:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:39:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:39:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:39:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:48:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 23 Jun 2022 22:48:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 23 Jun 2022 22:48:28 GMT
ENV TOMCAT_VERSION=9.0.64
# Thu, 23 Jun 2022 22:48:28 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Thu, 23 Jun 2022 22:48:28 GMT
COPY dir:c19733661a885c14442b3baa5c1eb4b5f54027a18405c357ec0d11eb7ee5f400 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:48:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:48:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:48:34 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:48:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9250eef0f01e9551fef0eaea0e242501ab3d09c6a7e72c66f5083b55a6daa18d`  
		Last Modified: Thu, 23 Jun 2022 05:19:07 GMT  
		Size: 5.5 MB (5532608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3969d4e96be0fe658c00f6470d43bed2ac921be1aa78ec4291152107219803d6`  
		Last Modified: Thu, 23 Jun 2022 05:19:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b052dd935874d534abf3e130c99d2be324d345c7c07b3fa578317369fc087`  
		Last Modified: Thu, 23 Jun 2022 05:19:13 GMT  
		Size: 47.2 MB (47206773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8086d979640f420396f5ac5c0a2533547a54ee79dfd699c69179369e4ec845`  
		Last Modified: Thu, 23 Jun 2022 23:07:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ece947b0187bd3b8385b5ac416a464309ec478f2f255e2175ab58ba2f51c25`  
		Last Modified: Thu, 23 Jun 2022 23:17:09 GMT  
		Size: 12.2 MB (12217511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60fb192a5a6c268fea91df7cbae14cfbcace56075a07a856bc7ea9c4e223eb1`  
		Last Modified: Thu, 23 Jun 2022 23:17:08 GMT  
		Size: 461.0 KB (460962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9329e431ba258cb2d4786a1a0e26bcab4ccde305fa8a91561039dd5643698ce`  
		Last Modified: Thu, 23 Jun 2022 23:17:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9d9bd7370d57675f52b11da1708d4c05c5c6c6abccaa5c1889fd08cb8fd56efd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131179146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff47eb0b869ef00c3c526b6b8c8f09adf70ba345d306c42b1cb075a355001c6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:54 GMT
ADD file:a5e3c0ffa9f9754a6d77fafd8288e699a70f7f6ff7c5912a065f1c69f1393e99 in / 
# Thu, 23 Jun 2022 00:40:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:12:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:23:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Jun 2022 15:23:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:23:49 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:23:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:23:51 GMT
ENV JAVA_VERSION=11.0.15
# Thu, 23 Jun 2022 15:23:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 24 Jun 2022 02:33:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 24 Jun 2022 02:33:30 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 02:33:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 24 Jun 2022 02:33:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 24 Jun 2022 02:33:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:33:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:47:57 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 24 Jun 2022 02:47:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 24 Jun 2022 02:47:59 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 24 Jun 2022 02:48:00 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 24 Jun 2022 02:48:02 GMT
COPY dir:32518fbf54a10bbc8a5ae870af55879cb5b7fb777e9b49aa28acc270151c6874 in /usr/local/tomcat 
# Fri, 24 Jun 2022 02:48:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 02:48:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 24 Jun 2022 02:48:08 GMT
EXPOSE 8080
# Fri, 24 Jun 2022 02:48:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8d6f1451981514e25c21542f5c7ee9bb90052b8856b484ce47294cbf1fd5a234`  
		Last Modified: Thu, 23 Jun 2022 00:47:46 GMT  
		Size: 49.2 MB (49229092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc9fb4baf6e7f2e6ee18ed689c8ee1171c6751c8bbd317d580a193da27a5f1`  
		Last Modified: Thu, 23 Jun 2022 01:23:09 GMT  
		Size: 7.7 MB (7719858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620d55693ed5943ab298346d9ccafefdd6d6f33994e6820a857737df89b65f3a`  
		Last Modified: Thu, 23 Jun 2022 01:23:08 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1526a71e18ef448919ed36a09acd6ab5e51909b4d8ecad3afd47d17881eeaae1`  
		Last Modified: Thu, 23 Jun 2022 15:51:42 GMT  
		Size: 5.5 MB (5506784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960a30d3eda4127834b5316c92a308eba32b1c4d6fd86c4ab6cc574ff7642308`  
		Last Modified: Thu, 23 Jun 2022 15:51:42 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb75fae09bd0e9badb8eed268f177ef0431c4756a89789a8027fccfd96364371`  
		Last Modified: Thu, 23 Jun 2022 15:51:49 GMT  
		Size: 46.5 MB (46506772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d1ed5ce46df7fd0648fc66731039377cb691eea5fb0a0897d32bb448b10f56`  
		Last Modified: Fri, 24 Jun 2022 03:19:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77e0540c200532505b0bf0cba24db2ac6bc5e5afa3c8900de822079a06de218`  
		Last Modified: Fri, 24 Jun 2022 03:32:04 GMT  
		Size: 12.2 MB (12230675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae645b5d5f4a9fff0af9fc5ea35bcde4cce1f02f8be5d07c3a2e41b81f450b9`  
		Last Modified: Fri, 24 Jun 2022 03:32:03 GMT  
		Size: 218.3 KB (218308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
