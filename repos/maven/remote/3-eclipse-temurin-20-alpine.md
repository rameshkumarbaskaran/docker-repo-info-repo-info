## `maven:3-eclipse-temurin-20-alpine`

```console
$ docker pull maven@sha256:27eedda17253d7286d45268a93469065241af14ab12e32f82078d253661e6e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-20-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7b73f9ef9a31c77fef5a3b0f989f1e6dfd8524be53e5909b58d05ea3460c94d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225204434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1193b3e31ca578446700ee71bcc26d81eb5d4b15ca7b27b6982ecbc2978fee9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jun 2023 05:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jun 2023 05:11:54 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 15 Jun 2023 05:13:51 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 15 Jun 2023 05:14:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d0f0c468064e944e304cab64fc162335d4d9bc0ddab7e6ff7a395a0bceda74';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 15 Jun 2023 05:14:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 15 Jun 2023 05:14:04 GMT
CMD ["jshell"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aadc9aaa732ac5b0edd00545607971071fa1868047a65249e483ba2443982e6`  
		Last Modified: Thu, 15 Jun 2023 05:15:34 GMT  
		Size: 7.6 MB (7648372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d7d7d1600692ee70c8098f819ea5dab900fe619a1d0ce9ab60decceed7b3b7`  
		Last Modified: Thu, 15 Jun 2023 05:17:58 GMT  
		Size: 202.0 MB (201970803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d91e43deec5874b6a039c7a0713c640be552f639cdbcb59f5f31a37982f0e6`  
		Last Modified: Thu, 15 Jun 2023 05:17:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57af81420b70011b0fb4b9b22c8b819c053e2d0a723fc50268dd6180682d6190`  
		Last Modified: Thu, 15 Jun 2023 09:33:11 GMT  
		Size: 2.9 MB (2871419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4221ca46ec2cf2839d43ab86a2f7c8a3e656f66f0dad1980f73622f66af8f35`  
		Last Modified: Thu, 15 Jun 2023 09:33:12 GMT  
		Size: 9.3 MB (9314415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a023dbcd16377c9bc1596a0f7261f059c318a9ecf527bfa60187ae5e1271c50`  
		Last Modified: Thu, 15 Jun 2023 09:33:11 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aef29bdd15b11ff8a3cb9a13a7313a4c5ddb6ef9a0be8658a45d10c5adf8b01`  
		Last Modified: Thu, 15 Jun 2023 09:33:11 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5db67716f38dc3652e0f78804d9837b7d92cfa9a8b067a1c8e48659d0a5cc0`  
		Last Modified: Thu, 15 Jun 2023 09:33:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
