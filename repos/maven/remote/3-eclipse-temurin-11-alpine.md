## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:4c200b95e6b69ed4d301220839afb30dc0f697752843ff9e30042cee4f84fcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:5ee1550a43cd2a4705e9cacfd1aa2bf8dd0e504abe8a57bc6486bc615c7c6d51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207253647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa97c4b0ef1136b7f065d3ff8d490a73f833b3b6a874710fdb85989c2949730`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 10:55:44 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 05 Apr 2022 10:56:22 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 05 Apr 2022 10:56:52 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='99e13a167ac27fac3dbfcc394a024fd9f4d84d24734ad5c250f97215d496ee36';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 10:56:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:56:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 05 Apr 2022 10:56:53 GMT
CMD ["jshell"]
# Tue, 05 Apr 2022 13:34:09 GMT
RUN apk add --no-cache curl tar bash procps
# Tue, 05 Apr 2022 16:56:18 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 16:56:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 16:56:18 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 16:56:18 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 16:56:20 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 16:56:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 16:56:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 16:56:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 16:56:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 16:56:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 16:56:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3277e9a7631c57d573722746688faad867a5b43dda77316e369e08ba94b713d`  
		Last Modified: Tue, 05 Apr 2022 10:59:33 GMT  
		Size: 430.5 KB (430455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60774dae93e5fecd3a84daedfec3fdc3f15b82a411731498edba51a50c5d3beb`  
		Last Modified: Tue, 05 Apr 2022 11:00:31 GMT  
		Size: 192.9 MB (192891699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa5918533881648f140f26c59db4faace77d32f81094090aa5c6d79abe80266`  
		Last Modified: Tue, 05 Apr 2022 11:00:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b712594b22cfd144a552e3e51bcdd5582355578cf864cf2261dc66e302b340`  
		Last Modified: Tue, 05 Apr 2022 17:03:20 GMT  
		Size: 2.4 MB (2379176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5255d7c01f24e85b481f28f742fc465e97220d14e39ddb1ffe705e231812c208`  
		Last Modified: Tue, 05 Apr 2022 17:03:21 GMT  
		Size: 8.7 MB (8736380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6fa31c9be401653c51fbf7cb4660479d3f78090c09d1c54f850f19c85ba9df`  
		Last Modified: Tue, 05 Apr 2022 17:03:19 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f642f023b70f77ad13e065ef079e644b97fa493619c5f279caf032a3a0ecae72`  
		Last Modified: Tue, 05 Apr 2022 17:03:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
