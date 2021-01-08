## `clojure:openjdk-16-boot-buster`

```console
$ docker pull clojure@sha256:0f27c6cfcc50d4066217da68f42b716653bd4aa67c7f8cf5886f19439720ae16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:19b52c86e772de7afe54e75437d31ebf219889377bc65b3fe35f4cfa1da832e7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377734668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b58a23b50ab05bc5f641f3c03def0690e9476602466645130224bd4afbb3499`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:52 GMT
ADD file:6014cd9d7466825f80d4a3345847efd6fd7ef600b8135811cab4f0e304f66cd7 in / 
# Fri, 11 Dec 2020 02:05:52 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:58:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:58:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 16:58:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Dec 2020 04:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Dec 2020 04:49:57 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 04:49:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Fri, 18 Dec 2020 04:49:57 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 04:49:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 08 Jan 2021 19:35:26 GMT
ENV JAVA_VERSION=16-ea+31
# Fri, 08 Jan 2021 19:35:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-aarch64_bin.tar.gz; 			downloadSha256=619122347e25dccbc419168329b659cdb1967570431bc09f597a791107484554; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-x64_bin.tar.gz; 			downloadSha256=f43aa41b3c71b9e278a37fd33a94579a8039e07abd21841ad9e1e0a4582abf24; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Jan 2021 19:35:39 GMT
CMD ["jshell"]
# Fri, 08 Jan 2021 20:12:01 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 08 Jan 2021 20:12:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:12:02 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:12:03 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 08 Jan 2021 20:12:03 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:12:03 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 08 Jan 2021 20:12:23 GMT
RUN boot
# Fri, 08 Jan 2021 20:12:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6c33745f49b41daad28b7b192c447938452ea4de9fe8c7cc3edf1433b1366946`  
		Last Modified: Fri, 11 Dec 2020 02:12:07 GMT  
		Size: 50.4 MB (50397728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef072fc32a84ef237dd4fcc7dff2c5e2a77565f24d63977d0fa654a6d8512dd8`  
		Last Modified: Thu, 17 Dec 2020 17:25:57 GMT  
		Size: 7.8 MB (7812075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0afb8e68e0bcdc1b6e05acaa713a6fe0d818086c596bd1ad99133665c4efe63`  
		Last Modified: Thu, 17 Dec 2020 17:25:58 GMT  
		Size: 10.0 MB (9996417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599c07d28e6c920ef615f4f9b5cd0d52eb106fcd20c3a7daef389f14edd4ef5`  
		Last Modified: Thu, 17 Dec 2020 17:26:19 GMT  
		Size: 51.8 MB (51829485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fa4eb1e951cd03e1e1ada47951e6cee0ec635dd8ab218565664a8973b12901`  
		Last Modified: Fri, 18 Dec 2020 04:55:16 GMT  
		Size: 13.9 MB (13920463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b539d967223d3b68cc49afb5cc108c7f86d8463443ce173e53eb27497f210890`  
		Last Modified: Fri, 18 Dec 2020 04:55:14 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4839c5a0d3a2c9e42400a60f9f7bf6027c1e15e30cb47bc54ac1adb77afc74`  
		Last Modified: Fri, 08 Jan 2021 19:44:34 GMT  
		Size: 185.0 MB (184951290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb66e05aa69a0093c0c08c222cf796390cb29127431083978ccd802529915b01`  
		Last Modified: Fri, 08 Jan 2021 20:16:42 GMT  
		Size: 6.9 KB (6898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58179104647f8f5eda569a6a8093c672d39e3f66e2e1880be17be5cca97b0b92`  
		Last Modified: Fri, 08 Jan 2021 20:16:46 GMT  
		Size: 58.8 MB (58820101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4cafbeb8403b5874125331bbca3eeb4d06dc1f88967c5c4c174a506d21674cfe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371820487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6078aa4df656c86bdd01182996dc204310cdbb6f72b0c59a7b49a2366b390403`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:23 GMT
ADD file:b08f373022952dba7d08b7fc02909d9e369c9727e0e4f62d6110e41e70e668cc in / 
# Fri, 11 Dec 2020 02:45:25 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 10:05:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 10:06:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 10:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 13:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 13:38:57 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 13:38:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Thu, 17 Dec 2020 13:38:58 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 13:39:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 08 Jan 2021 19:44:32 GMT
ENV JAVA_VERSION=16-ea+31
# Fri, 08 Jan 2021 19:44:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-aarch64_bin.tar.gz; 			downloadSha256=619122347e25dccbc419168329b659cdb1967570431bc09f597a791107484554; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_linux-x64_bin.tar.gz; 			downloadSha256=f43aa41b3c71b9e278a37fd33a94579a8039e07abd21841ad9e1e0a4582abf24; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Jan 2021 19:44:49 GMT
CMD ["jshell"]
# Fri, 08 Jan 2021 20:27:57 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 08 Jan 2021 20:27:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 08 Jan 2021 20:27:59 GMT
WORKDIR /tmp
# Fri, 08 Jan 2021 20:28:01 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 08 Jan 2021 20:28:01 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 Jan 2021 20:28:02 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 08 Jan 2021 20:28:25 GMT
RUN boot
# Fri, 08 Jan 2021 20:28:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:99e5136f81cd2a8cc226c42435d6f4f30584d168cc51f4d4afd2d5611e4d2215`  
		Last Modified: Fri, 11 Dec 2020 02:52:45 GMT  
		Size: 49.2 MB (49180317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e84abcfad00e501f51bf9945429b6856c10fe31c1504e62c6520d85fff4382`  
		Last Modified: Thu, 17 Dec 2020 10:38:12 GMT  
		Size: 7.7 MB (7682276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97012cb1831f37b45ec32c7b23a4a1bbd2d92d45324067362d15f9c5ed5341b0`  
		Last Modified: Thu, 17 Dec 2020 10:38:13 GMT  
		Size: 10.0 MB (9984302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ab763a154e0e4765c5e67269e4bb776478e2abfb52f24bae39ee817ad26bbc`  
		Last Modified: Thu, 17 Dec 2020 10:38:37 GMT  
		Size: 52.2 MB (52163991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3064b8887142575b19ad7bd3f3d470baf54814c3f79971a38db7d0799d442b7e`  
		Last Modified: Thu, 17 Dec 2020 13:46:33 GMT  
		Size: 14.7 MB (14674226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce620033e68eb00439d4211493274b3a8e06a7ec50f8cb84f63a1d762813d773`  
		Last Modified: Thu, 17 Dec 2020 13:46:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2243c22a8f502c46bb63ee7c843b22753237af2d0d91621bd134882c3d6dab2a`  
		Last Modified: Fri, 08 Jan 2021 19:54:42 GMT  
		Size: 179.3 MB (179308041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e84dfee6ac58d919f2746d2a79a01ca77a3c192a1abd88e179618fb1bee14`  
		Last Modified: Fri, 08 Jan 2021 20:33:11 GMT  
		Size: 6.9 KB (6899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8e9a6dbc8ac14080e22b68026351c444490b96230ada3cebe88d4cdbc9bab6`  
		Last Modified: Fri, 08 Jan 2021 20:33:17 GMT  
		Size: 58.8 MB (58820226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
