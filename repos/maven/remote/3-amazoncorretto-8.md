## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:7c6e6469d66ff0d1792e4c8982891d23703a0d655f1bc15a9e8d59e1db53c570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:a7b39efc89d44c210d0d73288a66bbb4174e8062dd31bbbb81fd8c6d4f3f46a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150508160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5a63c6302eb39def00f9b5171b122d2e14e16329724974a591f8fab4f5cfa2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jul 2021 00:19:58 GMT
ARG version=1.8.0_302.b08-1
# Wed, 21 Jul 2021 00:20:19 GMT
# ARGS: version=1.8.0_302.b08-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 21 Jul 2021 00:20:19 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jul 2021 00:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jul 2021 01:06:17 GMT
ARG MAVEN_VERSION=3.8.1
# Wed, 21 Jul 2021 01:06:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jul 2021 01:06:17 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Wed, 21 Jul 2021 01:06:17 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Wed, 21 Jul 2021 01:06:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 21 Jul 2021 01:06:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 21 Jul 2021 01:06:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jul 2021 01:06:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jul 2021 01:06:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jul 2021 01:06:30 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 21 Jul 2021 01:06:30 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 21 Jul 2021 01:06:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jul 2021 01:06:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7345e871527554f60a16d3ccbb1227c55c86687fe1b3a27de765c1dd3b461`  
		Last Modified: Wed, 21 Jul 2021 00:22:06 GMT  
		Size: 75.3 MB (75332988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce76e8ec7bf2e40523308094d26447a1810e3e669062af1e8eb16f8ab2e30c7`  
		Last Modified: Wed, 21 Jul 2021 01:10:25 GMT  
		Size: 3.6 MB (3597009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969931957e639d81715d566b9d288b4e82cd0b6b3b817be1a47f5e7f2a4a870e`  
		Last Modified: Wed, 21 Jul 2021 01:10:25 GMT  
		Size: 9.6 MB (9610947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912041a6ee90a1f99bbb5f4f64d99f84130978efcae964bc7895b5b665c23ab2`  
		Last Modified: Wed, 21 Jul 2021 01:10:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558cc377a7f7097dc0adc3325f13f82e6c2d935c1bec993b9db1df8906902cc3`  
		Last Modified: Wed, 21 Jul 2021 01:10:24 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f1e8cfae4101a27f046f803b0a53540ad690deaf64331ecaf04efe89bab24130
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136156434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37086fd423e12d852425dceff7e0add595b100ba51b46f8264ec5cb0a2ce9de8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:39:02 GMT
ARG version=1.8.0_292.b10-1
# Fri, 16 Jul 2021 00:39:22 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Jul 2021 00:39:22 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jul 2021 00:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 16 Jul 2021 01:06:41 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 16 Jul 2021 01:06:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jul 2021 01:06:41 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 16 Jul 2021 01:06:41 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 16 Jul 2021 01:06:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 16 Jul 2021 01:06:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 16 Jul 2021 01:06:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jul 2021 01:06:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jul 2021 01:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 16 Jul 2021 01:06:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 16 Jul 2021 01:06:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 16 Jul 2021 01:06:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jul 2021 01:06:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604b7366edbac69a6f522c717afc260aae1a8fbd27de1238ad50b924c50ea415`  
		Last Modified: Fri, 16 Jul 2021 00:41:25 GMT  
		Size: 59.4 MB (59385628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2094069dacaba2efaa237abfd10fec4098f64da3e5cd08fb0e0391a838d6dc`  
		Last Modified: Fri, 16 Jul 2021 01:11:35 GMT  
		Size: 3.6 MB (3590733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ae64d4b8fab8d7e7690bf3651aa7f7f5a5e8cb1e72fa6837a68d747a3648cd`  
		Last Modified: Fri, 16 Jul 2021 01:11:35 GMT  
		Size: 9.6 MB (9610972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb22bb4532f1c1ad0199e027c9f333f51bc0f2ce05dcbec1b421d5d3caaef1ed`  
		Last Modified: Fri, 16 Jul 2021 01:11:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4169410804f98b74454f4c1a56e807aa8ceb4c16ffbf53a870dae60cca95bdf2`  
		Last Modified: Fri, 16 Jul 2021 01:11:34 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
