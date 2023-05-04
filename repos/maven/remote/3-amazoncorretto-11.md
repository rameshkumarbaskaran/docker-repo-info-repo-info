## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:70ad5c8ba7afb8456721f83f84e86a2a1ad4aa8c3190c7df9fc44cc0a8a35af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:84d04f40afc86bdeabe80015373237cd65de3bc0311a5950b416c09e226317eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370300662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8681dc5c4266562b5ec551f86b11b2e9c655cac993d3802ed535a14329b7d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:39:07 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 19:39:31 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 19:39:31 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:39:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 04 May 2023 19:39:32 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 19:39:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 19:39:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 19:39:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 19:39:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 19:39:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 19:39:32 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 19:39:32 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 19:39:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 19:39:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 19:39:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba9a7b3f80b34f78a02e3b4893afa6a121c457d71db0cb2fe82057f656d538`  
		Last Modified: Thu, 04 May 2023 19:45:03 GMT  
		Size: 147.8 MB (147808136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505d8150080c6d81b3d7fcdc6c9350fe96332b9601dbcd9def6677b7fcecd113`  
		Last Modified: Thu, 04 May 2023 20:21:05 GMT  
		Size: 150.9 MB (150872659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1518fd99a4685c3af1cb33f5b648ac71add444db5b9b27e73d77607b8d58ab4`  
		Last Modified: Thu, 04 May 2023 20:20:53 GMT  
		Size: 9.1 MB (9106145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76825cf5a20932acbf89e715e909a5b234eb06d2dc96fbfdbfa423dd30f54cae`  
		Last Modified: Thu, 04 May 2023 20:20:52 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bc85d14cbec95ce07aad547a3a299af22accb9e8189fa3ff79b6111b292a07`  
		Last Modified: Thu, 04 May 2023 20:20:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a6561e6409ebb45b617462d1a1517c7f29248cd1ec4c4eb6b36e8f3e0bf31f`  
		Last Modified: Thu, 04 May 2023 20:20:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3e2f31d5aa15b71c2422a272a77406fd5d81031d4cac7dfd50232af165b65fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334121680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd700c7f2d68f98136a3397ef46f37b347cdb407292e8bbee748bc124f32244b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 04 May 2023 20:02:54 GMT
COPY dir:dcba415a4a8d9f29c0f5914e2b9ce92b35bd4109c9cd4a8feba13044e94360bf in / 
# Thu, 04 May 2023 20:02:55 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:16:20 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 21:16:38 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 04 May 2023 21:16:40 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 21:16:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 04 May 2023 21:16:40 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 04 May 2023 21:16:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 04 May 2023 21:16:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 04 May 2023 21:16:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 04 May 2023 21:16:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 04 May 2023 21:16:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 04 May 2023 21:16:40 GMT
ARG MAVEN_VERSION=3.9.1
# Thu, 04 May 2023 21:16:40 GMT
ARG USER_HOME_DIR=/root
# Thu, 04 May 2023 21:16:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 04 May 2023 21:16:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 04 May 2023 21:16:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7691241ca28307f278612dad94d3164926fb17e58a2302a47349e0d6e001249e`  
		Last Modified: Tue, 25 Apr 2023 06:49:36 GMT  
		Size: 64.1 MB (64130990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9410ea473ac2fdcf5a9f1c5e36b37c7693a3f37b9e2ea71d5e3fdd2bf25b8626`  
		Last Modified: Thu, 04 May 2023 21:21:16 GMT  
		Size: 145.0 MB (144954077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bfcae16692c6440790ad03085554c7eb92cb4f783cacc7ee5ffc259bf4b0b0`  
		Last Modified: Thu, 04 May 2023 21:41:20 GMT  
		Size: 115.9 MB (115929082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d23c023180a2e9235b04c022af48550f8056fd95171dafa2460e15ec86903`  
		Last Modified: Thu, 04 May 2023 21:41:13 GMT  
		Size: 9.1 MB (9106152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174fabe5e40b440c583b13154943356f0845cc0c8eaeb86ffa87abf739087739`  
		Last Modified: Thu, 04 May 2023 21:41:12 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840d69ef79603f6b5ea787328e1769bc17ab1c6f25a3bf31ab99d892dba9aa72`  
		Last Modified: Thu, 04 May 2023 21:41:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b471c618cac88e0e7d5ffc257487d4e1fdfdf7363866f6528d1d29dc0c0c4c`  
		Last Modified: Thu, 04 May 2023 21:41:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
