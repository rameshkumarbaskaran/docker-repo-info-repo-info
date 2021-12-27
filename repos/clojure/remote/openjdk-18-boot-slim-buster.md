## `clojure:openjdk-18-boot-slim-buster`

```console
$ docker pull clojure@sha256:dfed66ff940a1d002435df7fb14950f64ecce61c95c3028fa4a44fff69734340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:b338eecb1dfea58f3e94088cc02797026be2d261348e7d34f38245ff15bc40b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278535812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ffed8730e5958dff5b028125ffac9e56fe7911df0be670b63fa653076205f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 22:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:59:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 22:59:58 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 22:59:59 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 22:59:59 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 23:00:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 23:00:14 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:41:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 22 Dec 2021 13:41:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 22 Dec 2021 13:41:06 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:41:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 22 Dec 2021 13:41:11 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Dec 2021 13:41:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 22 Dec 2021 13:41:33 GMT
RUN boot
# Wed, 22 Dec 2021 13:41:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:41:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:41:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c983bcc370920d99695dc288c345343be841987206e4ce762a4e7599f28c96`  
		Last Modified: Tue, 21 Dec 2021 23:16:09 GMT  
		Size: 3.3 MB (3269567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f54dcb284410f41e55cf4f4ca250e28e480947f47fd02d4a206df1320d7be4d`  
		Last Modified: Tue, 21 Dec 2021 23:19:07 GMT  
		Size: 189.0 MB (189011832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b0cf21ef4e234beccdc95446ab2beb7dadb2da58336e844d188866eb9bf0d`  
		Last Modified: Wed, 22 Dec 2021 13:59:57 GMT  
		Size: 279.8 KB (279768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8416f62fc1ff12cad9ed3f38af6bcacb037d1342786e726b8d466dfa19bb053`  
		Last Modified: Wed, 22 Dec 2021 14:00:00 GMT  
		Size: 58.8 MB (58820515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfde9c9b5a3217e162a4fab042bdc05237959bf13fbaeefaad614d58ec3fc65b`  
		Last Modified: Wed, 22 Dec 2021 13:59:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ac75bc6c847c586a814be5e3dd0c8b6e6e391bcf49b15d67f5e3c260d4e1a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275669993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa05b6df83c7498c6993d4103c8102f9802760f6047aa9cd2867dc1550de76a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:56:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 02:56:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:56:43 GMT
ENV LANG=C.UTF-8
# Mon, 27 Dec 2021 17:48:09 GMT
ENV JAVA_VERSION=18-ea+29
# Mon, 27 Dec 2021 17:48:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='79501105196281bcb3b1c356529238c3f943a51a24e8695bcee0e3b3e1881507'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/29/GPL/openjdk-18-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='cecaad040cc1f7b0507c8b62275e90ddc32a203da239dccfd5d711f47518bc3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 27 Dec 2021 17:48:29 GMT
CMD ["jshell"]
# Mon, 27 Dec 2021 18:31:34 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 27 Dec 2021 18:31:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 27 Dec 2021 18:31:36 GMT
WORKDIR /tmp
# Mon, 27 Dec 2021 18:31:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 27 Dec 2021 18:31:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 27 Dec 2021 18:31:43 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 27 Dec 2021 18:31:56 GMT
RUN boot
# Mon, 27 Dec 2021 18:31:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 27 Dec 2021 18:31:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 27 Dec 2021 18:31:59 GMT
CMD ["repl"]
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
	-	`sha256:50ff7733b5b1ab1cf10b328fe519660202acb09f6833d27bec0a9bccf4618401`  
		Last Modified: Mon, 27 Dec 2021 18:08:09 GMT  
		Size: 187.7 MB (187744390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5d5f62e9dbf0d5376850c9e47d713fae2daf53859d0fa4ae012ff376cd076a`  
		Last Modified: Mon, 27 Dec 2021 18:46:49 GMT  
		Size: 67.5 KB (67507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f7b104fd70340c870b8f24d799c8e47786b068e8e1f44d6bc29fe2427a07ea`  
		Last Modified: Mon, 27 Dec 2021 18:46:54 GMT  
		Size: 58.8 MB (58815687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf40bbd9f505d059de77d6e5457ee673c2c9ccbe248ec5dab379324e9220008`  
		Last Modified: Mon, 27 Dec 2021 18:46:49 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
