## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:0d683f66624265935e836c9d2c3851ce3cf250cb48c9929d979d8d80f62d8590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:55b14dfc83edd1b284c604b7b581dd6a2d6bf56d07d42cb755f01cf694a1e060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371826683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98e089d897042db8736217257c192e40c9a1b6b78390fd2f0b03bbf85691563`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:51 GMT
COPY dir:d74df4759bcd6e2619baa3ec354d8703c77c836345c6a887554df76aaf1d9965 in / 
# Tue, 28 Mar 2023 18:20:52 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:11:48 GMT
ARG version=17.0.6.10-1
# Tue, 28 Mar 2023 19:12:12 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 28 Mar 2023 19:12:13 GMT
ENV LANG=C.UTF-8
# Tue, 28 Mar 2023 19:12:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 28 Mar 2023 19:12:13 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 28 Mar 2023 19:12:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 28 Mar 2023 19:12:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 28 Mar 2023 19:12:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 28 Mar 2023 19:12:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 28 Mar 2023 19:12:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 28 Mar 2023 19:12:13 GMT
ARG MAVEN_VERSION=3.9.0
# Tue, 28 Mar 2023 19:12:13 GMT
ARG USER_HOME_DIR=/root
# Tue, 28 Mar 2023 19:12:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 28 Mar 2023 19:12:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 28 Mar 2023 19:12:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:128d54f2c9b134270b406c5f3a41296da7c1111d3a6927f0b4451131d636151e`  
		Last Modified: Thu, 23 Mar 2023 21:24:22 GMT  
		Size: 62.5 MB (62483466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e597cbeaf86c2c1b977f1c9529c0fc3a17dc6e0371188326b13c785c4954405c`  
		Last Modified: Tue, 28 Mar 2023 19:18:01 GMT  
		Size: 151.9 MB (151935280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef588e1a3ace5a139be035f017e81d2e313be97e197699073d0cd70172766270`  
		Last Modified: Tue, 28 Mar 2023 19:56:21 GMT  
		Size: 148.3 MB (148315825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b070490859e2d4bfc24c695c18dfc96bdd2a7fb72285543fdba0a5f414dc5cee`  
		Last Modified: Tue, 28 Mar 2023 19:56:09 GMT  
		Size: 9.1 MB (9090726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233d43ebea5b30dc0313b602fd1822920d1b0711f356da5f94f5fd298125597`  
		Last Modified: Tue, 28 Mar 2023 19:56:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60449be411b2fc3dfd48197aae9badca81579139df0ca6723209915e5f98385c`  
		Last Modified: Tue, 28 Mar 2023 19:56:08 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e777f712439fe3b93b6b4fa63bb59c04de70657285bbab98ee7913b74a9634a`  
		Last Modified: Tue, 28 Mar 2023 19:56:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a2304d63815a78eab560bcab4f6d0d048162e8897de493845f1fe70a36eaf065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337174639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b20255e2cf2643b42141ccc4a6bf4e49f2d8138074c2098a1cf6d1023868d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:07:26 GMT
ARG version=17.0.6.10-1
# Tue, 28 Mar 2023 19:07:45 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 28 Mar 2023 19:07:46 GMT
ENV LANG=C.UTF-8
# Tue, 28 Mar 2023 19:07:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 28 Mar 2023 19:07:47 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 28 Mar 2023 19:07:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 28 Mar 2023 19:07:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 28 Mar 2023 19:07:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 28 Mar 2023 19:07:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 28 Mar 2023 19:07:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 28 Mar 2023 19:07:47 GMT
ARG MAVEN_VERSION=3.9.0
# Tue, 28 Mar 2023 19:07:47 GMT
ARG USER_HOME_DIR=/root
# Tue, 28 Mar 2023 19:07:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 28 Mar 2023 19:07:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 28 Mar 2023 19:07:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3539e5099b0fdc23ffc14488ab8faf14b6f3bac7c7262ff82265ba39cff95170`  
		Last Modified: Tue, 28 Mar 2023 19:11:47 GMT  
		Size: 150.5 MB (150486081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e160100fba92b32378b40a457ee26fbb6c73dda49d4f940dbbf39974979023`  
		Last Modified: Tue, 28 Mar 2023 19:36:11 GMT  
		Size: 113.5 MB (113469555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c67479e38e4b6988f0224fb6f00cf0836bfa38189ba9c2a6462c39999064e95`  
		Last Modified: Tue, 28 Mar 2023 19:36:03 GMT  
		Size: 9.1 MB (9090680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3163e2c559c4012771ea8ff23840bbb1cbc3044a2b9502a1842cd88a902b1170`  
		Last Modified: Tue, 28 Mar 2023 19:36:03 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49421a8e6f7e7372b1b73ea5ecfda90f476ef9d6812836ecda7f293a214c42a`  
		Last Modified: Tue, 28 Mar 2023 19:36:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7fb1376a3d8fadb37eb06f0055bbf3ef1d607c004b7711fab219051e6a400b`  
		Last Modified: Tue, 28 Mar 2023 19:36:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
