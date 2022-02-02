## `maven:3-eclipse-temurin-17-alpine`

```console
$ docker pull maven@sha256:0bf9d5432964c78c6f62c710bfdd78e1315b994627b17c87aad2d137f570a2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:240900eb83b8c91f34a129881dfd2fd14f0be37ecd324af2ea02a47bffd36923
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206663018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ab0e8a5279638ee1d22fa220b53981a56dbad202b07b25fbe4e34f0410199`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Thu, 13 Jan 2022 17:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Jan 2022 17:19:46 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 01 Feb 2022 22:23:01 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Tue, 01 Feb 2022 22:23:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a07cc09db0e71d06ea388902f8fcea8151b2b9ba51a16f75f9c0a3ac9acbfb61';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 01 Feb 2022 22:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 22:23:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 01 Feb 2022 22:23:22 GMT
CMD ["jshell"]
# Wed, 02 Feb 2022 01:47:33 GMT
ARG MAVEN_VERSION=3.8.4
# Wed, 02 Feb 2022 01:47:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 02 Feb 2022 01:47:33 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Wed, 02 Feb 2022 01:47:34 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Wed, 02 Feb 2022 01:47:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apk add --no-cache curl tar bash procps
# Wed, 02 Feb 2022 01:47:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 02 Feb 2022 01:47:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 02 Feb 2022 01:47:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 02 Feb 2022 01:47:37 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 02 Feb 2022 01:47:37 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 02 Feb 2022 01:47:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 02 Feb 2022 01:47:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7418fdfb53d3b677d087a50df49ad12829a9eab2f0b2c8c19b162589387891`  
		Last Modified: Thu, 13 Jan 2022 17:22:44 GMT  
		Size: 430.3 KB (430278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c6eec7d0d4afbf6a62c060714524c6eafd527203c35bad33de1def979461d4`  
		Last Modified: Tue, 01 Feb 2022 22:29:03 GMT  
		Size: 191.9 MB (191924678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bb53f0d0415a3a233710f20352eed166af27bd439de5d8732f264e58cddf03`  
		Last Modified: Tue, 01 Feb 2022 22:28:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fa4cc926b9508d06cdee029f2041c627201e4012577563ac45e52c25d2e69d`  
		Last Modified: Wed, 02 Feb 2022 01:50:53 GMT  
		Size: 2.4 MB (2378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38830b435de09ba12d8a774d24f93ea69f06e4e4887a8415a841b46403073a92`  
		Last Modified: Wed, 02 Feb 2022 01:50:54 GMT  
		Size: 9.1 MB (9109820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f52e01dfd875d8f10d91761035eb97598c45b6fb0c70be108f3d9ef26b14649`  
		Last Modified: Wed, 02 Feb 2022 01:50:53 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85872780b33f27b5a716d070ec0a431f1eaa598ea6092c7e760c5c9d9c818a2`  
		Last Modified: Wed, 02 Feb 2022 01:50:53 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
