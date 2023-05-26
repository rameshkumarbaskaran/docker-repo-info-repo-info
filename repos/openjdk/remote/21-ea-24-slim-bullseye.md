## `openjdk:21-ea-24-slim-bullseye`

```console
$ docker pull openjdk@sha256:b029484da0d6b0675e3e00ed12f8ead1e4cf8a4dede60daabd5af990e56c4b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:21-ea-24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f14735dd1152ff2870e6dc05e3a99ce0312fa90088552a1b1ac07acb12250623
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233475662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb094552c7960c2ca909d52b0a55fa9763ac9780c6fec84178a59492c360ac3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:45:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 23 May 2023 02:45:24 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:45:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 May 2023 23:40:33 GMT
ENV JAVA_VERSION=21-ea+24
# Thu, 25 May 2023 23:40:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='437e740a3ee795a3cf08d6cf5006d03668023151200d5e09ada16d94ef30db22'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='ecabd8a50340461d04d06b8f587bf06c614aed9cb441ee3ff9577e1b10e53035'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 25 May 2023 23:40:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2720cbf9c47906a0307f15640e572385cf4a861c09321177843a6399e647c`  
		Last Modified: Tue, 23 May 2023 02:47:18 GMT  
		Size: 1.6 MB (1566444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cc7f46d1d1f4b1f5f5f5205de2ced5efe2badda05134134b60dca90a9bf568`  
		Last Modified: Thu, 25 May 2023 23:43:31 GMT  
		Size: 201.9 MB (201856471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
