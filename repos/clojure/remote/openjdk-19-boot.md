## `clojure:openjdk-19-boot`

```console
$ docker pull clojure@sha256:7166d35591d6a2fb012122944b61b923d96bb9dce00adb35ce34d98818f84c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot` - linux; amd64

```console
$ docker pull clojure@sha256:dfd69119d0ddb59bf7ec9b260cfcfa5876480cf0cac38fb4700b5750d97f6558
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285617654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efa54366866992c6d6bd38c60836e63d1c1d411fc62d5a39e5f6fe81e27b07d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:52:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 00:52:15 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:52:15 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 01:24:52 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 01:25:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 01:25:31 GMT
CMD ["jshell"]
# Thu, 07 Apr 2022 08:41:59 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Apr 2022 08:41:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Apr 2022 08:41:59 GMT
WORKDIR /tmp
# Thu, 07 Apr 2022 08:42:04 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Apr 2022 08:42:04 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Apr 2022 08:42:04 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Apr 2022 08:42:44 GMT
RUN boot
# Thu, 07 Apr 2022 08:42:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Apr 2022 08:42:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Apr 2022 08:42:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc05f270bad654ee17f1143c48586c188a72929a128d61fd8ae15905d7b00`  
		Last Modified: Tue, 29 Mar 2022 01:04:32 GMT  
		Size: 1.6 MB (1582122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98497f177a1ab8e4ea080e0813483512cc296e960481603957d9972f3e52a141`  
		Last Modified: Thu, 07 Apr 2022 01:34:14 GMT  
		Size: 193.6 MB (193552649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ed43f2213e0086508a37f0561057d304dcac8bbd4003d929477b4de999c5f`  
		Last Modified: Thu, 07 Apr 2022 10:28:40 GMT  
		Size: 283.1 KB (283094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e523608bd9845de839d5240dd85b3226f550c88d2e376e4fe48c7e5e1910b32a`  
		Last Modified: Thu, 07 Apr 2022 10:28:43 GMT  
		Size: 58.8 MB (58820925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663f1e1e5132c186d75bb74b5b9c21a2ac9937ebecf1b0296629cc597bd8870f`  
		Last Modified: Thu, 07 Apr 2022 10:28:39 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2ee70cf2d38ba784bc872674a4e007b66291c33543972366640d7b4f435492d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282539121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7155f2b5bf32b07422ff869d75db14436bb7e41e8621e64cffa7e937297dd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:18:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 01:18:13 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:18:14 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 00:45:57 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 00:46:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 00:46:09 GMT
CMD ["jshell"]
# Thu, 07 Apr 2022 07:09:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Apr 2022 07:09:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Apr 2022 07:09:07 GMT
WORKDIR /tmp
# Thu, 07 Apr 2022 07:09:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Apr 2022 07:09:12 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Apr 2022 07:09:13 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Apr 2022 07:09:38 GMT
RUN boot
# Thu, 07 Apr 2022 07:09:39 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Apr 2022 07:09:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Apr 2022 07:09:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee14fdb7a0a09a9e31998d2906081734dba985b95da3f35b7bd79d79b73330`  
		Last Modified: Tue, 29 Mar 2022 01:37:54 GMT  
		Size: 1.4 MB (1361189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1efcf5789d547f10ff5c96eb912309149f5e3e715a989f17e6fd7db541078a`  
		Last Modified: Thu, 07 Apr 2022 01:00:48 GMT  
		Size: 192.2 MB (192229593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c959bdc23da24184a4e494420e9cd7bdac9bdf222d2d58f95b655b3f657f62d8`  
		Last Modified: Thu, 07 Apr 2022 07:19:09 GMT  
		Size: 67.3 KB (67264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a196448c80027513a1e3176f1a21f42abcb5038421097098f7284c7c47b5bb1e`  
		Last Modified: Thu, 07 Apr 2022 07:19:13 GMT  
		Size: 58.8 MB (58816359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c801855bde863dcb1c189c41fa77dcf78173ac1fd58488fb0147cfa36fc9e3`  
		Last Modified: Thu, 07 Apr 2022 07:19:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
