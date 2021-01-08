## `clojure:openjdk-16-boot-slim-buster`

```console
$ docker pull clojure@sha256:b0ecd4195e5e45af5ff06d8b7ec3ce2d19ec91182a9806fae67dfc8da0717354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:86472a403e74803ddbffc5b71b437b030024e4d9eb820e47c7c0a754afaea08f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274662674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebcd34c21a671b77fae926f4cad5eb9a342d14155297bbe3d457380a3e8a2fb`
-	Default Command: `["boot","repl"]`

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
# Fri, 08 Jan 2021 20:11:32 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 08 Jan 2021 20:11:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:11:32 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:11:37 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 08 Jan 2021 20:11:37 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:11:38 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 08 Jan 2021 20:11:57 GMT
RUN boot
# Fri, 08 Jan 2021 20:11:57 GMT
CMD ["boot" "repl"]
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
	-	`sha256:8cb9ab69eb3d17107f5f9d5f0b3696ed6c498cad4a89b48801a20f06559a053d`  
		Last Modified: Fri, 08 Jan 2021 20:16:24 GMT  
		Size: 279.6 KB (279612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b9fdfbe6f9ce561a82926d102b6f60251d4f88ffe5c7e79bb04b557a1fcb5f`  
		Last Modified: Fri, 08 Jan 2021 20:16:31 GMT  
		Size: 58.8 MB (58820262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6409baff889711895cc124fb30df498caa971251f3e19a67aae6e07c8b9193cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267631611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dc9a11a0db5ad8915a1ffe38231a32aee4ed0ff50d8e1d666005fd4cd65c86`
-	Default Command: `["boot","repl"]`

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
# Fri, 08 Jan 2021 20:27:00 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 08 Jan 2021 20:27:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:27:02 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:27:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 08 Jan 2021 20:27:12 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:27:12 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 08 Jan 2021 20:27:50 GMT
RUN boot
# Fri, 08 Jan 2021 20:27:50 GMT
CMD ["boot" "repl"]
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
	-	`sha256:6fc8bb2977a2743f42d7507c6f73252085bc3f25eb58de0a45b9cb5a742a15e5`  
		Last Modified: Fri, 08 Jan 2021 20:32:49 GMT  
		Size: 279.5 KB (279541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230f1de05993880ecc390a6ce27ece78d3be7de2ec790f0b344c859fa4ae6f4d`  
		Last Modified: Fri, 08 Jan 2021 20:32:57 GMT  
		Size: 58.8 MB (58820626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
