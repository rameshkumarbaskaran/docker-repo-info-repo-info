## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:2083e402638db456b65b4a769a26dc3f663cb266dcb10e5da2c4209fe449cc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:2d3400cce837fc38d2ad896593d0a6cb2d523c841e4aa4b3deb48543932bc357
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349032572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35007819e2b84d8f841d1b8379784d038b041c89a205fbad285e40f2f9326fc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:21:31 GMT
ADD file:02670bc2999f43239e261c6f4e819f10471cfababa139f0eeba033a934c44eed in / 
# Fri, 24 Jul 2020 00:21:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:28:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Aug 2020 21:28:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Aug 2020 21:29:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 26 Aug 2020 21:29:17 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Aug 2020 21:29:17 GMT
ENV JAVA_VERSION=15
# Wed, 26 Aug 2020 21:30:03 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Wed, 26 Aug 2020 21:30:03 GMT
CMD ["jshell"]
# Wed, 26 Aug 2020 22:06:07 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 26 Aug 2020 22:06:07 GMT
ARG USER_HOME_DIR=/root
# Wed, 26 Aug 2020 22:06:07 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 26 Aug 2020 22:06:07 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 27 Aug 2020 18:21:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Thu, 27 Aug 2020 18:21:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 27 Aug 2020 18:21:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Aug 2020 18:21:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Aug 2020 18:21:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 27 Aug 2020 18:21:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 27 Aug 2020 18:21:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Aug 2020 18:21:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1bbe67b820dbc81dda19341c188f2504cb57d03d540dc94bf12e3f752102adf8`  
		Last Modified: Fri, 24 Jul 2020 00:23:22 GMT  
		Size: 53.2 MB (53238241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c479ccfad94616e2be168f7843f91429bd9a7d0996b687d670bfe633136895a`  
		Last Modified: Wed, 26 Aug 2020 21:33:04 GMT  
		Size: 13.4 MB (13417665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ca405b312fe1edfc03f2a3de122ddb66568ec43d1817dad6f916d7bda5261`  
		Last Modified: Wed, 26 Aug 2020 21:33:57 GMT  
		Size: 195.7 MB (195748417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91498bc98cfb76d020869b64968a8d23c0344f8b6625f7add300adaa1ebe1306`  
		Last Modified: Thu, 27 Aug 2020 18:23:26 GMT  
		Size: 77.0 MB (77045800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d3f94515f30aa4a1947b4bdab392c712c5111f946f0e1e55351488b10d617a`  
		Last Modified: Thu, 27 Aug 2020 18:23:22 GMT  
		Size: 9.6 MB (9581231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f830c0613ce10ae914d6e61149bf8b58c26fb7f2435457a8866dfe16e83efc`  
		Last Modified: Thu, 27 Aug 2020 18:23:21 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cab988b28f56788aa6652d8c5db4d632d864cae54c72d7ee4bc52f645fbfa1`  
		Last Modified: Thu, 27 Aug 2020 18:23:21 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-15` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8cf2895e8faa54a8591e1693ca65475e6ad3d7bfa99aeec9b992618abe131b4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304797434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f5a63a7c67e7a796972def22c732641b99c135288cc6a6aedcca03c20e85cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:53:42 GMT
ADD file:2ad87b72223c423a2c0741208d69b5b361aabaa96bfbe1510fa44745a72c0e7f in / 
# Fri, 24 Jul 2020 00:53:46 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:35:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Aug 2020 21:36:01 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Aug 2020 21:37:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 26 Aug 2020 21:37:30 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Aug 2020 21:37:31 GMT
ENV JAVA_VERSION=15
# Wed, 26 Aug 2020 21:38:40 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Wed, 26 Aug 2020 21:38:48 GMT
CMD ["jshell"]
# Thu, 27 Aug 2020 18:40:12 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 27 Aug 2020 18:40:13 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Aug 2020 18:40:13 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 27 Aug 2020 18:40:14 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 27 Aug 2020 18:40:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Thu, 27 Aug 2020 18:40:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 27 Aug 2020 18:40:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Aug 2020 18:40:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Aug 2020 18:40:51 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 27 Aug 2020 18:40:51 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 27 Aug 2020 18:40:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Aug 2020 18:40:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4e618d2a55163b9d055a0c627bc7faff5f4210ee92e01ce1b82dd0738d8c5e12`  
		Last Modified: Fri, 24 Jul 2020 00:55:39 GMT  
		Size: 53.3 MB (53345174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03d65a39d352a49fbfba9a4223490a35071d814a500f1e7a378ce915dd32f6`  
		Last Modified: Wed, 26 Aug 2020 21:40:32 GMT  
		Size: 14.3 MB (14331702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65ebdbc9d70b195f30e8d9d09e8643180f2e44cf31aa42d6c758bc2d61abe6f`  
		Last Modified: Wed, 26 Aug 2020 21:41:47 GMT  
		Size: 174.9 MB (174858488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8792dad5765d583cdb6b5e597121d5a37e6ac845dd05f36a6d506354530a7da3`  
		Last Modified: Thu, 27 Aug 2020 18:42:27 GMT  
		Size: 52.7 MB (52679647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8de937e59bfc2b544af7da05f4cbbe1a0790325a7d81197926e18dd9fb79ff`  
		Last Modified: Thu, 27 Aug 2020 18:42:22 GMT  
		Size: 9.6 MB (9581207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f98830c75e34b2f4662f8c97dfe53c98a902e5ad16e6595937e428ecad3907`  
		Last Modified: Thu, 27 Aug 2020 18:42:20 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a162cf8e33ceb2f56e1e11ff9ac6fab30c2ea8ffd7ebab90177b24f5d1b558`  
		Last Modified: Thu, 27 Aug 2020 18:42:20 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
