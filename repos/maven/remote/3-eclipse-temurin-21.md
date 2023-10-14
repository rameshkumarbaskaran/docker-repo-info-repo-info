## `maven:3-eclipse-temurin-21`

```console
$ docker pull maven@sha256:1dec2264ec3b7b0939d5f332ef0ea9e39e082a8acce7c18c78f77012a59e4813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-21` - linux; amd64

```console
$ docker pull maven@sha256:7357a177f1690195d3a7b2b7c09a66833217d8b9dae8f9e66d70ed6aa3275717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234895635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb1d31e5bc605bfaaf399932afb7c53638f41deb7ef42d2e277319588e63184`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 05:51:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 05:51:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 05:51:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 05:53:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:54:38 GMT
ENV JAVA_VERSION=jdk-21+35
# Fri, 13 Oct 2023 05:54:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='33e440c237438aa2e3866d84ead8d4e00dc0992d98d9fd0ee2fe48192f2dbc4b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='82f64c53acaa045370d6762ebd7441b74e6fda14b464d54d1ff8ca941ec069e6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 05:54:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 05:54:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 05:54:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Oct 2023 05:54:50 GMT
CMD ["jshell"]
# Fri, 13 Oct 2023 18:45:01 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Oct 2023 18:45:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Oct 2023 18:45:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 13 Oct 2023 18:45:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 13 Oct 2023 18:45:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 13 Oct 2023 18:45:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 13 Oct 2023 18:45:01 GMT
ARG MAVEN_VERSION=3.9.4
# Fri, 13 Oct 2023 18:45:01 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Oct 2023 18:45:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Oct 2023 18:45:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Oct 2023 18:45:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50431c77a77b7f46c78e4929a36d42dcb3551c22e0404d2bee6e8a15cc650640`  
		Last Modified: Fri, 13 Oct 2023 05:59:21 GMT  
		Size: 17.5 MB (17454843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e07be1056944b456e6ae4c431838842cdff25e6667df2885e729aff6c8b5107`  
		Last Modified: Fri, 13 Oct 2023 06:00:42 GMT  
		Size: 158.6 MB (158598847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a4e81ff64592dc35a6b44699633daf9e06dee439e1b2203c9b2d5a843e6680`  
		Last Modified: Fri, 13 Oct 2023 06:00:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756161029e803bc7a96348ebd32dc72ec6b7bc3f378de0a3b88a3b8f5ea05bcd`  
		Last Modified: Fri, 13 Oct 2023 06:00:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e687d9cf8d67bf15f98c3490a89e379e83c1f9f99883a15bdcaf9b6aef41e7`  
		Last Modified: Sat, 14 Oct 2023 01:22:43 GMT  
		Size: 19.0 MB (18994135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15d0d8fed9ca5bba99d7cdd75acd2a39b9be2213c8b5e1d91a7671c0b5b2e0f`  
		Last Modified: Sat, 14 Oct 2023 01:22:41 GMT  
		Size: 9.4 MB (9406422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8393816e1541353a696c0e4358c161fd02ab1bf41a457c5540990a601bf28`  
		Last Modified: Sat, 14 Oct 2023 01:22:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284308e75ea9a0da2bccfe24bea420d13768b7bde107b9e0a3619815827c81af`  
		Last Modified: Sat, 14 Oct 2023 01:22:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd9fb66ee71976be54a6f257ea6d25bf9e67bdbac211e315831f4674d75744`  
		Last Modified: Sat, 14 Oct 2023 01:22:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
