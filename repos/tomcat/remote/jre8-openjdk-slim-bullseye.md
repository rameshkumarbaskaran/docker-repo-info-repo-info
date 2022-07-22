## `tomcat:jre8-openjdk-slim-bullseye`

```console
$ docker pull tomcat@sha256:b3ba9a3dcb8f702e902bd0ac494f2fbec1ff2d6192788d2a0641b84271fb2563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-slim-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:f5561b4b7cdb915ccdbc564de2e6f5ab6a4a40edbb1726d7904fa3e6d298f4e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87550160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef21ded04ad9721b7bbe0775660d602affedf5beca85eebd80e52c815782634c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:01:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 02:01:16 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 02:01:16 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 02:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 02:01:16 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 02:02:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Tue, 12 Jul 2022 18:55:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 Jul 2022 18:55:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:55:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 12 Jul 2022 18:55:53 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 Jul 2022 18:55:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:55:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:55:53 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 12 Jul 2022 18:55:53 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 Jul 2022 18:55:53 GMT
ENV TOMCAT_VERSION=10.0.22
# Tue, 12 Jul 2022 18:55:53 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Fri, 22 Jul 2022 02:55:56 GMT
COPY dir:232cbcfa8234e0dd0feef71863cac5e64ab129cdcf56a91cca505a13b9f4b6b0 in /usr/local/tomcat 
# Fri, 22 Jul 2022 02:56:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Jul 2022 02:56:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Jul 2022 02:56:02 GMT
EXPOSE 8080
# Fri, 22 Jul 2022 02:56:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ccc3e1b7514ad8fa7bfa6796a0b7ab22927e96bacec0834dbead204f9f524e`  
		Last Modified: Tue, 12 Jul 2022 02:19:53 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fd0b64cee2b853e61b440e6478ddf6570bb864d971153a15dda19eb92387b`  
		Last Modified: Tue, 12 Jul 2022 02:20:57 GMT  
		Size: 41.7 MB (41697344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb91d89c4f1d1c0f0f9b75f94db4fdfb541dfd72f32f1d90ebedf9d8f6d157`  
		Last Modified: Tue, 12 Jul 2022 19:26:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f81de0e4ddb66bb797627763d7af38fd96130c91e19c4ede4c70b0d278303c`  
		Last Modified: Fri, 22 Jul 2022 03:44:50 GMT  
		Size: 12.5 MB (12507102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf64ebb753f8a5c412f700d5bd21229ee04943140fc8ff484eb01321603a60`  
		Last Modified: Fri, 22 Jul 2022 03:44:49 GMT  
		Size: 396.3 KB (396316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8546a0c8adadc703859ccdd6f42bfcde314aa16c6b3c5d0c17e9ed9def4ce8a`  
		Last Modified: Fri, 22 Jul 2022 03:44:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3dbd5ac21d1a73e5c5166d0cf153e7ae43e6becb29c27ce6421318436297c47c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85038485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12e07f5f3e2e3cce7bcdf96b158ba072a0d7d10e03109fe91f9085a44d4a12c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:37:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Jul 2022 01:37:10 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 01:37:11 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:37:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 01:37:13 GMT
ENV JAVA_VERSION=8u332
# Tue, 12 Jul 2022 01:38:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Tue, 12 Jul 2022 18:41:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 Jul 2022 18:41:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 18:41:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 12 Jul 2022 18:41:54 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 Jul 2022 18:41:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:41:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 Jul 2022 18:41:57 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 12 Jul 2022 18:41:58 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 Jul 2022 18:41:59 GMT
ENV TOMCAT_VERSION=10.0.22
# Tue, 12 Jul 2022 18:42:00 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Tue, 12 Jul 2022 18:42:02 GMT
COPY dir:c0b9eecdc6cd31ffb69161920787ee9ea0f9fd288e360ba5350d7a7693a9e7a3 in /usr/local/tomcat 
# Tue, 12 Jul 2022 18:42:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 18:42:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 12 Jul 2022 18:42:08 GMT
EXPOSE 8080
# Tue, 12 Jul 2022 18:42:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0eebdbddd0a55d86b14d45ff4aaee7c446d9188afe15e3a3295ef44d82e156`  
		Last Modified: Tue, 12 Jul 2022 01:49:35 GMT  
		Size: 1.6 MB (1565943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78856b16fcfe678909f086cc7d5351ecddda121fd1194853eff5314c9521ab4d`  
		Last Modified: Tue, 12 Jul 2022 02:02:41 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4823a2b276021af69c349280b7b52e473604ced07f62640ecabd7c518d7d108`  
		Last Modified: Tue, 12 Jul 2022 02:03:56 GMT  
		Size: 40.7 MB (40720854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2341952bac5e91c3473c28b5795a9153db89d424b5a3b865f2b7ea315cf5c5a`  
		Last Modified: Tue, 12 Jul 2022 19:29:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5284058685a1df483b48c319b1199df545a5ea0c0fa218ffc8b812af685a704d`  
		Last Modified: Tue, 12 Jul 2022 19:30:00 GMT  
		Size: 12.5 MB (12517172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99456086ebf0747c79038415ee436fa82a2ddc94853643488ba63caf4f713bf5`  
		Last Modified: Tue, 12 Jul 2022 19:29:59 GMT  
		Size: 179.9 KB (179940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
