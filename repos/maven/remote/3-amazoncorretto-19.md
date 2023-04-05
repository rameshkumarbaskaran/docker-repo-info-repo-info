## `maven:3-amazoncorretto-19`

```console
$ docker pull maven@sha256:f03397d19ff99a9348bcd29b42eacd96cba06bc88ccaf6acf1603706e8dd80e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-19` - linux; amd64

```console
$ docker pull maven@sha256:1279a05316ef1390408018ccd471eb69539e5006438d8d32a01524d94ca90864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379302691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfc2cdab195433ef4ab588f661232879be510542678a083e4a845aa3a84a67f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:51 GMT
COPY dir:d74df4759bcd6e2619baa3ec354d8703c77c836345c6a887554df76aaf1d9965 in / 
# Tue, 28 Mar 2023 18:20:52 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:13:16 GMT
ARG version=19.0.2.7-1
# Tue, 28 Mar 2023 19:13:40 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 28 Mar 2023 19:13:41 GMT
ENV LANG=C.UTF-8
# Tue, 28 Mar 2023 19:13:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Sun, 02 Apr 2023 19:35:52 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ARG MAVEN_VERSION=3.9.1
# Sun, 02 Apr 2023 19:35:52 GMT
ARG USER_HOME_DIR=/root
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 02 Apr 2023 19:35:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 02 Apr 2023 19:35:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:128d54f2c9b134270b406c5f3a41296da7c1111d3a6927f0b4451131d636151e`  
		Last Modified: Thu, 23 Mar 2023 21:24:22 GMT  
		Size: 62.5 MB (62483466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbce202e8c18f6a6ea945545d4a6008f86250c482b86dc99ccde3363b803e09`  
		Last Modified: Tue, 28 Mar 2023 19:19:26 GMT  
		Size: 159.4 MB (159395636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e861da11cdb27cca48f6c9ecd425ee169829c8496eaa22e3a996aae737619985`  
		Last Modified: Tue, 28 Mar 2023 19:56:45 GMT  
		Size: 148.3 MB (148316048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bd625d29ca65c2463d625d3b5327022e65c45d68a97b92895bf5370b90470f`  
		Last Modified: Wed, 05 Apr 2023 17:32:51 GMT  
		Size: 9.1 MB (9106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef100366559819bdfc84ae8c7313f36289cd65236a95d859112d0a2ecb82faa8`  
		Last Modified: Wed, 05 Apr 2023 17:32:50 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70212587692b7f8a7f74d2bd9754c3b2de421751532eb5e88413123c45b8b3f3`  
		Last Modified: Wed, 05 Apr 2023 17:32:50 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6441973889f61b7184d008b8bf8ff8cb6c763ff2f8c0466b0dd6ee30e51471a`  
		Last Modified: Wed, 05 Apr 2023 17:32:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-19` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5dd1cf8c36fc57ffb344e072c0af6ad345ee884df7d936d86b61740bb725c813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344552913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf7c11e5c82a24e8873963bff7282416e5b7daf3853c9c7ad1a695bc6b50da8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:08:38 GMT
ARG version=19.0.2.7-1
# Tue, 28 Mar 2023 19:08:57 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 28 Mar 2023 19:08:59 GMT
ENV LANG=C.UTF-8
# Tue, 28 Mar 2023 19:08:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
# Sun, 02 Apr 2023 19:35:52 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ARG MAVEN_VERSION=3.9.1
# Sun, 02 Apr 2023 19:35:52 GMT
ARG USER_HOME_DIR=/root
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 02 Apr 2023 19:35:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 02 Apr 2023 19:35:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1162dc152fc88dd65e94c5411e7919d4a1f714f675823bb48cb01cfe9029d14b`  
		Last Modified: Tue, 28 Mar 2023 19:13:01 GMT  
		Size: 157.8 MB (157848978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275d16b98f6f8b63c053bfc529207948b05511acbb17f09fb3cda9ef1a738f83`  
		Last Modified: Tue, 28 Mar 2023 19:36:29 GMT  
		Size: 113.5 MB (113469471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dee2aa9da3b718e06d2206f17800863d6734199a5294d60eceae1325f7eeede`  
		Last Modified: Wed, 05 Apr 2023 16:44:02 GMT  
		Size: 9.1 MB (9106149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e855b2281fbebf0fa2e199ec1b6782c75faebe95ae3efaf387a198324730b4c`  
		Last Modified: Wed, 05 Apr 2023 16:44:01 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3953b9477f2b6d3f327a91cc6e083390ffa3467a3583af06d03084a2db2767b7`  
		Last Modified: Wed, 05 Apr 2023 16:44:01 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a948de3c807602ad890ebf843dfe6b3d091f326df707fd727cb2fbb83aeda8`  
		Last Modified: Wed, 05 Apr 2023 16:44:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
