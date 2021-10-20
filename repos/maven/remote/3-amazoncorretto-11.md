## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:7550be7e95393336d765f99a9f3b4694faab049137d307e2a6390ea4b5cb84d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:c93fb9909b64a8c9d034b20e31cb289bbca50ff9468d1c6adaf6b123638615c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221452850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c99ae3a49a437149c3603a3fc4b2fe0eac359e77b4d38b9bb95a6ba7fe1f7e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:20:20 GMT
ADD file:21dc1ad70daefae1cf0e1b3e78fab06decda5cb9bc958d8a178adb3eddd1fb32 in / 
# Fri, 01 Oct 2021 21:20:20 GMT
CMD ["/bin/bash"]
# Wed, 20 Oct 2021 18:20:32 GMT
ARG version=11.0.13.8-1
# Wed, 20 Oct 2021 18:20:55 GMT
# ARGS: version=11.0.13.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 20 Oct 2021 18:20:56 GMT
ENV LANG=C.UTF-8
# Wed, 20 Oct 2021 18:20:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 20 Oct 2021 18:45:24 GMT
ARG MAVEN_VERSION=3.8.3
# Wed, 20 Oct 2021 18:45:24 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 Oct 2021 18:45:25 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Wed, 20 Oct 2021 18:45:25 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Wed, 20 Oct 2021 18:45:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 20 Oct 2021 18:45:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 20 Oct 2021 18:45:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 Oct 2021 18:45:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 Oct 2021 18:45:38 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 20 Oct 2021 18:45:38 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 20 Oct 2021 18:45:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 Oct 2021 18:45:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0728ce74490afacced1ac863ee989913071f97c52ab996e46cdd6b5369a2d63a`  
		Last Modified: Fri, 01 Oct 2021 10:54:14 GMT  
		Size: 62.0 MB (61952638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca4fabc705f5f3348d7a370cf7895a4b95d666504fef2464d3975ca04e9e9b8`  
		Last Modified: Wed, 20 Oct 2021 18:25:56 GMT  
		Size: 146.8 MB (146775670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c25c779f28dbd657f2358b8e87c7870a69746734a48d68c678139d695181396`  
		Last Modified: Wed, 20 Oct 2021 18:48:32 GMT  
		Size: 3.6 MB (3617691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99df486fbf852a5fd5a1f1ec4bb7e45c26ee5b83057f0cb7987e3b24e8160a5c`  
		Last Modified: Wed, 20 Oct 2021 18:48:32 GMT  
		Size: 9.1 MB (9105635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c139a934f3fdc663899d4b831b7b1cfc643c771f37c42018647b726dc40e8d3`  
		Last Modified: Wed, 20 Oct 2021 18:48:31 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a829b1261e548fe86e8830c788bae996d9d7a3fc86650cc04d74d7ee05b49ea`  
		Last Modified: Wed, 20 Oct 2021 18:48:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a59c98be89f3fdee767c98ea07accbd2944a0134d1a807e61a7920f7886aec0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220234100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ad42b6d659983a08101d04b89fbb8ebd33433e2d574a6954b709814a1a9326`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 01 Oct 2021 21:39:54 GMT
ADD file:1d2ae2bfc4c1f83dc53f48b42503812d345622ab95d8fc84536216ef3d53d807 in / 
# Fri, 01 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:57:58 GMT
ARG version=11.0.12.7-1
# Fri, 01 Oct 2021 21:58:16 GMT
# ARGS: version=11.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:58:17 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:58:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 13 Oct 2021 08:12:43 GMT
ARG MAVEN_VERSION=3.8.3
# Wed, 13 Oct 2021 08:12:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 13 Oct 2021 08:12:44 GMT
ARG SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa
# Wed, 13 Oct 2021 08:12:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries
# Wed, 13 Oct 2021 08:12:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 13 Oct 2021 08:13:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.3/binaries MAVEN_VERSION=3.8.3 SHA=1c12a5df43421795054874fd54bb8b37d242949133b5bf6052a063a13a93f13a20e6e9dae2b3d85b9c7034ec977bbc2b6e7f66832182b9c863711d78bfe60faa USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 13 Oct 2021 08:13:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 13 Oct 2021 08:13:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 13 Oct 2021 08:13:09 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 13 Oct 2021 08:13:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 13 Oct 2021 08:13:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 13 Oct 2021 08:13:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5aa4871be3ec1bcadf7a5257231adc7740edac9a612749884f03ab14b4b2d4ec`  
		Last Modified: Fri, 01 Oct 2021 16:32:04 GMT  
		Size: 63.6 MB (63581978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87829fc1e99051b1d0bd4d87cc846a9834a9eaeddc6d19b39329f500236f687a`  
		Last Modified: Fri, 01 Oct 2021 22:00:57 GMT  
		Size: 143.9 MB (143938375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afd8066aaa08379478c280ad15af54fd4c196ca95a008f5bfae304729a03f0f`  
		Last Modified: Wed, 13 Oct 2021 08:24:45 GMT  
		Size: 3.6 MB (3606933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4e9b166301d5ce1ee74eed66f53648a7c27a771c78b201478d477102d27924`  
		Last Modified: Wed, 13 Oct 2021 08:24:45 GMT  
		Size: 9.1 MB (9105596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97363e76a41efda776716059ac188b6e4ee12bf19dd512e5cdc0e6a9a368adee`  
		Last Modified: Wed, 13 Oct 2021 08:24:44 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575eaf0a864dc71b3348b3966be977558a0a36a0875d8c4ef20774def023117e`  
		Last Modified: Wed, 13 Oct 2021 08:24:44 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
