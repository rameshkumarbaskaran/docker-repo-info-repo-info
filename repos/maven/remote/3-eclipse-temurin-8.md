## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:529670854b9281ef43a8cf0c2a9a2b28f88e837f49d0a2d9fb0628f9ed7dc7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-eclipse-temurin-8` - linux; amd64

```console
$ docker pull maven@sha256:041e206d526d5e390574abe5fab779ba0a33f7d8ed7d10b1e63385b5b4b16851
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188488494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d61c790e5f43dc8b7dc80dd46f9802d6b149931c0f8b0c5873d18932b565924`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:19:30 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:19:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87ff502eba3008cac71edeb9595398a73dc14883fe3072d152e731bf0877897e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5a9e72c6c20373aa380554a6d7191a258540d2a0399d842223b8d5eb0f74b298';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ddce3f067eab6fd98bb2a8ea3d18de6b09ea41d10382c76ad22bd3e7895951cf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='699981083983b60a7eeb511ad640fae3ae4b879de5a3980fe837e8ade9c34a08';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:19:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:19:38 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 23 Nov 2021 01:04:01 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 01:04:02 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 01:04:02 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 01:04:02 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 01:04:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:04:23 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 01:04:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 01:04:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 01:04:24 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 01:04:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 01:04:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 01:04:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237daeb1ae282fe20092079ef6d5de7924746d0f2e9ad88797d08524a4d842fd`  
		Last Modified: Sat, 16 Oct 2021 02:47:20 GMT  
		Size: 16.0 MB (16036029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88c0023b74602928576f2bb752c14dfefcc0e829993e068bd306fdb7bb1e25b`  
		Last Modified: Fri, 05 Nov 2021 19:22:47 GMT  
		Size: 103.6 MB (103602669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2410290cfe6c0f5a5693b798208ee4c4f4d7813f71c9c88bb4bea341a40d188b`  
		Last Modified: Fri, 05 Nov 2021 19:22:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c2989e4ca49332cd54219ab1932dda5483a804e6147d377d5742023d776e86`  
		Last Modified: Tue, 23 Nov 2021 01:12:08 GMT  
		Size: 31.2 MB (31171499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb657abff893d62e4f99f00b367a331f6dbf3c5d123c0bfc162b1634d2622ebf`  
		Last Modified: Tue, 23 Nov 2021 01:12:03 GMT  
		Size: 9.1 MB (9109824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2734b4a531ca7b77a19e1b17f4e7bc791a7785fbcc1c4576c4b644634a7feb`  
		Last Modified: Tue, 23 Nov 2021 01:12:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338b0bacd4200bcbf8a2ae4a49ae24e473a6b82074b3b67316961bbd53788e8f`  
		Last Modified: Tue, 23 Nov 2021 01:12:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:5b23b0bcbe208057624ada06450471eeaebcc93455818abfb52d6209abfbb8cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174642672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209f2c10d60945001be1ae1ee9a2d39fc49c90571c270b8ec0c697da27b5e4bc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:39:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 18:57:41 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 18:58:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87ff502eba3008cac71edeb9595398a73dc14883fe3072d152e731bf0877897e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5a9e72c6c20373aa380554a6d7191a258540d2a0399d842223b8d5eb0f74b298';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ddce3f067eab6fd98bb2a8ea3d18de6b09ea41d10382c76ad22bd3e7895951cf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='699981083983b60a7eeb511ad640fae3ae4b879de5a3980fe837e8ade9c34a08';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 18:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 18:58:08 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 23 Nov 2021 01:52:04 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 01:52:05 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 01:52:05 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 01:52:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 01:52:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 01:52:39 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 01:52:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 01:52:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 01:52:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 01:52:41 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 01:52:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 01:52:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437a7367762ea761c5abbcde550ac6e83ab2fd882f50cc7c0b8a3ef2bcc5505b`  
		Last Modified: Sat, 16 Oct 2021 02:44:07 GMT  
		Size: 14.9 MB (14902308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5304e4c948d1ea493512103e596754065144e4dd554b128a408a4fb01e69f0f`  
		Last Modified: Fri, 05 Nov 2021 19:03:15 GMT  
		Size: 99.3 MB (99267900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f044d3a6331e4a0681eddf00dda63fa26afe2c6317d75221e906d97326fba2`  
		Last Modified: Fri, 05 Nov 2021 19:02:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1735257ce074bb09bbe104443ea8cf690d11983f5ee5f56b3d9d56c9aaebbd1e`  
		Last Modified: Tue, 23 Nov 2021 01:56:13 GMT  
		Size: 27.3 MB (27296841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f255f1fd6c01733c9c354b639a6bb3dc016ce59406c1ba7bc2b2b4fc2af294d`  
		Last Modified: Tue, 23 Nov 2021 01:56:00 GMT  
		Size: 9.1 MB (9109802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769eb0f4099115e965f050dacbd4d238789825b187c28bb7de7ba7f2a8d06400`  
		Last Modified: Tue, 23 Nov 2021 01:55:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac721c9445834b4becc66e597dd967a5377995d2bc6d10a46dba327cbf1bbbad`  
		Last Modified: Tue, 23 Nov 2021 01:55:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:69a1429f0a8c9585754e3e6998705cf07b977be24f67230e5134327ce462d6f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194746918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393c0212ccb0f1d85f63d61173d30a8f04639f4bef11be9e9cd7a9de98d69b15`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Nov 2021 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales python-is-python3     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 19:40:02 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Mon, 29 Nov 2021 19:40:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87ff502eba3008cac71edeb9595398a73dc14883fe3072d152e731bf0877897e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5a9e72c6c20373aa380554a6d7191a258540d2a0399d842223b8d5eb0f74b298';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ddce3f067eab6fd98bb2a8ea3d18de6b09ea41d10382c76ad22bd3e7895951cf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='699981083983b60a7eeb511ad640fae3ae4b879de5a3980fe837e8ade9c34a08';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 29 Nov 2021 19:40:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Nov 2021 19:40:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 29 Nov 2021 21:01:03 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 29 Nov 2021 21:01:04 GMT
ARG USER_HOME_DIR=/root
# Mon, 29 Nov 2021 21:01:05 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 29 Nov 2021 21:01:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 29 Nov 2021 21:01:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Nov 2021 21:01:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 29 Nov 2021 21:01:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 29 Nov 2021 21:01:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 29 Nov 2021 21:01:27 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 29 Nov 2021 21:01:28 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 29 Nov 2021 21:01:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 29 Nov 2021 21:01:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa42563dc02061b51ce62bff7340de9cea06ea720e8658d2a7693902aa8f700`  
		Last Modified: Mon, 29 Nov 2021 19:44:11 GMT  
		Size: 24.8 MB (24763049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343dd1f534fdf1b2da680fddc088c67d53fe32f7fd576b0f6be005126354cdf7`  
		Last Modified: Mon, 29 Nov 2021 19:44:17 GMT  
		Size: 102.7 MB (102728946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b923b78169a827f6588a2eeffba72af636d621c7523caa0ef1a430da82a5c6a`  
		Last Modified: Mon, 29 Nov 2021 19:44:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79eb4537998693cdf807c3902b343a134952a115d93498a062f007735b9d2be8`  
		Last Modified: Mon, 29 Nov 2021 21:05:23 GMT  
		Size: 31.0 MB (30972902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9acad7d1d896d2bfb50ae6c1a421e3ecf50965af20a5bc93cd05fb16dc65ef`  
		Last Modified: Mon, 29 Nov 2021 21:05:20 GMT  
		Size: 9.1 MB (9109781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44701519366ecb93c2b8df999d1f38954a208d0ef698fbd433324846a5e7adf8`  
		Last Modified: Mon, 29 Nov 2021 21:05:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e950d8e1a4cdcd9057143f7a59fb12cd37200053c3bd0ce179df405b8f8f71`  
		Last Modified: Mon, 29 Nov 2021 21:05:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:32742463105b885cb9e7cc2a9b5f1b013d8c08bde0b92c5c125fb5d0dd64b0f4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199069226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976c9447294c7938902e0c9509a0375ca92be916e875c010e0ef328365014fdf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:55:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 20:39:01 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 20:39:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='87ff502eba3008cac71edeb9595398a73dc14883fe3072d152e731bf0877897e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5a9e72c6c20373aa380554a6d7191a258540d2a0399d842223b8d5eb0f74b298';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='ddce3f067eab6fd98bb2a8ea3d18de6b09ea41d10382c76ad22bd3e7895951cf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='699981083983b60a7eeb511ad640fae3ae4b879de5a3980fe837e8ade9c34a08';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 20:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 20:39:33 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 23 Nov 2021 00:44:36 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 23 Nov 2021 00:44:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 Nov 2021 00:44:40 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 23 Nov 2021 00:44:41 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 23 Nov 2021 00:45:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 00:45:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 23 Nov 2021 00:45:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 Nov 2021 00:45:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 Nov 2021 00:45:26 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 23 Nov 2021 00:45:28 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 23 Nov 2021 00:45:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 Nov 2021 00:45:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c930749dacf55e37561edab7967f5a2f51660034fee0da501c2d71cb783301`  
		Last Modified: Sat, 16 Oct 2021 01:03:26 GMT  
		Size: 17.2 MB (17210510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589c2aa78a7742f07aed96b0f822fbb575ce64fc14d614f0cba7fd0e38a73823`  
		Last Modified: Fri, 05 Nov 2021 20:47:26 GMT  
		Size: 101.1 MB (101091923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d567706d977f4e1ae840778268e18a69b0a7884b74e5ab9b1527073c5b74bdf1`  
		Last Modified: Fri, 05 Nov 2021 20:47:14 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9082e6662fd2efcbaa7d8235ce1e528f47d4ba23c89d6af4337d656ed2d8e39e`  
		Last Modified: Tue, 23 Nov 2021 00:49:00 GMT  
		Size: 38.4 MB (38368376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2acf8599f93bfe837adf5107d7fa873b495250d9a4daa0685f13e73bad6dea6`  
		Last Modified: Tue, 23 Nov 2021 00:48:54 GMT  
		Size: 9.1 MB (9109805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58484a20c03f1daa6e3d9359cd8997e15704818c03dbb9163ffd855dca007ac`  
		Last Modified: Tue, 23 Nov 2021 00:48:53 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd46daebff5cf0ed70cc0990b31f3ee1c0c9c6cf3dc07905c7bddf5dab0a550d`  
		Last Modified: Tue, 23 Nov 2021 00:48:53 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
