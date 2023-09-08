## `openjdk:22-ea-14-jdk-slim`

```console
$ docker pull openjdk@sha256:ad52a94c65207d9cc024720560b5c0fc7ed5019bd612625b49c7a036454cff00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:22-ea-14-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:c075f8ee23e3d1a2689d8ad8bd89d89ffce93f8a0c7e30f08898b9674b5fbc39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238448767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f46c83943710d36ca7e9c001d02429a93abcd8fff3ab3d79160f44d71fb3001`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:51 GMT
ADD file:3a8cd4de7f163d93718670f4db1de49045f5e04af3a8aa27d81c0f14647db707 in / 
# Thu, 07 Sep 2023 00:20:51 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:01:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 05:01:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 05:01:41 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 19:44:30 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:44:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='2d6b271eaaecdedb8eee2e64b7cca4f36000039d3bdfe618460424fb8e449fcc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='62b2cad2a14380255f3f0dee68193a8d2953c0b8cce04eae1f65427d4ab2b707'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Sep 2023 19:44:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:360eba32fa65016e0d558c6af176db31a202e9a6071666f9b629cb8ba6ccedf0`  
		Last Modified: Thu, 07 Sep 2023 00:25:22 GMT  
		Size: 29.1 MB (29124494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a66b3b6aa0adca35c00a3a7dbe60f62cd8e91d39bd9df30ca203b250061f3f4`  
		Last Modified: Thu, 07 Sep 2023 05:05:23 GMT  
		Size: 4.0 MB (4008106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3c3390c69897487208a3a42c7478e158e447fb5c6c4068cdc55a7cc852af1d`  
		Last Modified: Fri, 08 Sep 2023 19:48:26 GMT  
		Size: 205.3 MB (205316167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
