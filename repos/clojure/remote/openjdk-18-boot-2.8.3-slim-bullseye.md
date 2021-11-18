## `clojure:openjdk-18-boot-2.8.3-slim-bullseye`

```console
$ docker pull clojure@sha256:ff76bc7e183a0f66f4b140a9a588a5116a0665b21be9681f520a2d72e8b1708c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7a226357575d675b37ee81c75e228e8281833bcf05236d3cbaf8149782460d0e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280632912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0282f0f1c940022ab9361d5f6619dcb65b67cbad167584c2bc3bb5f082b99c2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:41 GMT
ADD file:a2405ebb9892d98be2eb585f6121864d12b3fd983ebf15e5f0b7486e106a79c6 in / 
# Wed, 17 Nov 2021 02:20:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:24:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 09:24:02 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:24:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:24:02 GMT
ENV JAVA_VERSION=18-ea+23
# Wed, 17 Nov 2021 09:24:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 17 Nov 2021 09:24:17 GMT
CMD ["jshell"]
# Thu, 18 Nov 2021 13:10:50 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 18 Nov 2021 13:10:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 18 Nov 2021 13:10:51 GMT
WORKDIR /tmp
# Thu, 18 Nov 2021 13:10:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 18 Nov 2021 13:10:55 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 18 Nov 2021 13:10:56 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 18 Nov 2021 13:11:14 GMT
RUN boot
# Thu, 18 Nov 2021 13:11:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:eff15d958d664f0874d16aee393cc44387031ee0a68ef8542d0056c747f378e8`  
		Last Modified: Wed, 17 Nov 2021 02:25:45 GMT  
		Size: 31.4 MB (31370267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66aa43e8673fbe291330e91f1b1541b15d22a49a7b04297a5efea392ca5355d9`  
		Last Modified: Wed, 17 Nov 2021 09:40:19 GMT  
		Size: 1.6 MB (1582092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcc80089dd7d03997d236fc7c9f150b4ff416dca7c755da479ae543c18d8faa`  
		Last Modified: Wed, 17 Nov 2021 09:40:37 GMT  
		Size: 188.6 MB (188577146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036c8691f212a4e6b8ab65c20634da75004860591edd7062d3f2b3ad491294ec`  
		Last Modified: Thu, 18 Nov 2021 13:28:11 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5eb4f93426d0abfde4d9ce782a94b2ca849ab76bdbf3b9e0847f0fc411db9f`  
		Last Modified: Thu, 18 Nov 2021 13:28:14 GMT  
		Size: 58.8 MB (58820321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c91726705be1cd2f8097e211a01efb80f68075c2ab98020fd0a2f4c1b1b830b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277586434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aef0f71b83430deac7f8537cd929efe129703735fc4779b82f48d343a6e52d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:15 GMT
ADD file:4203242b2b09a65239092c4780b59181da7b861b3c0be40810b3588aa200f72c in / 
# Wed, 17 Nov 2021 02:40:16 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 06:19:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 06:19:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 06:19:28 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 06:19:29 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 06:19:30 GMT
ENV JAVA_VERSION=18-ea+23
# Wed, 17 Nov 2021 06:19:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 17 Nov 2021 06:19:48 GMT
CMD ["jshell"]
# Wed, 17 Nov 2021 16:33:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Nov 2021 16:33:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Nov 2021 16:33:07 GMT
WORKDIR /tmp
# Wed, 17 Nov 2021 16:33:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Nov 2021 16:33:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Nov 2021 16:33:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Nov 2021 16:33:29 GMT
RUN boot
# Wed, 17 Nov 2021 16:33:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:eb9a2845ed124d072b117aba4f0508e00c1ecd0d147dc324d14b00d24092046c`  
		Last Modified: Wed, 17 Nov 2021 02:47:17 GMT  
		Size: 30.1 MB (30056521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56148104a70127abacd50cd70c5a74c0bdf67f5861e668f44a97a9a22f02a5c7`  
		Last Modified: Wed, 17 Nov 2021 06:34:51 GMT  
		Size: 1.4 MB (1361241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcdff5a036e2c3b7bbba2e65f943377c532288baa3e5d34043ab97938d540a8`  
		Last Modified: Wed, 17 Nov 2021 06:35:13 GMT  
		Size: 187.3 MB (187285815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b12e6c9ddbbbef6174f04e3241d113cbd80ac5af2e5c29f5d0e345e87d03c7`  
		Last Modified: Wed, 17 Nov 2021 16:46:42 GMT  
		Size: 67.2 KB (67232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6824145ef0189fcb0b0c1e72460fbe7dbf76ef1c0c6ad439060ab3bfcd1550a`  
		Last Modified: Wed, 17 Nov 2021 16:46:49 GMT  
		Size: 58.8 MB (58815625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
