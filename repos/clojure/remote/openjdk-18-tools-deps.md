## `clojure:openjdk-18-tools-deps`

```console
$ docker pull clojure@sha256:d91454d6b0413dee8433ae5d2be02ac5ce3fc33081f7c9df8a51c5b793e87af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:2a1dada8663a53fc85691e1319705ef6fc716b3f8b3c11db3bf5e5c0796060c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (282039211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf0dfda434b7cf22094f3a881a9106c3a0c33e61f371d951141ff115a79a6ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:53:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 00:53:51 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:53:51 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 00:54:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:54:04 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:51:01 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 29 Mar 2022 23:51:02 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:51:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 29 Mar 2022 23:51:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 29 Mar 2022 23:51:19 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:51:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:51:19 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:a3ec12f55ff233e6960d51b1349a5884b1f2300e618a24dd458a986e0f24cec9`  
		Last Modified: Tue, 29 Mar 2022 01:08:10 GMT  
		Size: 189.0 MB (189046956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f70ba3b58f378805f2b9575b94e8f1f1c819ceff0c7bddcf6cf9329310b0d7`  
		Last Modified: Wed, 30 Mar 2022 00:11:18 GMT  
		Size: 60.0 MB (60030649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a185297c3cae557d4a1434b78dd735f382001ccdf1b1199016f825cbe4bf69`  
		Last Modified: Wed, 30 Mar 2022 00:11:10 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84aca573c01469f20392b76f3590610c2903e1a1389dc06496da3de75fb9980`  
		Last Modified: Wed, 30 Mar 2022 00:11:10 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6665dca5bb7a2c242690e4c4cbc8c0425fe7e50158f94bf476649430fa4bf0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279137489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce037c5b40b156dfdd93c383d029054d290c86aa3cc654e3c750799fad08f98b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:19:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 01:19:54 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:19:55 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:19:56 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 01:20:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:20:20 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 10:02:22 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 30 Mar 2022 10:02:22 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 10:02:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 30 Mar 2022 10:02:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 30 Mar 2022 10:02:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 10:02:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 10:02:45 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:93d3495a1ee24807a6fac4b6164fbb5252c3d749dcc59f0112467025450f9c60`  
		Last Modified: Tue, 29 Mar 2022 01:40:35 GMT  
		Size: 187.8 MB (187756733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d4946e6aa57e02eef3b42003aa89d299a11b4f8795e33fbaf0cf090554f28a`  
		Last Modified: Wed, 30 Mar 2022 10:29:02 GMT  
		Size: 60.0 MB (59954231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64581d607991208a952e5779da47fa6ac761a003f16b14ed39af1a0bf8d4d4b`  
		Last Modified: Wed, 30 Mar 2022 10:28:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411141d2db26b9000fc5ddc551ff8f8cb5ffe9f07d26403a12cb62b856ad569`  
		Last Modified: Wed, 30 Mar 2022 10:28:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
