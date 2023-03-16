## `maven:3-eclipse-temurin-19-alpine`

```console
$ docker pull maven@sha256:2d08d8b341db5653efbdcc2facd45a91d16388db36f1c09df5e0a6b2ff7e1b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-19-alpine` - linux; amd64

```console
$ docker pull maven@sha256:929b0d4010bb15071f354cb98f97385f513a9fd5a80a24ad0dc92da1e9cf841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226952843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c49622d7a9f8fc363b6444c1b551ac5c03397da27e086866d5a2207765c011`
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
# Sat, 11 Feb 2023 05:26:26 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Sat, 11 Feb 2023 05:26:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2d971400ad2db25ad43ea6fa2058b269c0236e3977986dcdee2097da301beb2';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:26:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 05:26:51 GMT
CMD ["jshell"]
# Thu, 16 Mar 2023 19:21:51 GMT
RUN apk add --no-cache bash procps curl tar # buildkit
# Thu, 16 Mar 2023 19:21:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Mar 2023 19:21:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Mar 2023 19:21:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Mar 2023 19:21:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Mar 2023 19:21:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Mar 2023 19:21:52 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Mar 2023 19:21:52 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Mar 2023 19:21:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Mar 2023 19:21:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Mar 2023 19:21:52 GMT
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
	-	`sha256:179e78b7ac3beb399f002d9c566af29327c2fd2ac6956665f64f53aecf8d1119`  
		Last Modified: Sat, 11 Feb 2023 05:31:21 GMT  
		Size: 200.3 MB (200308729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ece7618d1e8c49aa5ff521f5133d9ab5bd61543cfe7493b40e99d10a2ec5d6`  
		Last Modified: Sat, 11 Feb 2023 05:31:05 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b57d8a1699691ed3ce2eb747c074d71b15662ed890e6ddb7e73f779ce59925f`  
		Last Modified: Thu, 16 Mar 2023 19:28:21 GMT  
		Size: 2.2 MB (2157250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f349e68076d8740a9ae50da27025fd6098929d8e8db5979d4252643cbf7f9f7`  
		Last Modified: Thu, 16 Mar 2023 19:28:21 GMT  
		Size: 9.1 MB (9090702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c65f81afc06c53479b64eb1d9da207b04b9437316bcb4acc8886f1729a21de`  
		Last Modified: Thu, 16 Mar 2023 19:28:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b709c1363f02153ea461050f5fe71fff26efb322df008d63ef843f83b97ff39e`  
		Last Modified: Thu, 16 Mar 2023 19:28:21 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec33e5120953f5a72688f0159886de014a1d657e9a9d55aa7cbc10d76842c94`  
		Last Modified: Thu, 16 Mar 2023 19:28:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
