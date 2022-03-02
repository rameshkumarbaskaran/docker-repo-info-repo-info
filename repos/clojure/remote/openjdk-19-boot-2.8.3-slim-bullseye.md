## `clojure:openjdk-19-boot-2.8.3-slim-bullseye`

```console
$ docker pull clojure@sha256:103dcb8cfff2ad8b2e7ae95170fa5cc7a693a6793ac434a28f3ae17d67a3d292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot-2.8.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ceb16fc7beecffa8323f0cefad0e6fc81cf81a260af5cd5b01a8a0237e369c81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282697680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393342eea24fa1c3997bff40f61dcc74572a2f1f3b038d21f043659313e471fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:48:14 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:48:15 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 08:05:34 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 08:05:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 08:05:48 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:48:50 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Mar 2022 08:48:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Mar 2022 08:48:51 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:48:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Mar 2022 08:48:56 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Mar 2022 08:48:57 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Mar 2022 08:49:10 GMT
RUN boot
# Wed, 02 Mar 2022 08:49:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:49:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:49:12 GMT
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
	-	`sha256:3f4461e0f627056d9006dfdaca6f09749d52a9199712504126eeb3a0d57a9876`  
		Last Modified: Wed, 02 Mar 2022 08:20:34 GMT  
		Size: 192.2 MB (192191250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6fce37b196609e5e7919b3e1eaa8322e440ccc870c0eaa12d078b36a3937dc`  
		Last Modified: Wed, 02 Mar 2022 09:18:01 GMT  
		Size: 67.2 KB (67210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644123820e4866b8210bc308cc1cf98d469b5beac5909c4f16941429650ae6a5`  
		Last Modified: Wed, 02 Mar 2022 09:18:08 GMT  
		Size: 58.8 MB (58815870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe0c42cfd6d67fe5ef3d546c23d78f59e14a7487ecb8d198d313bfb16ce9f9`  
		Last Modified: Wed, 02 Mar 2022 09:18:01 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
