## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:883a866057089a6645ff142a2f6ddb1c5d97d99df684da5656d44027636dfeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:9de75c77e41c2904a7f43445f2f143705085a3c0cb087ac88a3f36471a23a04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301047801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c65d395d9236ef6c23f253583ccd28afe3263c24aafc6f938563fd867512e7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 19:20:11 GMT
COPY dir:1ad47ba01d0d349e7e7d7ca6f7f5a60739b61c1a0bb68b6f66605d9af77bb0d5 in / 
# Mon, 05 Jun 2023 19:20:12 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:37:25 GMT
ARG version=1.8.0_372.b07-1
# Mon, 05 Jun 2023 19:37:46 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 05 Jun 2023 19:37:47 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:37:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 May 2023 11:35:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a168ccb1c126cd9267eedd2686bc6d0e5415b7fe1009cd832c78ba00655a34d9`  
		Last Modified: Wed, 24 May 2023 21:22:43 GMT  
		Size: 62.5 MB (62493087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d8989daabd4eea208270e98498a105563ce04e6f09fe7b3e95e6f941d0ecf`  
		Last Modified: Mon, 05 Jun 2023 19:43:26 GMT  
		Size: 75.6 MB (75550664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa79f8c4e3aa3280b734a2d6c7692fe6323e4ac6a6bca8fd6b4c77cb257da69`  
		Last Modified: Mon, 05 Jun 2023 20:23:55 GMT  
		Size: 153.7 MB (153688248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d665bae18091b7f6135cd7d06fbd6e900fdaf7c5023283137d3a36c7323e91b`  
		Last Modified: Mon, 05 Jun 2023 20:23:44 GMT  
		Size: 9.3 MB (9314416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adccae951420994de49b93e066eace265819999b2526c75d3f84bf3de5aeada5`  
		Last Modified: Mon, 05 Jun 2023 20:23:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad18a6e8db75bcdee5452c4c3baad935ce37fd7ef7f139e050997bb19096f876`  
		Last Modified: Mon, 05 Jun 2023 20:23:43 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b953f22e1a48e9c5945e8f7c105cac532699842c871514db3e637a80e88095`  
		Last Modified: Mon, 05 Jun 2023 20:23:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5b0e1c1b57206ec492d53caed73a0de75a5edf66773943f25a560608d14aed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248930760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ad04eeed9686a9d4de3a8848d94584bffa3be1db4ce4e9d8bef2aae62131d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:30:16 GMT
ARG version=1.8.0_372.b07-1
# Sat, 13 May 2023 02:30:32 GMT
# ARGS: version=1.8.0_372.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:30:33 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:30:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 May 2023 11:35:55 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ed20885ae48fa1760360e568c1aaba07f51cc6d418715514060ff0826a40c72`  
		Last Modified: Fri, 12 May 2023 19:28:02 GMT  
		Size: 64.1 MB (64134800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfa1555745f6ec2f41f038c73b730475dfd13aebbd12d4da092b0a9f2a29cf3`  
		Last Modified: Sat, 13 May 2023 02:33:02 GMT  
		Size: 59.6 MB (59568514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29acc32a112d9b3aabbdddc51a931f8b97ffe92e032c76e9db52298381eeefa7`  
		Last Modified: Sat, 13 May 2023 04:27:57 GMT  
		Size: 115.9 MB (115911650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71550f797a46645c68dbffa071962135290c764fbada791439c2d4447d2049f5`  
		Last Modified: Tue, 16 May 2023 18:46:41 GMT  
		Size: 9.3 MB (9314414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c449f9d216f9195ffc01cdc549d6bace130f3ad112dc4a97eaf95273bf3b3b`  
		Last Modified: Tue, 16 May 2023 18:46:41 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e6158544611de1120c98c890e363c4acb95203c622e72b4e3fefe47e6f5033`  
		Last Modified: Tue, 16 May 2023 18:46:41 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f2546f897a6d3e3c181948789711a13bff1a2fd87c1ef5af3dedd017c92b95`  
		Last Modified: Tue, 16 May 2023 18:46:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
