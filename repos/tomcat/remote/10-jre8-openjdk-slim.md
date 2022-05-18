## `tomcat:10-jre8-openjdk-slim`

```console
$ docker pull tomcat@sha256:1c399b441d7d6438f9b45e98bca626cf6ad00d188e5a20323312d5527d05247a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre8-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:5e8503a1956d73436c8ba98e00f1d3bd7d198d9de09ada8760b52ca4ac5968de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89467683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d089a211780717f55aab16b30fa1a0bdb089e1a7b0322786809f1d786eea8978`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:52:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 11 May 2022 05:52:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 05:52:48 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:52:48 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:52:48 GMT
ENV JAVA_VERSION=8u332
# Wed, 11 May 2022 05:53:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 11 May 2022 23:57:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 May 2022 23:57:14 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 23:57:15 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 11 May 2022 23:57:15 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 May 2022 23:57:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:57:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:57:15 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 11 May 2022 23:57:15 GMT
ENV TOMCAT_MAJOR=10
# Wed, 18 May 2022 03:10:24 GMT
ENV TOMCAT_VERSION=10.0.21
# Wed, 18 May 2022 03:10:24 GMT
ENV TOMCAT_SHA512=a20d905486fc446bcc67501418520ab8a30425944fe30f30fb3306ef975573cd0a6c439c0b764bcec9144083684668ebe4aa0c80ccc7dd931af6c2f487f2fdba
# Wed, 18 May 2022 03:10:24 GMT
COPY dir:88e238fa4123c839a5cdb2e0aa966f42c92d364eb1f95eec6bde0a664d5a486f in /usr/local/tomcat 
# Wed, 18 May 2022 03:10:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 03:10:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 18 May 2022 03:10:30 GMT
EXPOSE 8080
# Wed, 18 May 2022 03:10:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf31789c5c1a5e3676cbd7a34472d61217c52c819552f5b116565c22cb6d2f1`  
		Last Modified: Wed, 11 May 2022 05:58:33 GMT  
		Size: 1.6 MB (1582150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab322dde1f12d492973b342aa950279496dee9b7fdb430c4b4f0e920834f86e5`  
		Last Modified: Wed, 11 May 2022 06:08:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff82a7b3b2f760df06cd87d736902cf2b0341f4401da6668078481224fc761b`  
		Last Modified: Wed, 11 May 2022 06:09:57 GMT  
		Size: 41.7 MB (41697386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b90ab2702fbc3771a76927b25a12fcc50680d96e289ae393926b693f0a114a3`  
		Last Modified: Thu, 12 May 2022 00:26:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb209fd4639d4209d974d71137d5676b3c321c132c43df2aef01a3757eedf72b`  
		Last Modified: Wed, 18 May 2022 03:44:19 GMT  
		Size: 12.5 MB (12502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee4bb4a1131936b6a663e30015a869e635583db67e6318aaf9f20de237e3deb`  
		Last Modified: Wed, 18 May 2022 03:44:19 GMT  
		Size: 2.3 MB (2305391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2609bb2189c03007b7a9c668be88f696997861528d1dcc0bb358fa8f035a8`  
		Last Modified: Wed, 18 May 2022 03:44:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre8-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e6ba74c106ccccc8ffbf3395e3fea41a0d73d9aef3820108fe0cb6bd1d9d142c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86822578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af0f24eadcf03eba8659aca45e62f40fb746d8394cfd9b4df0b41966279ee3f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:24:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 11 May 2022 14:24:06 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 14:24:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:24:08 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 14:24:09 GMT
ENV JAVA_VERSION=8u332
# Wed, 11 May 2022 14:25:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 12 May 2022 03:18:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 12 May 2022 03:18:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 03:18:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 12 May 2022 03:18:42 GMT
WORKDIR /usr/local/tomcat
# Thu, 12 May 2022 03:18:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 03:18:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 03:18:45 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 12 May 2022 03:18:46 GMT
ENV TOMCAT_MAJOR=10
# Wed, 18 May 2022 02:33:39 GMT
ENV TOMCAT_VERSION=10.0.21
# Wed, 18 May 2022 02:33:39 GMT
ENV TOMCAT_SHA512=a20d905486fc446bcc67501418520ab8a30425944fe30f30fb3306ef975573cd0a6c439c0b764bcec9144083684668ebe4aa0c80ccc7dd931af6c2f487f2fdba
# Wed, 18 May 2022 02:33:41 GMT
COPY dir:f5a465a0b6e67bf737dccbad801ecb9190a6449cb707f93f409a7964a82298fb in /usr/local/tomcat 
# Wed, 18 May 2022 02:33:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 May 2022 02:33:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 18 May 2022 02:33:47 GMT
EXPOSE 8080
# Wed, 18 May 2022 02:33:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5ad7be01b68fe78dada799da391fe706a6e51b7a0ec158e40069f53de08619`  
		Last Modified: Wed, 11 May 2022 14:33:48 GMT  
		Size: 1.4 MB (1361175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a3a458e5745e12ff663067f4fe5ece6d232739516d1f554489372a00bfd922`  
		Last Modified: Wed, 11 May 2022 14:45:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd1977a7e8a5939cc541b5deb904e8e4379ed336a85cc70eb18f82077b3e34f`  
		Last Modified: Wed, 11 May 2022 14:47:48 GMT  
		Size: 40.7 MB (40720750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11add825215dbaa0b565d022b14ab3f21c036616d9e910d3e34e754ae7dc43db`  
		Last Modified: Thu, 12 May 2022 04:03:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411a7584bf938cf87c446a7371d099cc1b9f0e8b17d8b6ee5def57ca9cc83317`  
		Last Modified: Wed, 18 May 2022 03:21:10 GMT  
		Size: 12.5 MB (12513040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa5dc9bc81bbc8c921c7947bec239ac267be1f2d6bf70e56ceac86d37adc1d`  
		Last Modified: Wed, 18 May 2022 03:21:09 GMT  
		Size: 2.2 MB (2161571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
