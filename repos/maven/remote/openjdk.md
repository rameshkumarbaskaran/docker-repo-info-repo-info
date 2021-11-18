## `maven:openjdk`

```console
$ docker pull maven@sha256:ae9822e3b015945bfbda6a2d578ad64b7afeeb7eaa8cc909fa17990e239db5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:openjdk` - linux; amd64

```console
$ docker pull maven@sha256:8cf438526646e93550137cc3a37b87af4be36161bf5920ce2410005d62c621ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.1 MB (413060945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c759eb291627e9e29f51a59d61f05e980381afe728078f0a8fa8478a6c93c45b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Nov 2021 22:20:09 GMT
ADD file:ee2c184d933cfe1848f54f94d92f5c14d073160b62ec403259b18392d4ec6e1b in / 
# Wed, 03 Nov 2021 22:20:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 22:37:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 03 Nov 2021 22:37:43 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 22:37:43 GMT
ENV LANG=C.UTF-8
# Wed, 03 Nov 2021 22:37:43 GMT
ENV JAVA_VERSION=17.0.1
# Wed, 03 Nov 2021 22:37:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Nov 2021 22:37:55 GMT
CMD ["jshell"]
# Wed, 03 Nov 2021 23:03:14 GMT
ARG MAVEN_VERSION=3.8.3
# Wed, 03 Nov 2021 23:03:14 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Nov 2021 23:03:14 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Wed, 03 Nov 2021 23:03:14 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Wed, 03 Nov 2021 23:03:42 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN microdnf install findutils git
# Wed, 03 Nov 2021 23:03:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 03 Nov 2021 23:03:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Nov 2021 23:03:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Nov 2021 23:03:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 03 Nov 2021 23:03:45 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 03 Nov 2021 23:03:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Nov 2021 23:03:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0a6167eaa66c8f2dc1c8dbed1a335f3d4052409454c9f7fbcd8fc35d8576a7e2`  
		Last Modified: Wed, 03 Nov 2021 22:21:16 GMT  
		Size: 42.0 MB (41968115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88dabbf57eeb24f57debafeba0a2f7b2f4e4e76d1aa9a3bd27edf0682e0f15`  
		Last Modified: Wed, 03 Nov 2021 22:43:12 GMT  
		Size: 13.5 MB (13491241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b155ffb89768057e29fde0298c8288907d16e07888ca6fe324ff03247c3b0c9`  
		Last Modified: Wed, 03 Nov 2021 22:44:33 GMT  
		Size: 187.2 MB (187170410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413ce1aac9048a9f52d95da3e3b92cb0f41f99b99b888da51ad1f24aec10d1ea`  
		Last Modified: Wed, 03 Nov 2021 23:05:50 GMT  
		Size: 161.3 MB (161324328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15c294b74e6557948d48f5f29e7fbe09806c0649664dfa246b46f3d6f010911`  
		Last Modified: Wed, 03 Nov 2021 23:05:37 GMT  
		Size: 9.1 MB (9105637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da27e3212be05fc50a35986ed0e4cfd678d4be1109d8f1cc9cbf8e1590b96f26`  
		Last Modified: Wed, 03 Nov 2021 23:05:36 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97151e59d3e1e43c7d8b1f6ffb4f4603e26605b751ed00b1555a061bed3e2d2a`  
		Last Modified: Wed, 03 Nov 2021 23:05:36 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:openjdk` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:10af588f5c23745b515bfa2b29e771b5d8e0b39887045a1377f136e00a331e43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.0 MB (405022728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e698652281552fc21ee5abe4e949ae23fac7ea90f9147ee78991f70967852`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Nov 2021 08:24:53 GMT
ADD file:98b355b05026edaab234cff8ee34d8335b233cbaa04a19ac82df4a2b0c7fdc4d in / 
# Thu, 18 Nov 2021 08:24:54 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 10:14:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 10:15:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 18 Nov 2021 10:15:57 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:15:58 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 10:15:59 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 18 Nov 2021 10:16:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 10:16:12 GMT
CMD ["jshell"]
# Thu, 18 Nov 2021 10:57:52 GMT
ARG MAVEN_VERSION=3.8.3
# Thu, 18 Nov 2021 10:57:52 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Nov 2021 10:57:53 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Thu, 18 Nov 2021 10:57:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Thu, 18 Nov 2021 10:58:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN microdnf install findutils git
# Thu, 18 Nov 2021 10:59:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 18 Nov 2021 10:59:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Nov 2021 10:59:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Nov 2021 10:59:18 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 18 Nov 2021 10:59:19 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 18 Nov 2021 10:59:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Nov 2021 10:59:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1bdb3a9e404c972ab03f65fd56b5b815b51d6a68324015dc69707d48e2ba3cdf`  
		Last Modified: Thu, 18 Nov 2021 08:26:02 GMT  
		Size: 42.0 MB (42010198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9356b5c0bb88b90b52af9c2836e152e11b910a0e88807e8327df1e2a965a7d1`  
		Last Modified: Thu, 18 Nov 2021 10:27:05 GMT  
		Size: 14.3 MB (14300065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebcde57d02d35340ce36ec0552bcaf6b57a0d93eb1f76e4984608a1a0d73072`  
		Last Modified: Thu, 18 Nov 2021 10:28:46 GMT  
		Size: 186.0 MB (185976746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3849bf82f2af426f484c807dbc7b3007b9d354611385967706fe9bb411debf`  
		Last Modified: Thu, 18 Nov 2021 11:02:57 GMT  
		Size: 153.6 MB (153628936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a9f74a51a5bb51abb1a3cb81202c30c15a2d12f2b968afbdb11c72ae40413`  
		Last Modified: Thu, 18 Nov 2021 11:02:42 GMT  
		Size: 9.1 MB (9105564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4db797d1fe8f20940780c1b07a8400228722e3cf479565ab91b6c2d9521cd1`  
		Last Modified: Thu, 18 Nov 2021 11:02:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37159e19b71b44b12182c5be50cef9ad2ac2bf14e81301e43a4f93a2d88fecfd`  
		Last Modified: Thu, 18 Nov 2021 11:02:40 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
