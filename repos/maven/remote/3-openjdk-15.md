## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:75d356c47a7693e951b3ce70ea06449fcda4211304e6c0c5d50fac2069c75086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:f56a68b45fe148efc7e0760bf685b1c99599a2ad548b50b8ff728c1f8c303dd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263547187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab1412293cf62eb7693f829b2d169e88d5d53e4d5eb5d054f66168a02ec74b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:22:32 GMT
ADD file:79bb5b8b89fe54ba99fd9d42d4f8774bfb9c1319ac3ead17a2005a3bde852451 in / 
# Wed, 10 Jun 2020 18:22:32 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 18:39:27 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 18:39:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Jun 2020 18:39:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 10 Jun 2020 18:39:28 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2020 21:23:53 GMT
ENV JAVA_VERSION=15-ea+27
# Mon, 15 Jun 2020 21:24:28 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/27/GPL/openjdk-15-ea+27_linux-aarch64_bin.tar.gz; 			downloadSha256=9195473bcb8e4ceaf0113cdb7b3dad468f3c045ebb9c0ce326bf01818c089269; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/27/GPL/openjdk-15-ea+27_linux-x64_bin.tar.gz; 			downloadSha256=db20094a26993699a0c6beb10dc5d07d9e708ab1fc0bfb7aff637944c3319374; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 15 Jun 2020 21:24:28 GMT
CMD ["jshell"]
# Mon, 15 Jun 2020 21:52:20 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 15 Jun 2020 21:52:20 GMT
ARG USER_HOME_DIR=/root
# Mon, 15 Jun 2020 21:52:20 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 15 Jun 2020 21:52:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 15 Jun 2020 21:52:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 15 Jun 2020 21:52:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 15 Jun 2020 21:52:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 15 Jun 2020 21:52:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 15 Jun 2020 21:52:23 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 15 Jun 2020 21:52:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 15 Jun 2020 21:52:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fa926a7d213a8145d6a906d68a085b21909a4b26871f142804e68b322bf8881f`  
		Last Modified: Wed, 10 Jun 2020 18:23:43 GMT  
		Size: 43.5 MB (43457466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aed8993d2fb0bb3a658c631a1dfbd05c0e5d42218f419d18238996bd06ea08`  
		Last Modified: Wed, 10 Jun 2020 18:42:25 GMT  
		Size: 14.8 MB (14760261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c9c7fdc1fda1d116b16d789507a33e9d21aa509a9e15e93084b1190bee0353`  
		Last Modified: Mon, 15 Jun 2020 21:27:05 GMT  
		Size: 195.7 MB (195746579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa652ea6790574f0281bc28ba32357b93c8d95b3dab426c6ce17c1b680bf788`  
		Last Modified: Mon, 15 Jun 2020 21:53:35 GMT  
		Size: 9.6 MB (9581667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba28d5f08666f70773788cef2f1aa8d23b8423332272de5019b97f469e32585`  
		Last Modified: Mon, 15 Jun 2020 21:53:35 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6020db59b80291d5cd8daa66acd825e2a67cd383e41470403ca918f9385edafd`  
		Last Modified: Mon, 15 Jun 2020 21:53:35 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
