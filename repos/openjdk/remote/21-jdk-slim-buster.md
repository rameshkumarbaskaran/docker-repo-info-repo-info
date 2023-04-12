## `openjdk:21-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:42abe9457c46e6588535ba3a393f92e8f36a566609dab5823a5594ed34350f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:4b82ce54d95f64064e85058c9cc94d51f7e286a3f86c9d6a5b0041074dd0c351
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232230383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cf50363289930732be647af26522bb1d1040ec83af1d90d3f01b8ebe173c7e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 16:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 16:45:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 23 Mar 2023 16:45:09 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 16:45:09 GMT
ENV LANG=C.UTF-8
# Tue, 11 Apr 2023 23:33:57 GMT
ENV JAVA_VERSION=21-ea+17
# Tue, 11 Apr 2023 23:34:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 Apr 2023 23:34:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f772363f2f03538e8571b0aa7f01bbd7481c1c1d38c404f5f08756fb7e9c41ae`  
		Last Modified: Thu, 23 Mar 2023 16:47:36 GMT  
		Size: 3.3 MB (3278783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33886e2e773d784b41e062902f6f86e256637d3c0b9096d76f3869d28a04f97b`  
		Last Modified: Tue, 11 Apr 2023 23:37:50 GMT  
		Size: 201.8 MB (201811731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6843bb1ebbd985111f941736ad0ef6b01567f560ebb48ebcf6c624c969d0d7bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229229229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bba77ecd237f3e5776ca9bc6feb3479c127746eeaa4003b4109bd11921c3c44`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:40:02 GMT
ADD file:39d4ef5cc48487567b857a8527ab3c106b5099eafffbeaa8b70df450fb8409e3 in / 
# Wed, 12 Apr 2023 00:40:02 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:11:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 05:11:47 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 05:11:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 Apr 2023 05:11:47 GMT
ENV JAVA_VERSION=21-ea+17
# Wed, 12 Apr 2023 05:11:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='98dcda513be6f72005f9b52c79d88f7e6bef066baddf0b89d9847c125b6d9bed'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/17/GPL/openjdk-21-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='795231d9254753b31583afabc08fb092c00cc2459962cfdd3e0b0bd32edcad92'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Apr 2023 05:12:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:27bec964ec41cf69bd5df2ffd45c27623ae4bb0eb6f9f366179f7ac9b47d9840`  
		Last Modified: Wed, 12 Apr 2023 00:43:11 GMT  
		Size: 25.9 MB (25922011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe87b3c027f2b1952babc2b86de6d9f2011dfb0410c3f340d15409fba01477`  
		Last Modified: Wed, 12 Apr 2023 05:14:03 GMT  
		Size: 3.1 MB (3131734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e415eb43cf8e7d3cf7376bb524d58bf0fce0043988a73da34b0545a115e8ea5`  
		Last Modified: Wed, 12 Apr 2023 05:14:15 GMT  
		Size: 200.2 MB (200175484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
