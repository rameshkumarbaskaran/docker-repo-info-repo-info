## `clojure:openjdk-17`

```console
$ docker pull clojure@sha256:0ebbaa77c69b8ead6f1afd582cc7feef95e5ee3efe94bcdd127b862b9489dd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17` - linux; amd64

```console
$ docker pull clojure@sha256:44ea2d9ba8fb624d27e388146fa07d70a8109e7ba29df32b5f00c9544ab0eded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233935525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fe54bbd960c48b816df77efb6c77114783175075da9a6d8f54cafc3d4ad456`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:01:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 23 Jun 2021 08:01:12 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 08:01:12 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jul 2021 19:27:19 GMT
ENV JAVA_VERSION=17-ea+29
# Fri, 02 Jul 2021 19:27:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c277cda62e368aa595450d3ffa018fbe98adc97c08e0ab777f5f74e86e3bf3f3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='8d5901a58b02e77d255166678c54cdc14c293d17730d794d70bb13434a934bb4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Jul 2021 19:27:33 GMT
CMD ["jshell"]
# Fri, 02 Jul 2021 20:41:21 GMT
ENV LEIN_VERSION=2.9.6
# Fri, 02 Jul 2021 20:41:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Jul 2021 20:41:22 GMT
WORKDIR /tmp
# Fri, 02 Jul 2021 20:41:40 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Jul 2021 20:41:40 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jul 2021 20:41:40 GMT
ENV LEIN_ROOT=1
# Fri, 02 Jul 2021 20:41:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Jul 2021 20:41:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee45ae9730633057cf9bd12924f9a1bf2b590631d3d085b14c96f4466557794`  
		Last Modified: Wed, 23 Jun 2021 08:12:04 GMT  
		Size: 3.3 MB (3268886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb8e9f570c359ade64ca79840f3b6c3cf805683c6baf3dc3ccd66ef3de27253`  
		Last Modified: Fri, 02 Jul 2021 19:37:24 GMT  
		Size: 187.5 MB (187513983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954c0cffc6a0b53988ad04d1deb1d50ff94b3612a91009eeffda7e054486d66c`  
		Last Modified: Fri, 02 Jul 2021 20:47:54 GMT  
		Size: 11.8 MB (11803074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffaf90fc4d9f4ea93dea5b44291d9bfc462688da7da6a9ed2c945c52012e045`  
		Last Modified: Fri, 02 Jul 2021 20:47:54 GMT  
		Size: 4.2 MB (4203731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e5918f6133dd513c61e9cd81e40e6f973242c86696a35f27f5ae17ed28c8d2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231368819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3056007c8ba54089c3274889bb8c1ae4b90d9b6a4770cad29b07c11fedd784`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:57:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 23 Jun 2021 04:57:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 04:57:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jul 2021 19:33:32 GMT
ENV JAVA_VERSION=17-ea+29
# Fri, 02 Jul 2021 19:33:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c277cda62e368aa595450d3ffa018fbe98adc97c08e0ab777f5f74e86e3bf3f3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='8d5901a58b02e77d255166678c54cdc14c293d17730d794d70bb13434a934bb4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Jul 2021 19:33:46 GMT
CMD ["jshell"]
# Fri, 02 Jul 2021 21:32:06 GMT
ENV LEIN_VERSION=2.9.6
# Fri, 02 Jul 2021 21:32:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Jul 2021 21:32:06 GMT
WORKDIR /tmp
# Fri, 02 Jul 2021 21:32:21 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Jul 2021 21:32:21 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jul 2021 21:32:21 GMT
ENV LEIN_ROOT=1
# Fri, 02 Jul 2021 21:32:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Jul 2021 21:32:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5c013aa648ff2c30dafc35db9efb2faa7f9fa6f1c98a2f31c1b5fee0334dc`  
		Last Modified: Wed, 23 Jun 2021 05:11:10 GMT  
		Size: 3.1 MB (3118894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4510388e2a517a9bf344b2e92523cda174ea6ce69f295436ef4db499ef0c8`  
		Last Modified: Fri, 02 Jul 2021 19:50:21 GMT  
		Size: 186.3 MB (186328337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a2eba2a5ffa9eb821266dc0f93c8eabdf8d8247944d57015b8aa9f82e41c2c`  
		Last Modified: Fri, 02 Jul 2021 21:38:15 GMT  
		Size: 11.8 MB (11802892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bd68cb5c8888bbe68a434c581e71e9a4678775d5a3e7ac50a9d0156419a6b1`  
		Last Modified: Fri, 02 Jul 2021 21:38:14 GMT  
		Size: 4.2 MB (4203703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
