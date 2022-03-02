## `clojure:openjdk-18-boot-slim-bullseye`

```console
$ docker pull clojure@sha256:a635754d57ffe821fc14f9373665f478b3df6dea7e66cff207eb1e6d9d9924a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:81c5ed13e08c7f19241dbcfc544aacf0309273aad406c6f3014b0dab79c7ef1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281099121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afc89d9bfec724f7c8d4682571109f37e3590158cc1c801c6ff81a72b919264`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:29 GMT
ENV LANG=C.UTF-8
# Mon, 21 Feb 2022 18:27:34 GMT
ENV JAVA_VERSION=18
# Mon, 21 Feb 2022 18:27:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 21 Feb 2022 18:27:49 GMT
CMD ["jshell"]
# Mon, 21 Feb 2022 19:34:19 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 21 Feb 2022 19:34:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 21 Feb 2022 19:34:19 GMT
WORKDIR /tmp
# Mon, 21 Feb 2022 19:34:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 21 Feb 2022 19:34:24 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 21 Feb 2022 19:34:24 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 21 Feb 2022 19:34:43 GMT
RUN boot
# Mon, 21 Feb 2022 19:34:44 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 21 Feb 2022 19:34:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 21 Feb 2022 19:34:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbe94065893d704df703cdce028b6afceedbc3361c228e328f33c02b9d525a1`  
		Last Modified: Mon, 21 Feb 2022 18:39:27 GMT  
		Size: 189.0 MB (189046918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901adb0a7fb252bd8c859ab6fccb3dccb578d0bfec59c3300ca2ec04da183059`  
		Last Modified: Mon, 21 Feb 2022 19:41:11 GMT  
		Size: 283.1 KB (283059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da1e0db622c50578e5e9f167cbf28ab4bd91d35be5fedbec82dd77bab5889cb`  
		Last Modified: Mon, 21 Feb 2022 19:41:15 GMT  
		Size: 58.8 MB (58820430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f830decb74feef50d279ed359008cb01542d5bed1ac0f0f108501f92650a6a32`  
		Last Modified: Mon, 21 Feb 2022 19:41:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf07d160dd9a7e434d8f0342fc354a62fe4390b63b1715b27377bf8e566eaac1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278262616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4ecc7e6ccff78676526af00181a8cf949f73420d38f05ddfb80e88f7f128be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:50:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 01 Mar 2022 13:50:32 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:50:33 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 13:50:34 GMT
ENV JAVA_VERSION=18
# Tue, 01 Mar 2022 13:50:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:50:49 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:46:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Mar 2022 08:46:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Mar 2022 08:46:13 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:46:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Mar 2022 08:46:18 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Mar 2022 08:46:19 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Mar 2022 08:46:33 GMT
RUN boot
# Wed, 02 Mar 2022 08:46:34 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:46:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:46:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee4a8201309b4b9bb0e0e0efc8d45265ae39d932512f5edb149b65eaf107d9`  
		Last Modified: Tue, 01 Mar 2022 14:12:59 GMT  
		Size: 1.6 MB (1565936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f95ae87dbe04893c9f64e3c91cd1b09aa16e52ee20ff8c555686d7994f5081a`  
		Last Modified: Tue, 01 Mar 2022 14:16:12 GMT  
		Size: 187.8 MB (187756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd25cdf21bda9f3c678a56b1935c5efba1c7300eea90f7ab2a010a141e0e27`  
		Last Modified: Wed, 02 Mar 2022 09:15:26 GMT  
		Size: 67.2 KB (67218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43e5725c4bde5ca6b86f6b1f327ff0c4d9e5a5242b18feda918d9dfdeea3ea4`  
		Last Modified: Wed, 02 Mar 2022 09:15:31 GMT  
		Size: 58.8 MB (58815461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee4ed95546e797375eacde3d477d1c6cd228c5ec28ab5d5d5927f3c0deb6e10`  
		Last Modified: Wed, 02 Mar 2022 09:15:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
