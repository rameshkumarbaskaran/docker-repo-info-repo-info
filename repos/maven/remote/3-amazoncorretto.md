## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:9c5b5adc93a2e8d151a184d5222c806ffc5e86ffe58bc84f35ed6e32cf535d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:9049991eacc980be5cf07a29517d39baf99d00f8084aedf1e578b62fbc2ec45c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221959936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be64c2583eb9b69d7e4cbbe8a2c962d5646e78b901e2db79505bb26bddb266f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jul 2021 00:20:24 GMT
ARG version=11.0.12.7-1
# Wed, 21 Jul 2021 00:20:47 GMT
# ARGS: version=11.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 21 Jul 2021 00:20:47 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jul 2021 00:20:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jul 2021 01:05:53 GMT
ARG MAVEN_VERSION=3.8.1
# Wed, 21 Jul 2021 01:05:54 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jul 2021 01:05:54 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Wed, 21 Jul 2021 01:05:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Wed, 21 Jul 2021 01:06:04 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 21 Jul 2021 01:06:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 21 Jul 2021 01:06:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jul 2021 01:06:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jul 2021 01:06:06 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 21 Jul 2021 01:06:07 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 21 Jul 2021 01:06:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jul 2021 01:06:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac426d7253aaa8ec4b49b208798a7d7c8cda86ffb0cc7d02bc61a1fabfb0518`  
		Last Modified: Wed, 21 Jul 2021 00:22:44 GMT  
		Size: 146.8 MB (146787358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597bfba89d57f280ef25b836f81c0845a44b30425b87429e9eab4e0ed1baff1e`  
		Last Modified: Wed, 21 Jul 2021 01:09:55 GMT  
		Size: 3.6 MB (3594412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0e252a4b4d8efda033e676ce1ce6dc6fae848817e81051456d1cf535b01c93`  
		Last Modified: Wed, 21 Jul 2021 01:09:56 GMT  
		Size: 9.6 MB (9610946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e17e72a10a973792d218b227a30bd242fefeffa6a221d19f8c32a7f1d5f0c5`  
		Last Modified: Wed, 21 Jul 2021 01:09:54 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc727dbead71b69cf5a98f690e93e48d48c498f56fbb307bfd46808d92e161bb`  
		Last Modified: Wed, 21 Jul 2021 01:09:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6c054bb7ca61ef5fc405f0dbc8a48b1984db61c015308059f53009d6d60f11e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220706695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd01074708cff7f2fc2dc9ac4732060cfdfd97b990e9e56d60efd1f8f329d29d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jul 2021 00:39:45 GMT
ARG version=11.0.12.7-1
# Wed, 21 Jul 2021 00:40:04 GMT
# ARGS: version=11.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 21 Jul 2021 00:40:04 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jul 2021 00:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jul 2021 01:25:18 GMT
ARG MAVEN_VERSION=3.8.1
# Wed, 21 Jul 2021 01:25:18 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jul 2021 01:25:18 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Wed, 21 Jul 2021 01:25:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Wed, 21 Jul 2021 01:25:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 21 Jul 2021 01:25:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 21 Jul 2021 01:25:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jul 2021 01:25:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jul 2021 01:25:34 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 21 Jul 2021 01:25:34 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 21 Jul 2021 01:25:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jul 2021 01:25:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41d3967e6fc72ca7a70b8846afd61f0043fcb846c06d06eedc019d004bf92e`  
		Last Modified: Wed, 21 Jul 2021 00:41:40 GMT  
		Size: 143.9 MB (143933851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803fc76c00985acb82ca2e6ff4afa5f706cd01b1b194c985a7b478ddd1d5339e`  
		Last Modified: Wed, 21 Jul 2021 01:30:58 GMT  
		Size: 3.6 MB (3592792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02e5b58a66cb17ee53c597ab9b38b44cd0692bc419650d586dcc9a0578635b5`  
		Last Modified: Wed, 21 Jul 2021 01:30:58 GMT  
		Size: 9.6 MB (9610947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c621effdcd9c609cc619b2db0fa916435e04cdd9cdef15a39609d0ddd03231de`  
		Last Modified: Wed, 21 Jul 2021 01:30:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a5747938278a76db31b436105ecb5eea1238bccddc9652da666675b76085b8`  
		Last Modified: Wed, 21 Jul 2021 01:30:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
