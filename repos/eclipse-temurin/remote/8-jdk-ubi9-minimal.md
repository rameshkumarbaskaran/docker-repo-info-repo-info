## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a2ed697038ec088df17a77bb9a4ee79ba459726fb4a08837d651654c88856666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:60f8e316c9f6706e0821d2097a0ce9e8e96276bfab72e139870820e0cde25f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120388579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9514eba628464c561da968c7a38d6849dfe8725603cbcd5a107467abfc8442f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 May 2023 09:08:14 GMT
ADD file:1dd09d13cf92c39f4a00e8bd8b2454fcc670168bf12b904a0ed35fd620636966 in / 
# Wed, 03 May 2023 09:08:14 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 09:08:14 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 09:08:15 GMT
ADD multi:b9f1efa6d4eb264a2ccbb760b4589e8b42e4ef0554a87cf7fab6ba883b0df687 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 09:08:15 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 09:08:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 03 May 2023 09:08:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 09:08:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 May 2023 09:08:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 May 2023 09:08:15 GMT
ENV container oci
# Wed, 03 May 2023 09:08:15 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 09:08:15 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 09:08:15 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 09:08:15 GMT
LABEL release=484
# Wed, 03 May 2023 09:08:15 GMT
ADD file:97e6d44cd73a1cd3019b47e4290eec69d0892ec31df6cdec5164cc966aeaad00 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-484.json 
# Wed, 03 May 2023 09:08:16 GMT
ADD file:4fc80951d1835450df30cf06475145109b1dabb433c2017b5cceb6e12e97be86 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-484 
# Wed, 03 May 2023 09:08:16 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T08:55:50" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-484"
# Wed, 03 May 2023 09:08:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-5b631.repo' '/etc/yum.repos.d/repo-f1088.repo'
# Wed, 03 May 2023 09:08:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 09:08:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 10 May 2023 01:17:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 May 2023 01:17:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 May 2023 01:17:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 May 2023 01:17:37 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 10 May 2023 01:17:37 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Wed, 10 May 2023 01:17:42 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:17:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a9f076b473b10f92470b5c7fe238962e80f6eedd374d74105fcfad39afb4f699`  
		Last Modified: Tue, 09 May 2023 18:09:18 GMT  
		Size: 37.9 MB (37882347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec7cccb5a3f6e76c2bb4335ad738d4f6ff59913b03c6d47ba7bf7855cdb5224`  
		Last Modified: Wed, 10 May 2023 01:20:13 GMT  
		Size: 27.9 MB (27863734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bf598b8a68cf35c805c202275e3b6bad0171aaae38f345268747046dca07f0`  
		Last Modified: Wed, 10 May 2023 01:20:15 GMT  
		Size: 54.6 MB (54642339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b4d4a800966a73839b93aba6facb42c8f9cf22551ae2e52374314b7943de64`  
		Last Modified: Wed, 10 May 2023 01:20:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:18849510b1b48a25d6a683ef25e2db30bd8046d585af52f161dd6d0a2e2a0f3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118235111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8784eb8beef143601cd5a219b843783906623edf84cc0a580f59ec90e1b7a94b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 May 2023 09:08:14 GMT
ADD file:4be34f167a8d152eb1c269f3acbcc7ef9acca742971e5487e418a12b7dc2ac99 in / 
# Wed, 03 May 2023 09:08:15 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 09:08:15 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 09:08:15 GMT
ADD multi:b9f1efa6d4eb264a2ccbb760b4589e8b42e4ef0554a87cf7fab6ba883b0df687 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 09:08:15 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 09:08:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 03 May 2023 09:08:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 09:08:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 May 2023 09:08:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 09:08:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 May 2023 09:08:15 GMT
ENV container oci
# Wed, 03 May 2023 09:08:15 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 09:08:15 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 09:08:16 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 09:08:16 GMT
LABEL release=484
# Wed, 03 May 2023 09:08:17 GMT
ADD file:961390d2717d39a95a230aede6672e618a2f4a42d6008ca0eb6e020beaef23a9 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-484.json 
# Wed, 03 May 2023 09:08:17 GMT
ADD file:31cc2312708cc9d767aec9d39192f74d4cd3eacd247b92131f2465f3cc568578 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-484 
# Wed, 03 May 2023 09:08:17 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T08:55:50" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-484"
# Wed, 03 May 2023 09:08:18 GMT
RUN rm -f '/etc/yum.repos.d/repo-5b631.repo' '/etc/yum.repos.d/repo-f1088.repo'
# Wed, 03 May 2023 09:08:19 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 09:08:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 10 May 2023 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 May 2023 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 May 2023 01:11:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 May 2023 01:11:23 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 10 May 2023 01:11:24 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Wed, 10 May 2023 01:11:29 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:11:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:b81bd7d46297303ebca20e322b800dc4c838f5162f122690015340d5dfa5b5dd`  
		Last Modified: Tue, 09 May 2023 18:09:32 GMT  
		Size: 36.2 MB (36201832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb186e1854dee70909788c166791dd6c0e64f6a7c27d3761e21f4e9e44f774c4`  
		Last Modified: Wed, 10 May 2023 01:13:42 GMT  
		Size: 28.3 MB (28290191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a693c806fdcf815af0c69f05c11dc6828279ab415f7104dc7f0983d0fdf3f541`  
		Last Modified: Wed, 10 May 2023 01:13:44 GMT  
		Size: 53.7 MB (53742928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cba24b770b46d45756483d023b8d2e75a2f93ae86266a8e1ec5ddd312d1963e`  
		Last Modified: Wed, 10 May 2023 01:13:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:75724a2be39b2bbc2f60d0800d979e571bfa8e5e92b8399230587f2fba4844c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124876850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db82b694da71fa45718ae489acff2c82393ab7c44d0e0e587f5953cdf8e8f2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 May 2023 09:08:18 GMT
ADD file:45c337b0ba6935c93f70f84a0f904ba0319f6858175dbbaf1285aa846df88282 in / 
# Wed, 03 May 2023 09:08:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 May 2023 09:08:20 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 03 May 2023 09:08:21 GMT
ADD multi:b9f1efa6d4eb264a2ccbb760b4589e8b42e4ef0554a87cf7fab6ba883b0df687 in /etc/yum.repos.d/ 
# Wed, 03 May 2023 09:08:21 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 May 2023 09:08:21 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 03 May 2023 09:08:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 May 2023 09:08:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 May 2023 09:08:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 May 2023 09:08:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 May 2023 09:08:21 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 May 2023 09:08:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 May 2023 09:08:21 GMT
ENV container oci
# Wed, 03 May 2023 09:08:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 09:08:21 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 09:08:22 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 09:08:22 GMT
LABEL release=484
# Wed, 03 May 2023 09:08:23 GMT
ADD file:6936919424b14671b64c3c4ccb79fe3e1f20fee22f943b446c6adbcbbd5a2559 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-484.json 
# Wed, 03 May 2023 09:08:23 GMT
ADD file:c44377c0b01c07d8a7864619996382992a6363676985aef28324c01493f5caca in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-484 
# Wed, 03 May 2023 09:08:23 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T08:55:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-484"
# Wed, 03 May 2023 09:08:25 GMT
RUN rm -f '/etc/yum.repos.d/repo-5b631.repo' '/etc/yum.repos.d/repo-f1088.repo'
# Wed, 03 May 2023 09:08:27 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 09:08:29 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 10 May 2023 01:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 May 2023 01:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 May 2023 01:19:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 May 2023 01:20:25 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 10 May 2023 01:20:27 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Wed, 10 May 2023 01:20:37 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:20:40 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5584a52281efb9b8fe4e87d9b1bc5d28b7381c9925759f785eeb08104d364d6a`  
		Last Modified: Tue, 09 May 2023 18:09:44 GMT  
		Size: 42.3 MB (42328666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbe54fcabf956a5ec5603c8548be288b8a247595c5c35095e8ed0a77f9ad5`  
		Last Modified: Wed, 10 May 2023 01:23:51 GMT  
		Size: 30.4 MB (30414419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509bce47fd27b8d724ab73144d7f968a8499e4b9e4af1b8716a809b821c9b8ca`  
		Last Modified: Wed, 10 May 2023 01:23:54 GMT  
		Size: 52.1 MB (52133603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce46170d11e2c535a9830a9a07a3b31196a7d982e88a2e4e29d7582161bfb116`  
		Last Modified: Wed, 10 May 2023 01:23:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
