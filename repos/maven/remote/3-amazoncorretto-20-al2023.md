## `maven:3-amazoncorretto-20-al2023`

```console
$ docker pull maven@sha256:70404638995c0eb1ebb5d3805c0d0a7c871a92f06b9f13f49b261a4c8515fce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20-al2023` - linux; amd64

```console
$ docker pull maven@sha256:35c494fab3b13500a59542a52381ac9562422c54774b461700241f4b13342412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306421162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c85440d2b21abb6d14e4883e55ff5f8d2fb99f596af835bd0ef57fb6dcff5b3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 22 Aug 2023 20:19:35 GMT
COPY dir:c2400bc0d1a5c32eb725de8e35d10b308c821586fa71a0a3f5ba3aa5cf9bb127 in / 
# Tue, 22 Aug 2023 20:19:35 GMT
CMD ["/bin/bash"]
# Tue, 22 Aug 2023 21:35:44 GMT
ARG version=20.0.2.9-1
# Tue, 22 Aug 2023 21:36:11 GMT
# ARGS: version=20.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Tue, 22 Aug 2023 21:36:12 GMT
ENV LANG=C.UTF-8
# Tue, 22 Aug 2023 21:36:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Mon, 28 Aug 2023 11:26:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
ARG MAVEN_VERSION=3.9.4
# Mon, 28 Aug 2023 11:26:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Aug 2023 11:26:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Aug 2023 11:26:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Aug 2023 11:26:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e6dafe971b21b19c13aac9adec0ca5084ccd36d780a9b704ea649071d8e7bb9`  
		Last Modified: Thu, 10 Aug 2023 03:05:52 GMT  
		Size: 52.3 MB (52305790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7049dc0d822e17072d80ca0bba2258903d210d9aca499fac2ad4b2cd82b7c0a`  
		Last Modified: Tue, 22 Aug 2023 21:45:07 GMT  
		Size: 208.2 MB (208154614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9da2286c1a186096eb476e5932a50b10d340b12841ca2aefc5835752ef2368`  
		Last Modified: Tue, 29 Aug 2023 18:35:46 GMT  
		Size: 36.6 MB (36552973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90af104799420afee5543665ee4fca237420f7ec2d47e8151025ab7b93ea4b0`  
		Last Modified: Tue, 29 Aug 2023 18:35:44 GMT  
		Size: 9.4 MB (9406406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f64f759126a3100956f3ae85db7a57587e078ec9f71704982b998e4293f330`  
		Last Modified: Tue, 29 Aug 2023 18:35:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89554caf8bfbe8fc9a9d47be868b3693ed0f678d43829ed2fbdb30b44606fa3c`  
		Last Modified: Tue, 29 Aug 2023 18:35:42 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c80a20485743fea2d8fcf72667683c339549622af8b32ab959041a4406bf70`  
		Last Modified: Tue, 29 Aug 2023 18:35:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:527caae3541d7b194112b6877e6cf3789e22800f37b4c88b4c333341728702f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303166228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd48f0a0ab26a1c64a389a0e4fb788d9994d6f102deda8cf13ef5556b459346b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 22 Aug 2023 19:39:35 GMT
COPY dir:92c63817c19adbcfee66efbdf593beff7587a951a074d0392645d3c4900d19b4 in / 
# Tue, 22 Aug 2023 19:39:36 GMT
CMD ["/bin/bash"]
# Tue, 22 Aug 2023 21:14:05 GMT
ARG version=20.0.2.9-1
# Tue, 22 Aug 2023 21:14:28 GMT
# ARGS: version=20.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Tue, 22 Aug 2023 21:14:31 GMT
ENV LANG=C.UTF-8
# Tue, 22 Aug 2023 21:14:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
# Mon, 28 Aug 2023 11:26:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 28 Aug 2023 11:26:15 GMT
ARG MAVEN_VERSION=3.9.4
# Mon, 28 Aug 2023 11:26:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 28 Aug 2023 11:26:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 28 Aug 2023 11:26:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 28 Aug 2023 11:26:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9fbecb9d3a17a188c49f0cab3521b4c760f46722f3e0e83726ccf3f972d8acbf`  
		Last Modified: Thu, 10 Aug 2023 03:04:18 GMT  
		Size: 51.3 MB (51348140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7e0e0d49b41776f1b14e84acb557fe54d795131140ff925f87ed4f4bf07b4`  
		Last Modified: Tue, 22 Aug 2023 21:22:32 GMT  
		Size: 206.1 MB (206099889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e253f9140498a16685aefab1c3582aaf37f8c5df66bc5790dc3e96659f29cefb`  
		Last Modified: Tue, 29 Aug 2023 17:52:29 GMT  
		Size: 36.3 MB (36310401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b6df97d0e2614328c2f713ab4c2a15b26960ac3a53d3ee114d71103e1860c2`  
		Last Modified: Tue, 29 Aug 2023 17:52:27 GMT  
		Size: 9.4 MB (9406415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba91dd81b1c354704024c401b24241da95891b089b9c0985beb33792f9c4d417`  
		Last Modified: Tue, 29 Aug 2023 17:52:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ff9739a618e9d1fe6b9ff8dccb693bb6458066cd28a9915b850871272bfd0d`  
		Last Modified: Tue, 29 Aug 2023 17:52:27 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d49a7f10d09c962557c09ef4ee8dd8f3972672c9e18239fbf725074d8c71174`  
		Last Modified: Tue, 29 Aug 2023 17:52:26 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
