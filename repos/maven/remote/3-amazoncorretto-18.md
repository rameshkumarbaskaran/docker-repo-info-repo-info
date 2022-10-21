## `maven:3-amazoncorretto-18`

```console
$ docker pull maven@sha256:83f34d22ee22a680bc90eb73a522352f827c13b119be36598652089e0dfad3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-18` - linux; amd64

```console
$ docker pull maven@sha256:1b9bfe76e8538572ff75a89cfef13dc664b4c4cde90985205f581ce2b117988b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227366028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6937b6cec153e040022eda9eb67cdb1b3e4f5fa33d06c24729699dc0b8a091a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 01:10:09 GMT
ARG version=18.0.2.9-1
# Fri, 21 Oct 2022 01:10:34 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 21 Oct 2022 01:10:35 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 01:10:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
# Fri, 21 Oct 2022 02:02:24 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 21 Oct 2022 02:02:24 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 21 Oct 2022 02:02:24 GMT
ARG USER_HOME_DIR=/root
# Fri, 21 Oct 2022 02:02:25 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 21 Oct 2022 02:02:25 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 21 Oct 2022 02:02:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 21 Oct 2022 02:02:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 21 Oct 2022 02:02:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 21 Oct 2022 02:02:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 21 Oct 2022 02:02:33 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 21 Oct 2022 02:02:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 21 Oct 2022 02:02:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd810cad0bdf6453bee2dabf5abe8def538559a37f10dd606b86c1a61d9247`  
		Last Modified: Fri, 21 Oct 2022 01:15:45 GMT  
		Size: 152.7 MB (152698907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6be694ed44843398d93b774f866c3e735cd4e8e2933063ece9e1fae01ad65f`  
		Last Modified: Fri, 21 Oct 2022 02:05:41 GMT  
		Size: 3.6 MB (3619753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6310748bf4f3b0278bab92a0e7259bd2d628b52e6bcbd600cfec7c140ce0f1`  
		Last Modified: Fri, 21 Oct 2022 02:05:41 GMT  
		Size: 8.7 MB (8739514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10170ff4e45e3dd2e3891896ff3103e5a12a6f66535879fe656d243f999e88aa`  
		Last Modified: Fri, 21 Oct 2022 02:05:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e10688a22756eacdb4385f8a99fcd4cbd13893b0dabf53f47ed3eab90c24bf`  
		Last Modified: Fri, 21 Oct 2022 02:05:40 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6b8df6daf69c053349c9728933f3f52523dde963c4b53cb150601f61ffe2f620
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae223fabaf029701c25d676887b8c234127c7de647485a9937679b8b78ea14b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 20 Oct 2022 23:39:31 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Thu, 20 Oct 2022 23:39:32 GMT
CMD ["/bin/bash"]
# Thu, 20 Oct 2022 23:57:52 GMT
ARG version=18.0.2.9-1
# Thu, 20 Oct 2022 23:58:04 GMT
# ARGS: version=18.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-18-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-18-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 20 Oct 2022 23:58:05 GMT
ENV LANG=C.UTF-8
# Thu, 20 Oct 2022 23:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-18-amazon-corretto
# Fri, 21 Oct 2022 00:57:56 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 21 Oct 2022 00:57:56 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 21 Oct 2022 00:57:57 GMT
ARG USER_HOME_DIR=/root
# Fri, 21 Oct 2022 00:57:58 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 21 Oct 2022 00:57:59 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 21 Oct 2022 00:58:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 21 Oct 2022 00:58:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 21 Oct 2022 00:58:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 21 Oct 2022 00:58:13 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 21 Oct 2022 00:58:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 21 Oct 2022 00:58:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 21 Oct 2022 00:58:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d79b74e04609c53b3251846bbfc91daae1e1e0143fa7547e36c706d8b4c63c`  
		Last Modified: Fri, 21 Oct 2022 00:01:21 GMT  
		Size: 151.3 MB (151344534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ae53007402dcc0b4df6fab877e10d2b090bca30257222b8af8d1fdd57e3ba5`  
		Last Modified: Fri, 21 Oct 2022 01:02:23 GMT  
		Size: 3.6 MB (3641658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5ff33a8da0ac16cab8075f0678ebbd20030841345bf1476f97f5e4500356b9`  
		Last Modified: Fri, 21 Oct 2022 01:02:23 GMT  
		Size: 8.7 MB (8739466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188d597555febf9e5c5e7ce319b15dc5c8e3e5321336717913f91199a1f64946`  
		Last Modified: Fri, 21 Oct 2022 01:02:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e96ca701fd6dbab8b9cfcfe5bed3c3db3c5a3b2e0fa44cb8c7aacb7630fa2`  
		Last Modified: Fri, 21 Oct 2022 01:02:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
