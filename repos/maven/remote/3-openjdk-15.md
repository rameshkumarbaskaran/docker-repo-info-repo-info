## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:a2999f1d7042daf2afcc736a608d299a4082a504d57b4511cf5dbe1fa74111ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:e56132a7b9391c6db208044af45ceecdb0d026a4d6291ad8a2a2551648a5d32c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263483949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f45f51037f633fe6bece43f80338c8089dcf9fd2177e7bd8e3245da2953d885`
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
# Mon, 22 Jun 2020 19:32:16 GMT
ENV JAVA_VERSION=15-ea+28
# Mon, 22 Jun 2020 20:22:00 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/28/GPL/openjdk-15-ea+28_linux-aarch64_bin.tar.gz; 			downloadSha256=5537ebe5b7beaa80af444a8494dcc1bad474ffae19803ba5327a14071a244869; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/28/GPL/openjdk-15-ea+28_linux-x64_bin.tar.gz; 			downloadSha256=dd7a0712379df213edd7dcee8c7e0ab06b117d851f05c55dbcaabf72536c347e; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Mon, 22 Jun 2020 20:22:00 GMT
CMD ["jshell"]
# Mon, 22 Jun 2020 21:04:09 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 22 Jun 2020 21:04:09 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2020 21:04:09 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 22 Jun 2020 21:04:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 22 Jun 2020 21:04:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 22 Jun 2020 21:04:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2020 21:04:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2020 21:04:14 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 22 Jun 2020 21:04:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 22 Jun 2020 21:04:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2020 21:04:15 GMT
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
	-	`sha256:bb3e97c919a8e8c1c80fb75854496ad6d2f7ad4063962c88d66307a4e7f3032f`  
		Last Modified: Mon, 22 Jun 2020 20:26:43 GMT  
		Size: 195.7 MB (195683330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1428ad74b6768681471660d558120343d23ebf3fd788ee09de19c2c5fd8a2c73`  
		Last Modified: Mon, 22 Jun 2020 21:05:41 GMT  
		Size: 9.6 MB (9581681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793dc41c84693687777bc8e714b6f0da122081385a7a76991eaa5e77e3c6e008`  
		Last Modified: Mon, 22 Jun 2020 21:05:41 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250817c926096026b9890770e618460bdee0e27d8985ffbff5f4935226ac8501`  
		Last Modified: Mon, 22 Jun 2020 21:05:40 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
