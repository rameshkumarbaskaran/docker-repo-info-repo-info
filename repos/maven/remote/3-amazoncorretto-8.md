## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:00a7c0e0639befd3278f91d82edc26517498036c8ce6ac1aa60d82a1fb21814f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:fdf1fb02be77c29524f14f90239bec944d50c5a60f0298e81c08a75a7b698f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294225645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e1c5724984c6517b33d0892b943c3236be37baa4593590acc800d1c1da17fb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Mar 2023 01:20:24 GMT
COPY dir:1fe253a28ffa7545ac05b2d6b2410c0b48083e8195b6557287b6a94e845122d3 in / 
# Fri, 10 Mar 2023 01:20:24 GMT
CMD ["/bin/bash"]
# Fri, 10 Mar 2023 01:38:03 GMT
ARG version=1.8.0_362.b08-1
# Fri, 10 Mar 2023 01:38:25 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 10 Mar 2023 01:38:25 GMT
ENV LANG=C.UTF-8
# Fri, 10 Mar 2023 01:38:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 16 Mar 2023 19:24:31 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 16 Mar 2023 19:24:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Mar 2023 19:24:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Mar 2023 19:24:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Mar 2023 19:24:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Mar 2023 19:24:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Mar 2023 19:24:32 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Mar 2023 19:24:32 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Mar 2023 19:24:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Mar 2023 19:24:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Mar 2023 19:24:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:07e4d356f367b468402d36db62e60b734522576ce93a8e7246f1b36899c58f5e`  
		Last Modified: Thu, 09 Mar 2023 17:52:43 GMT  
		Size: 62.5 MB (62477005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31af72bf09a886cd3b0a63926d1351da28d400e7a4fadec011b41ac3e9b7f9b`  
		Last Modified: Fri, 10 Mar 2023 01:43:28 GMT  
		Size: 75.6 MB (75576600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080dc57664d853b52e1ac97fb1bf654c1e4fdf2197644ca9e2cb148a9e3c1c47`  
		Last Modified: Thu, 16 Mar 2023 19:32:07 GMT  
		Size: 147.1 MB (147079938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167e04981e50a49ee8da275b2fbb90c73c336207a7ff5fd42656209aacc7e370`  
		Last Modified: Thu, 16 Mar 2023 19:31:55 GMT  
		Size: 9.1 MB (9090725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd733bdf6880ce399c56a349b4deff6d72db8a00accab32eea01d4449575b466`  
		Last Modified: Thu, 16 Mar 2023 19:31:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc58e95a64fd7a7638feb47d087bbe8770ef08241cbdc8fed155a158e8ad0ef`  
		Last Modified: Thu, 16 Mar 2023 19:31:54 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b1d907ea64761fae4fcd5cecd624b0f12bd3df400ac669f03dcad8c514988`  
		Last Modified: Thu, 16 Mar 2023 19:31:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cebc5dc4bab8ca7787df7e2ab8c4ae36974b758b08e8492565770fd5da3185ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245035570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b40adfec4e87d80dcb177e46e57f1958bcbc3c6ed570404bbd980284037ad75`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Mar 2023 01:39:35 GMT
COPY dir:1997e4057e1f8b7df06806432d2b2c303c1f6ef5b18e8273d4393b867415d8b2 in / 
# Fri, 10 Mar 2023 01:39:36 GMT
CMD ["/bin/bash"]
# Fri, 10 Mar 2023 02:03:16 GMT
ARG version=1.8.0_362.b08-1
# Fri, 10 Mar 2023 02:03:31 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 10 Mar 2023 02:03:32 GMT
ENV LANG=C.UTF-8
# Fri, 10 Mar 2023 02:03:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 16 Mar 2023 19:58:04 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 16 Mar 2023 19:58:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Mar 2023 19:58:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Mar 2023 19:58:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Mar 2023 19:58:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Mar 2023 19:58:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Mar 2023 19:58:05 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Mar 2023 19:58:05 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Mar 2023 19:58:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Mar 2023 19:58:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Mar 2023 19:58:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:042c9cfa8a36c0ffe86667a7dd7d488f78cbe295aa845213c01fdf8784165a92`  
		Last Modified: Fri, 10 Mar 2023 01:40:11 GMT  
		Size: 64.1 MB (64125204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ef846573efdf933db57fc67084e92a8dc0b9407317e91c7b5169c60dbabec6`  
		Last Modified: Fri, 10 Mar 2023 02:05:41 GMT  
		Size: 59.6 MB (59613155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8800e1cc7591e5904e91e8d97d9473bdb20d5903cbc9b988d68f7084e1a05a`  
		Last Modified: Thu, 16 Mar 2023 20:03:49 GMT  
		Size: 112.2 MB (112205154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4968d13c6200a4266a163c8743a6a6a557e79cc58c8f286bfc201e66a881409`  
		Last Modified: Thu, 16 Mar 2023 20:03:42 GMT  
		Size: 9.1 MB (9090680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8231900221d6a8bc98b62dada0f7eb5bdc416c65e50d59d8189d4e7df708e9`  
		Last Modified: Thu, 16 Mar 2023 20:03:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2649e7b95966ba9e370d557f182190375f9c47d42ad3eab7e449a81ba7227012`  
		Last Modified: Thu, 16 Mar 2023 20:03:41 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe2e5caf19b8a18489a369b102fb8906edc88d3ea8c833bcc7623a1ec2fd07a`  
		Last Modified: Thu, 16 Mar 2023 20:03:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
