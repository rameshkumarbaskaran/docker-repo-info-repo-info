## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:64ca08305940bd90d7a9c1fa3ad05a1c90858b82c8779144f4afbd4b9b7323f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c94a69f50c12294549738a2e032a4c1e80aa1dc7f3ff9734695ddf6f2416d83e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221567408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b7e39f9575bba97e0cb236ba9c31241477bfc48a45822ca72a2e8b2989485`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Apr 2022 22:19:57 GMT
ADD file:4eb88d9d977dadb40c630d693a07ca066069b30b9751b7a421dfb4ba0b99d862 in / 
# Thu, 21 Apr 2022 22:19:58 GMT
CMD ["/bin/bash"]
# Fri, 22 Apr 2022 01:16:14 GMT
ARG version=11.0.15.9-1
# Fri, 22 Apr 2022 01:16:39 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Apr 2022 01:16:40 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 01:16:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 Apr 2022 08:11:01 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 22 Apr 2022 08:11:01 GMT
ARG MAVEN_VERSION=3.8.5
# Fri, 22 Apr 2022 08:11:01 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Apr 2022 08:11:01 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Fri, 22 Apr 2022 08:11:01 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Fri, 22 Apr 2022 08:11:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 22 Apr 2022 08:11:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Apr 2022 08:11:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Apr 2022 08:11:03 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 22 Apr 2022 08:11:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 22 Apr 2022 08:11:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Apr 2022 08:11:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ac1397dc8419bf1767b60a5cc5849b7130406030581d4542e48965801c303a70`  
		Last Modified: Thu, 21 Apr 2022 22:08:36 GMT  
		Size: 62.3 MB (62265199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cec6ee88046f5dc72c1feb945b812e2dca597283b8abfb36964929d67b99de`  
		Last Modified: Fri, 22 Apr 2022 01:20:49 GMT  
		Size: 147.0 MB (146956590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ac15040803ee2f6f9d0473a66161ed27bd2ada6336f3c826f9b9c6a5fab486`  
		Last Modified: Fri, 22 Apr 2022 08:17:05 GMT  
		Size: 3.6 MB (3608020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3d09732f9e6fabaec531dc458284ea44572b53648af29c4a31bfa7f98b2f7b`  
		Last Modified: Fri, 22 Apr 2022 08:17:05 GMT  
		Size: 8.7 MB (8736386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159fa512d5e4033de5675a1bec935c8a35af4fff847a4ebb208059f7a51ab171`  
		Last Modified: Fri, 22 Apr 2022 08:17:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f694490ec260c149884da7ca8a524e7b5ce9db424a97ec0eddd830cd1cc106`  
		Last Modified: Fri, 22 Apr 2022 08:17:04 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a34d6e8fb0ce2fdc8daac44c34a6cc666e77ab2d8f8f2439035121ae29aece38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220466171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9575d81959d007e3222acb6771c47c188d0f23b775509f1058cee0f4e3619d11`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Apr 2022 22:57:49 GMT
ADD file:76e1ee72575f50a75573a46483631e239d3b6afda9fdd53086883bd03db5364b in / 
# Thu, 21 Apr 2022 22:57:51 GMT
CMD ["/bin/bash"]
# Fri, 22 Apr 2022 02:35:43 GMT
ARG version=11.0.15.9-1
# Fri, 22 Apr 2022 02:36:06 GMT
# ARGS: version=11.0.15.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Apr 2022 02:36:06 GMT
ENV LANG=C.UTF-8
# Fri, 22 Apr 2022 02:36:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 Apr 2022 04:51:20 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 22 Apr 2022 04:51:20 GMT
ARG MAVEN_VERSION=3.8.5
# Fri, 22 Apr 2022 04:51:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Apr 2022 04:51:22 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Fri, 22 Apr 2022 04:51:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Fri, 22 Apr 2022 04:51:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 22 Apr 2022 04:51:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Apr 2022 04:51:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Apr 2022 04:51:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 22 Apr 2022 04:51:37 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 22 Apr 2022 04:51:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Apr 2022 04:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:86bcd0b49e3391c117b5e27756fdf585aadc1a7b9054d19af0faa050839a6633`  
		Last Modified: Thu, 21 Apr 2022 22:59:02 GMT  
		Size: 63.9 MB (63888157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ec32940f389e919db4659896d9c8fdc1de568be3ed714f36bd4319e4e3888`  
		Last Modified: Fri, 22 Apr 2022 02:38:28 GMT  
		Size: 144.2 MB (144202926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad40c667daa4247237cb8da2d23c92bd0fe2129f410826d6573b71744bab9919`  
		Last Modified: Fri, 22 Apr 2022 04:58:00 GMT  
		Size: 3.6 MB (3637542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b685d5a286e851d23d5409ef950219483f5a4c905b915f7519d45a7e341dd37`  
		Last Modified: Fri, 22 Apr 2022 04:58:00 GMT  
		Size: 8.7 MB (8736333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8147663253b888bd3fdbdd5f88e16af61d6f927a3702ef781dfc02327172c56`  
		Last Modified: Fri, 22 Apr 2022 04:57:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06389c857139db1bf7d31948f0fde9db34074067d5dd79dd03e681177d618b07`  
		Last Modified: Fri, 22 Apr 2022 04:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
