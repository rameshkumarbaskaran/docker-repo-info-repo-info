## `eclipse-temurin:19-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:2769a69eebfe8d3a486462d03889a621e3d2754dcc07bfb07912489d6d9286fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9e4d213443f0284c187d7eb85a759b5f387fc9929b0d3d480ce0c054f94a76e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116235825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86001c73753bab0ff917babdd10c4e73ce636aab051ae421c33edc94e48907bb`
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
# Tue, 29 Nov 2022 20:23:39 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 29 Nov 2022 20:24:26 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c69ffc5474be076b200e8cc72417b838e4f830b36603d593fb8ca6d11b81969b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c5f3d67edfa0d9b5ec935f944c177c0ee4b2d7a2b5846feaf187b77e954f4242';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6293529eba7872b47dfaa1ccfd321661720d538d22a0abfe53259d61f348d070';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='68cae46c973e48ca6777cd0026bbf25f3457bd3d6730c36bd79d4f3b398c8338';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:24:26 GMT
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
	-	`sha256:c46380d8b0360706bc5606c5fd9265183ff24fbd607dec37be63e17c109c5288`  
		Last Modified: Tue, 29 Nov 2022 20:31:58 GMT  
		Size: 49.4 MB (49445857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a604ddefee88fe5e91195f9ee997ff7e703f837aeca8bb58b490184a0ece43f5`  
		Last Modified: Tue, 29 Nov 2022 20:31:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:85568f699e98e3b47d40cb3807cf384bc8408a515f0aa2cc0725257dd08794f6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114357438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e0f066647e1ed347c80e0f422e6199c624ab8e178bce33aefebde6d7597018`
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
# Tue, 29 Nov 2022 20:42:02 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 29 Nov 2022 20:42:31 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c69ffc5474be076b200e8cc72417b838e4f830b36603d593fb8ca6d11b81969b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c5f3d67edfa0d9b5ec935f944c177c0ee4b2d7a2b5846feaf187b77e954f4242';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6293529eba7872b47dfaa1ccfd321661720d538d22a0abfe53259d61f348d070';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='68cae46c973e48ca6777cd0026bbf25f3457bd3d6730c36bd79d4f3b398c8338';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:42:33 GMT
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
	-	`sha256:6c65c84796f5c6a9fde32cae76c1ada6f37ad41aa4d039f280359999e00a114a`  
		Last Modified: Tue, 29 Nov 2022 20:46:55 GMT  
		Size: 48.9 MB (48896874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de85180be0165d0ee9b8ead5894513de6af654c528bcd04bbdf0594036b9d7a`  
		Last Modified: Tue, 29 Nov 2022 20:46:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6de36748994972d18de24e6c9dcfbd007d8b560020bf9bcdf7efc165e6be86c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121708698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278f3e194d09577c5369a04ca6cb2e3affd30837abd97dff3624103676d44789`
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
# Tue, 29 Nov 2022 20:21:40 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 29 Nov 2022 20:22:45 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c69ffc5474be076b200e8cc72417b838e4f830b36603d593fb8ca6d11b81969b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c5f3d67edfa0d9b5ec935f944c177c0ee4b2d7a2b5846feaf187b77e954f4242';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6293529eba7872b47dfaa1ccfd321661720d538d22a0abfe53259d61f348d070';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='68cae46c973e48ca6777cd0026bbf25f3457bd3d6730c36bd79d4f3b398c8338';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:22:48 GMT
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
	-	`sha256:493bc0232d1cc1631c6ce0c4b2102e06446d6a34c24b18d12c88e5ca31c201b2`  
		Last Modified: Tue, 29 Nov 2022 20:30:36 GMT  
		Size: 49.2 MB (49193893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3adad6d23301a19163bbe2db9a912b4edb5abad1f1174ba6d96db4b8ee2add4`  
		Last Modified: Tue, 29 Nov 2022 20:30:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5f24e81e564c453c833f1506c326ed48363474d59d14677110b43c56caa283b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117059096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646d73cfdd4987f5ba17bc7d3549dd1b6ec86a7db336fb232f75cc28252c1dce`
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
# Tue, 29 Nov 2022 20:46:40 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Tue, 29 Nov 2022 20:47:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c69ffc5474be076b200e8cc72417b838e4f830b36603d593fb8ca6d11b81969b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='c5f3d67edfa0d9b5ec935f944c177c0ee4b2d7a2b5846feaf187b77e954f4242';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6293529eba7872b47dfaa1ccfd321661720d538d22a0abfe53259d61f348d070';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='68cae46c973e48ca6777cd0026bbf25f3457bd3d6730c36bd79d4f3b398c8338';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:48:04 GMT
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
	-	`sha256:f5d495acfeb47b4ffb8fcb555a08371bcc767b50b2d3f9a4438292c53d4334e9`  
		Last Modified: Tue, 29 Nov 2022 20:52:26 GMT  
		Size: 46.0 MB (46026804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aaa8a499460b86639d9d0b4b2b4e58508a6bb1d110f6e6a4250b3e79925384`  
		Last Modified: Tue, 29 Nov 2022 20:52:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
