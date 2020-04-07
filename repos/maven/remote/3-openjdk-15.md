## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:a7b6e73f87090aa584a7b7175742464185fa3f5c8201ab335cf406635d38d287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:2d18b8052c370a024be74e0295c9ecf60ef4a7f889ecca2420280f9a5cc809ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265713995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a422f774ce5413928bef84cf6ebde59afca4cdf2cb47203355f065e98b0166`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:37:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 10 Mar 2020 02:37:58 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_VERSION=15-ea+17
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/17/GPL/openjdk-15-ea+17_linux-x64_bin.tar.gz
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_SHA256=e8022a7a00c3f8cc7518cbe89f7023356322c2583ce884e2c727218c07595b1a
# Mon, 06 Apr 2020 23:22:50 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 06 Apr 2020 23:22:50 GMT
CMD ["jshell"]
# Mon, 06 Apr 2020 23:56:38 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 06 Apr 2020 23:56:38 GMT
ARG USER_HOME_DIR=/root
# Mon, 06 Apr 2020 23:56:38 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 06 Apr 2020 23:56:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 06 Apr 2020 23:56:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 06 Apr 2020 23:56:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 06 Apr 2020 23:56:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 06 Apr 2020 23:56:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 06 Apr 2020 23:56:41 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 06 Apr 2020 23:56:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 06 Apr 2020 23:56:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486662a04f2c248e506892b8a1027b60a01a9eb4b5c0a8a4f58d9a30df53c59d`  
		Last Modified: Mon, 06 Apr 2020 23:25:33 GMT  
		Size: 198.6 MB (198635263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7275fa7b5a161c1b59dd36d2fbdc765c53e1a80e5f4e9589eb251fc3e565ab`  
		Last Modified: Mon, 06 Apr 2020 23:57:25 GMT  
		Size: 9.6 MB (9581685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d5a3bfd9c41e33bb6536a9e9727a7881abf98c0d269422e8891f6884b82b08`  
		Last Modified: Mon, 06 Apr 2020 23:57:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce309a9b23bd3a41f75d5dedd677244e961638fe081246ade0a33c8ba7232148`  
		Last Modified: Mon, 06 Apr 2020 23:57:23 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
