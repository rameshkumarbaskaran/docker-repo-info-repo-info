## `clojure:openjdk-14-boot-buster`

```console
$ docker pull clojure@sha256:e955bcb3f1d70a8812f68f7bf98c6c22c7f5a1f423869a3ac5adf1bde0b6cca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:e3ff0a0e085eca66c0c678642014101601f08fb98fc48e883e8bd42d1ca24414
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.0 MB (391990904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a069a7f31a8fcd7b4531b1de39ff1cc3c14250737d1172ae201e6d4b9817b7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:56:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:57:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 21:31:31 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 21:32:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Tue, 31 Mar 2020 21:32:43 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 21:32:44 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 14 Apr 2020 21:29:19 GMT
ENV JAVA_VERSION=14.0.1
# Tue, 14 Apr 2020 21:29:19 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14.0.1/664493ef4a6946b186ff29eb326336a2/7/GPL/openjdk-14.0.1_linux-x64_bin.tar.gz
# Tue, 14 Apr 2020 21:29:20 GMT
ENV JAVA_SHA256=22ce248e0bd69f23028625bede9d1b3080935b68d011eaaf9e241f84d6b9c4cc
# Tue, 14 Apr 2020 21:29:30 GMT
RUN set -eux; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Tue, 14 Apr 2020 21:29:30 GMT
CMD ["jshell"]
# Tue, 14 Apr 2020 22:08:45 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 14 Apr 2020 22:08:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 14 Apr 2020 22:08:46 GMT
WORKDIR /tmp
# Tue, 14 Apr 2020 22:08:47 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 14 Apr 2020 22:08:47 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 14 Apr 2020 22:08:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 14 Apr 2020 22:09:04 GMT
RUN boot
# Tue, 14 Apr 2020 22:09:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebfd3d2fd0de99b1c63aa36a507bf5555481d06e571d84ed84440d30671494`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 7.8 MB (7812166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998346ba308e3362a85c7bf7faed28d0277c68203696134192fe812f809abb2`  
		Last Modified: Tue, 31 Mar 2020 02:09:57 GMT  
		Size: 10.0 MB (9996302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ec562c947a8ca1b168415da6a4a8f8920808f9b5d6f420ef8fa9af249b1f1`  
		Last Modified: Tue, 31 Mar 2020 02:10:13 GMT  
		Size: 51.8 MB (51790297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bdaf2f151ec945dbcaf0355685f51dfefdcdf882b30fc65259d4b30b410184`  
		Last Modified: Tue, 31 Mar 2020 21:35:43 GMT  
		Size: 13.9 MB (13920151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0ae0909e9495ba00fbfaa0824535d0415b80b3bd0afbdb499ae8adf41eada5`  
		Last Modified: Tue, 31 Mar 2020 21:36:12 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bd66307276a18e45bc56ba2bf5fedaa31ac9d16d3844e2340d88dde61c565e`  
		Last Modified: Tue, 14 Apr 2020 21:32:09 GMT  
		Size: 199.3 MB (199262745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388edcc035ab2fbad0c5f9d9e9166cbd1aa0e52a6e9b1190d004a307bcdfac7`  
		Last Modified: Tue, 14 Apr 2020 22:10:36 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c612827843aa85a52bd685d7af2b002fb5668d40fb3561c2c9dd4f126fae4d`  
		Last Modified: Tue, 14 Apr 2020 22:10:40 GMT  
		Size: 58.8 MB (58820097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
