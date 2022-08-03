## `tomcat:9-jre8-openjdk-slim`

```console
$ docker pull tomcat@sha256:5b93699fc007896b2a4fef7167f61e93be99cdefe55b045a77660742ad07baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:9520fabcc6d620297e1d6b891a3fa2e10f3ca740c43b1e912df065efbbdd1a5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87201502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d135e2d0a58e37305fc253f89a0aec656713281e49feb894dfb3576f827c5227`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:29:45 GMT
ENV JAVA_VERSION=8u342
# Mon, 25 Jul 2022 20:30:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_8u342b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_8u342b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Mon, 25 Jul 2022 23:14:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 23:14:25 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 23:14:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 23:14:26 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 23:14:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:14:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:20:49 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Jul 2022 23:20:49 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Jul 2022 23:20:49 GMT
ENV TOMCAT_VERSION=9.0.65
# Mon, 25 Jul 2022 23:20:49 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Mon, 25 Jul 2022 23:20:50 GMT
COPY dir:40a2e83a97352fee9310034acf80a3d33406c77cdbdddf19df68e5dc24143929 in /usr/local/tomcat 
# Mon, 25 Jul 2022 23:20:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Jul 2022 23:20:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Jul 2022 23:20:55 GMT
EXPOSE 8080
# Mon, 25 Jul 2022 23:20:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c195552e7f0d9051e292aab20f5a012de83951109edb0fcb133afd5af9cdb5b`  
		Last Modified: Mon, 25 Jul 2022 20:49:34 GMT  
		Size: 41.7 MB (41696209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014ae659d4df1633b279981d5c5a577c22777056b35247525ac0d0edd82f305d`  
		Last Modified: Mon, 25 Jul 2022 23:42:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386136d165e7518b4160e9c453ddbd135ce4d4a51509bb363eda7336f58aa1e6`  
		Last Modified: Mon, 25 Jul 2022 23:48:09 GMT  
		Size: 12.2 MB (12159604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d0d6bcc25852574b14ec0aa7ca7053d0b6153143b22e1ec76427a64f6800a`  
		Last Modified: Mon, 25 Jul 2022 23:48:08 GMT  
		Size: 396.3 KB (396291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d0253b55224b36fb730f3d83c3ef318b8b455511feeb9705afe2f82b2580c5`  
		Last Modified: Mon, 25 Jul 2022 23:48:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:4f68ee08980fce39c95fb4aac144d810673976773782931710190c36264a1e2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e60eddeb233b1c3385ff2a58b969a4264aad063c0e9b9e8bd36b83c1ab6569`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:51:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 02 Aug 2022 04:52:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 02 Aug 2022 04:52:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:52:02 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 04:52:03 GMT
ENV JAVA_VERSION=8u342
# Tue, 02 Aug 2022 04:53:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_8u342b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_8u342b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 03 Aug 2022 02:03:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 02:03:06 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 02:03:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 02:03:08 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 02:03:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:03:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:19:47 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 03 Aug 2022 02:19:48 GMT
ENV TOMCAT_MAJOR=9
# Wed, 03 Aug 2022 02:19:49 GMT
ENV TOMCAT_VERSION=9.0.65
# Wed, 03 Aug 2022 02:19:50 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Wed, 03 Aug 2022 02:19:52 GMT
COPY dir:df63d799bf9a9a2c3ca3e6ff15d122996f036259af110215d13cd3b0dcbf4a6a in /usr/local/tomcat 
# Wed, 03 Aug 2022 02:19:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:19:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 02:19:57 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 02:19:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4015b6e8cc8db11af172df5c0369552bc2a74cd69094b0756d21fc6b0b2a5393`  
		Last Modified: Tue, 02 Aug 2022 05:03:25 GMT  
		Size: 1.6 MB (1565954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86b181efa02db2dd92e3f621ee71d8ddebe2669b3dba8a0320d1d9419b1c7a`  
		Last Modified: Tue, 02 Aug 2022 05:18:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94abd992e68d552cfc81a28ad6e8a9000e08769135a27bad79a59d05044bd63b`  
		Last Modified: Tue, 02 Aug 2022 05:20:31 GMT  
		Size: 40.7 MB (40732494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37315976878163c22f5f880c2fd3a959c2d52498a094aec357dd1d976c70bc15`  
		Last Modified: Wed, 03 Aug 2022 03:09:57 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b84bcc7b86a62f9a0d76383141a48db14055c81d588d35cf14c03bc9071cc8`  
		Last Modified: Wed, 03 Aug 2022 03:21:11 GMT  
		Size: 12.2 MB (12168573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a269df965d6ddc50ef07b465092a1eea5bd7dcd6683455a6fed414043879019e`  
		Last Modified: Wed, 03 Aug 2022 03:21:09 GMT  
		Size: 179.9 KB (179883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
