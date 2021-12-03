## `clojure:openjdk-18-tools-deps-buster`

```console
$ docker pull clojure@sha256:4019db21a5d749a057eb5b43ec018a049d8b6535454e3ad593cc31f788ef870f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-buster` - linux; amd64

```console
$ docker pull clojure@sha256:441a4bcfeb572532664520ccb3e727045f7694d498096a04a6a96880acd1135f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350659525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48a5c41906bb413b79696cc9140140955b89237c0dbedb1bd4dc001dc1b92ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:15:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:16:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:24:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 09:24:31 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:24:32 GMT
ENV LANG=C.UTF-8
# Tue, 30 Nov 2021 04:44:51 GMT
ENV JAVA_VERSION=18-ea+25
# Tue, 30 Nov 2021 04:45:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 30 Nov 2021 04:45:03 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 10:16:16 GMT
ENV CLOJURE_VERSION=1.10.3.1020
# Tue, 30 Nov 2021 10:16:16 GMT
WORKDIR /tmp
# Tue, 30 Nov 2021 10:16:28 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "afc87e2c8cfbf87e43553439c69a4c8e36bc2094405d08f39ca542b4cca0920a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Thu, 02 Dec 2021 02:33:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Dec 2021 02:33:35 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 Dec 2021 02:33:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 Dec 2021 02:33:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17d0de332ca1b34d53ca41c2b39ea52ce72f8c1e81c5200e27a8bade3e6ecbb`  
		Last Modified: Wed, 17 Nov 2021 03:24:34 GMT  
		Size: 7.8 MB (7833787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7474d56348f5333567750c1e5f06f899477fd437330627341eafa71bfa1a36ab`  
		Last Modified: Wed, 17 Nov 2021 03:24:34 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211c565de40518c5dac4498ccebbf3833fcfaa5db17d4bf94e6bef466136278b`  
		Last Modified: Wed, 17 Nov 2021 03:24:55 GMT  
		Size: 51.8 MB (51840474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ac470b62ae01e47a534a6c4db393f282c6a587101e308f0984c957017d68a0`  
		Last Modified: Wed, 17 Nov 2021 09:41:18 GMT  
		Size: 13.9 MB (13921165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7328c14a0cb8bfeb167acbbec9c08b5a9a857bc25957441f24aab130b043ca80`  
		Last Modified: Tue, 30 Nov 2021 04:54:09 GMT  
		Size: 188.7 MB (188665916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3d6f50bed9d701fb32a493c7cac1883b1292205018ed941fa399d22e3f2127`  
		Last Modified: Tue, 30 Nov 2021 10:25:19 GMT  
		Size: 28.0 MB (27962878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b36f1f002989fb48781e34bc24510f6f6793252d91406765a824064e996ee4`  
		Last Modified: Thu, 02 Dec 2021 02:41:22 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29516b48520ec9350454aab4669ef8f0cfcaff8dd23271446d5058a96ddc28f`  
		Last Modified: Thu, 02 Dec 2021 02:41:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45941087612c87b2b01858100cfe9e12206060278825cb56f50d7b7825e4f56b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348459423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3a26c25d451e5806534e2d26ba6dc7ae7502d09c2bc111f8649ee2c9f2f846`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:20 GMT
ADD file:82c1819d8416d9d44564980e25e98a081f813bc2ee8ad2789114fe37e802848f in / 
# Thu, 02 Dec 2021 08:08:20 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:54:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:54:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:55:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:02:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:02:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:02:54 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:02:55 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:02:56 GMT
ENV JAVA_VERSION=18-ea+25
# Thu, 02 Dec 2021 11:03:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:03:09 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 05:55:47 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Fri, 03 Dec 2021 05:55:48 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 05:55:59 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Fri, 03 Dec 2021 05:56:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Dec 2021 05:56:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 05:56:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 05:56:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:39e4f823356a9e2dbba530f9d363b4d76beaff75a13bad788d38eebeae67e5b0`  
		Last Modified: Thu, 02 Dec 2021 08:41:08 GMT  
		Size: 49.2 MB (49223045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66cf961d4016eccee4ce9bc5dc18dcd99e9f9963e66c4980a66e6492a421b2`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 7.7 MB (7695103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6c547e43b8b6afdfae413ba7a49c1120d0534fff63c4a242ef611d562a678c`  
		Last Modified: Thu, 02 Dec 2021 10:03:39 GMT  
		Size: 9.8 MB (9767269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9db99d12f5104a75bf8a56c5cf2b3e59dc9252fe78fe750c76e1dbb54f2a709`  
		Last Modified: Thu, 02 Dec 2021 10:03:57 GMT  
		Size: 52.2 MB (52165947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c7d675d3a1843a5028f6bf94810baf2db96515900d628336cf7d1a4b908802`  
		Last Modified: Thu, 02 Dec 2021 11:24:16 GMT  
		Size: 14.7 MB (14671106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccab2a8e6af93730bca84abdd949de79baafa63fcccd81a80fbbe21eb497066`  
		Last Modified: Thu, 02 Dec 2021 11:24:30 GMT  
		Size: 187.6 MB (187613929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7e88b0a2ba5836d11ea662a77aca860e87740baa87f991122607bb013efba2`  
		Last Modified: Fri, 03 Dec 2021 06:17:53 GMT  
		Size: 27.3 MB (27321997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df89d2c6f7031080fe2f14b241034978b304a6ee7d2dc3bb9f6deebb35522a5`  
		Last Modified: Fri, 03 Dec 2021 06:17:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafe3437765fa77b30f24c9cb35688d04389a11c8cba42a034090b807f0d7de0`  
		Last Modified: Fri, 03 Dec 2021 06:17:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
