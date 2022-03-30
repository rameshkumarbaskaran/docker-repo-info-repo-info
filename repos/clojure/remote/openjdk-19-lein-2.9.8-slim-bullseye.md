## `clojure:openjdk-19-lein-2.9.8-slim-bullseye`

```console
$ docker pull clojure@sha256:69fd75cab55ca36bf7e7acdd858849f5e23ace185958bbc9ecb940bd38b8a9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-lein-2.9.8-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:420baa5a59080ae82a38cf958f243567b4762e812d67f22d3d801e71c5e979b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242609929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f51abe8d924bfab61926a08920143f4d7d42626d5166fbbc0bc3eeea8d0e7`
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
# Tue, 29 Mar 2022 00:52:16 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:52:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:52:29 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:51:32 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 29 Mar 2022 23:51:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:51:32 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:51:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 29 Mar 2022 23:51:42 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:51:42 GMT
ENV LEIN_ROOT=1
# Tue, 29 Mar 2022 23:51:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 29 Mar 2022 23:51:46 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:51:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:51:46 GMT
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
	-	`sha256:a4d100fc3e7b0dc5fbbf4534f7688cb06df0e07a6a9cdc51f10e7689f324fb53`  
		Last Modified: Tue, 29 Mar 2022 01:04:47 GMT  
		Size: 193.6 MB (193580462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7435cf11385fdd852b8d05fa42e91dc389ae828c8875efb0da3798b55e68793`  
		Last Modified: Wed, 30 Mar 2022 00:11:54 GMT  
		Size: 11.9 MB (11861312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93d1dbee748338645b11da8aa607c512b1d3b01180bb31e7bac1e0a99b63eea`  
		Last Modified: Wed, 30 Mar 2022 00:11:53 GMT  
		Size: 4.2 MB (4207171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b78aeb31ec425eeda7360ec8d2d30677793f513b8b0c17d1af0013ffa2a040`  
		Last Modified: Wed, 30 Mar 2022 00:11:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-lein-2.9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da4d91518367b01be35d998ef27030ceebd47291a7aa2811af7ab7f2fa1031d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239524610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977aa7d8bb43be395c91f301850e457a0d4e9eef38e2587b4a6d53c9df3b6914`
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
# Tue, 29 Mar 2022 01:18:15 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 01:18:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:18:32 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 10:03:13 GMT
ENV LEIN_VERSION=2.9.8
# Wed, 30 Mar 2022 10:03:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 10:03:15 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 10:03:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 30 Mar 2022 10:03:27 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 30 Mar 2022 10:03:28 GMT
ENV LEIN_ROOT=1
# Wed, 30 Mar 2022 10:03:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Wed, 30 Mar 2022 10:03:35 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 10:03:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 10:03:36 GMT
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
	-	`sha256:0a447b0d569e390a34c362c51161b1558896e102bb45aa429ff6677992dd6b1c`  
		Last Modified: Tue, 29 Mar 2022 01:38:11 GMT  
		Size: 192.2 MB (192246354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445b3efb0e28ed9195d644db1124c3408b18984b217426a3245f779996b22ad1`  
		Last Modified: Wed, 30 Mar 2022 10:29:44 GMT  
		Size: 11.6 MB (11645244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec2c8123e2b8da95690f8fea1b8ff7a70e1ad62c143ae51cf64f2b024d1a660`  
		Last Modified: Wed, 30 Mar 2022 10:29:43 GMT  
		Size: 4.2 MB (4207107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fba64d1025ef91e5b16ef019daa12dadc0a21c0fa2c992ba5aea2625805eae`  
		Last Modified: Wed, 30 Mar 2022 10:29:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
