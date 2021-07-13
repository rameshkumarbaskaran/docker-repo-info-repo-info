## `maven:3-openjdk-17`

```console
$ docker pull maven@sha256:dec2a7390f36c4b4abdd99f17b24c2c84e841cc795eb0a055e393282b4f72608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17` - linux; amd64

```console
$ docker pull maven@sha256:9c9cadc6314442e6e3f2225dce9cb68eaa1f20a4f6689c64e95e021cdc676027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.0 MB (418959834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8981a36b780f24a8769adfc32779f6cccb19e97f5761ba92d238642ff2df2dbc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 30 Jun 2021 17:23:40 GMT
ADD file:d49890823c4e8287f936eec210400575f79c20f14f048017368faed0584841a6 in / 
# Wed, 30 Jun 2021 17:23:41 GMT
CMD ["/bin/bash"]
# Wed, 30 Jun 2021 17:40:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Jun 2021 17:43:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 30 Jun 2021 17:43:12 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Jun 2021 17:43:12 GMT
ENV LANG=C.UTF-8
# Fri, 02 Jul 2021 19:26:29 GMT
ENV JAVA_VERSION=17-ea+29
# Fri, 02 Jul 2021 19:26:41 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c277cda62e368aa595450d3ffa018fbe98adc97c08e0ab777f5f74e86e3bf3f3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='8d5901a58b02e77d255166678c54cdc14c293d17730d794d70bb13434a934bb4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 02 Jul 2021 19:26:42 GMT
CMD ["jshell"]
# Fri, 02 Jul 2021 20:54:30 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 02 Jul 2021 20:54:30 GMT
ARG USER_HOME_DIR=/root
# Fri, 02 Jul 2021 20:54:31 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 02 Jul 2021 20:54:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 02 Jul 2021 20:54:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 02 Jul 2021 20:55:00 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 02 Jul 2021 20:55:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 02 Jul 2021 20:55:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 02 Jul 2021 20:55:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 02 Jul 2021 20:55:01 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 02 Jul 2021 20:55:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 02 Jul 2021 20:55:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9660ffb7976c51eb47b4425f6bb95173c170f4fcc442a2bb2b6ba7bf154f6fc8`  
		Last Modified: Wed, 30 Jun 2021 17:25:00 GMT  
		Size: 42.2 MB (42179226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f8b4ca74ea5f238671d4c7981ca7c99e6c70d3fcd8d4d0596ccdf6b8329dbe`  
		Last Modified: Wed, 30 Jun 2021 17:50:04 GMT  
		Size: 13.4 MB (13391447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d232cb69bc19e391b23d86daf9fb513e382855a72df89b5869dc79fefeee3a95`  
		Last Modified: Fri, 02 Jul 2021 19:35:24 GMT  
		Size: 187.1 MB (187136575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8934e505bff76758b3d234994a7d87307e778ff48b6034c2b233cfc5970410`  
		Last Modified: Fri, 02 Jul 2021 20:58:04 GMT  
		Size: 166.6 MB (166640406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bee541f7d946a4febebe70e2a6cebb1ff57544d98db496fd21d5dae1ea89382`  
		Last Modified: Fri, 02 Jul 2021 20:57:51 GMT  
		Size: 9.6 MB (9610967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e98eae4dd559f1e73b9af50bf494d70bfe73283fdd59ec979006582104272`  
		Last Modified: Fri, 02 Jul 2021 20:57:50 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba630e8df32254f542d3b52c0a54d5a84b2f58fe3fd87480c8c7b623382d023`  
		Last Modified: Fri, 02 Jul 2021 20:57:50 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e2e451eb41408a942e9c44956dfb6072bc009cde34126e1280878ebeb42e2489
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397945642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e19b584a8aa8bdb654c36db605fd97da2344e7a4806d4e5c82f9dc488d2f97`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jul 2021 20:40:32 GMT
ADD file:a184ed870dc7a85028f7ba3bd0cf3820d6f1b94ac4cea1ac94ca48c786901041 in / 
# Mon, 12 Jul 2021 20:40:33 GMT
CMD ["/bin/bash"]
# Mon, 12 Jul 2021 21:03:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jul 2021 21:04:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 12 Jul 2021 21:04:07 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jul 2021 21:04:07 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jul 2021 21:04:07 GMT
ENV JAVA_VERSION=17-ea+29
# Mon, 12 Jul 2021 21:04:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='c277cda62e368aa595450d3ffa018fbe98adc97c08e0ab777f5f74e86e3bf3f3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/29/GPL/openjdk-17-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='8d5901a58b02e77d255166678c54cdc14c293d17730d794d70bb13434a934bb4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jul 2021 21:04:17 GMT
CMD ["jshell"]
# Mon, 12 Jul 2021 21:57:13 GMT
ARG MAVEN_VERSION=3.8.1
# Mon, 12 Jul 2021 21:57:13 GMT
ARG USER_HOME_DIR=/root
# Mon, 12 Jul 2021 21:57:13 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Mon, 12 Jul 2021 21:57:14 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Mon, 12 Jul 2021 21:57:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Mon, 12 Jul 2021 21:57:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 12 Jul 2021 21:57:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 12 Jul 2021 21:57:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 12 Jul 2021 21:57:39 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 12 Jul 2021 21:57:39 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 12 Jul 2021 21:57:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 12 Jul 2021 21:57:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6186b25cabd91cbdd2c6bf65b0c5ef261f52719e7c6c4d6252e7082b7a51b42e`  
		Last Modified: Mon, 12 Jul 2021 20:41:48 GMT  
		Size: 42.1 MB (42072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8304774b066b61c2ae3dc6de204cb3d384a726b9376d301afc654577b50a9c0`  
		Last Modified: Mon, 12 Jul 2021 21:15:51 GMT  
		Size: 14.2 MB (14170180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fad876415c6c37eeb35cf7c8ce30e85f758a68fb2a4ae4818da58c713186b8c`  
		Last Modified: Mon, 12 Jul 2021 21:17:28 GMT  
		Size: 185.9 MB (185943235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c770f0bda98a79e0dc53d3524259c72862c33faa6994b986ff9b289718923646`  
		Last Modified: Mon, 12 Jul 2021 22:03:13 GMT  
		Size: 146.1 MB (146147379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5883a50f9577d333a40f2bf15e610ef5bf9112664e87f34c568f7e92c048c51b`  
		Last Modified: Mon, 12 Jul 2021 22:02:57 GMT  
		Size: 9.6 MB (9610916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbe3c66b206afe855a857d7de2731433425fe89855b3e737094eb0956aacdc6`  
		Last Modified: Mon, 12 Jul 2021 22:02:56 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603ca0ee1d6063508ed6b8ab9dd586a131b09cd4cc9ff5237f1697b5574f9fd0`  
		Last Modified: Mon, 12 Jul 2021 22:02:56 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
