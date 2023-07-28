## `openjdk:22-ea-7-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:45e88133fcae4c229a225119dfe04b65ab0a03e5fa9f4e7709fe51f47f01b943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-7-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5c6c67d0c396ef7ee88360c1ba0c602b780b4e5e24cfdc9136413ccb7ca4bf2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238212221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc08e81fea63c13c469a8ef7e8884d65b8310f103ee9ecc23686610c271f326`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:09:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 28 Jul 2023 04:09:43 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 04:09:43 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 04:09:43 GMT
ENV JAVA_VERSION=22-ea+7
# Fri, 28 Jul 2023 04:09:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 Jul 2023 04:09:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb66e7ec1c7a7454751d006538099f5227c45bf60b9bca6714a1f3df49c9637`  
		Last Modified: Fri, 28 Jul 2023 04:13:59 GMT  
		Size: 1.6 MB (1582416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54a4651fd93e912ae2810c8a25a3f6be1f0662a1ff65d4a21342a1d010099fb`  
		Last Modified: Fri, 28 Jul 2023 04:14:14 GMT  
		Size: 205.2 MB (205212203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-7-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3886b9d66fa0d2dfc93a61dcacd5c6185cc875105fb367ae1e59126871003da5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235156080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9addea3918ff728a7461aaa1bb05406fed49b8983ffc5ded9e62a3e633c53c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 10:41:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:41:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 28 Jul 2023 10:41:31 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 10:41:31 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 10:41:31 GMT
ENV JAVA_VERSION=22-ea+7
# Fri, 28 Jul 2023 10:41:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 Jul 2023 10:41:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfcd6c33d9e0f4dee755272a69686a8c3c0c86e69318d611216eda7d52d6aaa`  
		Last Modified: Fri, 28 Jul 2023 10:45:56 GMT  
		Size: 1.6 MB (1566457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2987ec70cb5020ae8c4ff945746eb40aec53ccb4d174fabd9bf8bf4845ad7c8b`  
		Last Modified: Fri, 28 Jul 2023 10:46:09 GMT  
		Size: 203.5 MB (203526792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
