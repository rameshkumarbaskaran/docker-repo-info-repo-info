## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6f58ce1d6118a2cd96aadc793ccdb369996ec217054d2d5faabeced9c60b8209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4e4c74aba3c781be4374cec62c28d7ac4d4cc6598863ae71bcddcc6029bb6155
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110442428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3179b9a53364feda5b44924437d30b4bd8663c81bc8b70d77ec1e5a30068994c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Nov 2022 10:35:30 GMT
ADD file:8fd6cdf50d42fcadcf7282ea1b0f408a499690f88ffc6c4348229f4bd705def2 in / 
# Mon, 28 Nov 2022 10:35:30 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Mon, 28 Nov 2022 10:35:30 GMT
ADD multi:f1823d64f56fc97d5c6f5f2ef362aa9c6e29575cf09672b66b45e6b3b92ad468 in /etc/yum.repos.d/ 
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Nov 2022 10:35:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Nov 2022 10:35:30 GMT
ENV container oci
# Mon, 28 Nov 2022 10:35:30 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Nov 2022 10:35:30 GMT
CMD ["/bin/bash"]
# Mon, 28 Nov 2022 10:35:31 GMT
RUN rm -rf /var/log/*
# Mon, 28 Nov 2022 10:35:31 GMT
ADD file:73aa3ff7ca5721ae1c0bb742582b71f09005171a7c2d51b6599f35a538d7f2be in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.1669627757.json 
# Mon, 28 Nov 2022 10:35:32 GMT
ADD file:692076e1e7b376cc31dc161a185a16c7bcc99babcc0b16f2f19664c4c832fa5c in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656.1669627757 
# Mon, 28 Nov 2022 10:35:32 GMT
LABEL "release"="1656.1669627757" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-28T09:53:29" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656.1669627757"
# Mon, 28 Nov 2022 10:35:32 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1630805-87970.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Mon, 28 Nov 2022 10:35:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 29 Nov 2022 20:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:20:15 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 29 Nov 2022 20:21:19 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 29 Nov 2022 20:21:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:21:53 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:28b395536b27807883bad9f86c9c44538624f3590ad5446769071b6317890415`  
		Last Modified: Tue, 29 Nov 2022 12:08:27 GMT  
		Size: 37.9 MB (37870404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c65b3a1235edfc700a77e5fa2004e45845e64ab2cd6c50b3fdec6b20f8a8c13`  
		Last Modified: Tue, 29 Nov 2022 20:26:43 GMT  
		Size: 28.9 MB (28919402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59355abcd31cdd468d3ac585bde43dec4e2203d9d89dc97c78a0ff32bb18097d`  
		Last Modified: Tue, 29 Nov 2022 20:29:03 GMT  
		Size: 43.7 MB (43652462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a01447f3116ff6cadbb3654917352a4cb99beee7f9d939f25d733908dc67d5`  
		Last Modified: Tue, 29 Nov 2022 20:28:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2d4973db6d0e85529dd91394c252568378984b9fc983c918e2b94665fdb40179
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107438654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d2fbaec5b1e6aacd6b7c84eb347ad66dbc28aa88c347a4f1374e4761cd7f29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Nov 2022 10:29:05 GMT
ADD file:caa467b557f0a9a857a22d9d78457daea6ff37f301d3de1be9eb69ea8e67e489 in / 
# Mon, 28 Nov 2022 10:29:05 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Mon, 28 Nov 2022 10:29:05 GMT
ADD multi:f1823d64f56fc97d5c6f5f2ef362aa9c6e29575cf09672b66b45e6b3b92ad468 in /etc/yum.repos.d/ 
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Nov 2022 10:29:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Nov 2022 10:29:05 GMT
ENV container oci
# Mon, 28 Nov 2022 10:29:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Nov 2022 10:29:05 GMT
CMD ["/bin/bash"]
# Mon, 28 Nov 2022 10:29:06 GMT
RUN rm -rf /var/log/*
# Mon, 28 Nov 2022 10:29:06 GMT
ADD file:748f162e3057d65d5f7730b81cf0c5add2fddf72ce76add3654df379a961a4a6 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.1669627757.json 
# Mon, 28 Nov 2022 10:29:06 GMT
ADD file:cb830f04b1be3cda717ba0e66b66bbab7ea8951d385a8e8c3d0174e434683c08 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656.1669627757 
# Mon, 28 Nov 2022 10:29:06 GMT
LABEL "release"="1656.1669627757" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-28T09:53:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656.1669627757"
# Mon, 28 Nov 2022 10:29:08 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1630805-87970.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Mon, 28 Nov 2022 10:29:09 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 29 Nov 2022 20:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:39:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:39:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:40:03 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 29 Nov 2022 20:40:38 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 29 Nov 2022 20:41:12 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:41:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5952a7fdd87dcf3c5cd09577bf9208c89283a65b31fcd21e48c5f9e4c9249eaa`  
		Last Modified: Tue, 29 Nov 2022 12:08:38 GMT  
		Size: 36.1 MB (36139198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d01954f03c8ffc1494c867c9720c1bb10748e8b094c3b6b809ae6880c5bd6`  
		Last Modified: Tue, 29 Nov 2022 20:44:24 GMT  
		Size: 29.3 MB (29321204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240ef6c70b5d5711ea08029a066cd2e59ba9ed881a91507c48c482b4d6e44688`  
		Last Modified: Tue, 29 Nov 2022 20:45:30 GMT  
		Size: 42.0 MB (41978090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60ea9c82a9b6a403a0a5373e765fb2560a572edc681c8b9294602af214ad4fc`  
		Last Modified: Tue, 29 Nov 2022 20:45:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0846f98dbbfe67975cdac99b8e208b073422e7025f57307cb291e96df72bb888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111627068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2d9070f27c60b53be8fb6ffdf210f2bc6c8fb7ce26a7a5311a9791faf692a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Nov 2022 10:29:10 GMT
ADD file:afa93e90bc11a4db2c2546375231ced481a9fb41956e8b922609595134fc767f in / 
# Mon, 28 Nov 2022 10:29:11 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Mon, 28 Nov 2022 10:29:11 GMT
ADD multi:f1823d64f56fc97d5c6f5f2ef362aa9c6e29575cf09672b66b45e6b3b92ad468 in /etc/yum.repos.d/ 
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Nov 2022 10:29:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Nov 2022 10:29:11 GMT
ENV container oci
# Mon, 28 Nov 2022 10:29:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Nov 2022 10:29:11 GMT
CMD ["/bin/bash"]
# Mon, 28 Nov 2022 10:29:13 GMT
RUN rm -rf /var/log/*
# Mon, 28 Nov 2022 10:29:13 GMT
ADD file:1060228e95f01a96b380286523e587f3e82dbd41294c18259830b1cf54c97eac in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.1669627757.json 
# Mon, 28 Nov 2022 10:29:14 GMT
ADD file:7b11f324301cf6a07f2dd2f3df3542190f83af5231b9a6cab466b20062fa02ff in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656.1669627757 
# Mon, 28 Nov 2022 10:29:14 GMT
LABEL "release"="1656.1669627757" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-28T09:53:29" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656.1669627757"
# Mon, 28 Nov 2022 10:29:15 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1630805-87970.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Mon, 28 Nov 2022 10:29:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 29 Nov 2022 20:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:17:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:17:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:17:34 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 29 Nov 2022 20:18:46 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 29 Nov 2022 20:19:58 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:20:00 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9b14c9a64724b0ce8870476b334886b2be9565fa963a2a37748531ec70b23e6d`  
		Last Modified: Tue, 29 Nov 2022 12:08:50 GMT  
		Size: 40.8 MB (40845502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a61f571c5ddb57e78327d3bb1f214876d12257d5214f7f4111b25d49f34188`  
		Last Modified: Tue, 29 Nov 2022 20:26:22 GMT  
		Size: 31.7 MB (31669142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3880d876c5ab201a4e93e2fc9de10f144e59e8f2d3b8417e77816b8428687ddc`  
		Last Modified: Tue, 29 Nov 2022 20:28:03 GMT  
		Size: 39.1 MB (39112264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb070ec1166296ddba7a6649f279b88e4e1fd929fb826fd4317a4330e95aaca`  
		Last Modified: Tue, 29 Nov 2022 20:27:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:ab0bcac2771b08cbf06414759d1e7503bc47a90a740040b8cd5ed8533a594eb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108527356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64052c2c9b3f95d567f09daf72c43ecb0a12591aed4cc2e5a387288154eb8b76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Nov 2022 10:29:14 GMT
ADD file:1385207a551a52b8339f894b4c7a9acf7e4ee70add533d97d8953304ca109711 in / 
# Mon, 28 Nov 2022 10:29:15 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Mon, 28 Nov 2022 10:29:15 GMT
ADD multi:f1823d64f56fc97d5c6f5f2ef362aa9c6e29575cf09672b66b45e6b3b92ad468 in /etc/yum.repos.d/ 
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Nov 2022 10:29:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 28 Nov 2022 10:29:15 GMT
ENV container oci
# Mon, 28 Nov 2022 10:29:15 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Nov 2022 10:29:15 GMT
CMD ["/bin/bash"]
# Mon, 28 Nov 2022 10:29:17 GMT
RUN rm -rf /var/log/*
# Mon, 28 Nov 2022 10:29:17 GMT
ADD file:2d234fdb3e989d8833a2e357e35593c1c992605a69ee8fdb1393ebdc62348858 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.1669627757.json 
# Mon, 28 Nov 2022 10:29:17 GMT
ADD file:c9936581fa26002b4b057c960eaab03741109c3ada5bfc0f209702f8a9ca1feb in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656.1669627757 
# Mon, 28 Nov 2022 10:29:17 GMT
LABEL "release"="1656.1669627757" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-28T09:53:29" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656.1669627757"
# Mon, 28 Nov 2022 10:29:19 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1630805-87970.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Mon, 28 Nov 2022 10:29:21 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 29 Nov 2022 20:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:42:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:42:45 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 29 Nov 2022 20:42:52 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 29 Nov 2022 20:44:09 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='bd6efe3290c8b5a42f695a55a26f3e3c9c284288574879d4b7089f31f5114177';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='0ca3d806131ab5834c501f9c625bb0248cd528af361c704503348e9c9605bedf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='dd3b159a374086e65cb07c4ccb226c90f9c02ef929cba6f0b642171d7ed97fa4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='752616097e09d7f60a3ad8bd312f90eaf50ac72577e55df229fe6e8091148f79';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:44:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:c4ed058fa577681c9207ce4a8affcf97033389750eb02da986f565163eb6c22e`  
		Last Modified: Tue, 29 Nov 2022 12:09:04 GMT  
		Size: 36.2 MB (36165323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d493010bec22be4186e31998c908ce86bcd75b934e50295afcbd116e064fa732`  
		Last Modified: Tue, 29 Nov 2022 20:50:30 GMT  
		Size: 34.9 MB (34866810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534b51a2097be72586b7dd70dc87f2e3dc1aba7be3479858fefecad59f4f8ef3`  
		Last Modified: Tue, 29 Nov 2022 20:50:54 GMT  
		Size: 37.5 MB (37495063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808d53351b34b493a546e313e8f675cba458069cd82d05115f26b92e4ffbd05f`  
		Last Modified: Tue, 29 Nov 2022 20:50:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
