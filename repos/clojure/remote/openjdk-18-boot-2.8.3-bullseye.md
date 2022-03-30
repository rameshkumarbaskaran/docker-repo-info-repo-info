## `clojure:openjdk-18-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:ad12e6be5c4e86e08959e0c90079657c7b15f2a9d9e3fd7305b7b872da64fb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:379e80bc853edb6cdd719f9780c64a8309c2ca6188f62efdac76fbbeb9f2af75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388236421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab692eb6233e3c6c3b313a8991bb0ad085375ed142ce9d6747352e2ee083aba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:29:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:08:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 23:08:38 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:08:38 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:08:38 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 23:08:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:08:48 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:50:28 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:50:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:50:28 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:50:32 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 29 Mar 2022 23:50:32 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:50:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:50:57 GMT
RUN boot
# Tue, 29 Mar 2022 23:50:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:50:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:50:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baf437a1badb6aad2dae5f2cd4a7b53a6c7ab6c14cba1ed1ecb42b4822b0e87`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 5.2 MB (5155705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ade5c59e324bd7cf369c72ad781c23d37e8fb48c9bbb4abbecafafd9be4cc35`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 10.9 MB (10874957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a994f6d4cdbb620339bd2e4ad47b229f14276b542060622ae447649294e5d`  
		Last Modified: Tue, 29 Mar 2022 17:38:33 GMT  
		Size: 54.6 MB (54576420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bf70d022dcc85ebcf204b1587cbb09fca454963d16c1afe48a80cc79c183e7`  
		Last Modified: Tue, 29 Mar 2022 23:19:25 GMT  
		Size: 14.1 MB (14071880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6500b78a3215164bc6689431ad128aeb1f21571aac629dfd9486317711a3be6`  
		Last Modified: Tue, 29 Mar 2022 23:21:57 GMT  
		Size: 188.8 MB (188781325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da1547903c33c500ba30b92f899b4bffb12b788d12be30e219d1653e50bc2fd`  
		Last Modified: Wed, 30 Mar 2022 00:10:57 GMT  
		Size: 1.0 MB (1017422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55af7f1ca4469b64f22370d31d5a0e7a3190564ba61ff71bab15eff679dfd680`  
		Last Modified: Wed, 30 Mar 2022 00:11:00 GMT  
		Size: 58.8 MB (58820601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9657ec2f4620f0963cde8bdeb607e06113951c1315f46f3c05b3388ab82c9ba`  
		Last Modified: Wed, 30 Mar 2022 00:10:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15760239a7bdb4a37aea61795f3da885accdfc70d397257dc899d3374905143d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386724576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b189b30e8d6c198d18e477e17336a8288c181f08ec801b56599803f1c1b2f803`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:01 GMT
ADD file:5e8f8c10da6d37a727fb5e1ed13b3dd78769f0ca7e91f0c3510e2edd25177117 in / 
# Tue, 29 Mar 2022 00:43:03 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:13:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:13:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:13:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 09:01:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 30 Mar 2022 09:01:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 09:01:11 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 09:01:12 GMT
ENV JAVA_VERSION=18
# Wed, 30 Mar 2022 09:01:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 09:01:24 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 10:01:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 30 Mar 2022 10:01:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 10:01:46 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 10:01:51 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 30 Mar 2022 10:01:52 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 30 Mar 2022 10:01:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 30 Mar 2022 10:02:12 GMT
RUN boot
# Wed, 30 Mar 2022 10:02:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 10:02:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 10:02:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fa223d8c149d7beec8e997e1415ee4961473cafaf88a932f70baf3da56f2c564`  
		Last Modified: Tue, 29 Mar 2022 00:49:33 GMT  
		Size: 53.6 MB (53633710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbd2ab15985c19f9e1e3199cdce06090266d20d11dbd3d55fba45de2fcc27`  
		Last Modified: Wed, 30 Mar 2022 02:24:13 GMT  
		Size: 4.9 MB (4938638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3953e76cee2ab175d909ccec1a3399912a690ad621ae88cff787d98419b97bb`  
		Last Modified: Wed, 30 Mar 2022 02:24:14 GMT  
		Size: 10.7 MB (10656993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f906570592fdd65a2fcfae6164990d0422e03ccadba25c5b1d1268a29f7c530`  
		Last Modified: Wed, 30 Mar 2022 02:24:36 GMT  
		Size: 54.7 MB (54671703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853816c9302dd46795217ad48fd4f824d07138762d488c289fb8f04937b99372`  
		Last Modified: Wed, 30 Mar 2022 09:20:08 GMT  
		Size: 15.5 MB (15524979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e36f21a4d478c1baffe912a8c394962beee1be23ab28137cd36eb389ef2f7fa`  
		Last Modified: Wed, 30 Mar 2022 09:23:08 GMT  
		Size: 187.7 MB (187705138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e2764723a0bf0fbf5cf9270cbbc7f1d67d1cd4ea8589413b25013eaeb09542`  
		Last Modified: Wed, 30 Mar 2022 10:28:36 GMT  
		Size: 777.4 KB (777398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe76d08d0247cce208b4e70f9ef97879a713fc2bc1509feb003faa14496afd1`  
		Last Modified: Wed, 30 Mar 2022 10:28:43 GMT  
		Size: 58.8 MB (58815613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa998ffe4bf45543b906c09a3d11725ed1bc0b34a39e01e9e0eac80cbccaca6e`  
		Last Modified: Wed, 30 Mar 2022 10:28:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
