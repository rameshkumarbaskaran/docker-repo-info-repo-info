## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:825aac62783925d755922a58247a42321269b94b0abb8fc680c74da07b678403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:12a81dc75cdd568dc7c7cd4d077d7acd05243e7fad502343c1bb52750ee9782c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389391033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da282fd63e244faf9500ed9651db2af1b06d6c1bb091a642e76e2317f30b7f0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 15 Jan 2021 00:30:38 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Fri, 15 Jan 2021 00:30:39 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:56:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 19:47:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 19:47:25 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:47:25 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:47:25 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 19:48:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:48:07 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 20:57:51 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 01 Feb 2021 20:57:51 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Feb 2021 20:57:51 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 01 Feb 2021 20:57:51 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 01 Feb 2021 20:58:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Mon, 01 Feb 2021 20:58:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 01 Feb 2021 20:58:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Feb 2021 20:58:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Feb 2021 20:58:22 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 01 Feb 2021 20:58:22 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 01 Feb 2021 20:58:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Feb 2021 20:58:22 GMT
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
	-	`sha256:892bf7047afcbaad9e98e2ee29fe5850d72f5aec866260583e1245222a2de146`  
		Last Modified: Mon, 01 Feb 2021 20:03:32 GMT  
		Size: 184.8 MB (184761945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c38b321d167219fd612498970cbce02ebfb28c0db3c711704888934209ea543`  
		Last Modified: Mon, 01 Feb 2021 21:03:33 GMT  
		Size: 139.7 MB (139699145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d0a84306f7abd5d774fea3ff226c75d14de55ba62ff260340369c47ab62508`  
		Last Modified: Mon, 01 Feb 2021 21:03:16 GMT  
		Size: 9.6 MB (9581216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85375066a3a000eca99fff2504d656798e31d31af3eeb1723f2abe3a797f2d43`  
		Last Modified: Mon, 01 Feb 2021 21:03:15 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eebac077ed979ddfec45888cf684a561022bdb6597491e1bac43ade0220d855`  
		Last Modified: Mon, 01 Feb 2021 21:03:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1f70f3df2e4df571a6b6ea683bc8dd7720f54e7638ccf2b6ef39d4c83625e02b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 MB (362786278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1268999c91ef8cc4af91f12989090f90a13e029d7d6837443ea89d082eecf9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:08:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 21:08:49 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:08:50 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 21:08:50 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 21:09:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:09:32 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 21:28:12 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 01 Feb 2021 21:28:12 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Feb 2021 21:28:13 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 01 Feb 2021 21:28:13 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 01 Feb 2021 21:28:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Mon, 01 Feb 2021 21:28:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 01 Feb 2021 21:28:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Feb 2021 21:28:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Feb 2021 21:28:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 01 Feb 2021 21:28:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 01 Feb 2021 21:28:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Feb 2021 21:28:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:17e75779b55909cd6075d706cc3fc9f838f287de73b35be3d551231217cbd32c`  
		Last Modified: Mon, 01 Feb 2021 21:02:50 GMT  
		Size: 42.0 MB (41996203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fad58a53edbb48f3027bc56f941db82a77fd6d28a6fc25d4bf2462f3bc62bc`  
		Last Modified: Mon, 01 Feb 2021 21:15:35 GMT  
		Size: 14.1 MB (14057108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b898a720d6e8a2a3e27f78c979bbd88064da63dfec9783cdea147cdcf7af1129`  
		Last Modified: Mon, 01 Feb 2021 21:17:25 GMT  
		Size: 179.1 MB (179144527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9778ae58add88196f9ec6f796eab7987946c9fe6956a350ace377c748d84d59a`  
		Last Modified: Mon, 01 Feb 2021 21:34:17 GMT  
		Size: 118.0 MB (118006022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138751934101edf701c302d07bf92e1f02a1ba4b99d0f7c75a8fc1562f2134ad`  
		Last Modified: Mon, 01 Feb 2021 21:33:58 GMT  
		Size: 9.6 MB (9581205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dd4137e35771270ce026803f762d8e66e7f2539f2cf8c0fb623b7e21789007`  
		Last Modified: Mon, 01 Feb 2021 21:33:57 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc94d26763ca805df39aa10fe7c7a42ad884599675a448d026363145384df01`  
		Last Modified: Mon, 01 Feb 2021 21:33:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
