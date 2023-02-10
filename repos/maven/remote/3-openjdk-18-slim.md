## `maven:3-openjdk-18-slim`

```console
$ docker pull maven@sha256:0ccb24680338459567324858307f64ccff55e4e5904487b9b376dcf672f6dafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18-slim` - linux; amd64

```console
$ docker pull maven@sha256:6e08ab80ed557294e30c9555c923e7620a8125b4f207996d961535789088339b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232931756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a7529964d0db55a9fa4ba31c7af092b0cc6d937e1e6cffa74eab21ccd15bcd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:50:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 09 Feb 2023 10:50:08 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:50:08 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 10:50:08 GMT
ENV JAVA_VERSION=18.0.2.1
# Thu, 09 Feb 2023 10:50:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Feb 2023 10:50:21 GMT
CMD ["jshell"]
# Fri, 10 Feb 2023 20:59:51 GMT
RUN apt-get update   && apt-get install -y curl procps   && rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 20:59:51 GMT
ARG MAVEN_VERSION=3.8.7
# Fri, 10 Feb 2023 20:59:51 GMT
ARG USER_HOME_DIR=/root
# Fri, 10 Feb 2023 20:59:51 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Fri, 10 Feb 2023 20:59:51 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Fri, 10 Feb 2023 20:59:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 10 Feb 2023 20:59:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 10 Feb 2023 20:59:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 10 Feb 2023 20:59:53 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 10 Feb 2023 20:59:54 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 10 Feb 2023 20:59:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 10 Feb 2023 20:59:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10286f48c71be2a630e155ceb33e8e5132e861088b8d5db5ae0b2589912a958d`  
		Last Modified: Thu, 09 Feb 2023 10:54:07 GMT  
		Size: 1.6 MB (1582324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718b77cc4686e40b578d074b3198c6047ddba87d7feb823af9b4307be83e449a`  
		Last Modified: Thu, 09 Feb 2023 10:59:24 GMT  
		Size: 189.1 MB (189120448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4591d9913c80ed9f9c6c9e2affafa0056e4754ff8a1364eb276793ed64d1b1`  
		Last Modified: Fri, 10 Feb 2023 21:01:54 GMT  
		Size: 2.5 MB (2464817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc43b75e66d34f3d3795f7d4ba91ee257fd53a7443a701211b76ff2facd41a3`  
		Last Modified: Fri, 10 Feb 2023 21:01:54 GMT  
		Size: 8.4 MB (8351143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30271a756915fc738d68a69b4632f93763ebe0175f99546f946de4158b074522`  
		Last Modified: Fri, 10 Feb 2023 21:01:53 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2995f37a2b84be2da3853e05100f7ced10cb31171b38db13194bb90272f4e8b`  
		Last Modified: Fri, 10 Feb 2023 21:01:53 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4757c1ff47a6139f6a7e6a3ef4c2bef630422b74a636d46f56ea5f16b966076a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230506185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38809959e71b90569b4bba47096881e21f1824787abd860965fdbfc329d0d403`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:07:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:10:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 09 Feb 2023 10:10:30 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:10:30 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 10:10:30 GMT
ENV JAVA_VERSION=18.0.2.1
# Thu, 09 Feb 2023 10:10:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Feb 2023 10:10:45 GMT
CMD ["jshell"]
# Thu, 09 Feb 2023 22:33:46 GMT
RUN apt-get update   && apt-get install -y curl procps   && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 22:33:46 GMT
ARG MAVEN_VERSION=3.8.7
# Thu, 09 Feb 2023 22:33:46 GMT
ARG USER_HOME_DIR=/root
# Thu, 09 Feb 2023 22:33:46 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Thu, 09 Feb 2023 22:33:46 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Thu, 09 Feb 2023 22:33:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 09 Feb 2023 22:33:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 09 Feb 2023 22:33:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 09 Feb 2023 22:33:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 09 Feb 2023 22:33:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 09 Feb 2023 22:33:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 09 Feb 2023 22:33:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12ec23d1569af13aa4b739730163609a2c012fc5a8c00a55e2c980462802868`  
		Last Modified: Thu, 09 Feb 2023 10:14:41 GMT  
		Size: 1.6 MB (1566302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7cd48779062df715bb03c2595611218b1a90a62edeeea24888e18ec78a2b28`  
		Last Modified: Thu, 09 Feb 2023 10:19:43 GMT  
		Size: 188.0 MB (188038690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055850bd9a72a033c5a543917d1168902edb0fe4a84d0a3f718bc29ee1baae65`  
		Last Modified: Thu, 09 Feb 2023 22:35:13 GMT  
		Size: 2.5 MB (2486314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636c7092e17cbc5aa67b5c1a7a1abcbf7fdb2d4adc3f51c31301dbea0ccf1b8f`  
		Last Modified: Thu, 09 Feb 2023 22:35:13 GMT  
		Size: 8.4 MB (8351156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3888b805b5ee03ff30af7aff348a3df7177e9f947d97fc950d2d8171604a71`  
		Last Modified: Thu, 09 Feb 2023 22:35:12 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879cc533feec8a5a1960cf8ec69ddbeb251f7c0f7d0f830b6380610197c0da86`  
		Last Modified: Thu, 09 Feb 2023 22:35:12 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
