## `maven:3-amazoncorretto-20`

```console
$ docker pull maven@sha256:7e39f09d011083c6d7c92c324d86b3b5903b3b0615f64742cc9978b1c2b5afb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20` - linux; amd64

```console
$ docker pull maven@sha256:227b782b4145d4375c1891497fd69cb083d6e9317f63bdcb6ff62e94bb2100a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386257921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21de0d8210ba42c065f8df1987f0cc96752fcb89b6140516255940570bcace6f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 19:20:11 GMT
COPY dir:1ad47ba01d0d349e7e7d7ca6f7f5a60739b61c1a0bb68b6f66605d9af77bb0d5 in / 
# Mon, 05 Jun 2023 19:20:12 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:41:56 GMT
ARG version=20.0.1.9-1
# Mon, 05 Jun 2023 19:42:19 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 05 Jun 2023 19:42:20 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:42:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
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
	-	`sha256:6f50472d35bcaf1dac70c662dbd806d8ddd2cd1ce134dfcef4c0139613607e13`  
		Last Modified: Mon, 05 Jun 2023 19:47:37 GMT  
		Size: 160.8 MB (160763489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcf6289222c0ffe4d7a238f777f53854d5d0a75e424953dd73d9403fa70074c`  
		Last Modified: Mon, 05 Jun 2023 20:23:31 GMT  
		Size: 153.7 MB (153685544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1deb9fdb851370cc1b7651c53aebe6b2bfd5cb764c336e01fb0a79b836865ca`  
		Last Modified: Mon, 05 Jun 2023 20:23:20 GMT  
		Size: 9.3 MB (9314416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454ce54e8fee779ef879d4b23201880002010624a508b5dbfe0ede6fd0c7915d`  
		Last Modified: Mon, 05 Jun 2023 20:23:19 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea47225ccc3ce599e9167647306ececd22141fcb158eed2b09daabfab4ba09d`  
		Last Modified: Mon, 05 Jun 2023 20:23:19 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fabdd6cee5a032bd67f065404bc4ba71640dfefd24d827f2d293def47828cea`  
		Last Modified: Mon, 05 Jun 2023 20:23:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8c1fd515f0b8614015b9120f926856eb706ced8957960f667ede695e56c15aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348149462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cd50a5144fa9fd0fd5373a96fd5398b0bc3f7b382249ade5ff374c19be9852`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 13 May 2023 00:39:27 GMT
COPY dir:71cecf11386ac326afd2beed7b45e00586f5b9ab017bb6ace5dec65e5aa62900 in / 
# Sat, 13 May 2023 00:39:27 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 02:31:47 GMT
ARG version=20.0.1.9-1
# Sat, 13 May 2023 02:32:06 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 13 May 2023 02:32:08 GMT
ENV LANG=C.UTF-8
# Sat, 13 May 2023 02:32:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
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
	-	`sha256:c50f769066b9e36d1bd010c73685ede42845abc3c60acabc6426f793e49463c7`  
		Last Modified: Sat, 13 May 2023 02:34:30 GMT  
		Size: 158.8 MB (158779798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569a99bb9342f4548e28f7e66994f293a6e846003dab49518ff33f7da0644770`  
		Last Modified: Sat, 13 May 2023 04:27:37 GMT  
		Size: 115.9 MB (115919052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a55f219bdfad3971b9186ae8977fee336037ae7da7bbf047e37863d2626ed9`  
		Last Modified: Tue, 16 May 2023 18:46:13 GMT  
		Size: 9.3 MB (9314433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b573c8ec2c57aa3a70872e4a591d6b9e2dd574e2387d45d3b418160d02ce39fa`  
		Last Modified: Tue, 16 May 2023 18:46:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db08b43263e7363d09fb6bb2924a54c641bfe3d5dbb0e07c69586eb19ee920d`  
		Last Modified: Tue, 16 May 2023 18:46:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748ee3904b06a0b8fa83ee6d13630e15b3b4250ee16482bb48bc99a8570cc71e`  
		Last Modified: Tue, 16 May 2023 18:46:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
