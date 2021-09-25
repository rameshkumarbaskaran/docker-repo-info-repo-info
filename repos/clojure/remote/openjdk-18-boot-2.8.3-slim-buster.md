## `clojure:openjdk-18-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:880391bd38af6a74261b1abb0124dd97334649c4cad795e91f0cf051ece69e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:73e961bd1191f41ab3f72c7af83d9a3c6d7bfa7f3c459e29896068541d2546be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277802746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd91bcf6539db5f8046e8988f8da71bb976c9500997a1b9c62e1671b683ba1e0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:32:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Fri, 03 Sep 2021 08:32:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 08:32:42 GMT
ENV LANG=C.UTF-8
# Sat, 25 Sep 2021 00:26:15 GMT
ENV JAVA_VERSION=18-ea+16
# Sat, 25 Sep 2021 00:26:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='ec604f7aef23624c0acdc0db346a2b226aab47d120538833070f0d5e01d571c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/16/GPL/openjdk-18-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='623eff3e61bd5f74442fb5699ac3dea167dbe0ade7dd6c1fa9cdd4788e316b96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 25 Sep 2021 00:26:30 GMT
CMD ["jshell"]
# Sat, 25 Sep 2021 01:17:54 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 25 Sep 2021 01:17:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 25 Sep 2021 01:17:55 GMT
WORKDIR /tmp
# Sat, 25 Sep 2021 01:18:00 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 25 Sep 2021 01:18:00 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 25 Sep 2021 01:18:00 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 25 Sep 2021 01:18:23 GMT
RUN boot
# Sat, 25 Sep 2021 01:18:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb538b78785f115f86e312f41ac522a9b30e0cb77d061dd273f331e57ae2e471`  
		Last Modified: Fri, 03 Sep 2021 08:50:36 GMT  
		Size: 3.3 MB (3269611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39de3f8ba0601a94ebc366f5a916de4aaec9d842925bf77229cb7ac55331bcd2`  
		Last Modified: Sat, 25 Sep 2021 00:35:52 GMT  
		Size: 188.3 MB (188286967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cb1957a0950c8dedfff2a0adcc459df0bb24b619ca97ae01dfa171dcf98ef7`  
		Last Modified: Sat, 25 Sep 2021 01:27:00 GMT  
		Size: 279.7 KB (279747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91670378c47f66560e76ace9b8a259090d0f1628c22db30aafc5640698faab40`  
		Last Modified: Sat, 25 Sep 2021 01:27:04 GMT  
		Size: 58.8 MB (58820577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:33ca399c9846b5589dd5fec6d61db9581653d92dfde4689a4a2b004a037ff332
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274996828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cda2308d9bb7cb44fd6544c972f1b6dced9d46ff7519d7bf1d9cda0dbc449b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:58 GMT
ADD file:4a1d7f2d989aee6bd83da076b6e9dd3da2da97cf5654bd37568e9baec30ac4b1 in / 
# Fri, 03 Sep 2021 00:40:58 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 10:45:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Fri, 03 Sep 2021 10:45:24 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 10:45:24 GMT
ENV LANG=C.UTF-8
# Fri, 17 Sep 2021 19:18:08 GMT
ENV JAVA_VERSION=18-ea+15
# Fri, 17 Sep 2021 19:18:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/15/GPL/openjdk-18-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d04e7163eb9519d4c918acc60d1f92fd7b6ff28bb0a43d7019790590b120725c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/15/GPL/openjdk-18-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='7a154bf56a56e4c4a4cdc6b5542e916b81baca431de262fa1a07e07ca313bd5e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Sep 2021 19:18:21 GMT
CMD ["jshell"]
# Fri, 17 Sep 2021 22:08:13 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 17 Sep 2021 22:08:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 17 Sep 2021 22:08:14 GMT
WORKDIR /tmp
# Fri, 17 Sep 2021 22:08:19 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 17 Sep 2021 22:08:19 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 17 Sep 2021 22:08:19 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 17 Sep 2021 22:08:46 GMT
RUN boot
# Fri, 17 Sep 2021 22:08:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d10c227306ce3db344a8399cbc02bbf0dcb36519318efbde3c6027c00be8b40e`  
		Last Modified: Fri, 03 Sep 2021 00:49:47 GMT  
		Size: 25.9 MB (25914860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4152925219b6247cb64144905f215af10ba4621b4f699e896b93191fc575742`  
		Last Modified: Fri, 03 Sep 2021 11:06:36 GMT  
		Size: 3.1 MB (3119119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4637a1b79dc8f7623b504da06a457fab72d3fbc225f82caeb6db413b7366a25a`  
		Last Modified: Fri, 17 Sep 2021 19:34:49 GMT  
		Size: 186.9 MB (186862722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b70baf7a76540e7597eea1144431911f11129fb13273ae74d9dc3ef77ffca28`  
		Last Modified: Fri, 17 Sep 2021 22:20:21 GMT  
		Size: 279.5 KB (279500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c0defd20dcc8cd2e7173bd953f84a9a2874a98786634222f82aa79fd265edf`  
		Last Modified: Fri, 17 Sep 2021 22:20:25 GMT  
		Size: 58.8 MB (58820627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
