## `openjdk:21-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:cffc93b6400e83c3267c6b290a8d31dbe900fd3b8f8c1912ba9492278ddb59af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:9460587d31732b703c51eb684339766c30add576fa942bc9f7e1b1acefa3c5ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230213989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8592339aa9f555dc87556889e50338b615b694358eeedf3f6a5dc1402897a641`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 08:43:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 08:43:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 08:43:15 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 08:43:15 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:27:50 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:28:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:28:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be15480d750c54bb843b324de2c368873a4a37cca927bddbc98058e7ca2127c`  
		Last Modified: Wed, 01 Mar 2023 08:47:51 GMT  
		Size: 3.3 MB (3278792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8ce01a145e0bfa8e2ca67188c39d577d15e4fcf91bde36db3b59bef4904200`  
		Last Modified: Sat, 04 Mar 2023 00:32:58 GMT  
		Size: 199.8 MB (199795315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:96d5518d09cf8d094a4f1371b34be5bc4fb98c0c2a69d9635ad4631cf76e1317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227333159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b0900eabcbf5e0264e98324bc8a8ea016d9ffc62eb455a766ea8550f93f210`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:25:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:25:13 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:25:13 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:13:16 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:13:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:13:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d097c08e52f9ff771689670d39bd09c2779339cc38112e4f75380522d71e9cf`  
		Last Modified: Wed, 01 Mar 2023 05:29:40 GMT  
		Size: 3.1 MB (3131731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579f3aec1831ebd78437dc99b414f20edcaaca75ca81b711b36abbf948b31cec`  
		Last Modified: Sat, 04 Mar 2023 00:18:12 GMT  
		Size: 198.3 MB (198278729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
