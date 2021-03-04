## `maven:3-openjdk-17-slim`

```console
$ docker pull maven@sha256:3beb23b4a4a852427bbc4ebd5619ea5828b2bd813321f7f6c9f79871b65c24b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17-slim` - linux; amd64

```console
$ docker pull maven@sha256:185e1f1500a4f4980eb1b526636172372a8b28f04cc036645984d7231d283a05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228652129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca08ae70ff0945aa9265ec683ab04854185148598e946c1a216da621cc4fff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:10:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:10:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 09 Feb 2021 17:10:18 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 17:10:18 GMT
ENV LANG=C.UTF-8
# Wed, 03 Mar 2021 23:38:53 GMT
ENV JAVA_VERSION=17-ea+12
# Wed, 03 Mar 2021 23:39:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e281f7d1fd2aaa858b02d5be451c51a9ed836c78d002cb82b114e6c36041eebf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ae713390655d0cfd8302cb2c840553404a3e366162ba5b9a2410ea7b6f1c27'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Mar 2021 23:39:23 GMT
CMD ["jshell"]
# Thu, 04 Mar 2021 00:24:49 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 04 Mar 2021 00:24:49 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 Mar 2021 00:24:49 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 04 Mar 2021 00:24:50 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 04 Mar 2021 00:24:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 00:25:05 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 04 Mar 2021 00:25:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 Mar 2021 00:25:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 Mar 2021 00:25:05 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 04 Mar 2021 00:25:06 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 04 Mar 2021 00:25:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 Mar 2021 00:25:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91c0c19c84860aaa974864243509770a5b009f3a88b4a228010a9ade71ac968`  
		Last Modified: Tue, 09 Feb 2021 17:20:14 GMT  
		Size: 3.3 MB (3267910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828cc7cfd65faf51f4ee90844aed4b96bd2265aa26db758e2d72f5ea54ce5af6`  
		Last Modified: Wed, 03 Mar 2021 23:46:29 GMT  
		Size: 186.1 MB (186089847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a33d32e485fca54e6976a29c211f34b48d4e0153b557509e9c9c576a6e16e2`  
		Last Modified: Thu, 04 Mar 2021 00:27:55 GMT  
		Size: 2.6 MB (2616789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf9694838bf589c118185a54f7726bf6d0e8f4b416920759be21784e5134fd`  
		Last Modified: Thu, 04 Mar 2021 00:27:57 GMT  
		Size: 9.6 MB (9581228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6552d5a6a306aa763c176d6bf0a24b1e75979fc93097c37ad4bec9a33bae4e`  
		Last Modified: Thu, 04 Mar 2021 00:27:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796137dd4e57b4ebc07e0a62b3127172fc645ffdf6f1e327632aec43eb6f60b5`  
		Last Modified: Thu, 04 Mar 2021 00:27:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9814e381630d6c197bec96e0f4626f999bddc4a53da6d3f3ab940a73fd742b17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223285339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c70eb7680e091e11ebbf5d52a4e4c6e3e817b0dcf062c57842617f929f3b488`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:12:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 07:12:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 09 Feb 2021 07:12:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 07:12:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Feb 2021 21:56:00 GMT
ENV JAVA_VERSION=17-ea+11
# Fri, 26 Feb 2021 21:56:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/11/GPL/openjdk-17-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='03f129a2a92537e3eea68a0f816baae2e97a228deb50176631d040f6895b3d78'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/11/GPL/openjdk-17-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8680345eaa4cd3e14584f480f75491fd20966a6fd6c9d4a418e0ec55d9d2ed12'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Feb 2021 21:56:26 GMT
CMD ["jshell"]
# Fri, 26 Feb 2021 22:29:22 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 26 Feb 2021 22:29:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Feb 2021 22:29:23 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 26 Feb 2021 22:29:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 26 Feb 2021 22:29:34 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Feb 2021 22:29:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 26 Feb 2021 22:29:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Feb 2021 22:29:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Feb 2021 22:29:47 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 26 Feb 2021 22:29:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 26 Feb 2021 22:29:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Feb 2021 22:29:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96062c0c15f683e4abb09efb938dfd7ff23002f72a375c75492d44bde3a6c26f`  
		Last Modified: Tue, 09 Feb 2021 07:22:32 GMT  
		Size: 3.1 MB (3118711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8686785edc66f81a75368e82afa9f07feea9de89d4811e9b6e4afe6a5669a6`  
		Last Modified: Fri, 26 Feb 2021 22:02:19 GMT  
		Size: 182.1 MB (182096095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25313e6154dfa3ff3d5433f533180ddebe0ec4526590a1e0d3262636350ef257`  
		Last Modified: Fri, 26 Feb 2021 22:32:20 GMT  
		Size: 2.6 MB (2636675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f463d002d04e157255e7b72851a465216920b2f8863d1dfc76f7ff8e78b42093`  
		Last Modified: Fri, 26 Feb 2021 22:32:23 GMT  
		Size: 9.6 MB (9581196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c401726f307bb72462edc42c9c36d7b953d771bfdf5da418fef6dd33ed7878`  
		Last Modified: Fri, 26 Feb 2021 22:32:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92fc38b793687495237b4e53979deed2dcbf8b47a1b9a12b7703cf531b609d7`  
		Last Modified: Fri, 26 Feb 2021 22:32:20 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
