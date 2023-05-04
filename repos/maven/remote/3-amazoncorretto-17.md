## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:849d94f9755ad06d2d98dbeac8283036cb561c474698543754c6c85f193ed69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:9e65ffb737a29bf09e0509e87a69359be12622b956d7944fdeb06a925e0b2024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374464740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d174a0c83686c70912cea56bd17c41f2942bf1c00f9d33354ca6aeb6555b99aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:40:39 GMT
ARG version=17.0.7.7-1
# Thu, 04 May 2023 19:41:03 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 19:41:03 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:41:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 04 May 2023 19:41:04 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 19:41:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 19:41:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 19:41:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 19:41:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 19:41:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 19:41:04 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 19:41:04 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 19:41:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 19:41:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 19:41:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7780aeb331e5891bc8c4a06b18a7ad6322941ae6b818c406b0b4e94b1152d647`  
		Last Modified: Thu, 04 May 2023 19:46:32 GMT  
		Size: 152.0 MB (151978682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b09ee812fed014337e228cc3d3db560559b5c4c6f790da6a687764a9d8d5ad`  
		Last Modified: Thu, 04 May 2023 20:21:36 GMT  
		Size: 150.9 MB (150866189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a44eba70bf21864cba5a81136779626af7d985aa27910149aa3e7827111f5f5`  
		Last Modified: Thu, 04 May 2023 20:21:25 GMT  
		Size: 9.1 MB (9106155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4e9f81a1aa5e58fc62c048411c4803a8bdcb85c1a5d67aeee93ce6cfa99368`  
		Last Modified: Thu, 04 May 2023 20:21:24 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdba5599275b21f4b8df2763eefaf95d0f12346c77edf6ca097fcc342bdce052`  
		Last Modified: Thu, 04 May 2023 20:21:24 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f84a0116635123946b01c82e0bf70d8324932a2fc987229dd7cfa9a5782b09`  
		Last Modified: Thu, 04 May 2023 20:21:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:69dfd4a3180d082b7f0796bb216612466d898d22a2cfc11ac037450cb2687fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338572329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831fa9b06c146ef0db6360dbe9658354ad1ebb85bfecef95e0676ac2bcdd3e60`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:42:46 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 17:43:06 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Apr 2023 17:43:08 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:43:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 04 May 2023 03:25:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 03:25:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 03:25:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 03:25:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 03:25:59 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 03:25:59 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 03:25:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 03:25:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 03:25:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d5f25839cc5d9c044ea00ba0de0880e3272fc9e31ae1d800e809913883f78b`  
		Last Modified: Thu, 20 Apr 2023 17:53:14 GMT  
		Size: 150.5 MB (150487733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156c43e9c3d8af2d90c6d0fa58cb3d644c05f7a235923991f65ec351c4de41b8`  
		Last Modified: Thu, 20 Apr 2023 18:21:09 GMT  
		Size: 114.9 MB (114850123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caf277928a23fe8d42a293c53757d2249517bdefa1d7278ef0df5b5f7dd8d28`  
		Last Modified: Thu, 20 Apr 2023 18:21:02 GMT  
		Size: 9.1 MB (9106152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2484ae0c639572557e9cde3cd0e9f5d50fdad41be9988a105051130193e06e`  
		Last Modified: Thu, 20 Apr 2023 18:21:01 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c7604c9ee2505b6439b95ffbecbccf0afb3b4ff00997edbbf9d101b254bf0`  
		Last Modified: Thu, 20 Apr 2023 18:21:01 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70edb93a4aecd96c2bbde87523c2018634d2d5bc7af75c4a07a3082cdbc52b1f`  
		Last Modified: Thu, 20 Apr 2023 18:21:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
