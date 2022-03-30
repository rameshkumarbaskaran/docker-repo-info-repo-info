## `clojure:openjdk-18-lein-buster`

```console
$ docker pull clojure@sha256:6c7295cbafda25d14ff43e6ed794159b76c7b658cdabe3edcb746ddac255941e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-lein-buster` - linux; amd64

```console
$ docker pull clojure@sha256:1eb9c2e695210169d1b620b4dd07c95c1471cd064203e2879bb03c693b41d778
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339533454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a270ddcb1d78e835bfca419f22b2a8cb0441ba62ff038c4f957a41ede70f67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:31:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:08:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 29 Mar 2022 23:08:54 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:08:54 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:08:54 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 23:09:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:09:04 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:41:50 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 29 Mar 2022 23:41:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:41:50 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:41:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Tue, 29 Mar 2022 23:41:57 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:41:57 GMT
ENV LEIN_ROOT=1
# Tue, 29 Mar 2022 23:42:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 29 Mar 2022 23:42:00 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:42:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:42:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98d6bb51c7ccadb2f72a1498db713088ec7c3f449b3c810d95dbca6ba7511ba`  
		Last Modified: Tue, 29 Mar 2022 17:39:41 GMT  
		Size: 51.8 MB (51843446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3355592f16f1c7af5aaf7bf2b59b429fc6d54e6a9d493142700d424847989c58`  
		Last Modified: Tue, 29 Mar 2022 23:20:09 GMT  
		Size: 13.9 MB (13921230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da2c15b3a26cf50e1f2ba899e3b89c1414e379b23eed1fe114f1d2919fb72a9`  
		Last Modified: Tue, 29 Mar 2022 23:22:23 GMT  
		Size: 188.8 MB (188787724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1655c4b7d9e5337c9cc3319b07e7a1a957b9196ea07b8def6460c09184c2c534`  
		Last Modified: Wed, 30 Mar 2022 00:02:51 GMT  
		Size: 12.5 MB (12481916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e239900581ea3f39d3fd103cf1bb0d8381a4a1c760f4a93f7f645eeae0ff363`  
		Last Modified: Wed, 30 Mar 2022 00:02:51 GMT  
		Size: 4.2 MB (4207228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2f2ca862a6a7e278be841c21addcfcc5645df8cfeaf0f523165b2991cf8135`  
		Last Modified: Wed, 30 Mar 2022 00:02:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-lein-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37d664cab4efb12d23fdfa966f134e119e297f84e512dbf36b383582edada711
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337716819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda8a6eb25f3a03882d379219bf5e44cccbeb5ca789e8cf74c4dcda111fc22f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 09:01:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 30 Mar 2022 09:01:38 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 09:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 09:01:40 GMT
ENV JAVA_VERSION=18
# Wed, 30 Mar 2022 09:01:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 09:01:53 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 09:49:07 GMT
ENV LEIN_VERSION=2.9.8
# Wed, 30 Mar 2022 09:49:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 30 Mar 2022 09:49:08 GMT
WORKDIR /tmp
# Wed, 30 Mar 2022 09:49:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Wed, 30 Mar 2022 09:49:21 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 30 Mar 2022 09:49:22 GMT
ENV LEIN_ROOT=1
# Wed, 30 Mar 2022 09:49:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Wed, 30 Mar 2022 09:49:28 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 30 Mar 2022 09:49:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 30 Mar 2022 09:49:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bff08cf9734159a77ecf001874bfd910561517c9c87811003564d4a2f00421`  
		Last Modified: Wed, 30 Mar 2022 02:25:51 GMT  
		Size: 52.2 MB (52174968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b271ee6d3652db1e127606e48dbdddd1d0197d93f24fe910a41298350932c02d`  
		Last Modified: Wed, 30 Mar 2022 09:20:58 GMT  
		Size: 14.7 MB (14671177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea71f16da2d66db91f1e7c288f5015cae0a94c0483076e4667b58d94e31e5e37`  
		Last Modified: Wed, 30 Mar 2022 09:23:38 GMT  
		Size: 187.7 MB (187710651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f965fddf27efa4da69b37fe651db16204985a27e0794368d53dd5f7d528f58d1`  
		Last Modified: Wed, 30 Mar 2022 10:18:19 GMT  
		Size: 12.2 MB (12239832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c2d5bfc1fd0db3eb11240906f5a3378cd16ccc89eff58d33037fbf54e68cc5`  
		Last Modified: Wed, 30 Mar 2022 10:18:19 GMT  
		Size: 4.2 MB (4207113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5fc2f4aeb766ad8d0cefe4afefc88535ac995c635d6ff98c202b7a522245`  
		Last Modified: Wed, 30 Mar 2022 10:18:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
