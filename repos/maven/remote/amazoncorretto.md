## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:4f3a2028ce95d5ad80fb46bbb2fcc0588ca000849a64489817f3866e4244e139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:3204b8dae96d8075eb697b99be21e8559da001da4c0aac098e2b83d71567d760
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222413660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf979acd797a18e06c420f50d439b225fe1d205473e7b63900bd1b31b7af0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Nov 2022 01:32:34 GMT
ADD file:d5f7c1dc2e62cbd216adb0c4ff82770915f2b4e4660989515782faeca4e486ed in / 
# Thu, 17 Nov 2022 01:32:35 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:50:32 GMT
ARG version=11.0.17.8-1
# Thu, 17 Nov 2022 01:50:56 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:50:56 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:50:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Nov 2022 02:32:16 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:32:16 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:32:16 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:32:16 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:32:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:32:22 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:32:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:32:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:32:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:32:23 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:32:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:32:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68028ec3b506bca4d81560b5fcbd408dc7cc49f4b1717a69d5396ff22700f80a`  
		Last Modified: Wed, 16 Nov 2022 20:32:28 GMT  
		Size: 62.3 MB (62262225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef215ea8d074f0c94eaca01c6b06d36fb0f4c6fba48ee0ef78e27af949e1d2b`  
		Last Modified: Thu, 17 Nov 2022 01:55:26 GMT  
		Size: 147.8 MB (147769396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcca442805e3b737009449270c196f790833773cbc162dc0079707eb9a15ae9f`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 3.6 MB (3641327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1e00f3752e3320f2375e9fac4e606e961ab5738c114f1cf43f1c25dd66366`  
		Last Modified: Thu, 17 Nov 2022 02:35:28 GMT  
		Size: 8.7 MB (8739498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda6c6842d25068d8c1f061d8c345cfde396866e4bb5af072b98ae5ac310c098`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4103a3371d8ed261215075ecabcac36c8dab859df24a6e34018af6c1709671d`  
		Last Modified: Thu, 17 Nov 2022 02:35:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2ae2ad3693437aab5578cad115a0d8c69f1f0cee84c10a5ba60cda77ffa2fcdd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221155454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856bd9dce363f6955fa9d4218127f8607c7554e32f095299bdc022c6ec04dd5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 17 Nov 2022 01:39:24 GMT
ADD file:ff78f504eef6d6952dca0350e26f9d78bcb442569cbd5a99bdc6206091485de4 in / 
# Thu, 17 Nov 2022 01:39:26 GMT
CMD ["/bin/bash"]
# Thu, 17 Nov 2022 01:56:26 GMT
ARG version=11.0.17.8-1
# Thu, 17 Nov 2022 01:56:44 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 17 Nov 2022 01:56:46 GMT
ENV LANG=C.UTF-8
# Thu, 17 Nov 2022 01:56:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Nov 2022 02:16:08 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 17 Nov 2022 02:16:08 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 17 Nov 2022 02:16:08 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Nov 2022 02:16:08 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 17 Nov 2022 02:16:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 17 Nov 2022 02:16:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Nov 2022 02:16:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Nov 2022 02:16:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Nov 2022 02:16:13 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Nov 2022 02:16:13 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Nov 2022 02:16:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Nov 2022 02:16:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4c4d0334d8224869629842fadc7a498ccbda1acc05e7995a0a7283b23fc39c24`  
		Last Modified: Wed, 16 Nov 2022 20:31:50 GMT  
		Size: 63.9 MB (63867424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3610944f82a8f2fa1bffb30d84fed434e25b320fa81ee9d68f663e8054d59bd5`  
		Last Modified: Thu, 17 Nov 2022 01:59:03 GMT  
		Size: 144.9 MB (144907910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b62ec7df2b3bf2ddcc504bed1191ca77d3257a40658d70039ccecdced286fc`  
		Last Modified: Thu, 17 Nov 2022 02:18:20 GMT  
		Size: 3.6 MB (3639420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e6d67031fb2dcad3bb3bb603649f39a6f61cd8d7a47dc49337a661de3e329`  
		Last Modified: Thu, 17 Nov 2022 02:18:20 GMT  
		Size: 8.7 MB (8739492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05507c400ddb7957d3e23123a2df7c6b7065701a51c4a2a33cd769cad69af38d`  
		Last Modified: Thu, 17 Nov 2022 02:18:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dba6e2bcfff1b68df4096316dcea07321a5c00993d00dd39129a23e41324b7`  
		Last Modified: Thu, 17 Nov 2022 02:18:20 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
