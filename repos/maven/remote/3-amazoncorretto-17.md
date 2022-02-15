## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:1e5280d56e816b8d0057e97f6d038eece1e78a12d2daf386653a8f30ec708e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:7e99f939dedfd99868e8b4ad210ac559e3683bbc698968f4e921a33eb74eba0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226576916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209814722a56696dc8b3661efa08b594a1bd3cf957a3967d1f939e1d7236588f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Feb 2022 23:40:28 GMT
ADD file:871c80292a1347a65a30c9d2cd343d927528a61b8d89fd82f268d5f8ad4d2944 in / 
# Fri, 04 Feb 2022 23:40:29 GMT
CMD ["/bin/bash"]
# Sat, 05 Feb 2022 06:33:09 GMT
ARG version=17.0.2.8-1
# Sat, 05 Feb 2022 06:33:35 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 05 Feb 2022 06:33:35 GMT
ENV LANG=C.UTF-8
# Sat, 05 Feb 2022 06:33:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 14 Feb 2022 20:25:29 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Mon, 14 Feb 2022 20:25:29 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 14 Feb 2022 20:25:30 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Feb 2022 20:25:30 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 14 Feb 2022 20:25:30 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 14 Feb 2022 20:25:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Feb 2022 20:25:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Feb 2022 20:25:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Feb 2022 20:25:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Feb 2022 20:25:33 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Feb 2022 20:25:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Feb 2022 20:25:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f964900200fc1f8473ac70d9da14cde8bae251ffb4a8f4792e2bf9baf6aaac70`  
		Last Modified: Thu, 27 Jan 2022 23:12:55 GMT  
		Size: 62.2 MB (62237845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eea47cce441eceb9678ae4bee2429cabff6fdcb803de5f7345cc008905a079d`  
		Last Modified: Sat, 05 Feb 2022 06:36:37 GMT  
		Size: 151.6 MB (151605789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cafbfe78b71e07c19467b3dfdcd2c547ac433ac7f092a7174204223149df65`  
		Last Modified: Mon, 14 Feb 2022 20:33:54 GMT  
		Size: 3.6 MB (3622226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36422853f7e815d1d47e4d18488e83f462cf7bf6984ee12ebd5d510b72347345`  
		Last Modified: Mon, 14 Feb 2022 20:33:55 GMT  
		Size: 9.1 MB (9109842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fc763a4150dbbddb9d41786c672452c8f417e0db2eb681709453e392b0aad8`  
		Last Modified: Mon, 14 Feb 2022 20:33:54 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a155e02fd56bf2a6940923d51f24c3899d4b8138a399a678c1b301edd4c0c00`  
		Last Modified: Mon, 14 Feb 2022 20:33:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3f2bd2882dc5adbecea5b4e9072091af311e603507cfe4816beda64ad90e2e5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858f30a3cf0f873b6e2ecb1563cb9c8fa95a812132f565460e20b42fe68025ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Feb 2022 21:33:28 GMT
ADD file:38bb92c68a8a2ac1145ea8d422911f6f0d9c62cccc02b3bdeda096047efecef5 in / 
# Fri, 04 Feb 2022 21:33:29 GMT
CMD ["/bin/bash"]
# Sat, 05 Feb 2022 00:11:42 GMT
ARG version=17.0.2.8-1
# Sat, 05 Feb 2022 00:11:59 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 05 Feb 2022 00:12:00 GMT
ENV LANG=C.UTF-8
# Sat, 05 Feb 2022 00:12:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 14 Feb 2022 19:48:27 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Mon, 14 Feb 2022 19:48:27 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 14 Feb 2022 19:48:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Feb 2022 19:48:29 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 14 Feb 2022 19:48:30 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 14 Feb 2022 19:48:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Feb 2022 19:48:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Feb 2022 19:48:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Feb 2022 19:48:39 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Feb 2022 19:48:40 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Feb 2022 19:48:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Feb 2022 19:48:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:591d91c97b5df29e14efc53ca38020094df8fa114d32d412bb8f02344aad2411`  
		Last Modified: Fri, 28 Jan 2022 02:04:32 GMT  
		Size: 63.9 MB (63857619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d829ba304c2bb185538433d6f9727cc84006b455746a86f38230605dde08072`  
		Last Modified: Sat, 05 Feb 2022 00:13:58 GMT  
		Size: 150.2 MB (150157959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f627e7729aa2b875e95b020b7ea0b57fb470f7512f78243ce61bac0f57092c`  
		Last Modified: Mon, 14 Feb 2022 19:56:41 GMT  
		Size: 3.6 MB (3636629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d599768679099a129a2f26bf6a50072420edc5e810f796507138b2301a4fec`  
		Last Modified: Mon, 14 Feb 2022 19:56:41 GMT  
		Size: 9.1 MB (9109769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0209121e76ec2cccf3cb984f84f72670353ed8b2e586d67adb09676e8acd98f`  
		Last Modified: Mon, 14 Feb 2022 19:56:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39661f8490eb4c973d097e398ad6caf45d959891ae0debd9517f6c6594485604`  
		Last Modified: Mon, 14 Feb 2022 19:56:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
