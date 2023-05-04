## `maven:3-amazoncorretto-20`

```console
$ docker pull maven@sha256:18c3cf30cf1ecace4296c38b263b51e150cf5895c3ccafca333cc69e64603e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20` - linux; amd64

```console
$ docker pull maven@sha256:d7f529df5c4e3a776b70bbcef9d82c865ebddf7957d5926c6e7367743f13e265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383257432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df1a794d945c8282e5d12a233f8befc9d1414163738cb3defee7e04f09eb76e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:42:11 GMT
ARG version=20.0.1.9-1
# Thu, 04 May 2023 19:42:34 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 19:42:34 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:42:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Thu, 04 May 2023 19:42:35 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 19:42:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 19:42:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 19:42:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 19:42:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 19:42:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 19:42:35 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 19:42:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 19:42:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 19:42:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 19:42:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f759079f01a2b6c5bb35d99a13862abb3d5341784e524a82aa32150b8e02973`  
		Last Modified: Thu, 04 May 2023 19:48:02 GMT  
		Size: 160.8 MB (160771990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0b30c398e41be96f32c9fa20767b3e5d7c688646ea43211fc8a23c824743db`  
		Last Modified: Thu, 04 May 2023 20:22:04 GMT  
		Size: 150.9 MB (150865572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b26f3c999fece6b33a85fac4118198989bd6f5a97783e18cd05897e63d333b`  
		Last Modified: Thu, 04 May 2023 20:21:51 GMT  
		Size: 9.1 MB (9106155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fd069a210363e992f601506b448497d7fde5fac292ac5c62c717c70643981c`  
		Last Modified: Thu, 04 May 2023 20:21:51 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f7c574a1ec6226887f67113dbe6afb886366beb7a3e979824a467f312d7138`  
		Last Modified: Thu, 04 May 2023 20:21:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013b10ace520359a0626bb1ca0ac2e56a7a3fa15bc6876b2f6212b338fdcc169`  
		Last Modified: Thu, 04 May 2023 20:21:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:03c6aaba9a3e3cd92c43b5f77ad355146b61aee678b3ea9bd0962b31732427ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347969317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e3afc6daa2667f7c608e81490ee9dfe4812fb63db585ee963101dc0ccadb7c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 04 May 2023 20:02:54 GMT
COPY dir:dcba415a4a8d9f29c0f5914e2b9ce92b35bd4109c9cd4a8feba13044e94360bf in / 
# Thu, 04 May 2023 20:02:55 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:19:01 GMT
ARG version=20.0.1.9-1
# Thu, 04 May 2023 21:19:19 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 21:19:21 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 21:19:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Thu, 04 May 2023 21:19:21 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 21:19:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 21:19:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 21:19:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 21:19:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 21:19:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 21:19:21 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 21:19:21 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 21:19:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 21:19:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 21:19:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7691241ca28307f278612dad94d3164926fb17e58a2302a47349e0d6e001249e`  
		Last Modified: Tue, 25 Apr 2023 06:49:36 GMT  
		Size: 64.1 MB (64130990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56aea19d8d42e5ab5271a0231d569c7f1dce63fd2948821b144eaa4ed690f2e`  
		Last Modified: Thu, 04 May 2023 21:23:56 GMT  
		Size: 158.8 MB (158803748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40131a088337b0966c8b0ac1daf60eac6e16b1a52175505723183cbca8c1ee20`  
		Last Modified: Thu, 04 May 2023 21:42:09 GMT  
		Size: 115.9 MB (115927046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e133fde3be145f7281f39528a080376192dba076eed79f802c184afc46003e8`  
		Last Modified: Thu, 04 May 2023 21:42:01 GMT  
		Size: 9.1 MB (9106152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f8779893dcaf17b7aa1f8fb00b19c2e8a91534de30264f7dba64f05eaf2960`  
		Last Modified: Thu, 04 May 2023 21:42:00 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f754440e22769dc089e43ebab05cac53db06292c188d4024029ae77e80e847a`  
		Last Modified: Thu, 04 May 2023 21:42:00 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91539a41c0a5e7de36db794a0aac6c814146fa311b37962e9f5a20b7d7da0a9b`  
		Last Modified: Thu, 04 May 2023 21:42:00 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
