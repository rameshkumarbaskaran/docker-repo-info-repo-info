## `eclipse-temurin:8-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1219b0a1a9eb15f5658009aa584356b79fcde0cfb2e383236c08f5711462fbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ddd9399daee4f44d365da77f573803ec67477df8fb74f3eb9ec449cb5354ca9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170320901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603bfa1e85be36808ef96fd1618698a1a9b11859cea1b524596fc2280e7064a2`
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
# Tue, 29 Nov 2022 20:20:16 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 29 Nov 2022 20:20:28 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:20:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:0db8ecff37bd618bfde92e3808a32f15cc447e67c8b50517cc40363579a21419`  
		Last Modified: Tue, 29 Nov 2022 20:26:48 GMT  
		Size: 103.5 MB (103530934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c4414e9ba0495e7f928d72146e56cf2f37fd9c9a62a44500f84bb0a15aebed`  
		Last Modified: Tue, 29 Nov 2022 20:26:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9fc61519784a6f0fe64b87585e11842a6b0c708ddc58c47b593f0af3c130a3b6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168087475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275d9e197a3c73c84ad75614ca1bb12c0cb8fa0e36e96992fbd2e00499e3da36`
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
# Tue, 29 Nov 2022 20:40:03 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 29 Nov 2022 20:40:13 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:40:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:227c9c4bbde19ac43a22e0d7c249e5c6f8d6d1296a8b4f27e56d7d09c8d742c5`  
		Last Modified: Tue, 29 Nov 2022 20:44:28 GMT  
		Size: 102.6 MB (102626914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490ac57f3e547759cb2576fa218477c95946c6f8c5957fce2f968ef3277614e0`  
		Last Modified: Tue, 29 Nov 2022 20:44:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4fb0923592320b7ffae700c44e206a6041e35cebaaa2379faef1a5950872275a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173543751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8e35e6ff6fd4bc95a9c1fbe9cba72ac361404ab94ef45c77428fc9b7b3667d`
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
# Tue, 29 Nov 2022 20:17:36 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 29 Nov 2022 20:17:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:17:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:05bbd3162c9a317157a890507220678428fd89d6d54c4d0e7c6a85e17eea6a88`  
		Last Modified: Tue, 29 Nov 2022 20:26:28 GMT  
		Size: 101.0 MB (101028947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cf73fd279eeef27c59cf14073949046e38a5417b5ab03551ae9793562dee2f`  
		Last Modified: Tue, 29 Nov 2022 20:26:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
