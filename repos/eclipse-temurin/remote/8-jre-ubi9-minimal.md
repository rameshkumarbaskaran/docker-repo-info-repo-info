## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:abe00c82f10f60fc304e43da2c3b814b0f7334754d980ca1cb5811126dc9179e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7b1228b1eb8ccef69cb3467fdff04a4d3c8fe18bf98d4bbd1960d45bda40466a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107566555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58acdf7d5719070d54fa8642ffa7d3a3100489259201b9234657f01727012e08`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Oct 2023 11:43:37 GMT
ADD file:139424fc60c0a17394da68faf4af3a17c9e959b6a1ce74c5b53ffc959145a63c in / 
# Wed, 18 Oct 2023 11:43:38 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 11:43:38 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 11:43:38 GMT
ADD multi:eed63f5f84efa377cb20d8bc2a3294d6aeffff59ee5380d49f1903b9673516dd in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 11:43:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Oct 2023 11:43:38 GMT
ENV container oci
# Wed, 18 Oct 2023 11:43:38 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 11:43:38 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 11:43:38 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 11:43:39 GMT
ADD file:d4e564939c7991d70e1c5392b02502c604ec36a1612a39fc922b8bb32a567932 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697625013.json 
# Wed, 18 Oct 2023 11:43:39 GMT
ADD file:7aa78ccab5aa351a2b340ceba6ac1dad0988268ffec2b6ff113734e516c775f9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697625013 
# Wed, 18 Oct 2023 11:43:39 GMT
LABEL "release"="750.1697625013" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:30:28" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697625013"
# Wed, 18 Oct 2023 11:43:39 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460177-f3ccb.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 18 Oct 2023 11:43:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 11:43:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 20 Oct 2023 00:05:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Oct 2023 00:05:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 00:05:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Oct 2023 00:05:43 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 20 Oct 2023 00:05:43 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Fri, 20 Oct 2023 00:06:06 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 20 Oct 2023 00:06:06 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 20 Oct 2023 00:06:07 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 20 Oct 2023 00:06:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2f5211d9dccf1de31345273282bf9a4f2a32341a7352b0435155277e54fc0cd1`  
		Last Modified: Thu, 19 Oct 2023 00:06:30 GMT  
		Size: 37.9 MB (37862118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a98b43dfb187483b2114c8d13929702f6916016006977eacf725a272cc9e0c`  
		Last Modified: Fri, 20 Oct 2023 00:09:11 GMT  
		Size: 27.9 MB (27858517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a962418a3acd566fafaf096fc5ecb70645167b686ef1b8f2d7c0a69202e91f30`  
		Last Modified: Fri, 20 Oct 2023 00:09:33 GMT  
		Size: 41.8 MB (41845049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07e3368e7b8347cab832b5d2808281d30a00a56e5ea6d7960842f565d603882`  
		Last Modified: Fri, 20 Oct 2023 00:09:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f723a7567e526529c47878481ddde7fbc1bd42ef557420a8fd3776ef9e1cb32`  
		Last Modified: Fri, 20 Oct 2023 00:09:28 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5598b985112bcc1e78e8297fb6d0badb53d90670edede233b06e9515cdf074a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105269198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0ca9191ab241a0c6c05a2c52103d2bedb866b4ed52ebdf2e3e8bf64c9bc5f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Oct 2023 11:43:35 GMT
ADD file:e691ccb76303edd2d82b816fda94f210ce903198b687214308ff27960f8efe7e in / 
# Wed, 18 Oct 2023 11:43:36 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 11:43:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 11:43:36 GMT
ADD multi:eed63f5f84efa377cb20d8bc2a3294d6aeffff59ee5380d49f1903b9673516dd in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 11:43:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Oct 2023 11:43:36 GMT
ENV container oci
# Wed, 18 Oct 2023 11:43:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 11:43:36 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 11:43:37 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 11:43:37 GMT
ADD file:4a13e96a4ab8bba5cc4ea503ebfefc7c94cec53a788f71e4c40f2e83ae23331e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697625013.json 
# Wed, 18 Oct 2023 11:43:37 GMT
ADD file:07283ec4d328adf575cda694a931e0281866cd74c6c9a6fde161775cb6be8ddb in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697625013 
# Wed, 18 Oct 2023 11:43:37 GMT
LABEL "release"="750.1697625013" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:30:28" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697625013"
# Wed, 18 Oct 2023 11:43:39 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460177-f3ccb.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 18 Oct 2023 11:43:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 11:43:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 20 Oct 2023 02:32:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Oct 2023 02:32:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 02:32:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Oct 2023 02:32:28 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 20 Oct 2023 02:32:29 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Fri, 20 Oct 2023 02:32:44 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 20 Oct 2023 02:32:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 20 Oct 2023 02:32:45 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 20 Oct 2023 02:32:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:472e9d218c02b84dcd7425232d8b1ac2928602de2de0efc01a7360d1d42bf2f6`  
		Last Modified: Thu, 19 Oct 2023 00:06:36 GMT  
		Size: 36.1 MB (36135743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24095761af408af8cb073e45179789c7c6aad05c8b2aea1d531b47efa3abc5c`  
		Last Modified: Fri, 20 Oct 2023 02:35:14 GMT  
		Size: 28.3 MB (28288942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7e91061764cd08be44464290337b6f878e080fd69c2c75214f13f58bc9861f`  
		Last Modified: Fri, 20 Oct 2023 02:35:37 GMT  
		Size: 40.8 MB (40843641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa15500101894c7d7b5bd8dfa543e3bf05e98ea733cd63580966d2e2f17b02b1`  
		Last Modified: Fri, 20 Oct 2023 02:35:33 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa295ac84e111c8b2e067534e3c48128b130a24b83ce8d72f17f23805a3593e2`  
		Last Modified: Fri, 20 Oct 2023 02:35:33 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bfdee1e59a908f94fe6eddf51f0802681c94f3d0dc7961afd282d49d656583a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113924315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698be456f6c62b02d962381cfbaf125867dc75f0e0974d3fca3d1948399ed8ee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 18 Oct 2023 11:43:39 GMT
ADD file:38ff720f4bd0542e52135d7ca8462094c1d1a25eb1abf1c9ca6eb62629b8fa8b in / 
# Wed, 18 Oct 2023 11:43:41 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 11:43:41 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 11:43:41 GMT
ADD multi:eed63f5f84efa377cb20d8bc2a3294d6aeffff59ee5380d49f1903b9673516dd in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 11:43:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 18 Oct 2023 11:43:41 GMT
ENV container oci
# Wed, 18 Oct 2023 11:43:41 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 11:43:41 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 11:43:42 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 11:43:43 GMT
ADD file:51bb6dd1dd93dba3254f6fc74f978bac7f55ca7d4182a71200a400302bb24286 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697625013.json 
# Wed, 18 Oct 2023 11:43:43 GMT
ADD file:8f43dd15756179218863800cd8e3e9eaf62665a86818b2b3df7d986f62a788db in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697625013 
# Wed, 18 Oct 2023 11:43:43 GMT
LABEL "release"="750.1697625013" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:30:28" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697625013"
# Wed, 18 Oct 2023 11:43:44 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460177-f3ccb.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 18 Oct 2023 11:43:46 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 11:43:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 20 Oct 2023 01:46:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Oct 2023 01:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 01:46:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Oct 2023 01:47:03 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 20 Oct 2023 01:47:05 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Fri, 20 Oct 2023 01:47:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 20 Oct 2023 01:47:40 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 20 Oct 2023 01:47:40 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 20 Oct 2023 01:47:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:56c49f9b2030400a6f12e76696bcf5a933a6bc310009c4f802ef70e51862c56a`  
		Last Modified: Thu, 19 Oct 2023 00:06:44 GMT  
		Size: 42.3 MB (42278290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed9e33ca5bf9d902656621c847347568f67c029655a664eb8cdf54def7fbe8c`  
		Last Modified: Fri, 20 Oct 2023 01:50:02 GMT  
		Size: 30.4 MB (30419048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40d3bbba88396158e9d82172bcae6e5fd6128dcbfca619d2e28901c2e7fa08`  
		Last Modified: Fri, 20 Oct 2023 01:50:26 GMT  
		Size: 41.2 MB (41226106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cd54aed0b9964856a6b387fc2856125f114bba75ad426672c7f852a50d7d0`  
		Last Modified: Fri, 20 Oct 2023 01:50:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d81a55c438f371a545cefd73c5696bc5b8d95f9b546e7a2469c14a36d63b0`  
		Last Modified: Fri, 20 Oct 2023 01:50:21 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
