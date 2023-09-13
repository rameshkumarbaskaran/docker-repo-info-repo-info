## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:37efbec1c0f74e79eafd8d1d4e90c4c56b16b619d1c926930595bac05065ca03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7d8a229804116d73018507c87347c06e3620a5b004c5148d0b4837a5771d04b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (207018286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9588b13f534625053b1969609d03457a541cafabd910c5d461f1bd1ed537e0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Wed, 13 Sep 2023 00:12:57 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 00:13:05 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:13:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:13:08 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:13:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:13:08 GMT
CMD ["jshell"]
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
	-	`sha256:494e26fccc02cf6e3218797f652ca24fa2ef7f5bce2f7ef12e654b420925cd9c`  
		Last Modified: Wed, 13 Sep 2023 00:16:55 GMT  
		Size: 141.3 MB (141285845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3047521b5f8f7b590a19443fd5c14d1da48aab7292d005fbbcf75ffbcf34a478`  
		Last Modified: Wed, 13 Sep 2023 00:16:44 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bae2763d70838c5e03df6f4ce92718d3c933b4b661dd046219a4f6a5d40e25`  
		Last Modified: Wed, 13 Sep 2023 00:16:44 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4d9d228b04f3aa279dee84b418e1a4afa1564c36778820719ddcc0b9fedec42b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202470227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f40dae22a293c500e7977de954f3f0feea5af576072ae431bf0224fe2fec92b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Wed, 13 Sep 2023 00:50:59 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 00:51:08 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:51:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:51:11 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:51:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:51:12 GMT
CMD ["jshell"]
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
	-	`sha256:b8fdce0d874647a243f68daf0f4aab1e7dca674c59c1e18f64db437012a77193`  
		Last Modified: Wed, 13 Sep 2023 00:54:07 GMT  
		Size: 138.0 MB (138032526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15d6d31dc0de7607f46acec3d5ca127901b0e4acd77eb52fe24ab0f196fe2dd`  
		Last Modified: Wed, 13 Sep 2023 00:53:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2971903079ceef150a81039e1196f2ca5931dbfd0dae027d8071023053e9a76`  
		Last Modified: Wed, 13 Sep 2023 00:53:58 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:283f26285048109d5477de44c6741c380b25cfdb7a2b4281a3b88631e7e9c153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201186160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008f768acde6bce3d137ec60a0690af98f7b6767536f3bc7cf31943cea6dcd37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Wed, 13 Sep 2023 00:21:20 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Wed, 13 Sep 2023 00:21:35 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:21:42 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:21:43 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:21:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:21:45 GMT
CMD ["jshell"]
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
	-	`sha256:124388d9f6b08e5a2cbe9d263b3c7014a6ceab5f06dc6c73c1d2b3bf5540841c`  
		Last Modified: Wed, 13 Sep 2023 00:25:03 GMT  
		Size: 128.5 MB (128486041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d5452b32ccf2ec23f009a66be698362ba51c338b54db2f6cd2cbf0d689ed`  
		Last Modified: Wed, 13 Sep 2023 00:24:45 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41b88d8fda410baf5acc1031575c75b0413c494bf3d31f285e2bc177ee70536`  
		Last Modified: Wed, 13 Sep 2023 00:24:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:22ddac25b0bf0f3041ad820fdee587e86308054389ea5e64896f244bce9d8f52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185573624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edc334d4708c14d9b9e50099ca44ab715d5553b965fc0edf4419e1c9797cae9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Sep 2023 09:12:47 GMT
ADD file:017287d254be48c2310c17f6af9180d3f40beab6e64582f0be4f1b0a1381c4f3 in / 
# Tue, 05 Sep 2023 09:12:48 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 05 Sep 2023 09:12:48 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 05 Sep 2023 09:12:48 GMT
ADD multi:724ed0e3f3beae9b8bce7fd72262ce34617b5e89ed2a1257879bb55c22d53483 in /etc/yum.repos.d/ 
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL io.openshift.expose-services=""
# Tue, 05 Sep 2023 09:12:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 05 Sep 2023 09:12:48 GMT
ENV container oci
# Tue, 05 Sep 2023 09:12:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Sep 2023 09:12:48 GMT
CMD ["/bin/bash"]
# Tue, 05 Sep 2023 09:12:49 GMT
RUN rm -rf /var/log/*
# Tue, 05 Sep 2023 09:12:49 GMT
LABEL release=750
# Tue, 05 Sep 2023 09:12:49 GMT
ADD file:0a62b914223b0d494e815e8af123d6ac7cd699b79f9c678e87b067129fbeb1d2 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.json 
# Tue, 05 Sep 2023 09:12:49 GMT
ADD file:c4e7b864082544fdcb9369e3083c6548ba9586479c037121374f52ba9570e25d in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750 
# Tue, 05 Sep 2023 09:12:49 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-09-05T09:00:56" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750"
# Tue, 05 Sep 2023 09:12:50 GMT
RUN rm -f '/etc/yum.repos.d/repo-f8785.repo' '/etc/yum.repos.d/repo-08a34.repo'
# Tue, 05 Sep 2023 09:12:51 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 05 Sep 2023 09:12:52 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 12 Sep 2023 23:58:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Sep 2023 23:58:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Sep 2023 23:58:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Sep 2023 23:58:16 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 12 Sep 2023 23:58:17 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Tue, 12 Sep 2023 23:58:24 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 12 Sep 2023 23:58:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Sep 2023 23:58:29 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 12 Sep 2023 23:58:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 Sep 2023 23:58:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4effe20cbfb4d79249e1f52052de14d70e1935e788f302e17a5e501052950063`  
		Last Modified: Tue, 12 Sep 2023 18:07:59 GMT  
		Size: 36.1 MB (36111447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3c020015672f341e3f93a1117473daf33520832c403634dba7af6e969d0a1f`  
		Last Modified: Wed, 13 Sep 2023 00:00:39 GMT  
		Size: 27.9 MB (27916326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e2f7d4c5643677478a82cff038b75fb2f83e046d6c07d3a6b9a450f63cb708`  
		Last Modified: Wed, 13 Sep 2023 00:00:43 GMT  
		Size: 121.5 MB (121544966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf676f1bcd81351509af6e65fc31058111207c9a05b7fbcda401af19ab7ccc2`  
		Last Modified: Wed, 13 Sep 2023 00:00:35 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cd0b181a16704f1525b17e9c605904c9b983a375bef0c3d8a94ec89a5707ed`  
		Last Modified: Wed, 13 Sep 2023 00:00:35 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
