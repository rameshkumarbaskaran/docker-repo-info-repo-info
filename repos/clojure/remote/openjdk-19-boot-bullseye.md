## `clojure:openjdk-19-boot-bullseye`

```console
$ docker pull clojure@sha256:3c9ea50b62b9cdd98da7aee46fb363a6ddb5b3a7ad65b572a3ca3975b12e0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f45fcc986f476cf01faf89703ed545ed4faca7b38ee9269f5dab6067db7846d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 MB (391335481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e8e48773a101741604fe6a942419e19322980c79f45829e4f87314dcee5357`
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
# Tue, 01 Mar 2022 13:47:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:47:34 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:47:35 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 08:05:13 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 08:05:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 08:05:27 GMT
CMD ["jshell"]
# Wed, 02 Mar 2022 08:49:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Mar 2022 08:49:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Mar 2022 08:49:22 GMT
WORKDIR /tmp
# Wed, 02 Mar 2022 08:49:26 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 02 Mar 2022 08:49:27 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Mar 2022 08:49:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Mar 2022 08:49:41 GMT
RUN boot
# Wed, 02 Mar 2022 08:49:43 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Mar 2022 08:49:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Mar 2022 08:49:44 GMT
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
	-	`sha256:e08a2ca54d2541fac4c87e0727675fd36abf45919333874cea89202b98d860d9`  
		Last Modified: Wed, 02 Mar 2022 08:19:48 GMT  
		Size: 192.1 MB (192139444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989509b3f9a1aa49a5e34bdb2dfef44b3cff1943ed01ac692a56e70b5155e1ae`  
		Last Modified: Wed, 02 Mar 2022 09:18:26 GMT  
		Size: 777.3 KB (777313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60e0c3d051ac9abd51e154f7da34160a517e874c59a4e588077d6e31e2db010`  
		Last Modified: Wed, 02 Mar 2022 09:18:31 GMT  
		Size: 58.8 MB (58815931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97f9c7ec37b147db2d570f3ccfaaf029c2eb3e0cc614dd14e67adb8c83d8791`  
		Last Modified: Wed, 02 Mar 2022 09:18:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
