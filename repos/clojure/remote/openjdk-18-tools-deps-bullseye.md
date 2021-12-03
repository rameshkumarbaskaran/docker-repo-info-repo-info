## `clojure:openjdk-18-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ed971fe598b4f68fa987461190eda466062afbd26c47d7e4c120b99b57cef430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4144fc0956e783a1989f06d67647405a6d45e0c82ccd78fafa6f4f39abc7a6d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347813297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c96430088b58976075f8d214aec911dd1f9f73328773ee79ac93361148a83b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:30 GMT
ADD file:5259fc086e8295ddbf02e48abef38e9bf93a183079d3631aa7a59306b7f2f9df in / 
# Wed, 17 Nov 2021 02:20:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:14:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:23:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 09:23:37 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:23:38 GMT
ENV LANG=C.UTF-8
# Tue, 30 Nov 2021 04:44:10 GMT
ENV JAVA_VERSION=18-ea+25
# Tue, 30 Nov 2021 04:44:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 30 Nov 2021 04:44:24 GMT
CMD ["jshell"]
# Tue, 30 Nov 2021 10:19:34 GMT
ENV CLOJURE_VERSION=1.10.3.1020
# Tue, 30 Nov 2021 10:19:35 GMT
WORKDIR /tmp
# Tue, 30 Nov 2021 10:19:44 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "afc87e2c8cfbf87e43553439c69a4c8e36bc2094405d08f39ca542b4cca0920a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Thu, 02 Dec 2021 02:34:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 Dec 2021 02:34:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 Dec 2021 02:34:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 Dec 2021 02:34:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:647acf3d48c2780e00cd27bb0984367415f270d78477ef9d5b238e6ebd5290da`  
		Last Modified: Wed, 17 Nov 2021 02:25:17 GMT  
		Size: 54.9 MB (54932774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02967ef003473d9adc6e20868d9d66af85b0871919bcec92419f65c974aa8ce`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 5.2 MB (5153337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad2231829e42e6f095971b5d2dc143d97db2d0870571ba4d29ecd599db62cb`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 10.9 MB (10871856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5576ce26bf1df68da60eeb5162dccde1b69f865d2815aba8b2d29e7181aeb62b`  
		Last Modified: Wed, 17 Nov 2021 03:23:31 GMT  
		Size: 54.6 MB (54566324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b28f29762d60d8bac863b4a63f2ba6c54c9742be3d86e501038eaeefeae3213`  
		Last Modified: Wed, 17 Nov 2021 09:39:40 GMT  
		Size: 14.1 MB (14071679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0686b9f2455ff8fd7b98be014f00f7de2fd4bf9bb74bc1a214b510a3c71ecb`  
		Last Modified: Tue, 30 Nov 2021 04:52:41 GMT  
		Size: 188.7 MB (188661128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38ceb48ce8ebce8ed3634772b8a69dbfb7bbfcc956b4690094deaf7ba4df300`  
		Last Modified: Tue, 30 Nov 2021 10:27:36 GMT  
		Size: 19.6 MB (19555169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4579e34aa9395333007d369224ef998fe92a5d5c89f897c440776b6e1e93b875`  
		Last Modified: Thu, 02 Dec 2021 02:46:25 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eb5d4ea53f313a24be84d6f219342150f0a1cd4c720f6e9483d50d9a21cfd6`  
		Last Modified: Thu, 02 Dec 2021 02:46:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d263d4225bc1b11cd349a2665487231f923aab21b9769a5faf36d14819f23d62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346344347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7657b236fd2efa8eb6b93ec40ae099b07130fa410c23f9ab1353cdae7d3a6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:07:54 GMT
ADD file:998dc1c35eeeed1ddf46156aeb337fb9b8cbb4855caf994201167a1061f4ecbf in / 
# Thu, 02 Dec 2021 08:07:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:53:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:53:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:01:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:01:46 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:01:47 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:01:48 GMT
ENV JAVA_VERSION=18-ea+25
# Thu, 02 Dec 2021 11:02:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:02:01 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 06:05:27 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Fri, 03 Dec 2021 06:05:27 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 06:05:35 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Fri, 03 Dec 2021 06:05:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 03 Dec 2021 06:05:38 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 06:05:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 06:05:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6476cb406b24c94f24348db05d154b814b14ee38860dea1625080e7e08295a80`  
		Last Modified: Thu, 02 Dec 2021 08:40:14 GMT  
		Size: 53.6 MB (53619027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96565d527970b1cc982493f96d6b317b1fbfdd7bf0ea6fd58d44942bb4f597c5`  
		Last Modified: Thu, 02 Dec 2021 10:02:24 GMT  
		Size: 4.9 MB (4937631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8c15f93136056df893ba8088992a38e90dc37210fd6ebb712413fd045c58de`  
		Last Modified: Thu, 02 Dec 2021 10:02:25 GMT  
		Size: 10.7 MB (10655914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42e24e52cb2f9b50ab14328865298f5ae6ac159219db890afc6366ec641a46`  
		Last Modified: Thu, 02 Dec 2021 10:02:46 GMT  
		Size: 54.7 MB (54669690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009bf5207e45bc64cf6af7e65c157106b890f904af8e570d361dfa9675e87778`  
		Last Modified: Thu, 02 Dec 2021 11:22:35 GMT  
		Size: 15.5 MB (15524985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d426b11bd4eb0845f4f444d9bd0f989982b346dfd7eed4aeb9b9aa27953ceca5`  
		Last Modified: Thu, 02 Dec 2021 11:22:50 GMT  
		Size: 187.6 MB (187603427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b3ce0c26df733f4281c9876cee6b8f18227efa74ef2803a862e0008f447fc9`  
		Last Modified: Fri, 03 Dec 2021 06:26:39 GMT  
		Size: 19.3 MB (19332644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c905b197a5efa78301d297f11bb4a85474a57e73af65851687b1461fc4b3d842`  
		Last Modified: Fri, 03 Dec 2021 06:26:37 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055a3ca1b5cdf803c1baf52ef438745811ee7977518651aca6b35c9fea39cd0d`  
		Last Modified: Fri, 03 Dec 2021 06:26:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
