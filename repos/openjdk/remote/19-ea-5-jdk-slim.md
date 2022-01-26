## `openjdk:19-ea-5-jdk-slim`

```console
$ docker pull openjdk@sha256:71ce78c7318344edc8bbfacea7b2d9b237f27be6d2ec7e04d493401c3b5e95e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-5-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:e973482357635d9630b16157698d4e3d606b80b8d6ba41810a884ed9d34638cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222933563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9d3b8fd1686918643e299ea87403997a9a96c747718152386581d2f92d816`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:18:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 26 Jan 2022 09:18:17 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:18:17 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:18:17 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 26 Jan 2022 09:18:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='bb5a59a9573422be1df23754d298fce48e8d530e78af478756f219b2a8df34e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='27ef9cda6adaf16f8b57abfbdff8dbfef8a0ece62a0e47c0744f5e8dba8fb354'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:18:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dcc4682d62b46440b601446ffc65774100a9df1f32471a2eae91f5a6dc6967`  
		Last Modified: Wed, 26 Jan 2022 09:41:51 GMT  
		Size: 190.0 MB (189985257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-5-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:99fe60a00877ee0ecc4883026288e10252142dfacefeea9272e958893f51d757
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2cfd9071d2db40b7d9c0982fd9781020cce39ccd25070a735fd6f7881fed7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:49:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 26 Jan 2022 05:49:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:49:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 05:49:54 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 26 Jan 2022 05:50:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='bb5a59a9573422be1df23754d298fce48e8d530e78af478756f219b2a8df34e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='27ef9cda6adaf16f8b57abfbdff8dbfef8a0ece62a0e47c0744f5e8dba8fb354'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 05:50:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc1fefe201e16e58e3b2fb2aeae482f2662e0438f5c144b633ba5c909777ec8`  
		Last Modified: Wed, 26 Jan 2022 06:13:20 GMT  
		Size: 188.7 MB (188692312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
