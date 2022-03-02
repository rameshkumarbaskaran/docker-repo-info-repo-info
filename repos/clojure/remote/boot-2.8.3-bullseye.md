## `clojure:boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:88f21357d29c319b4bdf65c241cdea3428062d938bf5cad57993b3a1efc3a643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0e5b67c49c9afdd5c1e0b82d359fdce197d171e3101a74483399875d1087e90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (387047828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63167d0881ac5a6419cf9707355f07147a3522bb0954daaf06dbe5db72a14907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:22:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 26 Jan 2022 09:22:01 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:22:01 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:22:01 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 26 Jan 2022 09:22:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:22:23 GMT
CMD ["jshell"]
# Thu, 27 Jan 2022 17:14:31 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 27 Jan 2022 17:14:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 27 Jan 2022 17:14:31 GMT
WORKDIR /tmp
# Thu, 27 Jan 2022 17:14:35 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Thu, 27 Jan 2022 17:14:36 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 27 Jan 2022 17:14:36 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 27 Jan 2022 17:14:58 GMT
RUN boot
# Thu, 27 Jan 2022 17:14:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 27 Jan 2022 17:14:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 27 Jan 2022 17:14:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461bb1d8c517c7f9fc0f1df66c9dc34c85a23421c1e1c540b2e28cbb258e75f5`  
		Last Modified: Wed, 26 Jan 2022 02:22:32 GMT  
		Size: 54.6 MB (54567492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ddade05c6dd5758c84ccfe52565f03e4d06ba792c42872aea370294d37c825`  
		Last Modified: Wed, 26 Jan 2022 09:40:55 GMT  
		Size: 14.1 MB (14071678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24ac58c934aead474e40ae517732aa6fc3ad44e31ceb73afcfb77660803e43c`  
		Last Modified: Wed, 26 Jan 2022 09:47:36 GMT  
		Size: 187.6 MB (187628670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb1d594e56295450093b48039eb60cff223870c15e8f822423d8bfa2b444741`  
		Last Modified: Thu, 27 Jan 2022 17:35:44 GMT  
		Size: 1.0 MB (1017271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5520ad840dbea2bb6c667d1a1be64db65e2cd8e822e7617bc4b191f70bfd4676`  
		Last Modified: Thu, 27 Jan 2022 17:35:48 GMT  
		Size: 58.8 MB (58820680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2256faff3757393785348b0141295e26a7da2a2ddb4ca735922ad5ed8fee2966`  
		Last Modified: Thu, 27 Jan 2022 17:35:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:463ee3126ddad41920a893664fdfd3c4a1c303b1fc589c1430ef12b757e134e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385668517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769001f592a707016b8b77035eff084c96655cbde486b9b504adedaa08cb5c97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:12 GMT
ADD file:9d66afa8fc90803d689e087b38b38a3bd58d0434b495ca4165ca520e73bccf55 in / 
# Tue, 01 Mar 2022 02:11:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:52:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 01 Mar 2022 13:52:07 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:52:08 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 13:52:09 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 01 Mar 2022 13:52:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:52:23 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:44:03 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Mar 2022 08:44:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Mar 2022 08:44:04 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:44:09 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 02 Mar 2022 08:44:09 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Mar 2022 08:44:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Mar 2022 08:44:23 GMT
RUN boot
# Wed, 02 Mar 2022 08:44:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:44:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:44:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c7869242ae9abf6340558e18846f64a05eb06f2eaf66c6bfa2dc66ff2c997976`  
		Last Modified: Tue, 01 Mar 2022 02:17:52 GMT  
		Size: 53.6 MB (53608753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9880592b351f34fa791bd7749a127063cd6a76b1190bd059c168696d700f6b04`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 5.1 MB (5141642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9934a374f1ba93d2da0983d2aac86c9b4bf6ca063aa108519d2588e0212ac`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 10.7 MB (10655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37be3698694527b9e5af78494bbcb68f6b045af5247de8c988b24ef7dcd877e`  
		Last Modified: Tue, 01 Mar 2022 10:44:48 GMT  
		Size: 54.7 MB (54671139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5dc6dcc457fec75c4796decb43a2b4f5f0bfce35e577de9171e96fb39eeee4`  
		Last Modified: Tue, 01 Mar 2022 14:12:17 GMT  
		Size: 15.5 MB (15524992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489ba763cf51566e878bf1172b7219d4d1ad7a5a98cb8caf4afaa7a789d9d69d`  
		Last Modified: Tue, 01 Mar 2022 14:18:01 GMT  
		Size: 186.5 MB (186472880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569ff01813bd5b168ca520766b99bbc0fc03d436c1f7d7f1889fd9a3d63763cd`  
		Last Modified: Wed, 02 Mar 2022 09:12:53 GMT  
		Size: 777.3 KB (777307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b63cf62c41f292f503811806eef763a69675749327b363e690dd5d577e90fe`  
		Last Modified: Wed, 02 Mar 2022 09:12:57 GMT  
		Size: 58.8 MB (58815535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600832c359bfcbca287a2d191f47f0122529ffd4d22ce0beeca1f08039ac0f45`  
		Last Modified: Wed, 02 Mar 2022 09:12:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
