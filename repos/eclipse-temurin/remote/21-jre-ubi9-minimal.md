## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c1361a33422730d10485faa78185c1d6046c2d75333b46b8cfdc1109da178559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2b7d0b2676b74506eb6f115175865eb129faef6953700a1bf0de971457db5f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119209651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5a93e27d7d31a0ce0b799e7babcd1a9d7182df65df4ba5daf37e1f850d12be`
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
# Fri, 20 Oct 2023 00:07:36 GMT
ENV JAVA_VERSION=jdk-21+35
# Fri, 20 Oct 2023 00:07:59 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a36cde2956749aaad502e1df6729072e5483265fce142230516261da9a391db';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='080a53a3f75b94450779199f09c8d91b53637d315f128c58a4f160fb6272502d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 20 Oct 2023 00:08:00 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 20 Oct 2023 00:08:00 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 20 Oct 2023 00:08:00 GMT
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
	-	`sha256:6a28d1e0384b4f28a5c041d3c7ac7a9093de908c1b61827338a0c74fe7c2e6bd`  
		Last Modified: Fri, 20 Oct 2023 00:11:40 GMT  
		Size: 53.5 MB (53488146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357614ee5024dc37e0eaea07fbc68349ed8c1aa8709f896834703169b57df906`  
		Last Modified: Fri, 20 Oct 2023 00:11:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eae2f5a6c8baa008f54f3297a04e9a90515c47e7f11993c9c7b461fb6fa727`  
		Last Modified: Fri, 20 Oct 2023 00:11:33 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d62b7c4d9c70de3e5155cc48900c8fd71f42df4ffa44ae9f0c89cfc146e5a5fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117084523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b43291b531835f8b703b59cd37822b3e3362e9864723bf2421dc0c9a797073`
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
# Fri, 20 Oct 2023 02:33:50 GMT
ENV JAVA_VERSION=jdk-21+35
# Fri, 20 Oct 2023 02:34:11 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a36cde2956749aaad502e1df6729072e5483265fce142230516261da9a391db';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='080a53a3f75b94450779199f09c8d91b53637d315f128c58a4f160fb6272502d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 20 Oct 2023 02:34:12 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 20 Oct 2023 02:34:12 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 20 Oct 2023 02:34:12 GMT
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
	-	`sha256:c7bf4bb5a4ac44fa4fbe4cb58ce1af696fcf33eaf8cd7e812769d92ac3a866e4`  
		Last Modified: Fri, 20 Oct 2023 02:37:43 GMT  
		Size: 52.7 MB (52658967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc5cce94a78a9d27a68fb00ee9f01e5803beceb1b650336d54af1715824eeae`  
		Last Modified: Fri, 20 Oct 2023 02:37:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654fcc1f98f5212ee74f1b5429cb7328f81b87e5c0d2ed005b4f8fefd18d24f3`  
		Last Modified: Fri, 20 Oct 2023 02:37:37 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
