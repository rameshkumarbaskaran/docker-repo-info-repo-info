## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1598c83e4902f534e9c2f7edc82789a70de651261c685e1c56445f8605252925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2d367f436b2c347c87a96cb0946319ed5bc15ffa5d2e284f34486d1ac9ccaa42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169202517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf13317e61d2c4b16753215d5706f3cfe32439359ccb4d593e8a83c875e882c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Nov 2023 16:53:45 GMT
ADD file:3ab05c00be3ac1a3a9c02ff85ae063226747050d4ed18c3a6006bd32bb2ed212 in / 
# Thu, 09 Nov 2023 16:53:45 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:53:45 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:53:45 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:53:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Nov 2023 16:53:45 GMT
ENV container oci
# Thu, 09 Nov 2023 16:53:45 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:53:45 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:53:46 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:53:46 GMT
ADD file:35832c36c4844d2b55c61e7f31f93da2e37c5013a7e01e33cdde2ac96ca1208e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1361.1699548032.json 
# Thu, 09 Nov 2023 16:53:46 GMT
ADD file:dced2941f7e8a6bb144e0bb042262434fbc0ab88cfc28be375e87aeb4d243255 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1361.1699548032 
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL "release"="1361.1699548032" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:47" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1361.1699548032"
# Thu, 09 Nov 2023 16:53:47 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:53:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:53:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:10:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:10:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:10:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Nov 2023 04:10:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 17 Nov 2023 04:10:17 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Fri, 17 Nov 2023 04:10:22 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 04:10:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 17 Nov 2023 04:10:23 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 04:10:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a032f50e22ae11b241fcf38b4a787f0e51009578eedaf9d05894f5f38fd12af5`  
		Last Modified: Wed, 15 Nov 2023 08:03:15 GMT  
		Size: 37.7 MB (37718602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce7e8160ea2f0ae8dda38a6801d1b04424c7be16d39121dc1ccebec76e15e73`  
		Last Modified: Fri, 17 Nov 2023 04:13:40 GMT  
		Size: 27.9 MB (27884497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a22bf3c9c808ac38d6ae6127d6b89705db8341f5b97c30c3435819bd2da06d`  
		Last Modified: Fri, 17 Nov 2023 04:13:45 GMT  
		Size: 103.6 MB (103598546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8393ed2303efaf129958608e81e488a1a12732e767cf8c986b76ed595865db80`  
		Last Modified: Fri, 17 Nov 2023 04:13:36 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cac71cfed4b0b3c4d4f7dcbbbc1488354563c00e8967313c7958e10631bfd9`  
		Last Modified: Fri, 17 Nov 2023 04:13:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8c2b05ecd203ba85adae94eaaee594572635fda1daae45bdee1fda5c181d9afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167035821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a107940ec9f65e3513ab070c636d5ad18d538aa693ac81fc34599d3e6f843b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Nov 2023 16:53:42 GMT
ADD file:5d1f2d165588621ba970c5e16b9764256b05657b67c9ef22a42f6a3d3055a9f8 in / 
# Thu, 09 Nov 2023 16:53:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:53:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:53:43 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:53:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Nov 2023 16:53:43 GMT
ENV container oci
# Thu, 09 Nov 2023 16:53:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:53:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:53:44 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:53:44 GMT
ADD file:b36fadb6916491a29afa9c0c3205f4af9153efdaf783fb39a005e8d963e3a156 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1361.1699548032.json 
# Thu, 09 Nov 2023 16:53:44 GMT
ADD file:cb5ad190e52f7186e166d6d6a03af745a3f8f6ca31aa837fd1246785ec33533c in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1361.1699548032 
# Thu, 09 Nov 2023 16:53:44 GMT
LABEL "release"="1361.1699548032" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:47" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1361.1699548032"
# Thu, 09 Nov 2023 16:53:45 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:53:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:53:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:26:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:26:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:26:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Nov 2023 03:27:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 17 Nov 2023 03:27:04 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Fri, 17 Nov 2023 03:27:09 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 03:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 17 Nov 2023 03:27:11 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 03:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f30351d9b93c570de8620ad709889ebb0ac8a747825d6009f4549c7d1626502c`  
		Last Modified: Wed, 15 Nov 2023 08:03:01 GMT  
		Size: 36.0 MB (36015710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c24e8fb733bfeb2206c8dd68d84c37ce2f76a249c8e5cf4ce556b740259b88`  
		Last Modified: Fri, 17 Nov 2023 03:29:39 GMT  
		Size: 28.3 MB (28317316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaffde152025f9f643ec2cf554b2a2a586fbd8260669340fc25d9cb0cea1718`  
		Last Modified: Fri, 17 Nov 2023 03:29:44 GMT  
		Size: 102.7 MB (102701923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e72cee7f106157114e864c5dd9215e1dd06414b64c05c8318675d056ba9863c`  
		Last Modified: Fri, 17 Nov 2023 03:29:36 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80848aceb6e7f74286c9bafa7c562dc962c5e22ebbc3ea5c221faa449516e61f`  
		Last Modified: Fri, 17 Nov 2023 03:29:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2e7c043c0bd8719446564106e869773e2bfe2025e91850c45e714579b6f71559
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173598436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154ac6ba42f6ae2cf80a7996444b1c5e8847490af394881bcdc13730ee29a0de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Nov 2023 16:53:44 GMT
ADD file:8fbe704c47283f79a952afd6861d213d57342118a7a3f18abb6886589ab8327f in / 
# Thu, 09 Nov 2023 16:53:45 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:53:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:53:46 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:53:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Nov 2023 16:53:46 GMT
ENV container oci
# Thu, 09 Nov 2023 16:53:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:53:46 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:53:47 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:53:47 GMT
ADD file:02cd7e3c680cb1e53d818dcce94ac112ac2917d9aff027d2c917e204adc1bf68 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1361.1699548032.json 
# Thu, 09 Nov 2023 16:53:48 GMT
ADD file:31bb1ec0f9d6b927af8fdc28f877b63bc118a7e90322571561fb6c0c25e57342 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1361.1699548032 
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL "release"="1361.1699548032" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:47" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1361.1699548032"
# Thu, 09 Nov 2023 16:53:49 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:53:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:53:52 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:46:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:46:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Nov 2023 03:47:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 17 Nov 2023 03:47:26 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Fri, 17 Nov 2023 03:47:39 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 03:47:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Fri, 17 Nov 2023 03:47:45 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 03:47:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cf11472d86e63d82be19f9e462d989984354de671e9403dc46b75ab1f5b7f70`  
		Last Modified: Wed, 15 Nov 2023 12:10:19 GMT  
		Size: 42.1 MB (42097715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f9ac7fefe0fba427e76fc932963256039d07f661a4655a854af1dafdb2067a`  
		Last Modified: Fri, 17 Nov 2023 03:53:15 GMT  
		Size: 30.4 MB (30435275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61814d0dc6291afb0c6d7f47cb606a7f89437e34e11da3df5ebad5fc4300a572`  
		Last Modified: Fri, 17 Nov 2023 03:53:20 GMT  
		Size: 101.1 MB (101064575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f442d35480bef4fe2c15e3442d3ec512d23bd15911973abae36584a0428eab`  
		Last Modified: Fri, 17 Nov 2023 03:53:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19a5fe7bd77db425bbdbf38114efaf11e1e3da4ff88bb6d87c5eda1afd2ad69`  
		Last Modified: Fri, 17 Nov 2023 03:53:10 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
