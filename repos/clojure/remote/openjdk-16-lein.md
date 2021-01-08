## `clojure:openjdk-16-lein`

```console
$ docker pull clojure@sha256:ba3e6a5f21d4e76d28b817cc674aeba46de40569aac69a0a97fe7f83ff6cd057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-lein` - linux; amd64

```console
$ docker pull clojure@sha256:ffd139fe03caac8add2d38a89f02f9fc2cc550dba831a4f448084a640421c82a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231541245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29af4b7ad1876a5f7a76d4ad13e39374bb48fc0e04b4120e35d38be3bb457e8c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 15:36:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 15:36:22 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 15:36:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Fri, 11 Dec 2020 15:36:22 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:36:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 08 Jan 2021 19:35:44 GMT
ENV JAVA_VERSION=16-ea+31
# Fri, 08 Jan 2021 19:36:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-aarch64_bin.tar.gz; 			downloadSha256=619122347e25dccbc419168329b659cdb1967570431bc09f597a791107484554; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-x64_bin.tar.gz; 			downloadSha256=f43aa41b3c71b9e278a37fd33a94579a8039e07abd21841ad9e1e0a4582abf24; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Jan 2021 19:36:01 GMT
CMD ["jshell"]
# Fri, 08 Jan 2021 20:10:53 GMT
ENV LEIN_VERSION=2.9.5
# Fri, 08 Jan 2021 20:10:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:10:54 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:11:05 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 08 Jan 2021 20:11:05 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:11:05 GMT
ENV LEIN_ROOT=1
# Fri, 08 Jan 2021 20:11:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 08 Jan 2021 20:11:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177617b11d133131d55a469644e5bcd4e402246268313630a2ae2b32b7a3bcf8`  
		Last Modified: Fri, 11 Dec 2020 15:43:03 GMT  
		Size: 3.2 MB (3248608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae219c900d801a6a0a49224b3347f4c57acf64592eb9d0631af88c939003ba`  
		Last Modified: Fri, 11 Dec 2020 15:43:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23634f0d3f113e9bbad847ae76ddff30bab16d9bd72a80b3ca9973b80f76b66b`  
		Last Modified: Fri, 08 Jan 2021 19:45:04 GMT  
		Size: 185.2 MB (185214688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36ebaac27c3601d16d4bc2da20e8da16625c756eeab3d9e439836ef1e5a614c`  
		Last Modified: Fri, 08 Jan 2021 20:16:06 GMT  
		Size: 11.8 MB (11798197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d4dfe1e843b95b4d48ccda82d7f89c3b9cf70dd5b471a5b3ef3e3a4cc31e29`  
		Last Modified: Fri, 08 Jan 2021 20:16:06 GMT  
		Size: 4.2 MB (4180248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7beb46b943412e0473faab17d376c7a20ec69757a12a8186ce35f38bb671bf4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224509961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300ec6978e812213bc9f95e884d67f817b87a4b756dee50f75d92f029e0a7364`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:08:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:08:44 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 17:08:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Fri, 11 Dec 2020 17:08:46 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 17:08:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 08 Jan 2021 19:44:55 GMT
ENV JAVA_VERSION=16-ea+31
# Fri, 08 Jan 2021 19:45:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-aarch64_bin.tar.gz; 			downloadSha256=619122347e25dccbc419168329b659cdb1967570431bc09f597a791107484554; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-x64_bin.tar.gz; 			downloadSha256=f43aa41b3c71b9e278a37fd33a94579a8039e07abd21841ad9e1e0a4582abf24; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Jan 2021 19:45:47 GMT
CMD ["jshell"]
# Fri, 08 Jan 2021 20:25:36 GMT
ENV LEIN_VERSION=2.9.5
# Fri, 08 Jan 2021 20:25:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:25:40 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:26:05 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "3601d55c4b5ac5c654e4ebd0d75abf7ad683f48cba8a7af1a8730b6590187b8a *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 08 Jan 2021 20:26:06 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:26:07 GMT
ENV LEIN_ROOT=1
# Fri, 08 Jan 2021 20:26:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 08 Jan 2021 20:26:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c25fa24001824e973532559552e813948d45a27f9f9f5af2c971a342c8be9e6`  
		Last Modified: Fri, 11 Dec 2020 17:15:22 GMT  
		Size: 3.1 MB (3101003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fccdbc841c29022496434a6931ffba3b0e753a49e80a169a782e0be509c0e1`  
		Last Modified: Fri, 11 Dec 2020 17:15:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0211d39fd7ab1fd354ac02b4480ab1ae94bcc5253f46c11698cd0f3f54944cc`  
		Last Modified: Fri, 08 Jan 2021 19:55:23 GMT  
		Size: 179.6 MB (179574039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3274fac01ff2b194b6827b9214c2b7d73fc6147a6ea0d592525e21795c8472`  
		Last Modified: Fri, 08 Jan 2021 20:32:17 GMT  
		Size: 11.8 MB (11798201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309dbf746e7b029053e75151ab8d984509994192c1aaad85edd4fb911a34d4c4`  
		Last Modified: Fri, 08 Jan 2021 20:32:16 GMT  
		Size: 4.2 MB (4180316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
