## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:4abc0a5c13455c10d8b17f046928371f862d2a8ab03979a41a34ec1a41586944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:7f2ad131d20d6c85bb963324527c35c6b6b019ce84a9670df6efdd6e7361ee44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226183972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a43f548892bd70f6d6c1930686405c8f13a5542a0febf4aec4739b26fada99`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 13 Apr 2022 21:26:09 GMT
ADD file:7fa33984010a56e1ee5aa401253e0d989c79d49005db9c39461482307d209f33 in / 
# Wed, 13 Apr 2022 21:26:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Apr 2022 22:10:02 GMT
ARG version=17.0.2.8-1
# Wed, 13 Apr 2022 22:10:25 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 13 Apr 2022 22:10:26 GMT
ENV LANG=C.UTF-8
# Wed, 13 Apr 2022 22:10:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 13 Apr 2022 22:32:02 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 13 Apr 2022 22:32:02 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 13 Apr 2022 22:32:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 13 Apr 2022 22:32:02 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 13 Apr 2022 22:32:02 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 13 Apr 2022 22:32:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 13 Apr 2022 22:32:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 13 Apr 2022 22:32:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 13 Apr 2022 22:32:08 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 13 Apr 2022 22:32:09 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 13 Apr 2022 22:32:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 13 Apr 2022 22:32:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b4b6ff8728329c46c11473e599b18813271c5059023956140f08ecaf87f7859a`  
		Last Modified: Wed, 13 Apr 2022 02:49:33 GMT  
		Size: 62.2 MB (62237641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c481770d8a196cee1f80d272c83040c4fde09d54f394f7ab5278585d586199f`  
		Last Modified: Wed, 13 Apr 2022 22:14:20 GMT  
		Size: 151.6 MB (151588781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedea5a8024c9de8018baad9dfbab59919139b87b27c690eed3d013d7509961d`  
		Last Modified: Thu, 14 Apr 2022 00:05:59 GMT  
		Size: 3.6 MB (3619956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6428b1e175766347fca5fb803dbc10316c5151f390913f50abd8018fa276c1`  
		Last Modified: Thu, 14 Apr 2022 00:05:59 GMT  
		Size: 8.7 MB (8736387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fab2ca33ff15a8f99aa20835673fa26de88c6bb5607336abe0202108ce0d2e`  
		Last Modified: Thu, 14 Apr 2022 00:05:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e802796f2e788e76843597c2a8d5722929554268c28d444fba2f1ba4adb2ac`  
		Last Modified: Thu, 14 Apr 2022 00:05:58 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5f50d8da973d2f3e295d4465422bb11f6349e71e0cef8fb3f05913328719dbf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226509646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b01812e22e2f82862862b5dd56eeca97140ad48f28ecf0ee4bdb1ec0ab9084`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 13 Apr 2022 21:39:23 GMT
ADD file:b2ebb2642f1562a48fcb84ac23c60719e85ce47ae98e58a9c3b80e90779c96bc in / 
# Wed, 13 Apr 2022 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 19 Apr 2022 21:40:10 GMT
ARG version=17.0.3.6-1
# Tue, 19 Apr 2022 21:40:29 GMT
# ARGS: version=17.0.3.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 19 Apr 2022 21:40:29 GMT
ENV LANG=C.UTF-8
# Tue, 19 Apr 2022 21:40:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 19 Apr 2022 23:03:43 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 19 Apr 2022 23:03:44 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 19 Apr 2022 23:03:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Apr 2022 23:03:46 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 19 Apr 2022 23:03:47 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 19 Apr 2022 23:03:51 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 19 Apr 2022 23:03:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Apr 2022 23:03:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Apr 2022 23:03:54 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 19 Apr 2022 23:03:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 19 Apr 2022 23:03:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Apr 2022 23:03:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7072f8fc5d0e256808f60aaf5dc2a7b918f5094683b66be0a216b4e8a859ee10`  
		Last Modified: Wed, 13 Apr 2022 02:49:29 GMT  
		Size: 63.9 MB (63870281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdfb6ad89f6087061f62524c201fb4db26a5d7e35fefeb35fb7128c753a0759`  
		Last Modified: Tue, 19 Apr 2022 21:43:09 GMT  
		Size: 150.3 MB (150267146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ae73f6e7445b408b0213f18bc82091e20d0ade2fafa79bc3d750cbc6507ab`  
		Last Modified: Tue, 19 Apr 2022 23:08:06 GMT  
		Size: 3.6 MB (3634670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086cebca51d4c5ba7cc21d845c60256cd04ff9f9b8bd86315816ef59fabcb139`  
		Last Modified: Tue, 19 Apr 2022 23:08:07 GMT  
		Size: 8.7 MB (8736337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d83a0b5d9f51a74d785d1272ac7f9140dadcdcf5817ef3bd037c783f080305`  
		Last Modified: Tue, 19 Apr 2022 23:08:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b73d20462c23e6056e281c7f6e290e77af3667a01a73d6598aa77f08d5cd60e`  
		Last Modified: Tue, 19 Apr 2022 23:08:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
