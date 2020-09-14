## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:97876108af4b1963957b8cf1739014c726bbb140c9e5190696cba73442d84557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:05f4d8023af321abd767b19b7561a55731f0e9a5607a87a0c8074c15926f018f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352193048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f6fb9338730a2f2e5e873ed06dae36913f0fdd82fdab77c312ebc11c36e6dc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 14 Sep 2020 18:33:21 GMT
ADD file:8011e31575cbf4b8ebb243821b300ba24330e02cab925024aa98f4ce27997846 in / 
# Mon, 14 Sep 2020 18:33:21 GMT
CMD ["/bin/bash"]
# Mon, 14 Sep 2020 18:50:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 14 Sep 2020 18:50:46 GMT
ENV LANG=C.UTF-8
# Mon, 14 Sep 2020 18:51:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 14 Sep 2020 18:51:54 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Sep 2020 18:51:54 GMT
ENV JAVA_VERSION=15
# Mon, 14 Sep 2020 18:52:40 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Sep 2020 18:52:40 GMT
CMD ["jshell"]
# Mon, 14 Sep 2020 19:19:52 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 14 Sep 2020 19:19:52 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Sep 2020 19:19:53 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 14 Sep 2020 19:19:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 14 Sep 2020 19:20:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Mon, 14 Sep 2020 19:20:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Sep 2020 19:20:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Sep 2020 19:20:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Sep 2020 19:20:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Sep 2020 19:20:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Sep 2020 19:20:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Sep 2020 19:20:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:79701ada7495177c292979fd69d41eee91dc93ef0feea5ff95bb453f4ab7a1c5`  
		Last Modified: Mon, 14 Sep 2020 18:35:00 GMT  
		Size: 54.2 MB (54164063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffa6cd00cf525ae203ffe0f93764b5d175c46f27a7e15bb0da88efb308e5292`  
		Last Modified: Mon, 14 Sep 2020 18:55:41 GMT  
		Size: 13.5 MB (13491747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b8613aa641f3057f2233da22f2218260f14fb12cc2e644f6e3c12f59f0555`  
		Last Modified: Mon, 14 Sep 2020 18:56:50 GMT  
		Size: 195.8 MB (195751073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc7c31afd3341c2c6d4897cf8c446b5dfa5741a730f666dc113aed1c2643ba1`  
		Last Modified: Mon, 14 Sep 2020 19:22:26 GMT  
		Size: 79.2 MB (79203757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124f775a01b01bc16373629fe07d93daf868b45411a6cc9aff87d16eb9c0b4f2`  
		Last Modified: Mon, 14 Sep 2020 19:22:22 GMT  
		Size: 9.6 MB (9581192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f42d8303af8b2efe7ee3f5bf35692010d7380ca2bc01834efeeaca5552728bb`  
		Last Modified: Mon, 14 Sep 2020 19:22:21 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be74aa545ae951585c9e519bf11a6cbfb14cae679d18ef66d6fd2ed1a0a717a5`  
		Last Modified: Mon, 14 Sep 2020 19:22:20 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-15` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:28984e37ca89939142189bc1b7494297a898d80a3d52157c3b4ea6af1cc8cc2c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307940651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb706138138e3afde7b099bf8df5aa70e03583186978899f2fc564b04055c2f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 14 Sep 2020 17:42:14 GMT
ADD file:b3bd5c2ec8ff0efe8a0b1384563b42f02d6bcf7531132d9ec4748ecfe264d476 in / 
# Mon, 14 Sep 2020 17:42:18 GMT
CMD ["/bin/bash"]
# Mon, 14 Sep 2020 17:59:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 14 Sep 2020 18:00:04 GMT
ENV LANG=C.UTF-8
# Mon, 14 Sep 2020 18:01:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 14 Sep 2020 18:01:47 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Sep 2020 18:01:49 GMT
ENV JAVA_VERSION=15
# Mon, 14 Sep 2020 18:02:39 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Sep 2020 18:02:42 GMT
CMD ["jshell"]
# Mon, 14 Sep 2020 21:24:56 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 14 Sep 2020 21:24:57 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Sep 2020 21:24:57 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 14 Sep 2020 21:24:58 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 14 Sep 2020 21:25:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Mon, 14 Sep 2020 21:25:34 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Sep 2020 21:25:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Sep 2020 21:25:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Sep 2020 21:25:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Sep 2020 21:25:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Sep 2020 21:25:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Sep 2020 21:25:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a805b9845b615e5963d09def3e5e9919b39e76b5122c2abecc98d4a4bb358394`  
		Last Modified: Mon, 14 Sep 2020 17:43:27 GMT  
		Size: 54.3 MB (54266593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dee2ba14d3dd42ac318a14c434bced8bd3cc7a2c58339deb209699b1d167b21`  
		Last Modified: Mon, 14 Sep 2020 20:56:35 GMT  
		Size: 14.4 MB (14366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c962550dadc0ccae13f43c26067641e639dd560cd6f0f96e1826189b592551db`  
		Last Modified: Mon, 14 Sep 2020 20:59:35 GMT  
		Size: 174.9 MB (174859078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd3cdf2f09edc8979b4d80326720afcd461d662640cada82cf956196034d613`  
		Last Modified: Mon, 14 Sep 2020 21:27:28 GMT  
		Size: 54.9 MB (54865721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27cf58b463921712722ae538c11026309dde4296f1224a93950060099a00583`  
		Last Modified: Mon, 14 Sep 2020 21:27:26 GMT  
		Size: 9.6 MB (9581208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb0b3a200b678fefe66f113515081de515792d4dc6de48d7dcf79c7044502b`  
		Last Modified: Mon, 14 Sep 2020 21:27:21 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7552dfd0b656f98ec8d96f2dda6d9b437692e48e5eb13d89cf2a5b613eff4fe0`  
		Last Modified: Mon, 14 Sep 2020 21:27:21 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
