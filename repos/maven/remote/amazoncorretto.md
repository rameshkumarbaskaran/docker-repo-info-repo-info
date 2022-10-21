## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:c1aeacdf9177218f49aa9b8b921fc3b14de58d69fe211929c28a05aec98d5b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:deab22636f57831a31f1e75779dc66c1ce316879e7e4b02519ccd01fcdd95306
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222430116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc667e22802bc7def970f02e0266a7861c4a1fae39138e1dd7639c0811d9c16b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 01:08:54 GMT
ARG version=11.0.17.8-1
# Fri, 21 Oct 2022 01:09:18 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 21 Oct 2022 01:09:18 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 01:09:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 21 Oct 2022 02:01:44 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 21 Oct 2022 02:01:44 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 21 Oct 2022 02:01:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 21 Oct 2022 02:01:44 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 21 Oct 2022 02:01:44 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 21 Oct 2022 02:01:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 21 Oct 2022 02:01:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 21 Oct 2022 02:01:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 21 Oct 2022 02:01:53 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 21 Oct 2022 02:01:53 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 21 Oct 2022 02:01:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 21 Oct 2022 02:01:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53db8cf37c5436d16c6462a1a7fddc9dd8057b3a68146f146079396fad78db57`  
		Last Modified: Fri, 21 Oct 2022 01:14:20 GMT  
		Size: 147.8 MB (147760529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b9d6bb55f30de1f17e3d0fc273570297e80c7371be305d630e1a4f8360cbde`  
		Last Modified: Fri, 21 Oct 2022 02:05:04 GMT  
		Size: 3.6 MB (3622229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fbf4632a9e0ef5dd77771265c1126b04557a65243fe5de8ef25ef237e33bb05`  
		Last Modified: Fri, 21 Oct 2022 02:05:05 GMT  
		Size: 8.7 MB (8739501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917afdfa7a20721944c33a58f91af7b410d3d935f55e4c286f6e7ff14668f67`  
		Last Modified: Fri, 21 Oct 2022 02:05:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ad01979597bf8ab6a80bca4cb6f9fcc239c3352a1d0bcd4862f1111e8c4e4f`  
		Last Modified: Fri, 21 Oct 2022 02:05:03 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0ab7c20f2567dedf3f1e2ed6819ab597f87a7f7f8ff680d6a6c3559b81563add
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221201760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f8406b3eb89a128255fd7595f797cc6f27f5247d1e60fbb15f355fb9bc74f3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Thu, 20 Oct 2022 23:57:10 GMT
ARG version=11.0.17.8-1
# Thu, 20 Oct 2022 23:57:23 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Oct 2022 23:57:24 GMT
ENV LANG=C.UTF-8
# Thu, 20 Oct 2022 23:57:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 21 Oct 2022 00:57:04 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 21 Oct 2022 00:57:05 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 21 Oct 2022 00:57:06 GMT
ARG USER_HOME_DIR=/root
# Fri, 21 Oct 2022 00:57:07 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 21 Oct 2022 00:57:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 21 Oct 2022 00:57:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 21 Oct 2022 00:57:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 21 Oct 2022 00:57:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 21 Oct 2022 00:57:15 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 21 Oct 2022 00:57:16 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 21 Oct 2022 00:57:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 21 Oct 2022 00:57:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33fdd0b6fa0e80819181b6cb202ac7604a4b77f8e149386d17bcdf872bf13b4`  
		Last Modified: Fri, 21 Oct 2022 00:00:08 GMT  
		Size: 144.9 MB (144903790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5157d2e5e6f5941ed8ffd66731493de6eef2eafb3be0626695c24ece95d0611`  
		Last Modified: Fri, 21 Oct 2022 01:01:39 GMT  
		Size: 3.6 MB (3637414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f83aa4e34df0f601fde4036bcebff3ce92134d6a4be1bf37fa4aa761af382d4`  
		Last Modified: Fri, 21 Oct 2022 01:01:39 GMT  
		Size: 8.7 MB (8739475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462005598083490286df96afcf606bdc00841a1343da703ee12cf10808c65998`  
		Last Modified: Fri, 21 Oct 2022 01:01:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b96b0ec9e6b0edc4d736bc85f5e5af0cc5dad7bc45feefc867c6cb0c66caa`  
		Last Modified: Fri, 21 Oct 2022 01:01:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
