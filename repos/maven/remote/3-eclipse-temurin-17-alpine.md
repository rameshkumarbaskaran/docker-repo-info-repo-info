## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:6d2574c7b8c387334e3e14a2473904065ba9ea50a6adc1276cb31bb9b88f0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:093d29409fa2d98ddb20420dfc0b095df53ea7f63eafcb00097b4b88ff7f3a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218437954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d240a8a8bc996adc9966ed6beb874f3d8d96c443a7700f9d7f5f7c724b1171c0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Feb 2023 05:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:24:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 11 Feb 2023 05:24:09 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 05:25:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Sat, 11 Feb 2023 05:25:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0df7c1a58debee2668931ba4a07cb642475b23a5c61473761b6f293eba7c024a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:25:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 05:25:58 GMT
CMD ["jshell"]
# Thu, 16 Mar 2023 16:09:38 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 16 Mar 2023 16:09:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Mar 2023 16:09:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Mar 2023 16:09:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Mar 2023 16:09:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Mar 2023 16:09:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Mar 2023 16:09:38 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Mar 2023 16:09:38 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Mar 2023 16:09:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Mar 2023 16:09:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Mar 2023 16:09:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55337210c571172bc884a7dfb6dc597adab6b6ef741c06ca3200884ffc4b2b`  
		Last Modified: Sat, 11 Feb 2023 05:28:55 GMT  
		Size: 12.0 MB (12020168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383e2293b907d32c7858537a6809dd478738e849ca592204cc0e265890510eb`  
		Last Modified: Sat, 11 Feb 2023 05:30:33 GMT  
		Size: 191.8 MB (191793857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1c4a54fb1014a2cb1df9c41d593556fbcec834958d0651d951ec8a27ad00da`  
		Last Modified: Sat, 11 Feb 2023 05:30:19 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29d747d538e02aa22f0145e70b7acde47658514d119921777ffebeb125a4ae2`  
		Last Modified: Thu, 16 Mar 2023 19:27:37 GMT  
		Size: 2.2 MB (2157247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2f3982fec60d348b27ad25664140f4e70b355ee12a3cea12f872a752f3b797`  
		Last Modified: Thu, 16 Mar 2023 19:27:37 GMT  
		Size: 9.1 MB (9090688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8e6894b3bf8431c6eb24f322fd057845317fe13cec94aebc8c45108905d2e`  
		Last Modified: Thu, 16 Mar 2023 19:27:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb293c26846455d71289d09ab170c2d8b1a5a9fddfbd18aa0ef0a76cf00d2bb`  
		Last Modified: Thu, 16 Mar 2023 19:27:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ac792f8c66239d9c3e86a67638a7dbcba914cd3a98e49d096bc7342d69dd13`  
		Last Modified: Thu, 16 Mar 2023 19:27:36 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
