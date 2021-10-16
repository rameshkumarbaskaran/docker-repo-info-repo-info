## `clojure:openjdk-17-boot-bullseye`

```console
$ docker pull clojure@sha256:2ad8680514f637d21fa4fe09e422163505e9e82f253540ce2ab916c8c791f7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f8dc30cc7d941569c546eaee86cbfbbe4b547791cee3b1116e8be4c3cc0291de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385660140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d303615d1236fb70c6769e8c300e4045c3de838b4ff15c29322128a198d3a255`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:42:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 15:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:29:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 12 Oct 2021 16:29:20 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:29:21 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 16:29:21 GMT
ENV JAVA_VERSION=17
# Tue, 12 Oct 2021 16:29:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Oct 2021 16:29:35 GMT
CMD ["jshell"]
# Wed, 13 Oct 2021 13:19:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 13 Oct 2021 13:19:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 13 Oct 2021 13:19:14 GMT
WORKDIR /tmp
# Wed, 13 Oct 2021 13:19:15 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 13 Oct 2021 13:19:15 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 13 Oct 2021 13:19:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 13 Oct 2021 13:19:34 GMT
RUN boot
# Wed, 13 Oct 2021 13:19:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b617c6a8c415a175f44d7e2c5d3b521059f2a6112c5f022e005a44a759f2d`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 5.2 MB (5153273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e17419b7ee61bbd89c2f0d2833a99cf45e594257d15cb567e4cf7771ce34a`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 10.9 MB (10871935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d2d81226a43a97871acd5afb7e8aabfad4d6b62ae1709c870df3ee230bc3f5`  
		Last Modified: Tue, 12 Oct 2021 15:53:13 GMT  
		Size: 54.6 MB (54567761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbae81fdbbf50b4f75c539f7e4ab9fa83b3fbad9f297ed467c5b05cae3a83872`  
		Last Modified: Tue, 12 Oct 2021 16:42:23 GMT  
		Size: 14.1 MB (14071834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97202075b49d620bce1b07a50c4d6cb2bb304b97ec089903ebacb527efc3269b`  
		Last Modified: Tue, 12 Oct 2021 16:45:32 GMT  
		Size: 187.3 MB (187250524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d8cf15d10944bbc85c0c1ebb3bdeab9294669c7e9bbc28938455531cea833b`  
		Last Modified: Wed, 13 Oct 2021 13:39:34 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b93a49b76f7645db3fd56ee5e289cb2ee7e834fe1c7ad574f7edf97cf745c`  
		Last Modified: Wed, 13 Oct 2021 13:39:37 GMT  
		Size: 58.8 MB (58820373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88e57a5f79c5f1a688d667a77bd065cb5ce22dce9e85ad84851f0602646b1c20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384481517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa4da16ce39cd3d988f1bfbd4ba02dd1b1bba19ec443772ad640413bd6d0401`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:04 GMT
ADD file:1529ae12e334fd992892d3fb97c103297cff7e0115b0475bec4c093939a2bff7 in / 
# Tue, 12 Oct 2021 01:41:04 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:58:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 16 Oct 2021 02:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 04:06:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 04:07:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 16 Oct 2021 04:07:57 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 04:07:58 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 04:07:59 GMT
ENV JAVA_VERSION=17
# Sat, 16 Oct 2021 04:08:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 16 Oct 2021 04:08:10 GMT
CMD ["jshell"]
# Sat, 16 Oct 2021 14:16:29 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Oct 2021 14:16:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Oct 2021 14:16:30 GMT
WORKDIR /tmp
# Sat, 16 Oct 2021 14:16:32 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 16 Oct 2021 14:16:32 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Oct 2021 14:16:33 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Oct 2021 14:16:46 GMT
RUN boot
# Sat, 16 Oct 2021 14:16:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1c47a423366578e5ce665d03788914bf0459485a627a27896fa9c5663ce55cdf`  
		Last Modified: Tue, 12 Oct 2021 01:47:41 GMT  
		Size: 53.6 MB (53603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889b1f128be8ebd64f787c46418ffe34ce1096d1ccd6938924d7397713720758`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 5.1 MB (5141861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c338d42ad921985fb8ebb6e2c48d381f6e03a91535eeffce7f08084b3dfbfdf4`  
		Last Modified: Sat, 16 Oct 2021 03:14:21 GMT  
		Size: 10.7 MB (10655847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27d3d9a061af78e3fcbefe5dbbe718db380687319e5ba8a7c9fd7ba55d16cc3`  
		Last Modified: Sat, 16 Oct 2021 03:14:43 GMT  
		Size: 54.7 MB (54669931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6184c33cbbd3e136683d125fb9cef775eb12f0f0e3140a8edc23406be025a964`  
		Last Modified: Sat, 16 Oct 2021 04:21:52 GMT  
		Size: 15.5 MB (15524863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f1505d3379c7792724ac992753a3e0194766ab549d21c3ee9e0a1c4af81cd`  
		Last Modified: Sat, 16 Oct 2021 04:23:50 GMT  
		Size: 186.1 MB (186063646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a213a61ebffccc0f7ff02681840ce9c04d03272cc42d642a9445029895b9b8`  
		Last Modified: Sat, 16 Oct 2021 14:31:23 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca223b7dc31caa608f3b000e614e1d1abfd932876290a07c749a0254cf98e3c3`  
		Last Modified: Sat, 16 Oct 2021 14:31:27 GMT  
		Size: 58.8 MB (58815454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
