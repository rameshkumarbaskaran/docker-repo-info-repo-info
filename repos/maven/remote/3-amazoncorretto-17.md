## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:c1a376ce0c60b66091e3f1e950407b1e9c3efb10415120a59cb44e1b2d210102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:6508904a8ac19a3f79caa2a2cfff62bec9b96711b3246b848c62b93a655856be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226193160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4986e284248fd32a299a1c458a61201e65de6e1bf9eedd59a3f6d08833736`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:36:55 GMT
ARG version=17.0.2.8-1
# Sat, 19 Mar 2022 00:37:27 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 00:37:28 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:37:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 05 Apr 2022 13:37:07 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 05 Apr 2022 16:57:26 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 16:57:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 16:57:27 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 16:57:27 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 16:57:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 16:57:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 16:57:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 16:57:29 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 16:57:29 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 16:57:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 16:57:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efe6dac67102bcfdf5d509e6ecae60bc439768df7e02101826619b7b238cd3`  
		Last Modified: Sat, 19 Mar 2022 00:45:34 GMT  
		Size: 151.6 MB (151604861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25709dc40a6d39a55e969f01138e334c3145fb6db02b256cf02d6e3889ff7d55`  
		Last Modified: Tue, 05 Apr 2022 17:07:04 GMT  
		Size: 3.6 MB (3645426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62cc382fee8390541ee2fd197964901b6307d6ab6e4295f215fad009075bcf6`  
		Last Modified: Tue, 05 Apr 2022 17:07:04 GMT  
		Size: 8.7 MB (8736386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32670e531160b45d51b96453f73719451fe87dff44bf780063289580b384003d`  
		Last Modified: Tue, 05 Apr 2022 17:07:03 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb9f4d153862d489490c7309b5ce1dffefc78fa4acfa61b7b7903d06d42b268`  
		Last Modified: Tue, 05 Apr 2022 17:07:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f3170a060f73d7c710fb5ea38420f9d709fc07dc7244fa6d2de9f9a6d611d2e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226711489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1fc36a2276cfafcbaebd808a01fa479d4d7b4d2a9eee7089c9048016899aab`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 04 Mar 2022 02:54:31 GMT
ADD file:d8fe7ad66f762a8aad81401877fc5d61f1a4b58eac91f47145e6e443aa3ac8ee in / 
# Fri, 04 Mar 2022 02:54:32 GMT
CMD ["/bin/bash"]
# Fri, 04 Mar 2022 03:12:48 GMT
ARG version=17.0.2.8-1
# Fri, 04 Mar 2022 03:13:05 GMT
# ARGS: version=17.0.2.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 04 Mar 2022 03:13:06 GMT
ENV LANG=C.UTF-8
# Fri, 04 Mar 2022 03:13:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 04 Mar 2022 03:32:31 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 04 Mar 2022 03:32:31 GMT
ARG MAVEN_VERSION=3.8.4
# Fri, 04 Mar 2022 03:32:32 GMT
ARG USER_HOME_DIR=/root
# Fri, 04 Mar 2022 03:32:33 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Fri, 04 Mar 2022 03:32:34 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Fri, 04 Mar 2022 03:32:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 04 Mar 2022 03:32:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 04 Mar 2022 03:32:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 04 Mar 2022 03:32:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 04 Mar 2022 03:32:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 04 Mar 2022 03:32:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 04 Mar 2022 03:32:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:12990ee66856745f12f3a508d82e3d48a09d0378d91aaca8ca153c3819e7a686`  
		Last Modified: Thu, 03 Mar 2022 02:21:31 GMT  
		Size: 63.8 MB (63816961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee75d8bec894bef0f7c450b86a0cca1fe2f5df59daff60b014c5d18275377df2`  
		Last Modified: Fri, 04 Mar 2022 03:15:08 GMT  
		Size: 150.2 MB (150157364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd5ec08d4256e500be46e37b6d7e092944948df10b96c2eff27cd0c57a8908`  
		Last Modified: Fri, 04 Mar 2022 03:37:50 GMT  
		Size: 3.6 MB (3626173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8b5164a4239e3fc023bc97710bd61a1fa49d54c1395986ad92dc522ec94b`  
		Last Modified: Fri, 04 Mar 2022 03:37:51 GMT  
		Size: 9.1 MB (9109778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29eef4a18ca39ae343f2071a9711a24627e6d9963165698e80018b0fdd96b41`  
		Last Modified: Fri, 04 Mar 2022 03:37:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8c0ee1fc2fc9c7e07ee39b0a641cf31e89a980893244876684e6c210f598bd`  
		Last Modified: Fri, 04 Mar 2022 03:37:50 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
