## `clojure:openjdk-16-slim-buster`

```console
$ docker pull clojure@sha256:e6b9d6d1a3b8da6881073a1fb8005c2a86e26f0bfa289597022e6742dffc9eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:bf00eddf1fa59225108ca6228a5f1c104a01bee086a9f799520c1f9974dc1c6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231563303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc34482c9d312e61c63a940c211facf0bbf0101380416aa5f57e87d4a3f9b08`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:42:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Wed, 31 Mar 2021 05:42:21 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 05:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:42:22 GMT
ENV JAVA_VERSION=16
# Wed, 31 Mar 2021 05:42:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='e952958f16797ad7dc7cd8b724edd69ec7e0e0434537d80d6b5165193e33b931'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='273d3ae0ff14af801c5ffa71fd081f1cc505354f308ce11c77af55302c83d2bf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 31 Mar 2021 05:42:44 GMT
CMD ["jshell"]
# Thu, 01 Apr 2021 01:46:34 GMT
ENV LEIN_VERSION=2.9.5
# Thu, 01 Apr 2021 01:46:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Apr 2021 01:46:34 GMT
WORKDIR /tmp
# Thu, 01 Apr 2021 01:46:48 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Apr 2021 01:46:48 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Apr 2021 01:46:48 GMT
ENV LEIN_ROOT=1
# Thu, 01 Apr 2021 01:46:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Apr 2021 01:46:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875a154571f097680e56e5acc7383853036fac0e52855a4dd4fa740bfabf3f95`  
		Last Modified: Wed, 31 Mar 2021 05:52:39 GMT  
		Size: 3.3 MB (3268916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25e3fb0c0afb43054525a2b8d4ecb1b5f20c0cd85dc1bf702f2303d29033b29`  
		Last Modified: Wed, 31 Mar 2021 05:55:10 GMT  
		Size: 185.2 MB (185152917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b25c594d81f41848a14a6885228185ee70960254492b2cd366264a34d0b3a8`  
		Last Modified: Thu, 01 Apr 2021 02:05:02 GMT  
		Size: 11.8 MB (11798442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9892544b6c999f16bcefe8d7fa04d1848814dd054e33775963a872c04a4076be`  
		Last Modified: Thu, 01 Apr 2021 02:05:01 GMT  
		Size: 4.2 MB (4203735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cff5b1e99c82c1a402f936596e32452ae90aa9883c99d0c726d903de95c69ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224555135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae8672c9df2a0a50ee82071b9a47dd56d8cbdfc1c985011d176146477575c2f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:32:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Sat, 10 Apr 2021 01:32:09 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:32:10 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 01:32:11 GMT
ENV JAVA_VERSION=16
# Sat, 10 Apr 2021 01:32:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='e952958f16797ad7dc7cd8b724edd69ec7e0e0434537d80d6b5165193e33b931'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='273d3ae0ff14af801c5ffa71fd081f1cc505354f308ce11c77af55302c83d2bf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Apr 2021 01:32:38 GMT
CMD ["jshell"]
# Sat, 10 Apr 2021 18:28:11 GMT
ENV LEIN_VERSION=2.9.5
# Sat, 10 Apr 2021 18:28:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 10 Apr 2021 18:28:15 GMT
WORKDIR /tmp
# Sat, 10 Apr 2021 18:28:36 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 10 Apr 2021 18:28:37 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 10 Apr 2021 18:28:38 GMT
ENV LEIN_ROOT=1
# Sat, 10 Apr 2021 18:28:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Sat, 10 Apr 2021 18:28:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ed82b9f1018dd9b8a3d8ed771ba8773bd33481ce655abab47d10bd3034f05`  
		Last Modified: Sat, 10 Apr 2021 01:37:31 GMT  
		Size: 3.1 MB (3118914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2060ae0682d0558a56e5ee2dbbd2abbd6b90302bac0513d202ac7d790440b5`  
		Last Modified: Sat, 10 Apr 2021 01:38:57 GMT  
		Size: 179.5 MB (179529512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d8726ef65f8a24fa59c930319bc469e72071b3297d6d25a12c31956c8201c0`  
		Last Modified: Sat, 10 Apr 2021 18:37:27 GMT  
		Size: 11.8 MB (11798386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240315fecbf739bacd01ad8e59d576e5ddc29c5e8e633a884346776cf718f4e4`  
		Last Modified: Sat, 10 Apr 2021 18:37:26 GMT  
		Size: 4.2 MB (4203741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
