## `openjdk:21-slim-buster`

```console
$ docker pull openjdk@sha256:653a4a5bc1b08dd69d175989b0f3639395976f923c9d5ad69e16154dff2453a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:536bb78b2756ef0cb45d3f2fc1199ae2a8c9f859a1b50abbecf29d210075cc80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232242251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768c13857ced65f9008351b00e41bd35fc0bdf5bcce8169e6860a7360aa5fbf2`
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
# Mon, 20 Mar 2023 23:54:09 GMT
ENV JAVA_VERSION=21-ea+14
# Mon, 20 Mar 2023 23:54:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 20 Mar 2023 23:54:23 GMT
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
	-	`sha256:4b230ce65aade247174d38623bf36b10d7124404b4f1a2b199c9a36a7dc8b496`  
		Last Modified: Mon, 20 Mar 2023 23:59:14 GMT  
		Size: 201.8 MB (201823577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3c471b68121636d600f0feef036d39faf061f84df6263662fec9ed7986db9af1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229348905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a120dcfb78fc5f148e50f328c10f1977a691076fb188e8f413e492a93cddaf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:33:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 23 Mar 2023 09:33:59 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 09:33:59 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 09:33:59 GMT
ENV JAVA_VERSION=21-ea+14
# Thu, 23 Mar 2023 09:34:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 23 Mar 2023 09:34:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7dd89b802d8cb9cc5435e5f3b74e44a0eb080ad95666566ad37b9821083291`  
		Last Modified: Thu, 23 Mar 2023 09:36:08 GMT  
		Size: 3.1 MB (3131724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8435718b24bb8587a04c551e48f882eda0a2943dd36ba4e736052e16aaba4efe`  
		Last Modified: Thu, 23 Mar 2023 09:36:19 GMT  
		Size: 200.3 MB (200294521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
