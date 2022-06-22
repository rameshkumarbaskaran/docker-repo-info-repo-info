## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:472c549f00e09569569a714959299d51adcd72ddcf4f06506afd329ee1844b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:f559c98f7dcfb11711f0c9a09256dff390dbf6cba2f5b807d64ca70a5e54dc04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226343109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785d746ff22398733935e7ab100a7a70347031ec753ff6569a9c7235d55d35ea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 00:03:52 GMT
ARG version=17.0.3.6-1
# Wed, 22 Jun 2022 00:04:18 GMT
# ARGS: version=17.0.3.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 00:04:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 00:04:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Jun 2022 02:39:38 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 22 Jun 2022 02:39:38 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 22 Jun 2022 02:39:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Jun 2022 02:39:38 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 22 Jun 2022 02:39:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 22 Jun 2022 02:39:46 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Jun 2022 02:39:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Jun 2022 02:39:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Jun 2022 02:39:46 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Jun 2022 02:39:47 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Jun 2022 02:39:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Jun 2022 02:39:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368aba68b102d7810e1273cef031aa2b8d269336955b93c1033779a40934d6ac`  
		Last Modified: Wed, 22 Jun 2022 00:07:59 GMT  
		Size: 151.7 MB (151687232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9514a0b107b923b727a289b35873641ba5422e55a05eafe08311386d216978ec`  
		Last Modified: Wed, 22 Jun 2022 02:42:39 GMT  
		Size: 3.6 MB (3620195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0592cb443800e0379d1c686ed4df9f3c6114bd18f521ee2104447c18bea3aa45`  
		Last Modified: Wed, 22 Jun 2022 02:42:39 GMT  
		Size: 8.7 MB (8739497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9e8c2d5f4ea12f02c2314559ac38c36ccd7fac649e33a10654dc43cdf828c5`  
		Last Modified: Wed, 22 Jun 2022 02:42:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055d4af6b84fe46d3374d54c1c85efc13c2d66cb0bac79d0e4b219c64bf14fc1`  
		Last Modified: Wed, 22 Jun 2022 02:42:38 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5f8e0023766757df1e4c8503f013f372a4dd639e097dd50e5f504b00477a2a8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226570044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ca5a71c005bebadc3ed2a63a3c60490b46547551844e709acbc72cd36690ae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:39:32 GMT
ADD file:ce3840583311a5848d47c22463b3a966c40bbf4824f1c9b9b2c51e2fb939de3a in / 
# Tue, 21 Jun 2022 23:39:33 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 01:02:23 GMT
ARG version=17.0.3.6-1
# Wed, 22 Jun 2022 01:02:38 GMT
# ARGS: version=17.0.3.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 01:02:39 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 01:02:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Jun 2022 04:37:38 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 22 Jun 2022 04:37:39 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 22 Jun 2022 04:37:40 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Jun 2022 04:37:41 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 22 Jun 2022 04:37:42 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 22 Jun 2022 04:37:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Jun 2022 04:37:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Jun 2022 04:37:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Jun 2022 04:37:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Jun 2022 04:37:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Jun 2022 04:37:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Jun 2022 04:37:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8cd18ebacb4abd924911c002d3ec5b8d76247c7ed5fff822c8cfb3961846f05a`  
		Last Modified: Wed, 15 Jun 2022 22:09:35 GMT  
		Size: 63.9 MB (63918642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac67b8ab407fc666ca5cb18f894cf94d55c9a97db687078134113b9fa620ab75`  
		Last Modified: Wed, 22 Jun 2022 01:05:06 GMT  
		Size: 150.3 MB (150273970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b278d2f94d17fe63f217b94d949f07eecc97388be1054ce44fee15796c9f2ab`  
		Last Modified: Wed, 22 Jun 2022 04:41:58 GMT  
		Size: 3.6 MB (3636759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7513c445233c3854eac7808523e0bb1b08236681ad2cc8e48cb1781e541221`  
		Last Modified: Wed, 22 Jun 2022 04:41:59 GMT  
		Size: 8.7 MB (8739461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab3a0ba2552de3f5a92492f210cac361759da96f2618078b5e44529bc4b955`  
		Last Modified: Wed, 22 Jun 2022 04:41:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae92238fef60f9ca1163640151af3fc4b97e409a8c66a1707d25b5eebb1d2fd`  
		Last Modified: Wed, 22 Jun 2022 04:41:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
