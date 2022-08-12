## `maven:3-eclipse-temurin-11`

```console
$ docker pull maven@sha256:9f96b500f1c1498659001e2c48e25f1359786bb3ebd6802fd48f1f0dc94a1d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-eclipse-temurin-11` - linux; amd64

```console
$ docker pull maven@sha256:60574b42e52f72c66fe78a6a2f08742091383d01d5271ee37ba17f84211b99c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271574078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506ddc02f209645c91db0610d57a7648c8213d3e065d1bd88549425fe49ece2f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:20:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:20:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:22:09 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Fri, 12 Aug 2022 17:22:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 12 Aug 2022 17:22:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Aug 2022 17:22:20 GMT
CMD ["jshell"]
# Fri, 12 Aug 2022 18:46:43 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 18:46:43 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 12 Aug 2022 18:46:43 GMT
ARG USER_HOME_DIR=/root
# Fri, 12 Aug 2022 18:46:43 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 12 Aug 2022 18:46:44 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 12 Aug 2022 18:46:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 12 Aug 2022 18:46:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 12 Aug 2022 18:46:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 12 Aug 2022 18:46:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 12 Aug 2022 18:46:45 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 12 Aug 2022 18:46:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 12 Aug 2022 18:46:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65811de5a1ce73e051835187b84371fd526024c2be009224c3a1f5adaa87c90`  
		Last Modified: Fri, 12 Aug 2022 17:28:31 GMT  
		Size: 12.5 MB (12456003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075d0c0e8bbb371e8dd0998a6df9602147fa94aaa29ea0c24a7e6579b879dd2b`  
		Last Modified: Fri, 12 Aug 2022 17:30:38 GMT  
		Size: 198.1 MB (198127118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8180b0c10f0e630efdfd7f7c94abba72a9cd8bf274c38592a8f60ff13285ac2`  
		Last Modified: Fri, 12 Aug 2022 17:30:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd7a2dc90f3a886e38327986be7d067b1630d2083d1947fdc7dc0a4b6e695b`  
		Last Modified: Fri, 12 Aug 2022 18:50:25 GMT  
		Size: 21.8 MB (21823953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197280f1f08d2dcb03879bbc8f4738ac4209dd847ac7d249754659e8b343953`  
		Last Modified: Fri, 12 Aug 2022 18:50:22 GMT  
		Size: 8.7 MB (8739486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ebdfdd3e645e84d84a8b4ad6afdf2053ef1b33d8c356485e0e8ecd6a039e3f`  
		Last Modified: Fri, 12 Aug 2022 18:50:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230c3d84ed4981df0b16d4d8d5c10ff277a05b2e5ceadaab45ff2497653ef12`  
		Last Modified: Fri, 12 Aug 2022 18:50:21 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm variant v7

```console
$ docker pull maven@sha256:8e409635c4b2ee973167438dd2bd8ed60d04170d302f9754652b8c0979df63d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258703293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064fba5138d7eb89918670eed472fd0a759fbb89ef44e44fd39c3738fb136201`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:56 GMT
ADD file:1bec4ea562c9a42add30f5e3626edc93bdfc0271cbd208a4447842fa31b5c114 in / 
# Tue, 02 Aug 2022 01:40:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:58:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:58:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:58:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 16:58:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 16:59:50 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Fri, 12 Aug 2022 16:59:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 12 Aug 2022 17:00:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Aug 2022 17:00:02 GMT
CMD ["jshell"]
# Fri, 12 Aug 2022 18:08:10 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 18:08:10 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 12 Aug 2022 18:08:10 GMT
ARG USER_HOME_DIR=/root
# Fri, 12 Aug 2022 18:08:10 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 12 Aug 2022 18:08:11 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 12 Aug 2022 18:08:12 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 12 Aug 2022 18:08:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 12 Aug 2022 18:08:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 12 Aug 2022 18:08:13 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 12 Aug 2022 18:08:13 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 12 Aug 2022 18:08:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 12 Aug 2022 18:08:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f1a5cf9a21e485b0a676c22ced0e80a140055b3ef0d7573caf5be408a10ddb04`  
		Last Modified: Tue, 02 Aug 2022 01:43:32 GMT  
		Size: 27.0 MB (27017015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f750e2d5f8b88349d4851becd87f9216149478e46f3c5da8cf34b92d6cf5975d`  
		Last Modified: Fri, 12 Aug 2022 17:06:31 GMT  
		Size: 12.0 MB (12033944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab82de343dcefdbbe437658b67e3e7a95f0b730380449985e75a62ea6d37276`  
		Last Modified: Fri, 12 Aug 2022 17:08:14 GMT  
		Size: 185.5 MB (185543377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e87c3986899c0841d1a633a7ff9eb5e8fc310e55c5d146ff300b6d321a0f6da`  
		Last Modified: Fri, 12 Aug 2022 17:07:58 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0a1b6d2c298fa5dcd22a803db6ae05e6cdf9015bbb0252e05b6f66b447a237`  
		Last Modified: Fri, 12 Aug 2022 18:11:42 GMT  
		Size: 25.4 MB (25368077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f76b49036a3fe783305bd373e72846fb38d31e1e59dda406eeafca4666c5484`  
		Last Modified: Fri, 12 Aug 2022 18:11:39 GMT  
		Size: 8.7 MB (8739492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48467ab0c15e074d28584086bdfb3d1316715376baa490b08a341a504210786f`  
		Last Modified: Fri, 12 Aug 2022 18:11:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c8c6528d3af4961fcf791acc7536863eca4a9ae27314d4f7b8a30cb4b6fc87`  
		Last Modified: Fri, 12 Aug 2022 18:11:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a5cb8c1f70ff48557e9d28a6797bf52f5f1aae5deba23a8cc6f869dbded60e0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262049581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215e2bbcea544e60472b2cac4f4e0dacc699d3a73101e8e3e864c039ccebd128`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 17:51:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:53:04 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Tue, 02 Aug 2022 17:53:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:53:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:53:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 02 Aug 2022 17:53:13 GMT
CMD ["jshell"]
# Wed, 03 Aug 2022 01:03:25 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 01:03:25 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 03 Aug 2022 01:03:26 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Aug 2022 01:03:27 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 03 Aug 2022 01:03:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 03 Aug 2022 01:03:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 03 Aug 2022 01:03:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Aug 2022 01:03:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Aug 2022 01:03:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 03 Aug 2022 01:03:41 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 03 Aug 2022 01:03:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Aug 2022 01:03:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a97efc1a354ae767e234943d1f6e30a9985c45f60c828e9af06c2cd98ae470`  
		Last Modified: Tue, 02 Aug 2022 18:00:04 GMT  
		Size: 12.1 MB (12078076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c37c8897a915abd082b9db602a3f52d185a22088a2a5885b6a663ba01f5d9f`  
		Last Modified: Tue, 02 Aug 2022 18:02:27 GMT  
		Size: 191.3 MB (191349043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfab8f26ab7e76ba52c4105f41779761ea9ce2758c5fe930e0eb244350c470d`  
		Last Modified: Tue, 02 Aug 2022 18:02:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b881fb35498e2ef57f5fe77f029e4c181a35e4b5081c52b6e3a667c3969992`  
		Last Modified: Wed, 03 Aug 2022 01:14:16 GMT  
		Size: 21.5 MB (21500497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67dc9ff4a496e746588ab7d7fa00b03bb396773476ec5a2eaa404758b5d9b4a`  
		Last Modified: Wed, 03 Aug 2022 01:14:13 GMT  
		Size: 8.7 MB (8739472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e571fb2824278c4174dab80f0238411d07789ebc099d577bbe5752a701b9c8eb`  
		Last Modified: Wed, 03 Aug 2022 01:14:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21347b35aa45036df9954f492c1c912889e7bf3ba7ad8972e4bc15a5d7e38c66`  
		Last Modified: Wed, 03 Aug 2022 01:14:13 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; ppc64le

```console
$ docker pull maven@sha256:2e18f83b543977f2b77f32766d58dacc9a411797ddcd02c929c17eab2a27f35f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259538015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688c193fb949022277854f1aec9ed0bd7e517adf68227c5c3df691cb5713a536`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:31:12 GMT
ADD file:b6916c28c03568df4c2efc3da91ea6320f639cdbd2fa3f6741fcea7acad4fd5f in / 
# Tue, 02 Aug 2022 01:31:14 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:20:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 03 Aug 2022 03:21:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 03:24:03 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 03 Aug 2022 03:24:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 03 Aug 2022 03:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 03:24:25 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 03 Aug 2022 03:24:25 GMT
CMD ["jshell"]
# Wed, 03 Aug 2022 23:44:47 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 23:44:48 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 03 Aug 2022 23:44:49 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Aug 2022 23:44:49 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 03 Aug 2022 23:44:49 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 03 Aug 2022 23:44:51 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 03 Aug 2022 23:44:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Aug 2022 23:44:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Aug 2022 23:44:52 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 03 Aug 2022 23:44:52 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 03 Aug 2022 23:44:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Aug 2022 23:44:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6f8c2fc0a4f976c1c0bd1c0e14022b3ed8b7c83cdb247c83016052c3678aaf28`  
		Last Modified: Tue, 02 Aug 2022 01:33:53 GMT  
		Size: 35.7 MB (35718004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12312efe1c15bed28c535aa9c41c1b820facd1b2a584f36ed7f7297df7eeac1c`  
		Last Modified: Wed, 03 Aug 2022 03:34:09 GMT  
		Size: 12.9 MB (12862334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd11471e7d39bd685636b2411059e44b70ab425e2da96f6dfb0fd53feed88d34`  
		Last Modified: Wed, 03 Aug 2022 03:37:03 GMT  
		Size: 176.5 MB (176541516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3f19a88ca2b7ce1872b7bdfbfdc3e4e2d85ea845785f450f1bff4a52d6a2fe`  
		Last Modified: Wed, 03 Aug 2022 03:36:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51057517350daef68bae3560ab6f50bf84d12d1d6d2c1447ba1b7e1989c86e16`  
		Last Modified: Wed, 03 Aug 2022 23:52:26 GMT  
		Size: 25.7 MB (25675321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0886b76a489f8980eede54717786b3afb7a535ae24480e20740fd25fdc704b`  
		Last Modified: Wed, 03 Aug 2022 23:52:19 GMT  
		Size: 8.7 MB (8739472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c507b5d27754e1d2d14c00e5bcea1dff57a3573c7679d5b205f7638a051ee64a`  
		Last Modified: Wed, 03 Aug 2022 23:52:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026536ed2e31e8055737f9deb316b71bfebbd7d803a668defd58ea66f22be335`  
		Last Modified: Wed, 03 Aug 2022 23:52:18 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-11` - linux; s390x

```console
$ docker pull maven@sha256:5c4afa82810e5fe7e1607dd1e6e7295e28539b7ceec373ee7aa17b57a033f1e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244117366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d4fb25a339d331afa7dacf1052fb69a8f457ae86db06294fd5430722dae0ef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:17 GMT
ADD file:d5a5e56e0ca8287f27b257e3ddbc9675a1bdac1912afbbab6cddd891056cd144 in / 
# Tue, 02 Aug 2022 01:02:19 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:42:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:42:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:42:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 17:42:41 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Fri, 12 Aug 2022 17:42:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='bb345cabf3e305ff3ce390918d5f69e5cfbced3d9844e0b0531c2690f9ed06ef';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.16_8.tar.gz';          ;;        armhf|arm)          ESUM='2b0b390ba17963d70883506a72b58d315cab7a24b418fdab5351728f328f398e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.16_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='40dea12da26443ad731f9348187b65451711659337e83b6409a2bcf0f057cd2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.16_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f7975c9670a6697d0afedd3ebebe545f04bdec9aa7efbe9136f1c5182eca62e1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.16_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f79506f80c796d8e6a382f00bd8c528a330c5e29581aaf5cb61e1831742d166f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 12 Aug 2022 17:42:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Aug 2022 17:42:58 GMT
CMD ["jshell"]
# Fri, 12 Aug 2022 18:27:53 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 18:27:54 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 12 Aug 2022 18:27:55 GMT
ARG USER_HOME_DIR=/root
# Fri, 12 Aug 2022 18:27:55 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 12 Aug 2022 18:27:55 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 12 Aug 2022 18:27:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 12 Aug 2022 18:27:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 12 Aug 2022 18:27:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 12 Aug 2022 18:27:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 12 Aug 2022 18:28:00 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 12 Aug 2022 18:28:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 12 Aug 2022 18:28:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f97967c51aac02138b615522a1bab9c75addd5896f43ade17ddaac44e0644283`  
		Last Modified: Tue, 02 Aug 2022 01:03:51 GMT  
		Size: 28.6 MB (28642785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b487214c25e1024a8781e65f9a2199413fa526aee2b0ad57feec90899ac822c`  
		Last Modified: Fri, 12 Aug 2022 17:48:54 GMT  
		Size: 12.5 MB (12518919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9191eacd184c568648eb52e629571311406cf85ee25a7ba1c5a5678952d7296`  
		Last Modified: Fri, 12 Aug 2022 17:49:04 GMT  
		Size: 172.3 MB (172259778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2ec8d8682931227df807dd763ac182ef32a6903a08a1336d1fb62e34e75b6`  
		Last Modified: Fri, 12 Aug 2022 17:48:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f38c6c2937a276f0ce721beede03fa52ee6a7e8f96d0ca7738966c56783e33`  
		Last Modified: Fri, 12 Aug 2022 18:31:54 GMT  
		Size: 22.0 MB (21955011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9260ed9ae95ae6fb17719070862c9dfc438e3f9598a2038f7140dfa3d94ca4`  
		Last Modified: Fri, 12 Aug 2022 18:31:51 GMT  
		Size: 8.7 MB (8739486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac58236ff488da730d785b1cc9bad5b6aaa2f72e11e2a29151dae88a179abb0a`  
		Last Modified: Fri, 12 Aug 2022 18:31:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea9bb4a956a6bbb67ebc1255119b656c4a72266a231359589935342ed5a6195`  
		Last Modified: Fri, 12 Aug 2022 18:31:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
