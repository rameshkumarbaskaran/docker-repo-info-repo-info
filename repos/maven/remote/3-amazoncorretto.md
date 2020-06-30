## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:85da4aef841807d52753cafc3e6e22e4d777d5a6f85bed45f16f36372d2640c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:bd7ef505fec1c6ad1c53fa4d686216843f8099576b631a0b70dbf56388ee9222
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306567754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e61fa733705971a401f625e759be4ab9eea5bc0ee54de4fe843585302c431ce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 20:55:22 GMT
ARG version=11.0.7.10-1
# Tue, 30 Jun 2020 20:55:56 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 30 Jun 2020 20:55:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 30 Jun 2020 21:37:16 GMT
ARG MAVEN_VERSION=3.6.3
# Tue, 30 Jun 2020 21:37:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Jun 2020 21:37:17 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Tue, 30 Jun 2020 21:37:17 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 30 Jun 2020 21:37:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Tue, 30 Jun 2020 21:37:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 30 Jun 2020 21:37:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Jun 2020 21:37:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Jun 2020 21:37:32 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 30 Jun 2020 21:37:32 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 30 Jun 2020 21:37:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Jun 2020 21:37:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab273e3d40f4b0aa1d84e06a6acc3e2ce0ef6c02e4c57cbdbd8e782b81276308`  
		Last Modified: Tue, 30 Jun 2020 20:56:41 GMT  
		Size: 145.1 MB (145105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77151a0aaf98a4fcc8724dee95680d2e44f326e1b6cca22590b9cfe663d049b0`  
		Last Modified: Tue, 30 Jun 2020 21:38:53 GMT  
		Size: 90.2 MB (90194819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5549f0b4a1941b4877c70992040b4a0eaabec895e272e4e3690e7795211a5`  
		Last Modified: Tue, 30 Jun 2020 21:38:43 GMT  
		Size: 9.6 MB (9581221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2dc5dd950c35f651b2d4fc9d02f4006d8e6c43d2eb02a3f788d38373adb106`  
		Last Modified: Tue, 30 Jun 2020 21:38:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44262e96f29498fff0fbe755e47d706155ab2aa8f71d74f0f5462181f5ddadb6`  
		Last Modified: Tue, 30 Jun 2020 21:38:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b0e3ef8ce400a75fbb6c1812a4128255911006da6d69850922517679a389c2e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268745812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afe688815c0f2f1f78c039c52201bf230460c2a16ccd3e1432dafdfd019c845`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2020 18:58:16 GMT
ADD file:85fc0908f460f80c41755d2b5ab9ff6a025bb2726628ccc4edceb21d2e3f8edf in / 
# Tue, 21 Apr 2020 18:58:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2020 19:26:46 GMT
ARG version=11.0.7.10-1
# Wed, 29 Apr 2020 23:40:57 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 29 Apr 2020 23:40:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 29 Apr 2020 23:58:01 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 29 Apr 2020 23:58:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 Apr 2020 23:58:02 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 29 Apr 2020 23:58:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 29 Apr 2020 23:58:15 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Wed, 29 Apr 2020 23:58:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 29 Apr 2020 23:58:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 Apr 2020 23:58:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 Apr 2020 23:58:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 29 Apr 2020 23:58:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 29 Apr 2020 23:58:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 Apr 2020 23:58:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0a37a5cd26f245ce54aff575389ef7765520d37d3ea7c437144c936c6adffc8a`  
		Last Modified: Tue, 21 Apr 2020 18:59:54 GMT  
		Size: 63.1 MB (63079760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc719ce9c572714bce34bed2d488330731b35adac7227db1447baef738078401`  
		Last Modified: Wed, 29 Apr 2020 23:42:00 GMT  
		Size: 144.0 MB (143963197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d197e07dbc8636a74241775ba20c4c43a837421f4618f9ae8172d55a66ef696`  
		Last Modified: Wed, 29 Apr 2020 23:59:37 GMT  
		Size: 52.1 MB (52120435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe19090f783911141ebb8566abbd00590ce2b3ad532b9f5998c0125c253b9ed`  
		Last Modified: Wed, 29 Apr 2020 23:59:29 GMT  
		Size: 9.6 MB (9581207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5079249d7b9a9d284453d5886e5663a41970027b9c7a2ca98f4b063be888bbd`  
		Last Modified: Wed, 29 Apr 2020 23:59:27 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fd3ce4e4a4dfcee136c297b12106efe9598c86cc89434fe0d6bffd9b1efca1`  
		Last Modified: Wed, 29 Apr 2020 23:59:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
