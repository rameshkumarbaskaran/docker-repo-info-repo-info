## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0fee08624f3c0283352bbce34edeea9e7c7b1e357e0db460fc595fdc52888c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:aef911e0bd33ed933b5de0867645dc68c66162e9dc0fedb508e07641883cecc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107552936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b233aa2cd390ea1e6f0750eb53a4ea32a8266dcf57b11822ae1437184a1903`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:2ff77282831ead8e1be2de9fcd07643f64492c64c71ed11f341e24f7332bd2a2 in / 
# Thu, 05 Oct 2023 14:38:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:58 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:58 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:58 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:38:58 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:38:58 GMT
ADD file:d69168032ac0af2ccddca7f0231c9160dfbc90a3f409177789bef1a6f93385f4 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:38:59 GMT
ADD file:8f0d5eacbb4a0d1c410cd94f86add6634846747273665c2ed843c128a3143840 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:38:59 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:39:00 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:49:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:49:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:49:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:49:26 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 10 Oct 2023 23:49:26 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 10 Oct 2023 23:49:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:49:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:49:49 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:49:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:516f7562f02267e05bc0f8b175363c70768471b977360d0f0ab5711a8a6d25ab`  
		Last Modified: Mon, 09 Oct 2023 09:57:09 GMT  
		Size: 37.8 MB (37848606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef34923412e703897363f1815dcc18d27c28eeafb818489cc210e1bb161c24`  
		Last Modified: Tue, 10 Oct 2023 23:52:57 GMT  
		Size: 27.9 MB (27858409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b046a1fabd1527fb69417a007f5293e254d8210d2b4d59cc70a56a0c6182cd19`  
		Last Modified: Tue, 10 Oct 2023 23:53:21 GMT  
		Size: 41.8 MB (41845051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05d92ac0a61bba2532c27547d80cd7d04ca80d2c3f3228067e59d243ef16c0`  
		Last Modified: Tue, 10 Oct 2023 23:53:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b7a71b9cdcab05ba2aed1fa5db48959004eb894dfd02a1dba3ac6a9d7bc0b`  
		Last Modified: Tue, 10 Oct 2023 23:53:16 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c4381e693fe7afda899c3f1d0fd167a12950ba31a53b39a84cd99d846d3abec5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105263698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5288ea905b3d47c8474f137aebe2287bec350b56a1867f739959566bbcc25269`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:54 GMT
ADD file:7a7d8fbf25992fd7276405ef49134834de1383be75681df1b04b4bcea089f511 in / 
# Thu, 05 Oct 2023 14:38:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:56 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:56 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:56 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:56 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:38:57 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:94efb4b1ab694ac83e1684e40584630e5704b83a70e136a93ecb2f97d83b276f in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:38:57 GMT
ADD file:5465d3cdb7730b7414c1833b9e5b836537236bbd6286f2bc7d43b9d5a125ab84 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:38:57 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:38:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:38:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:50:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:50:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:51:02 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 10 Oct 2023 23:51:03 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 10 Oct 2023 23:51:20 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:51:20 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:51:21 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:51:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4d01da1f57912d023cd75f254ad72c2683a95673c84d2dbd6a594fa4051e23c1`  
		Last Modified: Mon, 09 Oct 2023 12:07:27 GMT  
		Size: 36.1 MB (36134632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcc7cef3ec071bb58b1d161769efc4edc00bc85348312499035de02c7175867`  
		Last Modified: Tue, 10 Oct 2023 23:53:49 GMT  
		Size: 28.3 MB (28284554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4357bc582be182f5de9ab1e0b8cd22f94405178058b3a5e9bc8aca90477be9`  
		Last Modified: Tue, 10 Oct 2023 23:54:09 GMT  
		Size: 40.8 MB (40843641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c29791a151e8918198ca96bd0d251e0de861c204571e486a8fecf42186a4b4`  
		Last Modified: Tue, 10 Oct 2023 23:54:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ff131c2564f69b14c0c50abb4e51556b93791b80ad28c7506dec343981aad0`  
		Last Modified: Tue, 10 Oct 2023 23:54:06 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e85dd784bf0fe2ea72530d1d669220946f8a14d6f1c1e9e40f26a83201a34b7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113959510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab53f121d0393d81151d4a675fea3243d9fefc4b91177e0e617a293b0d18e5c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:58 GMT
ADD file:6d1fa1dd4f82effa3edd3df36cb6be0e361553a9a4ceb44387ec3c39709e1113 in / 
# Thu, 05 Oct 2023 14:38:59 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:59 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:59 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:59 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:59 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:39:01 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:39:01 GMT
ADD file:328ddeb1ec18f23aacb0d0a2878c45c71ef674135124723e62d867c8005005f2 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:39:01 GMT
ADD file:d7126bc8d11f5a5c0794401215ed55d7754bdb3563355e4d1cfcc331f47c63e8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:39:01 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:39:03 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:39:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:06 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:19:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:20:17 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 10 Oct 2023 23:20:20 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 10 Oct 2023 23:20:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:20:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:20:59 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:20:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:571735d1e71e07b1fa3a2fb676b0fb08b6139607cc00c69743cd5c964836cff8`  
		Last Modified: Mon, 09 Oct 2023 12:07:33 GMT  
		Size: 42.3 MB (42311719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cc747d263fea66ad8cdd4604f369660ef4ac8e363da97fcd971689c41886c8`  
		Last Modified: Tue, 10 Oct 2023 23:23:48 GMT  
		Size: 30.4 MB (30420809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd624b0db24156ea00d307d0acc64e71e08e61796702c29c2624eeddab3458c`  
		Last Modified: Tue, 10 Oct 2023 23:24:17 GMT  
		Size: 41.2 MB (41226110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945115dcbae75e995556ec39312e0b5465d9b9e1b663bdf2dd785b9ee32e6b1f`  
		Last Modified: Tue, 10 Oct 2023 23:24:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a09fb34773d9ef9b0d8aaeab65486c1b008edd8b4062bcf76269b1718fb3a`  
		Last Modified: Tue, 10 Oct 2023 23:24:09 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
