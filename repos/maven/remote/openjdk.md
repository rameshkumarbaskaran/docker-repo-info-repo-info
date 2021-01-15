## `maven:openjdk`

```console
$ docker pull maven@sha256:4ed3e8b6a426af743fffd7e92c43075102966b6a651fe4cab2616a32f4460f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:openjdk` - linux; amd64

```console
$ docker pull maven@sha256:9329a294e082ed035e32a1445361fa66c83ea65ebf481c4c5b2ac5e3165a04ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399944895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6519353c1d70c3422eb0b2e0f2569f239fe913275dce878bdc804d0cae3cf25c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 15 Jan 2021 00:30:38 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Fri, 15 Jan 2021 00:30:39 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:56:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:56:53 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 01:00:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 15 Jan 2021 01:00:41 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Jan 2021 01:00:42 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 15 Jan 2021 01:01:35 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Jan 2021 01:01:35 GMT
CMD ["jshell"]
# Fri, 15 Jan 2021 01:43:28 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 15 Jan 2021 01:43:28 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 Jan 2021 01:43:28 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 15 Jan 2021 01:43:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 15 Jan 2021 01:43:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 15 Jan 2021 01:43:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 15 Jan 2021 01:43:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 Jan 2021 01:43:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 Jan 2021 01:43:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 15 Jan 2021 01:44:00 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 15 Jan 2021 01:44:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 Jan 2021 01:44:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a73adebe9317092fb1f120a1d0d21f460296e9bde7ac683fd452cfc628c528cf`  
		Last Modified: Wed, 06 Jan 2021 20:23:26 GMT  
		Size: 42.1 MB (42069921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b73bcd34cfec7fc27d7cd00bc22af06df0471526a6d2ceb8e77391a82f300f0`  
		Last Modified: Fri, 15 Jan 2021 01:08:29 GMT  
		Size: 13.3 MB (13277589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08695d680cb5949b20a6469fea8323b239b1b8b0ff4418c08800d3959d9fad6`  
		Last Modified: Fri, 15 Jan 2021 01:11:47 GMT  
		Size: 195.8 MB (195778236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be3850dcaf3c963c191d60b73373738f8c6c22a490fabde4f17ca71a87998b`  
		Last Modified: Fri, 15 Jan 2021 01:48:03 GMT  
		Size: 139.2 MB (139236728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3d792d6604a32f05915fdabf9d6ac3f3c5c869ceb0972051f43b80a40a336e`  
		Last Modified: Fri, 15 Jan 2021 01:47:50 GMT  
		Size: 9.6 MB (9581204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d7a4d73a32d9686a6a9d99612fad4248a1578d7f5fd5f70a45a110e2bf35b3`  
		Last Modified: Fri, 15 Jan 2021 01:47:47 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1fd800fcc9fb287f9e4365c77ab2f16eaaa4acc70c81c3938aa73800682a5b`  
		Last Modified: Fri, 15 Jan 2021 01:47:46 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:openjdk` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:970c83cc6819a8b8ef61e27ce81fa589882c582821d05ac6cd7e9300d4d2d496
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358183387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d658fa2f80ef8c3774181e59e6ffc4eca18cea5279f6f4b105502af3c7e70d0a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 15 Jan 2021 00:05:48 GMT
ADD file:ad2b2ddca8e17229cc8d1380ecda32c4b2c04f1e2aed8f493f745c6352b34e60 in / 
# Fri, 15 Jan 2021 00:05:49 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:43:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:43:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:48:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 15 Jan 2021 00:48:42 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Jan 2021 00:48:43 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 15 Jan 2021 00:49:21 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Jan 2021 00:49:22 GMT
CMD ["jshell"]
# Fri, 15 Jan 2021 01:38:54 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 15 Jan 2021 01:38:54 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 Jan 2021 01:38:55 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 15 Jan 2021 01:38:56 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 15 Jan 2021 01:40:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 15 Jan 2021 01:40:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 15 Jan 2021 01:40:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 Jan 2021 01:40:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 Jan 2021 01:40:53 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 15 Jan 2021 01:40:53 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 15 Jan 2021 01:40:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 Jan 2021 01:40:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d0eecbd2c3e7306adbf5b4a0d9bebc7d266ebe78bda044d35b0994c1cf655a54`  
		Last Modified: Wed, 06 Jan 2021 20:47:00 GMT  
		Size: 42.0 MB (41996293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f86f1d6521cdc8416801b8dd0b15d9a5a85bfa3eb8f9afa832aa8cc652732`  
		Last Modified: Fri, 15 Jan 2021 00:55:15 GMT  
		Size: 14.1 MB (14057398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a792fab72e70e638b6bb816e8d2e66850c7c91af09372d8ad11c6c2d4d7d0e61`  
		Last Modified: Fri, 15 Jan 2021 00:59:13 GMT  
		Size: 174.9 MB (174887923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18a6749a2e0a9efeb1713916464e218fbf67d736594200daaf7a9732c6d38f`  
		Last Modified: Fri, 15 Jan 2021 01:45:30 GMT  
		Size: 117.7 MB (117659354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ae6bf12e9e20d03775b5c03a2ff637197383fda46dcf2c1a3045a954d062b1`  
		Last Modified: Fri, 15 Jan 2021 01:45:11 GMT  
		Size: 9.6 MB (9581201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565d53b5c11c52118587a98fa1940790c42426364ac39b9506e2ffffcbed37f`  
		Last Modified: Fri, 15 Jan 2021 01:45:10 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9251b11f40007e9d907c696ff9c9f75c9ee8d5e2086dba31d1b37631a00f68bc`  
		Last Modified: Fri, 15 Jan 2021 01:45:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
