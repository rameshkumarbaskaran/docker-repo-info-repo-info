## `clojure:openjdk-17-boot-slim-buster`

```console
$ docker pull clojure@sha256:4dd6a891b39ccebeaee3eb9b3cb45e341befa6cb29471859c321c72b2e4bdca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:04319adf90b5e6aff3459b14afb30a34773450b412c8b30b2be2ca1e082c976e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (277044389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7353c63d0e2582b733b4adb089f6c7cd4f122d3ec7e9c5ab91fe8819c2569502`
-	Default Command: `["boot","repl"]`

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
# Mon, 14 Jun 2021 21:52:04 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Jun 2021 21:52:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:52:05 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:52:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 14 Jun 2021 21:52:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:52:10 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Jun 2021 21:52:31 GMT
RUN boot
# Mon, 14 Jun 2021 21:52:31 GMT
CMD ["boot" "repl"]
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
	-	`sha256:f338836d6940119b16a1619a244f410da770422f6bc95dc2293f989b17950502`  
		Last Modified: Mon, 14 Jun 2021 21:56:22 GMT  
		Size: 279.8 KB (279763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4c8728fdbbb0fab80d6b071050f68656bcba75fc8e985a4dd1369ba240b73c`  
		Last Modified: Mon, 14 Jun 2021 21:56:25 GMT  
		Size: 58.8 MB (58820521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5abb335e68316a2746b1c13c0b126041166be03386f9ff25af82b809df41961
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274483624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ab34bfe8ae84071cb52d8f259da5bee678fe9be57b80e892068918f8f0ee93`
-	Default Command: `["boot","repl"]`

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
# Mon, 14 Jun 2021 21:22:44 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Jun 2021 21:22:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Jun 2021 21:22:45 GMT
WORKDIR /tmp
# Mon, 14 Jun 2021 21:22:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 14 Jun 2021 21:22:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Jun 2021 21:22:50 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Jun 2021 21:23:26 GMT
RUN boot
# Mon, 14 Jun 2021 21:23:26 GMT
CMD ["boot" "repl"]
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
	-	`sha256:8fabf27a20b68f63919d3b12f570dae743557ae3b0fcb68c939038ec756ed442`  
		Last Modified: Mon, 14 Jun 2021 21:29:03 GMT  
		Size: 279.6 KB (279560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c4a48bebdaa0da55869d89ae30b1307ff31210d35e453b1b5bcd1f6ddb6438`  
		Last Modified: Mon, 14 Jun 2021 21:29:07 GMT  
		Size: 58.8 MB (58820907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
