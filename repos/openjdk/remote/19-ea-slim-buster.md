## `openjdk:19-ea-slim-buster`

```console
$ docker pull openjdk@sha256:f9554bb5b0e0ccd671fe5a3ce81ade6b55b2235283f196db2293fe066c6ec692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:81ffd24435d5ad5a87a006c755512c76039c778e9de8bf3c5ba20ea206f3d8fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220279249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb585b22e374b79de55d40299361f2797f3c86fb449a5422e59a91d03c9971c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:30:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 Dec 2021 01:42:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 14 Dec 2021 01:42:38 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Dec 2021 01:42:38 GMT
ENV LANG=C.UTF-8
# Tue, 14 Dec 2021 01:42:38 GMT
ENV JAVA_VERSION=19-ea+1
# Tue, 14 Dec 2021 01:42:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/1/GPL/openjdk-19-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='652a141e1854a51df7991b003d6e9478021cb4a4ee67b320cb284e40dff46847'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/1/GPL/openjdk-19-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='fe09452d49aad26e03df3d5b5ebfc22f8b2d8a1e16dcc03a2f00b31f586a770a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 14 Dec 2021 01:42:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169731f46e61fb8aef8f7ed809068db98d3feb2466197e9680dbbdbb80d8ed90`  
		Last Modified: Thu, 02 Dec 2021 11:48:59 GMT  
		Size: 3.3 MB (3269625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bca3ab25a77ff44e5bb17e9a4ad3af8cd17f4d055a1aed7c8f5c498a2b9f43a`  
		Last Modified: Tue, 14 Dec 2021 01:52:54 GMT  
		Size: 189.9 MB (189855895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
