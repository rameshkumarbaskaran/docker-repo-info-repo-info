## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:4ade94fad8a2b99f7b65877116bd306951e6e1e26a0ad2e7fb41008e46569211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:206d30ec6f8b8013d3ca4ae13bb4c22068e7ec219604c93d511dc65ef32f3aff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149759882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4c90fb55d97eed21d6fa44aeaf6ac4d741ce8f59809c39712e3b45fd2f2224`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 23:19:51 GMT
ARG version=1.8.0_262.b10-1
# Wed, 15 Jul 2020 23:20:19 GMT
# ARGS: version=1.8.0_262.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 23:20:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 23:20:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 16 Jul 2020 00:13:49 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 16 Jul 2020 00:13:49 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Jul 2020 00:13:49 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 16 Jul 2020 00:13:49 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 28 Jul 2020 21:31:31 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 28 Jul 2020 21:31:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 28 Jul 2020 21:31:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 28 Jul 2020 21:31:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 28 Jul 2020 21:31:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 28 Jul 2020 21:31:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 28 Jul 2020 21:31:33 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 28 Jul 2020 21:31:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 28 Jul 2020 21:31:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e079711d48d2342e1225741ac30ca54f5d3adb2a262ca6b1c63723ef056b5b61`  
		Last Modified: Wed, 15 Jul 2020 23:21:13 GMT  
		Size: 74.9 MB (74949792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c98b53b4041164407062ed868205e9f0128eb4af62252ce2ab420ed24c95cc6`  
		Last Modified: Tue, 28 Jul 2020 21:32:20 GMT  
		Size: 3.5 MB (3542999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedf1b6acb03a8ccb0c30ce147540d0b547ba7ff06ba97600b4718a4ad5d5628`  
		Last Modified: Tue, 28 Jul 2020 21:32:20 GMT  
		Size: 9.6 MB (9581198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b448eebfcd8671e29d145493fcb8d516a85549a3d72e67326339a60b2656e7c2`  
		Last Modified: Tue, 28 Jul 2020 21:32:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7408c8c087e942d7564eea5b4f2dcfc62c23946aeb89bec21080b93f10ba00`  
		Last Modified: Tue, 28 Jul 2020 21:32:19 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9e9ad8d295fb7f8699d91d7017632eb415809f58c95255fa9d741655cc669f00
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135357804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9dfe77500087b88663b1c3f19fc196c0a223e5041e9a6fb0c9138c86b9dde2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Wed, 15 Jul 2020 22:40:04 GMT
ARG version=1.8.0_262.b10-1
# Wed, 15 Jul 2020 22:40:37 GMT
# ARGS: version=1.8.0_262.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 15 Jul 2020 22:40:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jul 2020 22:40:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Jul 2020 23:54:40 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 15 Jul 2020 23:54:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jul 2020 23:54:41 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 15 Jul 2020 23:54:42 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 28 Jul 2020 21:41:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 28 Jul 2020 21:41:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 28 Jul 2020 21:41:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 28 Jul 2020 21:41:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 28 Jul 2020 21:41:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 28 Jul 2020 21:41:24 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 28 Jul 2020 21:41:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 28 Jul 2020 21:41:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 28 Jul 2020 21:41:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4819df9ef1d60b632edfd0f18954c7f62b295b94fc86fcc95f7c9a05c3016802`  
		Last Modified: Wed, 15 Jul 2020 22:41:56 GMT  
		Size: 59.0 MB (59036101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e6158ede1aa7d2b19f7f519d17a63eb9f2e3c847b6e32ccf0ebf81c21866ef`  
		Last Modified: Tue, 28 Jul 2020 21:42:08 GMT  
		Size: 3.6 MB (3575502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3615811ec1bfb7ab460e45ec977bc7b94f2b5712dfc97612b33dc8b4f54f4ae`  
		Last Modified: Tue, 28 Jul 2020 21:42:08 GMT  
		Size: 9.6 MB (9581208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04566cba99da4ce59fbc445ac4599764d02277262be230cc4b86350da018f50b`  
		Last Modified: Tue, 28 Jul 2020 21:42:07 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25684c6c01e5ff26114d01b3428cad9cec39b9c7100ef2995b362874582aa16`  
		Last Modified: Tue, 28 Jul 2020 21:42:07 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
