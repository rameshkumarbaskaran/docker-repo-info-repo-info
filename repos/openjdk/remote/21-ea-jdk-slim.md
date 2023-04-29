## `openjdk:21-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:5077302663b4f781799bd6d8d4e30678ad1042397fe7a2fa3e00e74e0978b632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:81b398ea183cae4611e61b884d0360803429234dbe5cad5bc9403181e1b00c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235070687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb0c2509fb913901ff64e3dc24601e12284477c6e380ce30ef468a66a03633a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:38:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:38:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 09:38:20 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 09:38:20 GMT
ENV LANG=C.UTF-8
# Fri, 28 Apr 2023 23:25:12 GMT
ENV JAVA_VERSION=21-ea+20
# Fri, 28 Apr 2023 23:25:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/20/GPL/openjdk-21-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6dda27bb315b08ba166de341f4e10556f4e484274a28c907d158cf7f7d36d63d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/20/GPL/openjdk-21-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab11259011229aba0e7f3df57d86ca0aaeeff90d32e2f601742e3d7845aade15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 28 Apr 2023 23:25:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3ccfec852f335c3077cc27f9d826129c3799986d9e3b44f40f5df7a5a28b1c`  
		Last Modified: Wed, 12 Apr 2023 09:40:23 GMT  
		Size: 1.6 MB (1582448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d26fd4d1522abc7f62758221ebd9858a7ac1015f5666c603dd1735f3fdd5d2f`  
		Last Modified: Fri, 28 Apr 2023 23:28:24 GMT  
		Size: 202.1 MB (202070011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f9e669af3ae62c523401db6765b8e21d021caf2455d57acfaac0fa34c0a9cea9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231949702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee40af3bc99603f33f0a13a587797513e3fd4768f213a8ed16d29ffb5b648bdb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 05:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 05:11:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 12 Apr 2023 05:11:00 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 05:11:00 GMT
ENV LANG=C.UTF-8
# Fri, 21 Apr 2023 20:23:08 GMT
ENV JAVA_VERSION=21-ea+19
# Fri, 21 Apr 2023 20:23:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/19/GPL/openjdk-21-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5af95497753fbc33981f5ab1267fbd3be57e4095ceca9806490a25b56f819007'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/19/GPL/openjdk-21-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='d08fe17feea7fa18c4e9ee9918496974d0194d1fac9a485d47cc2d30601c3682'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 21 Apr 2023 20:23:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742e1b6db7553fd2059cce2c9672c6a73a94022701f01b4dd3569d492ec71a7`  
		Last Modified: Wed, 12 Apr 2023 05:13:00 GMT  
		Size: 1.6 MB (1566462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c7c54d0dc9ffedc740a624833a6c65a5f4689ae2b526b05f648184dea1c62d`  
		Last Modified: Fri, 21 Apr 2023 20:26:05 GMT  
		Size: 200.3 MB (200319414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
