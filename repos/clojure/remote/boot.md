## `clojure:boot`

```console
$ docker pull clojure@sha256:558824e6c67a2cce8aa24dc7be48ed59656a077178dd0b8abe9dea4dd953a1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:boot` - linux; amd64

```console
$ docker pull clojure@sha256:c1db5c221f7e6754288c7dcb5e347b2f0c793e2086eddd5cb254da17412cec5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380347301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9454dda26120cf8bfddba9fd67ddade84449dc165a8b9d0434f49fbc3269b0e9`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 15 May 2020 06:28:12 GMT
ADD file:fb54c709daa205bf9d04eb3d90ba068db4c34dfe3b6ec0d7691f677286120903 in / 
# Fri, 15 May 2020 06:28:13 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:32:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:32:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 17:32:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:02:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:02:20 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 21:02:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 15 May 2020 21:02:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:02:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 15 May 2020 21:02:22 GMT
ENV JAVA_VERSION=11.0.7
# Fri, 15 May 2020 21:02:22 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Fri, 15 May 2020 21:02:22 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Fri, 15 May 2020 21:02:39 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Fri, 15 May 2020 21:02:40 GMT
CMD ["jshell"]
# Tue, 02 Jun 2020 00:23:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 02 Jun 2020 00:23:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 02 Jun 2020 00:23:20 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:23:21 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 02 Jun 2020 00:23:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 02 Jun 2020 00:23:21 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 02 Jun 2020 00:23:40 GMT
RUN boot
# Tue, 02 Jun 2020 00:23:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:376057ac6fa17f65688c56977118e2e764b27c348b3f70637fa829cd2a12b200`  
		Last Modified: Fri, 15 May 2020 06:37:20 GMT  
		Size: 50.4 MB (50391294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a63a0a859d859478f30461786a49c2fca3ae7d89ab5b5ce3c81c54951d30f88`  
		Last Modified: Fri, 15 May 2020 17:50:44 GMT  
		Size: 7.8 MB (7812354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496548a8c952b37bdf149ab3654f9085d721ee126b8c73b16860778be5137f5e`  
		Last Modified: Fri, 15 May 2020 17:50:49 GMT  
		Size: 10.0 MB (9996284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adae3950d4d0f11875568c325d3d542d1f2e2d9b49bdd740bb57fcfc1f6478f`  
		Last Modified: Fri, 15 May 2020 17:51:06 GMT  
		Size: 51.8 MB (51827083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a297eafb9ac1e735f06c05d8ed0c60bbc1bf1ee8140e33d3011a3380c2061aa`  
		Last Modified: Fri, 15 May 2020 21:09:18 GMT  
		Size: 5.3 MB (5284714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a4142c5c9dde2fbf35e7a6e6475eba75a8c28540c375c80be7eade4b7cb438`  
		Last Modified: Fri, 15 May 2020 21:09:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e78d9befa393a5e54fedfb699d83945d057022433b067e247201dfd278fe17a`  
		Last Modified: Fri, 15 May 2020 21:09:38 GMT  
		Size: 196.2 MB (196208236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b1171cff5e3f60ea7d130a396f69e68bf8bdb5964b8d38dd3ca66ff0d082b2`  
		Last Modified: Tue, 02 Jun 2020 00:31:40 GMT  
		Size: 6.9 KB (6905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de199b7b11da87f7ddcde44e26dfdbc75875698850326df656ee8c935025d8e6`  
		Last Modified: Tue, 02 Jun 2020 00:31:44 GMT  
		Size: 58.8 MB (58820220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:baf7a7e7e4355de9e87218e99384ffa0ec5c5153af90411a75af17b5199de535
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (376953217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c9c4c5851e85d4d06d4bdca9b78d93ed604bc7e5aed7fc21dbe97dd6a81c6d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 15 May 2020 12:43:21 GMT
ADD file:be06dd722febf4e72f7e626f70029986a5c75880941cabd553f695dd66bcbaff in / 
# Fri, 15 May 2020 12:43:25 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:06:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:06:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 May 2020 20:07:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 23:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 23:04:41 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 23:04:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 15 May 2020 23:04:44 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 23:04:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 15 May 2020 23:04:46 GMT
ENV JAVA_VERSION=11.0.7
# Fri, 15 May 2020 23:04:47 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jdk_
# Fri, 15 May 2020 23:04:48 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Fri, 15 May 2020 23:05:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Fri, 15 May 2020 23:05:08 GMT
CMD ["jshell"]
# Mon, 01 Jun 2020 23:40:55 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 01 Jun 2020 23:40:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 01 Jun 2020 23:40:56 GMT
WORKDIR /tmp
# Mon, 01 Jun 2020 23:40:58 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 01 Jun 2020 23:40:59 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 01 Jun 2020 23:40:59 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 01 Jun 2020 23:41:37 GMT
RUN boot
# Mon, 01 Jun 2020 23:41:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d23bf71de5e1fea32788576972e233e80db7c51d831ed7edb269102dab298bf1`  
		Last Modified: Fri, 15 May 2020 12:53:11 GMT  
		Size: 49.2 MB (49170530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f6b089b3526111514262a58bbb27c5a292d7ef355184883365cdce9a7c61e5`  
		Last Modified: Fri, 15 May 2020 20:19:12 GMT  
		Size: 7.7 MB (7681693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34690136adb76fac1a121f6c4a9b5a63de1def4d65e0b2f99ff84c392ed8244`  
		Last Modified: Fri, 15 May 2020 20:19:13 GMT  
		Size: 10.0 MB (9983897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4287f76f52e4c390d78182615c75d2b3d6a5cd5b2c28dc554707a7cfbfa91f2b`  
		Last Modified: Fri, 15 May 2020 20:19:34 GMT  
		Size: 52.2 MB (52156755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5d569bcb572318c58ca67924282973af4990d289498fd736c8e7529dec254c`  
		Last Modified: Fri, 15 May 2020 23:09:27 GMT  
		Size: 5.3 MB (5276792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a677fbcec14bcca4d088f2e14ba5813a8b377563f9d369c5c4c68779a9ee304`  
		Last Modified: Fri, 15 May 2020 23:09:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8a38f600349c462adc19120b401cffc833bdf7d63a02e8b3af56ac8a11ac15`  
		Last Modified: Fri, 15 May 2020 23:09:59 GMT  
		Size: 193.9 MB (193855783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e51d0018f1d9b602d05287beea347b7642e008417804da80781df1ee02245`  
		Last Modified: Mon, 01 Jun 2020 23:44:36 GMT  
		Size: 6.9 KB (6907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbdea4e2919db7724aa8886017c839d24bf5978e8ee3486b5cbfc6e3d20af4d`  
		Last Modified: Mon, 01 Jun 2020 23:44:47 GMT  
		Size: 58.8 MB (58820648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
