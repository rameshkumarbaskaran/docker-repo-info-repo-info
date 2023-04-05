## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:5a29e39883192279562c8a942a14fe24d2631463e3f90e045c25a63ebf70a629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:bacd22e9ea81711f90040ce5b4b945bfd6775acd858d42dc1c6ab2d5c8ebcc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218453109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3c05542a2599413a25a5e05582fd69f660e8b7de2afb19bd6e8de9a2a3e012`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:48:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Mar 2023 19:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:48:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Mar 2023 19:48:58 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 29 Mar 2023 19:50:07 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 29 Mar 2023 19:50:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0df7c1a58debee2668931ba4a07cb642475b23a5c61473761b6f293eba7c024a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 29 Mar 2023 19:50:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 29 Mar 2023 19:50:20 GMT
CMD ["jshell"]
# Sun, 02 Apr 2023 19:35:52 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 02 Apr 2023 19:35:52 GMT
ARG MAVEN_VERSION=3.9.1
# Sun, 02 Apr 2023 19:35:52 GMT
ARG USER_HOME_DIR=/root
# Sun, 02 Apr 2023 19:35:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 02 Apr 2023 19:35:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 02 Apr 2023 19:35:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ed194273be4d4d02a2158c3e7c9ea96095ed70f65939d53f4968b0f225c628`  
		Last Modified: Wed, 29 Mar 2023 19:52:03 GMT  
		Size: 12.0 MB (12019605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447fb591121b7b0c1f352bc4baf3b7c840dcf32615f5b8504a4882e9048f2dca`  
		Last Modified: Wed, 29 Mar 2023 19:53:34 GMT  
		Size: 191.8 MB (191793866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cdd4cdb2078d3e1d61a38f6f6378966a085bf96adceecceeaffa29922faedb`  
		Last Modified: Wed, 29 Mar 2023 19:53:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8005cce708f4781f0238312e7adb87672b1bce342e5cd5dcba7f00d69110cfd`  
		Last Modified: Thu, 30 Mar 2023 02:59:01 GMT  
		Size: 2.2 MB (2157366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388a4b4a692ae39254b53b2270aaa6a04a33f22315cf2646f8f2631020f93585`  
		Last Modified: Wed, 05 Apr 2023 17:29:56 GMT  
		Size: 9.1 MB (9106159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c820bd4c78f39a9b234041d2700e56094d7b0839a067beb6f5446e330779c3e6`  
		Last Modified: Wed, 05 Apr 2023 17:29:55 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39e80ed03aa1f2a87a2cd7905edd71b8fca7f1414eac2c0a41371c2af4f5e0e`  
		Last Modified: Wed, 05 Apr 2023 17:29:55 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94e64e87ddf25ae7a58b7677163f323deaa6524e4a6c7c62c5b2e4d79a90a07`  
		Last Modified: Wed, 05 Apr 2023 17:29:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
