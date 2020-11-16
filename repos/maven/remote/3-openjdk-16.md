## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:5bb68f64a67afcb48d7c364113ed7c4900c3970100f29355d17a504d24157349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:8cbb5b42aec5a7c3762c2fc8befc48106c6f6013c82d5e36b812480bb2ab6956
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.5 MB (382537906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea152da52b2ade373c4523bef135623013a685c81596f111b398f7a6c43d30a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:37:29 GMT
ADD file:c6983fc83bb99ae9a8b343abf1e6852c64556f7c59e869f14f3f8835130d087d in / 
# Mon, 16 Nov 2020 19:37:29 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:19:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:19:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 16 Nov 2020 20:19:27 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:19:27 GMT
ENV JAVA_VERSION=16-ea+24
# Mon, 16 Nov 2020 20:20:08 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=9085bbb4f9e4d70ac385f85fbd706ab1fa570417beb28d09ff71e4908684cd8c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=ad1e33e43f923a8cde6e611e8ada1b76047f156d44b981d16daa440251f71823; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:20:08 GMT
CMD ["jshell"]
# Mon, 16 Nov 2020 20:48:59 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 16 Nov 2020 20:48:59 GMT
ARG USER_HOME_DIR=/root
# Mon, 16 Nov 2020 20:49:00 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 16 Nov 2020 20:49:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 16 Nov 2020 20:49:25 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Mon, 16 Nov 2020 20:49:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 16 Nov 2020 20:49:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 16 Nov 2020 20:49:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 16 Nov 2020 20:49:30 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 16 Nov 2020 20:49:30 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 16 Nov 2020 20:49:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 16 Nov 2020 20:49:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e69ec1c7b788c406991d1ce5f4a8f26a7ae9c0c9410d652237e2a6646ef53305`  
		Last Modified: Mon, 16 Nov 2020 19:38:51 GMT  
		Size: 42.1 MB (42053575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2259f1956e4980849285f91a1fd9fcc0f27002dddd076924e6801a2ae978db5a`  
		Last Modified: Mon, 16 Nov 2020 20:23:44 GMT  
		Size: 13.3 MB (13263119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca92ed3d79e4e38b59fbee06b306ca5291666513380d938b3ab534aa7271f03b`  
		Last Modified: Mon, 16 Nov 2020 20:23:58 GMT  
		Size: 183.5 MB (183540120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cd80150c0e5e7c47f0d671cc8cb30b2766511f87a782e90d45cedeb6e58e6b`  
		Last Modified: Mon, 16 Nov 2020 20:52:02 GMT  
		Size: 134.1 MB (134098668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f300c67e25a612c65ff8cb96999506556dd497393d9aef4ce1fb0b93bf64c24`  
		Last Modified: Mon, 16 Nov 2020 20:51:48 GMT  
		Size: 9.6 MB (9581204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f318caf1738c2b966d2b6faf9bb4f25ddf59fd8426a9326a28f4e28f6bb98b`  
		Last Modified: Mon, 16 Nov 2020 20:51:48 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19b9ac7f4d385fc37881b292dec6c5b869773d49df9059665960e1d7312a15`  
		Last Modified: Mon, 16 Nov 2020 20:51:47 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7527d3a2b3b216d8d1ce56546df79809351d3f10598ffc4476eb38c846a3bfea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356034168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee1fdfc819e44557d1c5f4c293cd3ab1f2451d42086fcf09f19557eb4e3cc3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:46:09 GMT
ADD file:91f2f5092142d551bd5542d693b0d6f9d6f9de47a18e19492b8db9dd24ef0786 in / 
# Mon, 16 Nov 2020 19:46:11 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:04:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:04:05 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:04:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 16 Nov 2020 20:04:06 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:04:07 GMT
ENV JAVA_VERSION=16-ea+24
# Mon, 16 Nov 2020 20:04:31 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=9085bbb4f9e4d70ac385f85fbd706ab1fa570417beb28d09ff71e4908684cd8c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=ad1e33e43f923a8cde6e611e8ada1b76047f156d44b981d16daa440251f71823; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:04:34 GMT
CMD ["jshell"]
# Mon, 16 Nov 2020 20:31:46 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 16 Nov 2020 20:31:47 GMT
ARG USER_HOME_DIR=/root
# Mon, 16 Nov 2020 20:31:47 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 16 Nov 2020 20:31:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 16 Nov 2020 20:33:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Mon, 16 Nov 2020 20:33:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 16 Nov 2020 20:33:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 16 Nov 2020 20:33:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 16 Nov 2020 20:33:16 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 16 Nov 2020 20:33:17 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 16 Nov 2020 20:33:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 16 Nov 2020 20:33:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:74c8bc77d8380334fed77b152e6228e91ad4e881fb67a762337f88c14031e719`  
		Last Modified: Mon, 16 Nov 2020 19:47:43 GMT  
		Size: 42.0 MB (41982578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01f480947edbfcab3306d055a8959aa86cba86597ea1e29c498fa3fd689e7e4`  
		Last Modified: Mon, 16 Nov 2020 20:08:26 GMT  
		Size: 14.1 MB (14060251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ece332526f8b9f4866a3843d8b32c3bfae6e17d2981e3598f718e67bb7598cb`  
		Last Modified: Mon, 16 Nov 2020 20:08:47 GMT  
		Size: 178.0 MB (178013510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7339a1849b9ba55892d92fda47000413257a6c53eab64eb6fc4695f6aa71564c`  
		Last Modified: Mon, 16 Nov 2020 20:36:08 GMT  
		Size: 112.4 MB (112395414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d73d0ee8bf60a678fd1febb24352f8982e4945e9e817c2b6eb398ff495a6a18`  
		Last Modified: Mon, 16 Nov 2020 20:35:48 GMT  
		Size: 9.6 MB (9581198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c495e9b6273c3cce7d566519d1dff75f222b95a092928d4d2db2b3d1d977348`  
		Last Modified: Mon, 16 Nov 2020 20:35:47 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f405422a0f95ba206a298e343b7c30b424d7c1a81f028bf5c98aa48710adfb`  
		Last Modified: Mon, 16 Nov 2020 20:35:47 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
