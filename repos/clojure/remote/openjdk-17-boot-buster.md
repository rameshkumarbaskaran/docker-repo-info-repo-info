## `clojure:openjdk-17-boot-buster`

```console
$ docker pull clojure@sha256:5d8e8901e4b509fd59d7b3641d14a9cfa27380bf5e2b93b5235eeef2c144c716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:9a548ce2606f118bd3b28e5bafe830e94ffe14b21ab370ef1b1729d667bb7db0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (378955976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec30a98c6a94e86e1664cb72dd9d214fd93fa6c034476d5e350d084fea40b3b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 12:44:08 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:44:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Apr 2021 23:21:39 GMT
ENV JAVA_VERSION=17-ea+19
# Mon, 26 Apr 2021 23:21:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='76ee253e411ed65c8166b48d36a9db9e77eea45ef61db577530faee399e0d441'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='313ee29d3a5620edab331814ee4fb9dd7090945cc0afeaf73a3e2e43c907afb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 26 Apr 2021 23:21:56 GMT
CMD ["jshell"]
# Tue, 27 Apr 2021 00:03:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 27 Apr 2021 00:03:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 27 Apr 2021 00:03:39 GMT
WORKDIR /tmp
# Tue, 27 Apr 2021 00:03:41 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 27 Apr 2021 00:03:41 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 27 Apr 2021 00:03:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 27 Apr 2021 00:04:00 GMT
RUN boot
# Tue, 27 Apr 2021 00:04:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37aabde37b87d272286df45e6a3145b0884b72e07e657bf1a2a1e74a92c6172`  
		Last Modified: Sat, 10 Apr 2021 02:02:22 GMT  
		Size: 51.8 MB (51841093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4aa53f9ffbf7bd8ebaa551102ae5146025c9f5063b12dda7d8d42de26e2ebcd`  
		Last Modified: Sat, 10 Apr 2021 12:53:45 GMT  
		Size: 13.9 MB (13921315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018e023aa1d6407cd32de1dbc811353dbebb924845f3dabeaf9dbf6ad5bc88f1`  
		Last Modified: Mon, 26 Apr 2021 23:28:19 GMT  
		Size: 186.1 MB (186103200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4188941df3f00f554945810a6a3dfcf3f95047d7a4323d4dec151ff8e4721f`  
		Last Modified: Tue, 27 Apr 2021 00:08:30 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d41262a45dc82db47750868721afc0a5c359dc3fba43e03853f3ed35a90c9d`  
		Last Modified: Tue, 27 Apr 2021 00:08:33 GMT  
		Size: 58.8 MB (58820348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd6cf2ddbaf4642627d75b0a56afc4bf378d0878d8b385cec2ba23d79cc5bf7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.8 MB (374752673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3b6dee3c56b5b273bdc6f62ce6fe07830730af149dd25c92e87be35a3f8f5c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:01:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 23:01:17 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 23:01:18 GMT
ENV LANG=C.UTF-8
# Mon, 26 Apr 2021 23:45:48 GMT
ENV JAVA_VERSION=17-ea+19
# Mon, 26 Apr 2021 23:46:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='76ee253e411ed65c8166b48d36a9db9e77eea45ef61db577530faee399e0d441'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='313ee29d3a5620edab331814ee4fb9dd7090945cc0afeaf73a3e2e43c907afb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 26 Apr 2021 23:46:08 GMT
CMD ["jshell"]
# Tue, 27 Apr 2021 00:31:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 27 Apr 2021 00:31:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 27 Apr 2021 00:31:18 GMT
WORKDIR /tmp
# Tue, 27 Apr 2021 00:31:22 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 27 Apr 2021 00:31:23 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 27 Apr 2021 00:31:24 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 27 Apr 2021 00:31:47 GMT
RUN boot
# Tue, 27 Apr 2021 00:31:49 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1cf823a7fca9771e278355d8924fac8d9cef1f8e3ecbc87332c4859d1d4f`  
		Last Modified: Sat, 10 Apr 2021 02:01:23 GMT  
		Size: 52.2 MB (52167974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c00066088349286faa32311c9ea25724917bd388d9a9fdf3b8b0235bfcd5cac`  
		Last Modified: Sat, 10 Apr 2021 23:07:43 GMT  
		Size: 14.7 MB (14673668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9017d7c0522744924f4989de97a936fcbf292cf6ccaf8cb5b6e59a7f7b37467d`  
		Last Modified: Mon, 26 Apr 2021 23:52:21 GMT  
		Size: 182.2 MB (182178581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b14715bb6f928ac64a0f63d98bbc355edc2b17a065dab351b5e453d4f6bdb1a`  
		Last Modified: Tue, 27 Apr 2021 00:37:00 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6236ca6e90055644ada1a4ea68be1ed173362d46d0e9056873c6ba857adce8`  
		Last Modified: Tue, 27 Apr 2021 00:37:06 GMT  
		Size: 58.8 MB (58820239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
