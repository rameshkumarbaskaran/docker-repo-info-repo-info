## `tomcat:jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:1fea0e7fabfa63b5685c91c013b76a733a1fffb049b0d1167755fa138d2bccb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:7817ab220978767ae699b8637515be58e05091b0e83c04bf48cbbc48c74b598a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90852613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb70f8d120c5f5ff3ebe907359425b9b85d4b9e9f3dd664e09249016db46890`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:00:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 02:00:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:00:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:00:03 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:00:03 GMT
ENV JAVA_VERSION=11.0.15
# Tue, 12 Jul 2022 02:01:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Tue, 12 Jul 2022 18:50:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 Jul 2022 18:50:08 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:50:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 12 Jul 2022 18:50:08 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 Jul 2022 18:50:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:50:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:50:09 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 12 Jul 2022 18:50:09 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 Jul 2022 18:53:28 GMT
ENV TOMCAT_VERSION=10.0.22
# Tue, 12 Jul 2022 18:53:28 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Fri, 22 Jul 2022 02:51:37 GMT
COPY dir:fd0f4397cf2e2b52494620a6077021626a6e782b34831cb219f027a3835023ff in /usr/local/tomcat 
# Fri, 22 Jul 2022 02:51:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Jul 2022 02:51:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Jul 2022 02:51:43 GMT
EXPOSE 8080
# Fri, 22 Jul 2022 02:51:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62264f680cd73ea710b719ee1e279e0a800def0defab33dd092436647625fa1a`  
		Last Modified: Tue, 12 Jul 2022 02:10:29 GMT  
		Size: 3.3 MB (3273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae5a288633626a7eef79f64b99bc7555aa73bda4a01c54f95e61acc538afa4c`  
		Last Modified: Tue, 12 Jul 2022 02:18:24 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5f1ee677f227a68c45582f412e2fc876ae5988b43301116aa1317f2a7985c7`  
		Last Modified: Tue, 12 Jul 2022 02:19:33 GMT  
		Size: 47.5 MB (47481960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fe26b319beb06a217fc037fa0e76ff48672639e8c3dcbb5e6055172f6be506`  
		Last Modified: Tue, 12 Jul 2022 19:20:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a621a376374c5c7a5d29ac3390f7e7a2a3c69b97453f49643a1fbceb92507`  
		Last Modified: Fri, 22 Jul 2022 03:40:32 GMT  
		Size: 12.6 MB (12569111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e69a2b8b925fd94e4ec374057d520fba91e9a52d9317b8eb5f077aa3724dc38`  
		Last Modified: Fri, 22 Jul 2022 03:40:31 GMT  
		Size: 387.8 KB (387752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235e9ba5b8b5ac5d151da376a99f8692388b01f1b4f79c4bd6180906f5c9a77d`  
		Last Modified: Fri, 22 Jul 2022 03:40:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c838f560e262608e712b326eab1b556545376250b6f935717d8adcbcaf0d9334
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88362295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3770513444ad72c0a8c521d749f578b56f9bcbaaa91009989fc774d5315324f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:29:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:35:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 01:35:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 01:35:24 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 01:35:26 GMT
ENV JAVA_VERSION=11.0.15
# Tue, 12 Jul 2022 01:36:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Tue, 12 Jul 2022 18:33:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 Jul 2022 18:33:07 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:33:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 12 Jul 2022 18:33:09 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 Jul 2022 18:33:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:33:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:33:12 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 12 Jul 2022 18:33:13 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 Jul 2022 18:37:59 GMT
ENV TOMCAT_VERSION=10.0.22
# Tue, 12 Jul 2022 18:38:00 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Fri, 22 Jul 2022 03:54:42 GMT
COPY dir:9c1cd8b8b30abeaa74f40a9c008838c65583f2fa25fceb3630eea4e8a6e436e6 in /usr/local/tomcat 
# Fri, 22 Jul 2022 03:54:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Jul 2022 03:54:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Jul 2022 03:54:48 GMT
EXPOSE 8080
# Fri, 22 Jul 2022 03:54:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebd82c0fcc991163b8dd04e396a3c7388adb7b021c0463cecaa0345cbd7ac1b`  
		Last Modified: Tue, 12 Jul 2022 01:51:21 GMT  
		Size: 3.1 MB (3126061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3571a14922164cb321228b249be6121c8361859747abeacc38af97fd1fb0670`  
		Last Modified: Tue, 12 Jul 2022 02:00:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935b34c942076836bc1050c8bdfb6a380fc9d49ac79147c72071954eb1d29e31`  
		Last Modified: Tue, 12 Jul 2022 02:02:17 GMT  
		Size: 46.6 MB (46566882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7735aa307f3fc4172ec537a26510530c8dcef085f05bde6cdb0925a3a02a29a`  
		Last Modified: Tue, 12 Jul 2022 19:22:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26a4adc598bf0a000c343f925eda2c334895be5e256b975f8117ba566a1bc9e`  
		Last Modified: Fri, 22 Jul 2022 05:01:30 GMT  
		Size: 12.6 MB (12581070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28248f36616c534dcaf84719848460d199354815f53e3a0e47bf120eb6ccea7e`  
		Last Modified: Fri, 22 Jul 2022 05:01:29 GMT  
		Size: 173.7 KB (173696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
