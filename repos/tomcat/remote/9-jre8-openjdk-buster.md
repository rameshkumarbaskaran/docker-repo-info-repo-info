## `tomcat:9-jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:1708506d6d5148582e214211b7c83295f039c3d6cf8d9d08be7a460ff185cdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:f8ccbe44c075b43a1d971ed9797a0f1ad289ff868c4ad2824d375fde355da4ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127937229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9b6125e91b2db01ccea032e4e6a2331c478a7ee4e1b18bc5f152740486b852`
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
# Thu, 23 Jun 2022 05:01:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:45 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:46 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:46 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:46 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:45:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:45:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:45:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:45:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:45:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:45:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:51:16 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 23 Jun 2022 22:51:16 GMT
ENV TOMCAT_MAJOR=9
# Thu, 23 Jun 2022 22:51:16 GMT
ENV TOMCAT_VERSION=9.0.64
# Thu, 23 Jun 2022 22:51:16 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Thu, 23 Jun 2022 22:51:17 GMT
COPY dir:0545d1d5de09bcc1c4aeee61b8087ffdd55635ebe819460f2caaf359dd4edd72 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:51:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:51:22 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:51:22 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:51:22 GMT
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
	-	`sha256:706a76fd54c3779c8650b52578c425ee9ea28faf52393424f3a137a9974627bc`  
		Last Modified: Thu, 23 Jun 2022 05:22:11 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99571f7ac24e01dd83ae457173630a53f6e3ef10ce6926ffcc4b23cff6a7c9c7`  
		Last Modified: Thu, 23 Jun 2022 05:22:16 GMT  
		Size: 41.4 MB (41432122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a683662b013655f930c6abe898746300080619143558b33246960906c92cbf23`  
		Last Modified: Thu, 23 Jun 2022 23:14:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b439c80594fac4cd80f422be8e5c5bd668262334e0c9a4be82cb6fdc12080`  
		Last Modified: Thu, 23 Jun 2022 23:19:49 GMT  
		Size: 12.2 MB (12216375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b644f0edc2fc3b1b1aacc0dc4f7a6bfd8eaaf8fb5e08a34d95731f37f36d384`  
		Last Modified: Thu, 23 Jun 2022 23:19:48 GMT  
		Size: 460.9 KB (460939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266ad001b36cffb21087ed705a6e91ea656089532ee4319276469ed5fe4f0346`  
		Last Modified: Thu, 23 Jun 2022 23:19:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:92a3c996901a81717f6f0f1d4e4f42539657818919a5c9589aa7e17ad7afcefb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125344050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970ffc4c7fc43624b02dbc311732c0e603d990ac251c2baff2388d081e9362d2`
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
# Thu, 23 Jun 2022 15:26:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 15:26:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:26:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:26:38 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:26:39 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 15:26:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 24 Jun 2022 02:42:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 24 Jun 2022 02:42:51 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 02:42:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 24 Jun 2022 02:42:53 GMT
WORKDIR /usr/local/tomcat
# Fri, 24 Jun 2022 02:42:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:42:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:52:07 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 24 Jun 2022 02:52:07 GMT
ENV TOMCAT_MAJOR=9
# Fri, 24 Jun 2022 02:52:08 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 24 Jun 2022 02:52:09 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 24 Jun 2022 02:52:11 GMT
COPY dir:ab3e96f03ddf83d649aa52cf204453e0f6d3ce2b39dfda1e3bcf5100847c35bc in /usr/local/tomcat 
# Fri, 24 Jun 2022 02:52:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 02:52:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 24 Jun 2022 02:52:17 GMT
EXPOSE 8080
# Fri, 24 Jun 2022 02:52:18 GMT
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
	-	`sha256:36963fd55f68e14878c2216840eb5933d1c5e38d079d47e50e30dbfc9f52a7e1`  
		Last Modified: Thu, 23 Jun 2022 15:55:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82ae156fc5dbaecc8a199937d610f9554311c772b7352b2b51432744fbbeed3`  
		Last Modified: Thu, 23 Jun 2022 15:55:26 GMT  
		Size: 40.7 MB (40672288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390fe37e14a25b7fbcf59ad6809b49e62dda7a8b9499168a17da49fc9244805a`  
		Last Modified: Fri, 24 Jun 2022 03:28:04 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf080b7ada17c6f1b31c2fb7aab54b448937d9b2b11aeb20ac1de0d3f70e67b9`  
		Last Modified: Fri, 24 Jun 2022 03:35:08 GMT  
		Size: 12.2 MB (12230119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faec8904ec9cc013a9a70f43ba9c14e8a40d42c3060fabebcab74ea43030ad90`  
		Last Modified: Fri, 24 Jun 2022 03:35:07 GMT  
		Size: 218.3 KB (218254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
