## `tomcat:9-jre17-temurin-jammy`

```console
$ docker pull tomcat@sha256:be7f9c0db1ef8728e514eb68b261307c60c033440df7cb1dd52d2a69c21c0699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre17-temurin-jammy` - linux; amd64

```console
$ docker pull tomcat@sha256:835b8c4018010c52d1be4bfae30ecc2245208cc4858e4e1a9905d27a91d5c97d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109681892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991e593cdd7f3fab2625a95097763c6dd986d2b530dd9ca403e4c056e472dda0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:42:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Jun 2023 01:44:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:35 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 02 Jun 2023 01:45:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Jun 2023 01:45:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sun, 04 Jun 2023 16:54:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 04 Jun 2023 16:54:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 16:54:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 04 Jun 2023 16:54:08 GMT
WORKDIR /usr/local/tomcat
# Sun, 04 Jun 2023 16:54:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:54:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:56:19 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 04 Jun 2023 16:56:19 GMT
ENV TOMCAT_MAJOR=9
# Sun, 04 Jun 2023 16:56:20 GMT
ENV TOMCAT_VERSION=9.0.75
# Sun, 04 Jun 2023 16:56:20 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Sun, 04 Jun 2023 16:56:20 GMT
COPY dir:b53c406b213357f15f933de2a8ed8785146b1482ddb347f32f760fc79ef9f0f8 in /usr/local/tomcat 
# Sun, 04 Jun 2023 16:56:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 16:56:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 04 Jun 2023 16:56:26 GMT
EXPOSE 8080
# Sun, 04 Jun 2023 16:56:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec73b48ae406646223453ca41d5d6b7cb739853fb7a44f15d35a31c238271d2`  
		Last Modified: Fri, 02 Jun 2023 01:48:00 GMT  
		Size: 17.0 MB (17038759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ed7897b25d52aaae312fc658507d20b8c5fdec7de7490dc16c77d3f997950c`  
		Last Modified: Fri, 02 Jun 2023 01:48:30 GMT  
		Size: 47.0 MB (47006223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefea741bc5a48dedcbf20bd5e126d8111185eb4ff00cd2c7b783dcb42bc069d`  
		Last Modified: Fri, 02 Jun 2023 01:48:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83dfa938a5577195515e69d6d30625b1dcabf769779081319e40133354ff6fd`  
		Last Modified: Sun, 04 Jun 2023 17:02:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2043c8b9246e2b4de8d701e820e5097e001a81ea88619e7993843ed1c59184`  
		Last Modified: Sun, 04 Jun 2023 17:05:48 GMT  
		Size: 12.2 MB (12236764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2d7033e6a03fc47da955e6627facd12b4b4b9fe3cad81cafa4c75335211f6`  
		Last Modified: Sun, 04 Jun 2023 17:05:47 GMT  
		Size: 3.0 MB (2969408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3f442b6290cebd6383cdbd7d4fc08b443a53de94c3fd6b5a87f4de9a0a7ce3`  
		Last Modified: Sun, 04 Jun 2023 17:05:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-jammy` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:035b15f059b64a774e1d7883e951b5c74fb99cbf07b9369c8ec1cfbd6eac45b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103399912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731a691b3423b3df1fcc911f7ef3a07daf7d5ba6c3a962e4afdad4ee47bbbae3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:59:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:59:30 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 01 Jun 2023 23:59:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:59:59 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 00:44:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 00:44:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:44:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 00:44:16 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 00:44:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 00:44:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 00:46:33 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 00:46:33 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 00:46:33 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 00:46:33 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 00:46:34 GMT
COPY dir:ac04cfe80a912ae0488e3e592cb38f2eff2cfe37986202e0fe1285cd8a5acfac in /usr/local/tomcat 
# Fri, 02 Jun 2023 00:46:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:46:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 00:46:39 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 00:46:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:493981aec623882c3786c4f3065d2e731f17ed403c7452a2ece9ff96b2b02ac5`  
		Last Modified: Tue, 23 May 2023 02:04:29 GMT  
		Size: 27.0 MB (27026262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931d415221d00249ab02b781a48cdb71506c851c6e0fe1d25a83077d365a69a7`  
		Last Modified: Fri, 02 Jun 2023 00:01:51 GMT  
		Size: 17.2 MB (17169501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9309f58346d0fff03b2c1343109ca7f145133f4352396e29dcdf7ade9eee8f`  
		Last Modified: Fri, 02 Jun 2023 00:02:22 GMT  
		Size: 44.6 MB (44579951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510fe2d58ce481a8b4d01477c6a8983c086f9322d81567c9eb9245fa375c131d`  
		Last Modified: Fri, 02 Jun 2023 00:02:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc8f0e6691601b583b55a059b778115c6e96712d328e807f3cab63b95c4c7c5`  
		Last Modified: Fri, 02 Jun 2023 00:52:27 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd34c8f08710cedb5295a490d351c8d71ed43c44ce788d8379ae9e182a2dee`  
		Last Modified: Fri, 02 Jun 2023 00:55:23 GMT  
		Size: 12.2 MB (12172492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1a5ef16bb97e5617ff564039027ef37e2951eb736d6975f3b143935d3430d8`  
		Last Modified: Fri, 02 Jun 2023 00:55:22 GMT  
		Size: 2.5 MB (2451242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f18fc1599ca350ad9ada53711cbf26bcbe6dd6328c49f93916c2625dc9695e`  
		Last Modified: Fri, 02 Jun 2023 00:55:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-jammy` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:78f666803d2a0c1a34d2bc4e8c924b37a905fef49d5d2c1d81167d70c633af97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108393348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d789e25836f3dc04acc06502245c0b568f664c5d593115369a1df423fb10447`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:19:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:19:48 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 01 Jun 2023 23:20:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:20:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 01:56:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 01:56:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:56:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 01:56:29 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 01:56:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:56:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:58:25 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 01:58:25 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 01:58:25 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 01:58:25 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 01:58:25 GMT
COPY dir:a960ed19880e3f51d9905edca66661afec74bb0f6e554d1c7c17d5a823d7c2cc in /usr/local/tomcat 
# Fri, 02 Jun 2023 01:58:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:58:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 01:58:30 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:58:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3eb20d332dad785127ed3f3e6dcc4b0d15bd0c80eed668d36d238b6c154998a`  
		Last Modified: Thu, 01 Jun 2023 23:22:35 GMT  
		Size: 18.5 MB (18463717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ae267c1b4e59f03e8fff83a395ddb46c6cb48d543a079dec5b2fc9b38a30b`  
		Last Modified: Thu, 01 Jun 2023 23:23:04 GMT  
		Size: 46.5 MB (46488674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b400f0ed15f184ce7b1dd7836ae9fcd85258d93ddab4a6ac6dbdaff191c7f`  
		Last Modified: Thu, 01 Jun 2023 23:22:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4351d51b156020979e2c7c319ad9758d3d8ed99a7b2154ccba03cffce7ca49c`  
		Last Modified: Fri, 02 Jun 2023 02:04:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55d89312e0228471c3fdb40d727d8726b7db6e07051718132d0a956ec9b977`  
		Last Modified: Fri, 02 Jun 2023 02:07:04 GMT  
		Size: 12.2 MB (12242250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808fc78f0165d0bcece6d73c96ecbed22ddf3598ca178a449fab95763e7f6793`  
		Last Modified: Fri, 02 Jun 2023 02:07:03 GMT  
		Size: 2.8 MB (2809198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877f3c242e5cd2092f251a89dd40a332bda2de38bcd3b30d1345343e0ba4745`  
		Last Modified: Fri, 02 Jun 2023 02:07:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-jammy` - linux; ppc64le

```console
$ docker pull tomcat@sha256:589fab9fa1a5c0b7e1bdd07a94a05ab7c65c7218dbf7cdf245f3057d53dce329
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116531234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f2a4448e03671f3ecbbe5b597789e3cc357801293405302e25900666b7431c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:33:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 00:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 00:33:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Jun 2023 00:36:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:36:52 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 02 Jun 2023 00:37:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Jun 2023 00:37:52 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 01:44:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 01:44:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 01:44:32 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 01:44:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:44:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:51:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 01:51:56 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 01:51:57 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 01:51:58 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 01:51:59 GMT
COPY dir:dc9920efd788d8a7ec1cb24042f88ed3ea14900f0ce483e0da017be6809659a8 in /usr/local/tomcat 
# Fri, 02 Jun 2023 01:52:22 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:52:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 01:52:27 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:52:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e39d2517f3d915af1b821fe306b14eba12466c4cae87efe57eaa0b749503166e`  
		Last Modified: Thu, 01 Jun 2023 23:48:51 GMT  
		Size: 35.7 MB (35712704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f659dc007d0950b5839b0b55be3c3b3d4b154ab8052efc8def4eb9ed73ae8f`  
		Last Modified: Fri, 02 Jun 2023 00:40:42 GMT  
		Size: 18.3 MB (18321005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e843fdcfb1f1bdecea7d809c1bd0884edaf135e451bb95b8d76a30e13d9a7c20`  
		Last Modified: Fri, 02 Jun 2023 00:41:26 GMT  
		Size: 46.9 MB (46872508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e4678477f94800be842b93dcfe548abbd4a661ed685193b2f38e91ed0e7003`  
		Last Modified: Fri, 02 Jun 2023 00:41:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494657278e55f734be36935e5e461a2fb275c8019b63fc3ca575f840c1bc798b`  
		Last Modified: Fri, 02 Jun 2023 02:08:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c051b3a801b648643fd49f85d0e469a1aa243c25c8ae34b772d6eacf26d945f`  
		Last Modified: Fri, 02 Jun 2023 02:12:12 GMT  
		Size: 12.3 MB (12266073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8efd1e65b8e1f0611f4b4670806289f9bbad273884dda940695ccb41e492bd1`  
		Last Modified: Fri, 02 Jun 2023 02:12:11 GMT  
		Size: 3.4 MB (3358479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885753a7255271ad2a58796d039d2b2f44bb042ce3995f7226590774d4800445`  
		Last Modified: Fri, 02 Jun 2023 02:12:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-jammy` - linux; s390x

```console
$ docker pull tomcat@sha256:dad739c012496b0c12cb5d1fd78bbb30510d252a0dba54138139f89df6581f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104128328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a60998cedd912e1320d3bf4d36279f6acb4199931cbd4f1aaf2739a0fe3d950`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:33:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:34:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:34:43 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 01 Jun 2023 23:35:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:35:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 15:42:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 15:42:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 15:42:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 15:42:35 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 15:42:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 15:42:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 15:44:41 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 15:44:41 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 15:44:41 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 15:44:42 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 15:44:42 GMT
COPY dir:e683039c8103c8296a09a964d22b489f4e3c2651e6125a5458dbe2b88684b18a in /usr/local/tomcat 
# Fri, 02 Jun 2023 15:44:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 15:44:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 15:44:46 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 15:44:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f2957179c3a13374d05630725d1d996f8083efadf7d2da999c9b4ca53ab7c98f`  
		Last Modified: Thu, 01 Jun 2023 23:19:06 GMT  
		Size: 28.6 MB (28648005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff49023eb8231a4489c04787627471c943342afea6aed42b66e0bd17f75307a`  
		Last Modified: Thu, 01 Jun 2023 23:36:33 GMT  
		Size: 16.8 MB (16817675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58123ce9cafda91814be25f8b9b9f99431886cfbee190fc6ba7f6be9abdfe781`  
		Last Modified: Thu, 01 Jun 2023 23:36:56 GMT  
		Size: 43.8 MB (43774489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c27d78a58220d69494be2a17dffa9c4de667bdcf0f6e85c869482d832b8af8f`  
		Last Modified: Thu, 01 Jun 2023 23:36:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251748c29e534d7003b3ad321ce523fef966d82707f181caf8d83abf95b8f396`  
		Last Modified: Fri, 02 Jun 2023 15:49:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cf3d6b50e6fccbca189bd41b1f49c057cbdf94df1a5ff689639d886a6ff394`  
		Last Modified: Fri, 02 Jun 2023 15:51:00 GMT  
		Size: 12.2 MB (12235555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1f00ca7e022c6ee9988cbca18137f231c70c00c4b28ac62bfd85c8b6232b79`  
		Last Modified: Fri, 02 Jun 2023 15:51:00 GMT  
		Size: 2.7 MB (2652140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0979fc6d435f3465833a7ef493e527a1d869b9aeafe5a93ffaeca64cd180c4a`  
		Last Modified: Fri, 02 Jun 2023 15:51:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
