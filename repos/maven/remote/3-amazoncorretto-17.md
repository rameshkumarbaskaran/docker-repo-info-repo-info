## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:c08b446eee6a941ff9da81bdfb641f35afd39de5ecbbc06fd7217928de1b64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:95fabd3c139ba947295076158e5160ffad5e34721907dbf8a8a18ff711d9f4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377464599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8afd95274ab41011d2f3edc56cfa4fa4c0b38b68c898df1ab876f0768fd2a3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 19:20:11 GMT
COPY dir:1ad47ba01d0d349e7e7d7ca6f7f5a60739b61c1a0bb68b6f66605d9af77bb0d5 in / 
# Mon, 05 Jun 2023 19:20:12 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:40:20 GMT
ARG version=17.0.7.7-1
# Mon, 05 Jun 2023 19:40:45 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 05 Jun 2023 19:40:45 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:40:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:96d6f06d8d0033f5280e4c0edc2be832e831c176dd379cdb9a0988241c40de54`  
		Last Modified: Mon, 05 Jun 2023 19:46:05 GMT  
		Size: 152.0 MB (151974028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f59c4646ab851c3896b431f5e0c21ff788e8e3ec7bd120ab80074888db06072`  
		Last Modified: Mon, 05 Jun 2023 20:23:08 GMT  
		Size: 153.7 MB (153681685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae0cea391656ed993891f4c2ca78c51b6d24070b249b3868e7f8277d9805e44`  
		Last Modified: Mon, 05 Jun 2023 20:22:56 GMT  
		Size: 9.3 MB (9314415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782eba97544732644be29db147d08c00d7ee1286c3898a5905d5742749647ba6`  
		Last Modified: Mon, 05 Jun 2023 20:22:55 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd243f343ac72ab6d7f319002b25b426721be563902f4ca54b2e3f60e9120e5`  
		Last Modified: Mon, 05 Jun 2023 20:22:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648ef9544ff0283f97034b7854416c8d5d68e8d086327ad34cd7119fe504398c`  
		Last Modified: Mon, 05 Jun 2023 20:22:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ef7b5e8a7557622f14e0ef1bc12682135854c22e772f299dcce737f799bf6d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339835620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8196155ae77c4ec6862c482f28cd77857893cb9aa3f3f26e2940ebe31c51901`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:31:16 GMT
ARG version=17.0.7.7-1
# Sat, 13 May 2023 02:31:36 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:31:38 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:31:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:f531e2cf78efc9a3808075863cbac8998096d9d52e7683e55f2b9908762bd327`  
		Last Modified: Sat, 13 May 2023 02:34:01 GMT  
		Size: 150.5 MB (150466246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3fb9da625022aaa467d95e802133758c80206ca35a786789bb0a461e9de82`  
		Last Modified: Sat, 13 May 2023 04:27:16 GMT  
		Size: 115.9 MB (115918773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c547b92c8b77051bc150e2a3417f8a7c93498313f2e2069531383a31d3e534`  
		Last Modified: Tue, 16 May 2023 18:45:45 GMT  
		Size: 9.3 MB (9314420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ff80883b802c174ffc3f84f7af4fc1463937c44b68719dc14a129101934408`  
		Last Modified: Tue, 16 May 2023 18:45:44 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be99b4513a999b8652ed9304ea3fb816a67425a80e5a2381d696e302d1d69ada`  
		Last Modified: Tue, 16 May 2023 18:45:44 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce895a72c864ee4dccd7f4c6b816c04f15df1ae5cb9d339b183ef4aa8fa6c10`  
		Last Modified: Tue, 16 May 2023 18:45:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
