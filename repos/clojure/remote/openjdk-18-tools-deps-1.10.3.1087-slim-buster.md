## `clojure:openjdk-18-tools-deps-1.10.3.1087-slim-buster`

```console
$ docker pull clojure@sha256:24fd32360ca34e34e69e07f6fdc3eeb75bb117680fa2149d90432f45f92483dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-1.10.3.1087-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:5c1395ba77183cf7298469ce333ca97d342f9f5c83650adf3a5f08785c074304
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281174859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f7c03907107fd1b17f11e509f64575c8bf54f7fed12494bab3c7d2e6bb81ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:54:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 00:54:09 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:54:09 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:54:09 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 00:54:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:54:23 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:43:05 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 29 Mar 2022 23:43:05 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:43:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 29 Mar 2022 23:43:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 29 Mar 2022 23:43:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:43:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:43:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a93b586a56127b277f2e371624af9ed70508966a2ca124e827d47b841391445`  
		Last Modified: Tue, 29 Mar 2022 01:05:57 GMT  
		Size: 3.3 MB (3273249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea92260f1d279f8e4a4fcdeee2ad037d348d72b7237de3cb3cde70ed081a89e`  
		Last Modified: Tue, 29 Mar 2022 01:08:41 GMT  
		Size: 189.1 MB (189051269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07313b3442e3eb5527a2bf87303b6d532fbcb923ec9a73ad9aecd527681066ba`  
		Last Modified: Wed, 30 Mar 2022 00:03:36 GMT  
		Size: 61.7 MB (61697342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e4d4dc2f3b68d7489d7c743ce7ebe95bd418311279dfb1fc26f3a3b23bf39`  
		Last Modified: Wed, 30 Mar 2022 00:03:28 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb628a4205398b9fae52cb94d265018eed806726d4d0c6c7ffcb32403e8b535`  
		Last Modified: Wed, 30 Mar 2022 00:03:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-1.10.3.1087-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db047e57c1cd7ce370c147d7b45a4fb25fbfba924d3c4fdeff38e69dda02ae8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278158894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5e2f621d3066ce6f6608b341bd1062861a9e48488e36c736fe65883f128ae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:19:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:20:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 01:20:30 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:20:31 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:20:32 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 01:20:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:20:49 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 09:50:58 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 30 Mar 2022 09:50:59 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:51:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 30 Mar 2022 09:51:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 30 Mar 2022 09:51:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 09:51:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 09:51:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b464c2cba1daef8144ee6cab94db7ab3e6c663c917369550b9b29d8cac37b`  
		Last Modified: Tue, 29 Mar 2022 01:39:33 GMT  
		Size: 3.1 MB (3125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f9851eea0f63f4e1441e8632210304b963bef313a55ca238b7ba1975c61ea7`  
		Last Modified: Tue, 29 Mar 2022 01:41:14 GMT  
		Size: 187.8 MB (187762163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a305bd743bd556273a55b340abeac63588819930a1893ac8e35d0ae36ba651`  
		Last Modified: Wed, 30 Mar 2022 10:19:09 GMT  
		Size: 61.4 MB (61350139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120687482677455c2f3d182d08e746e8d53ee60bd2e2986d6936ec3ce64d3ffb`  
		Last Modified: Wed, 30 Mar 2022 10:19:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1fe9d8fb57668bd6abcf9f32ace70df6459b41ad60cc31e3b2a4857c4ecf4b`  
		Last Modified: Wed, 30 Mar 2022 10:19:01 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
