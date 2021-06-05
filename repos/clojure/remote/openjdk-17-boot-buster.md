## `clojure:openjdk-17-boot-buster`

```console
$ docker pull clojure@sha256:cf03ddd57017e724bd29027e6bb90fa7c0a0811cda0e979f91d4aae9f46bec38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:d0dc11d89c7d45b4a92c61e12d76c43025c7d388e641d986c006e0fd064cc917
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379061385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae59a0c424cf4be09b1604015cdc4e6e8aad2cdc82c5e9d307bf2868369da38`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:47:27 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:47:27 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jun 2021 18:22:01 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 18:22:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='5da8f12ebc9f3c601a838d3b49222015ad418ccde5bdf7bc36dceaf5e7fd9976'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='149a417622b53f0933df2a9200126c7313bc13923d80b58ee041085aa087f62b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Jun 2021 18:22:12 GMT
CMD ["jshell"]
# Fri, 04 Jun 2021 19:50:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Jun 2021 19:50:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Jun 2021 19:50:44 GMT
WORKDIR /tmp
# Fri, 04 Jun 2021 19:50:45 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 04 Jun 2021 19:50:46 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Jun 2021 19:50:46 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Jun 2021 19:51:07 GMT
RUN boot
# Fri, 04 Jun 2021 19:51:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53c8574903f2e47274cfe45903823235a9b4b846f7771f2a75a8e6a1462162`  
		Last Modified: Wed, 12 May 2021 06:57:35 GMT  
		Size: 13.9 MB (13921268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613fdfd388a5273b8684d054076f92b5d36074f04284e24024402578b4cf7bd`  
		Last Modified: Fri, 04 Jun 2021 18:28:17 GMT  
		Size: 186.2 MB (186207914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e0668a28de1126e2ab9684c3ff127d5439d8ec6c7fd459f08bdf1f44996f3`  
		Last Modified: Fri, 04 Jun 2021 19:55:15 GMT  
		Size: 6.9 KB (6925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a324eea831b505d196a4902171659b0789ac41e1da11e9adf50051df032691c3`  
		Last Modified: Fri, 04 Jun 2021 19:55:20 GMT  
		Size: 58.8 MB (58820473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea027dfa173cbf3f3a5ae009475b116ec598fc73fe111d0ef5d9c9d0f083e674
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.8 MB (374808711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed3c85d7d6fe4d2e2c32e3b341f9969a67d9bfea735f6dd8f8984fb39ebf722`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 20:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 May 2021 05:20:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Fri, 28 May 2021 05:20:03 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 05:20:03 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jun 2021 18:43:23 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 18:43:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='5da8f12ebc9f3c601a838d3b49222015ad418ccde5bdf7bc36dceaf5e7fd9976'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='149a417622b53f0933df2a9200126c7313bc13923d80b58ee041085aa087f62b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Jun 2021 18:43:32 GMT
CMD ["jshell"]
# Fri, 04 Jun 2021 20:38:01 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Jun 2021 20:38:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Jun 2021 20:38:02 GMT
WORKDIR /tmp
# Fri, 04 Jun 2021 20:38:03 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 04 Jun 2021 20:38:03 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Jun 2021 20:38:03 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Jun 2021 20:38:21 GMT
RUN boot
# Fri, 04 Jun 2021 20:38:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8aff564b222789ed2823b88e0f1a69ac00cbcbf9349acb8a363d5ef9724182`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e893e0778bb86166fb6799aec4e4ac337c4f10172386c8ae9cf3c787331d7d`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 10.0 MB (9984325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf2dd6193dae84aecaec1d65081288ca49fe0843460035cc060b5aa4e7a9a7`  
		Last Modified: Thu, 27 May 2021 21:05:39 GMT  
		Size: 52.2 MB (52167766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e4f34f8162390a1c3755bde6c4b80914f4d5f6e0b090336929fcc052d69dd1`  
		Last Modified: Fri, 28 May 2021 05:32:23 GMT  
		Size: 14.7 MB (14673533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f91165eebcfb86ac92ded2fe4024687338a9abb661ef35e1511e287968edc2`  
		Last Modified: Fri, 04 Jun 2021 18:54:44 GMT  
		Size: 182.2 MB (182235570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f30246ba2ec47b3d8eda42191df0d1ebb9f8d6f9e24b5a37179a886da18ba0b`  
		Last Modified: Fri, 04 Jun 2021 20:43:44 GMT  
		Size: 6.9 KB (6923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f656da041afa8cd530ea9117b2a63f8583c7e23ba533d6f917d207d0e779d03`  
		Last Modified: Fri, 04 Jun 2021 20:43:48 GMT  
		Size: 58.8 MB (58820337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
