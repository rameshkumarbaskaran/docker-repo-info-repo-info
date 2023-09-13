## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:2036923f738de8d46185ae4757390ec8ec320ef975be98c2dae27bc49cb021a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:99dbc3245b958f5b6b98a64b5cc2c2d7efda91368b69f7e73e375adf23e589b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107577474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b06fce9f99884add8b255c283494ee9bf54946481f149ff6d1d593657ca1edc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 09:12:43 GMT
ADD file:941e8e63c7dda0f8bbbf5b9262a1b27948be3557d23e6a486c71b35a2c1bc4c2 in / 
# Tue, 05 Sep 2023 09:12:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 05 Sep 2023 09:12:44 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 05 Sep 2023 09:12:44 GMT
ADD multi:724ed0e3f3beae9b8bce7fd72262ce34617b5e89ed2a1257879bb55c22d53483 in /etc/yum.repos.d/ 
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 05 Sep 2023 09:12:44 GMT
ENV container oci
# Tue, 05 Sep 2023 09:12:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Sep 2023 09:12:44 GMT
CMD ["/bin/bash"]
# Tue, 05 Sep 2023 09:12:44 GMT
RUN rm -rf /var/log/*
# Tue, 05 Sep 2023 09:12:44 GMT
LABEL release=750
# Tue, 05 Sep 2023 09:12:45 GMT
ADD file:dd357e6a9eb4775817d5b3661766c059b0f8be7495521c94f4a1996e79b296af in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.json 
# Tue, 05 Sep 2023 09:12:45 GMT
ADD file:a135e818743f081adf270787e41a0c86edf6d9e4a7555d04157dac6afbec26c4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750 
# Tue, 05 Sep 2023 09:12:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-09-05T09:00:56" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750"
# Tue, 05 Sep 2023 09:12:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-f8785.repo' '/etc/yum.repos.d/repo-08a34.repo'
# Tue, 05 Sep 2023 09:12:46 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 05 Sep 2023 09:12:47 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 13 Sep 2023 00:12:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Sep 2023 00:12:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2023 00:12:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Sep 2023 00:12:18 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 13 Sep 2023 00:12:18 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 00:12:44 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:12:44 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:12:44 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:12:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:35e8d0567610305e5133f45eac553d3f57e4f33e2f764a1f16bab4f3bf24ad86`  
		Last Modified: Tue, 12 Sep 2023 17:06:17 GMT  
		Size: 37.9 MB (37869610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4b2d8ae9950ba9ad7cdcc984cea26a412f3c27beebefa591575d2a8cddac7a`  
		Last Modified: Wed, 13 Sep 2023 00:16:03 GMT  
		Size: 27.9 MB (27861943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51308e4ebd6e60e485e8afb0aa29b7890620355120addba35f16a52a01dd1b3b`  
		Last Modified: Wed, 13 Sep 2023 00:16:29 GMT  
		Size: 41.8 MB (41845051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215b557dec22322e8bbeda219c834797d7f1f4796ba4c3799ba183c789649adc`  
		Last Modified: Wed, 13 Sep 2023 00:16:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fce25b9b18dcbcab9b8d1c0c9afdeaf29e19e115ea180169943893d46ded8b`  
		Last Modified: Wed, 13 Sep 2023 00:16:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c3134ffbb37b0bbd5566061a427909183963967560402300a519ade27bc0ec1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105281359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e64bc8f7bac530d758a0b280385a8b5ec8b416661e81a8c972aed4d27d5da3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 09:12:45 GMT
ADD file:baa1ee1c9afcba391623d3d9bcfa72a48252ff1a781bb51977f2e8a4253fa61f in / 
# Tue, 05 Sep 2023 09:12:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 05 Sep 2023 09:12:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 05 Sep 2023 09:12:46 GMT
ADD multi:724ed0e3f3beae9b8bce7fd72262ce34617b5e89ed2a1257879bb55c22d53483 in /etc/yum.repos.d/ 
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 05 Sep 2023 09:12:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 05 Sep 2023 09:12:46 GMT
ENV container oci
# Tue, 05 Sep 2023 09:12:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Sep 2023 09:12:46 GMT
CMD ["/bin/bash"]
# Tue, 05 Sep 2023 09:12:47 GMT
RUN rm -rf /var/log/*
# Tue, 05 Sep 2023 09:12:47 GMT
LABEL release=750
# Tue, 05 Sep 2023 09:12:48 GMT
ADD file:531960867699fbf67533fa82e9e646d0115e0cd189f4895ce398ce0a7f2aad91 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.json 
# Tue, 05 Sep 2023 09:12:48 GMT
ADD file:036975ba39f9c9bed40995aa3672443e762ef5ebe6df0c2e8bcbd9f2f713fe55 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750 
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-09-05T09:00:56" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750"
# Tue, 05 Sep 2023 09:12:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-f8785.repo' '/etc/yum.repos.d/repo-08a34.repo'
# Tue, 05 Sep 2023 09:12:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 05 Sep 2023 09:12:52 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 13 Sep 2023 00:50:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Sep 2023 00:50:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2023 00:50:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Sep 2023 00:50:33 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 13 Sep 2023 00:50:34 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 00:50:51 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:50:52 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:50:52 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:50:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a068c9f5dd296d48ed9e43fcf6c6566f5b00a0ecb13ea26c9f08503d94e186bd`  
		Last Modified: Tue, 12 Sep 2023 18:07:48 GMT  
		Size: 36.2 MB (36150804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6624355316478773825d97a417732b826d10becf276dfd9daffa41742f521453`  
		Last Modified: Wed, 13 Sep 2023 00:53:21 GMT  
		Size: 28.3 MB (28286010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db20cc989157c11839a57685e65a215677c6e3aa3fd18f2b0b493da95ccd84b5`  
		Last Modified: Wed, 13 Sep 2023 00:53:44 GMT  
		Size: 40.8 MB (40843675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519d7433311c05c403efd132bab8d63661f53dcfeb4aca1fb70041b94989ce4f`  
		Last Modified: Wed, 13 Sep 2023 00:53:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d02486e342e240e600211a175bd449b5c0d252d7f6f4f34abe1c168ef2df398`  
		Last Modified: Wed, 13 Sep 2023 00:53:40 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:83f3754d339e167bb7638c90bbed254a090b21ba91bb31d00c127ddfa190aaa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113926202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5dc04f4dc6a33bfe8a63fa38e0f06f6a4bec336c22102816791990dd7dc87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 09:12:48 GMT
ADD file:0fedbe63c5a7da2e5eda52054ef58d55a1df3b84f0d0c2216dc9c7cb5d6c040c in / 
# Tue, 05 Sep 2023 09:12:49 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 05 Sep 2023 09:12:49 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 05 Sep 2023 09:12:50 GMT
ADD multi:724ed0e3f3beae9b8bce7fd72262ce34617b5e89ed2a1257879bb55c22d53483 in /etc/yum.repos.d/ 
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 05 Sep 2023 09:12:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 05 Sep 2023 09:12:50 GMT
ENV container oci
# Tue, 05 Sep 2023 09:12:50 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Sep 2023 09:12:50 GMT
CMD ["/bin/bash"]
# Tue, 05 Sep 2023 09:12:51 GMT
RUN rm -rf /var/log/*
# Tue, 05 Sep 2023 09:12:51 GMT
LABEL release=750
# Tue, 05 Sep 2023 09:12:51 GMT
ADD file:9abd7ee0b06efc65409d368005415727f43c179838e557b12790b66a8a9d8c0e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.json 
# Tue, 05 Sep 2023 09:12:51 GMT
ADD file:1a864e2324e3d4543af4a9e3c3c472668cca5706120866cdd68d3f86dd351657 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750 
# Tue, 05 Sep 2023 09:12:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-09-05T09:00:56" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750"
# Tue, 05 Sep 2023 09:12:53 GMT
RUN rm -f '/etc/yum.repos.d/repo-f8785.repo' '/etc/yum.repos.d/repo-08a34.repo'
# Tue, 05 Sep 2023 09:12:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 05 Sep 2023 09:12:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 13 Sep 2023 00:19:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Sep 2023 00:19:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2023 00:19:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Sep 2023 00:20:18 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 13 Sep 2023 00:20:20 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 13 Sep 2023 00:21:05 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:21:08 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:21:09 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:21:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:20db1a1583611ed74518b1e0a1a1c1728bc6222623adeb4942fd382ab8bc10cc`  
		Last Modified: Tue, 12 Sep 2023 18:07:53 GMT  
		Size: 42.3 MB (42274685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d182a7cfa10f2cb84e3f36fd527e83cec2342a528dbdfa7470d8c40eef2dac3c`  
		Last Modified: Wed, 13 Sep 2023 00:23:57 GMT  
		Size: 30.4 MB (30424550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c17d63e1ead4bb2736705257c45e0b6e731924f172686a63a2020c60f7a733`  
		Last Modified: Wed, 13 Sep 2023 00:24:32 GMT  
		Size: 41.2 MB (41226098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7828b9b8a66f80ddbb4ce7f48b27c244db4f6830fdb496795c77f9c2c4fc3ff5`  
		Last Modified: Wed, 13 Sep 2023 00:24:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226abe39b8f051b6953df7d11b93fb4a39b863273121a03a3690e982a2ef193f`  
		Last Modified: Wed, 13 Sep 2023 00:24:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
