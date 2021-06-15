## `clojure:openjdk-17-lein`

```console
$ docker pull clojure@sha256:5adffa87165a29be7336a1a80e4a07da0d17c6982e1b61958a8b7705979ebd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-lein` - linux; amd64

```console
$ docker pull clojure@sha256:9863ba50001251163e11bf1dba5bccfb2b8e157f9f8a38e6c6d8f249066d1351
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233950850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732399f66218558c7853504bbaccaad3e3b377f6d6bc1bc18c9d38783bf14a01`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:48:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:48:04 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:48:04 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 21:23:37 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:23:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:23:51 GMT
CMD ["jshell"]
# Mon, 14 Jun 2021 21:51:29 GMT
ENV LEIN_VERSION=2.9.6
# Mon, 14 Jun 2021 21:51:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:51:30 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:51:41 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Mon, 14 Jun 2021 21:51:41 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:51:41 GMT
ENV LEIN_ROOT=1
# Mon, 14 Jun 2021 21:51:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Mon, 14 Jun 2021 21:51:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b89b6081832b112f9483322d4710c661f12135e79279dc3fb1672883ada8d`  
		Last Modified: Wed, 12 May 2021 06:58:18 GMT  
		Size: 3.3 MB (3268772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30878168e6092e8e5d16a7dbb8ba57a5a3a41002bba73dbcb08a8198ba17e632`  
		Last Modified: Mon, 14 Jun 2021 21:33:26 GMT  
		Size: 187.5 MB (187529418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8e442a1fd3c013cb9f056b5b5efee10ec0cc4d681c63c83bbddfc8669da105`  
		Last Modified: Mon, 14 Jun 2021 21:55:47 GMT  
		Size: 11.8 MB (11803035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729f8155366d11799c1538da7d38d387274ccf22ed218f8feb05a5ae2c94f803`  
		Last Modified: Mon, 14 Jun 2021 21:55:47 GMT  
		Size: 4.2 MB (4203710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c1334ac8ea90557975b2a94b5049a36a69ebc12827c67807e5d0b836e07c131e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231389714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7be4d406eb8bee647448b4e3a1ebf5eb764a639a0699b3a091db9a69538916`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 12 May 2021 00:52:19 GMT
ADD file:91ba1791cab3ad29a1469d1e78f21f4c0b5d3d30598683b7104980604c318854 in / 
# Wed, 12 May 2021 00:52:34 GMT
CMD ["bash"]
# Thu, 27 May 2021 08:38:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 08:38:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 27 May 2021 08:38:57 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 08:38:57 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 20:45:19 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 20:45:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:45:33 GMT
CMD ["jshell"]
# Mon, 14 Jun 2021 21:22:00 GMT
ENV LEIN_VERSION=2.9.6
# Mon, 14 Jun 2021 21:22:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:22:00 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:22:10 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Mon, 14 Jun 2021 21:22:11 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:22:11 GMT
ENV LEIN_ROOT=1
# Mon, 14 Jun 2021 21:22:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Mon, 14 Jun 2021 21:22:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fcad0c936ea5c12e1c8c4edb81a97c0cde04ee71e7067ee3b246474cf1854d7a`  
		Last Modified: Wed, 12 May 2021 01:02:02 GMT  
		Size: 25.9 MB (25911250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb067f13654098b66e57229fcd818a7d0f0c73bd34d158e3bedc28ee2a7b821`  
		Last Modified: Thu, 27 May 2021 08:54:42 GMT  
		Size: 3.1 MB (3118848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd150995e7b7fd282c78e58248bc8bab3e95a04a8352b9814af8db2a9208bdc5`  
		Last Modified: Mon, 14 Jun 2021 21:01:52 GMT  
		Size: 186.4 MB (186353059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8226b0568e1a1edad9035c215caf33939e2d7298e177e5427e1946a78d8da3`  
		Last Modified: Mon, 14 Jun 2021 21:28:21 GMT  
		Size: 11.8 MB (11802879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920028ccc4229dd9d31cb1233a6277cea8aa8a87ab0ba7886cf9ea989dba2d1e`  
		Last Modified: Mon, 14 Jun 2021 21:28:20 GMT  
		Size: 4.2 MB (4203678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
