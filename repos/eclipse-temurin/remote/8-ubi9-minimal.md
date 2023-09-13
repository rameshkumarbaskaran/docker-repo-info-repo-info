## `eclipse-temurin:8-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c73f534ed6288c2e68b5a0a44e66944622bd96d9fbef10c4589d959a87c1ea0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4cea873110d099d5b5abc09f86344ff3c4f7d22983e66611f1d0627d55942ba3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169317720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63969f7f8ad654f9cd8f175b8db1d05f26b9f2e8aa9cd881bb30752f792b7bc`
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
# Wed, 13 Sep 2023 00:12:24 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:12:25 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:12:25 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:12:25 GMT
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
	-	`sha256:9f2c689344467639fd044d12a7265815c4516416795f5c7d423389a8da0fb674`  
		Last Modified: Wed, 13 Sep 2023 00:16:09 GMT  
		Size: 103.6 MB (103585296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f847b7c60c1c87c2f3f052d23709d83d47f679558c999b80f408aa54cd7fac`  
		Last Modified: Wed, 13 Sep 2023 00:15:59 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092fb1de19153bdb948e82c8193e9946389fed9854294af2ddf6b3a2ce9699db`  
		Last Modified: Wed, 13 Sep 2023 00:15:59 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:df5be9ad3aef96b0b9e3014625c2064ab72e9441a3d52d893d8f0832d4fc918a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167128450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb27d727a8f44120574481d495df788736d1b1f7bd1a447b5157de48fef7cde`
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
# Wed, 13 Sep 2023 00:50:39 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:50:41 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:50:41 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:50:41 GMT
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
	-	`sha256:f1c6ffbf0fcfafb163750bb1eac623a3cf54e6a6cadf8ab952569c6adb5e9e06`  
		Last Modified: Wed, 13 Sep 2023 00:53:26 GMT  
		Size: 102.7 MB (102690766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f632899526a9718cc52b500d4430b926d334436dd9d86f70b823d6162f7f2e2`  
		Last Modified: Wed, 13 Sep 2023 00:53:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96f5024956665711bc65d80336d44c4c837754fd99af6d165dd15e56cb4a865`  
		Last Modified: Wed, 13 Sep 2023 00:53:18 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:80e1698b9f186fb407b5f4093dcf706463e136e0ac71dc9c3501bb866f6f780b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173744707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07ab4a943628bffdfdc7d956369b0dd6c8bb7012c466dc49ecd602f84fa2513`
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
# Wed, 13 Sep 2023 00:20:32 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:20:37 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Wed, 13 Sep 2023 00:20:38 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:20:38 GMT
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
	-	`sha256:4904023099d8cc6e24068cb28988b74f5dc673b54e09d7acf7128d1f1d856a69`  
		Last Modified: Wed, 13 Sep 2023 00:24:09 GMT  
		Size: 101.0 MB (101044603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e5f7b59a89e00ca783124304c30bd2586947d815ff8c90e704d9854d6418`  
		Last Modified: Wed, 13 Sep 2023 00:23:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a060161bf338a4ff6980892b4dfacf9f575af1bb8cb9b8619130e9c18ca3b2f3`  
		Last Modified: Wed, 13 Sep 2023 00:23:50 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
