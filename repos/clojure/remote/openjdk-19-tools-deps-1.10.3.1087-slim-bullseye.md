## `clojure:openjdk-19-tools-deps-1.10.3.1087-slim-bullseye`

```console
$ docker pull clojure@sha256:922b80e7d64dfed3b93c2cab33223a59dba5d00570a95436134738c2f192f6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-tools-deps-1.10.3.1087-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:185c8f5856ea3a9923da6dc2d6b4276e8afe957aa0d35200ce8e7e6288742971
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286572806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966f676c25c353638e8f39fe89448c78bcff773bf43ea0430d1aa00d20d977fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Tue, 29 Mar 2022 00:52:16 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:52:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:52:29 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:53:24 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 29 Mar 2022 23:53:24 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:53:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 29 Mar 2022 23:53:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 29 Mar 2022 23:53:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:53:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:53:40 GMT
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
	-	`sha256:a4d100fc3e7b0dc5fbbf4534f7688cb06df0e07a6a9cdc51f10e7689f324fb53`  
		Last Modified: Tue, 29 Mar 2022 01:04:47 GMT  
		Size: 193.6 MB (193580462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e581a3522128b8f5b40e503a2a99eaf34eded5246b96f8148bded19a7623da`  
		Last Modified: Wed, 30 Mar 2022 00:13:03 GMT  
		Size: 60.0 MB (60030737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b29e3e2b545a24aec65a5dfcb559e6d717abb5a754a1796834b4cf6b7028f`  
		Last Modified: Wed, 30 Mar 2022 00:12:56 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16245713d97e0a6e19bedd25248f095f88b7dd867e1acec2487b5da463db123f`  
		Last Modified: Wed, 30 Mar 2022 00:12:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-tools-deps-1.10.3.1087-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae393c35160d414540b8cf722f0bc195814a1201ad60411e746568b5d4289cf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283627165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49714c37a393a2e792e5430d9a31d663aec70c8d775e962c7bfd195610092075`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Tue, 29 Mar 2022 01:18:15 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 01:18:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:18:32 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 10:05:21 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Wed, 30 Mar 2022 10:05:22 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 10:05:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 30 Mar 2022 10:05:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 30 Mar 2022 10:05:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 10:05:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 10:05:45 GMT
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
	-	`sha256:0a447b0d569e390a34c362c51161b1558896e102bb45aa429ff6677992dd6b1c`  
		Last Modified: Tue, 29 Mar 2022 01:38:11 GMT  
		Size: 192.2 MB (192246354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab786af2edbfd182be849147975bff98d95a39788d3a1995f0cfcfcf70c146`  
		Last Modified: Wed, 30 Mar 2022 10:30:59 GMT  
		Size: 60.0 MB (59954282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc166cb85fdca77864788a175084b1db510dbe40dd27ab67739295d841da6d9`  
		Last Modified: Wed, 30 Mar 2022 10:30:51 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f35d0e5da809c9fdbbfcdb329015babde20354512e9bc76b7e41d84126c2e1`  
		Last Modified: Wed, 30 Mar 2022 10:30:51 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
