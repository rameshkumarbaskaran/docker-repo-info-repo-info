## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:448f3f81431f55f8e444b53a64a49ea0d49539622e3434a3242e1e39be310825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:585743331e569ee5bf2d827dcfd8a768b1eb57b009059331bbef35a8e1021197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109434766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c19fe5dd7ff36a01ee77d33e33d43123e2977f16bc0223bb62fe96bcc90568`
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
# Wed, 10 May 2023 01:18:06 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 01:18:27 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:18:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:b6395e8df5958febf59e6fc41c12a64b60c642705c5f4ad8f592798a2674f45f`  
		Last Modified: Wed, 10 May 2023 01:21:15 GMT  
		Size: 43.7 MB (43688523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f35ce5921a98136fc63764fbbb54641759370d58280b7e246b8522d61940e0c`  
		Last Modified: Wed, 10 May 2023 01:21:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:24fefba831daa63e3621af576ed97bb0519ba61703d3e4379c024e42001d982f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106524072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e03644a6a4c98f9971b8b28a78b34f363cd7a7b8937f95250f354ef998f302`
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
# Wed, 10 May 2023 01:11:44 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 01:12:09 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:12:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:746088d6760eb9aeb1b455efd63a5227fcb901bcada389d19c51923f353e59ee`  
		Last Modified: Wed, 10 May 2023 01:14:37 GMT  
		Size: 42.0 MB (42031889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fab8cffe96d612a4478d6fa4ba56ecc9ad7bc356c61e36a4cd171e627d126c`  
		Last Modified: Wed, 10 May 2023 01:14:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:514fdbb523c722480cd5dfd6e29c9c6c572c96e29588d8e8b58267582d533953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111904987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ea264c3218a400150c74b39f9b437a96d3ff59e6a1e666db94a5b5796ea407`
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
# Wed, 10 May 2023 01:21:09 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 01:21:53 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:21:59 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:2563046e69ff700a18e46ff8bbf746a585edea006e16230d3970c09decfa1279`  
		Last Modified: Wed, 10 May 2023 01:25:11 GMT  
		Size: 39.2 MB (39161740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df74791df0dabee8c063353f1bff91acf857f7696124e67620f10a30f1f25589`  
		Last Modified: Wed, 10 May 2023 01:25:02 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:47b849584ab144f85acad0621c27996ba2bd88a85dab5733e24348efdffe8e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101689096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdff9cf4a3eb25200baa0b4c6f8c37c6695bdc0fa4ed8931906ad96e370ab02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 May 2023 09:08:19 GMT
ADD file:8f6c1f9d98d7cf5a18b3a603321298088334d2f7cb113f98a8b483c80cc59646 in / 
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
# Wed, 03 May 2023 09:08:23 GMT
RUN rm -rf /var/log/*
# Wed, 03 May 2023 09:08:23 GMT
LABEL release=484
# Wed, 03 May 2023 09:08:23 GMT
ADD file:9c2521292f5f4c34ed9a287ea2aad237a400b1f46623134f67dcfe55e36a7e91 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-484.json 
# Wed, 03 May 2023 09:08:24 GMT
ADD file:9ced5deb77fa1275a2c53167e709e9e46ed950a77073905e150c649620c77e53 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-484 
# Wed, 03 May 2023 09:08:24 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-05-03T08:55:50" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-484"
# Wed, 03 May 2023 09:08:25 GMT
RUN rm -f '/etc/yum.repos.d/repo-5b631.repo' '/etc/yum.repos.d/repo-f1088.repo'
# Wed, 03 May 2023 09:08:27 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 May 2023 09:08:28 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 10 May 2023 00:58:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 May 2023 00:58:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 May 2023 00:58:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 May 2023 00:59:19 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 10 May 2023 00:59:20 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Wed, 10 May 2023 00:59:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 00:59:54 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:7ab84bfb6db5dfa36dd3b2072e29fda9eab8e217469790e70893ed32fa7656a1`  
		Last Modified: Tue, 09 May 2023 18:09:52 GMT  
		Size: 36.2 MB (36244555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f098f9ae6a672823c18ca402ee63fefb70d0014d41d2c03f971ab626ddcdf50`  
		Last Modified: Wed, 10 May 2023 01:01:17 GMT  
		Size: 27.9 MB (27917608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405d0d6413a52f2e1c554d3f7a768433497f0f0b2d76aad3d2b4a3076cb0d74f`  
		Last Modified: Wed, 10 May 2023 01:01:37 GMT  
		Size: 37.5 MB (37526773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5e918640e12ac7bc1c41b6e3c5661a8715a7053d592ffc3c37642d8a65046e`  
		Last Modified: Wed, 10 May 2023 01:01:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
