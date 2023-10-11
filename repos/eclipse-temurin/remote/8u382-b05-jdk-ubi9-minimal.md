## `eclipse-temurin:8u382-b05-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1d58d85d0792fce154d55fc1ef22eb3de80cb4d1ce637dfdba6785de59384494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bd7426bd872e6f4df2b1f4f326bfd1530737470fd0f989daff909ec0a22953b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169293186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645d9092ed5488784375c8229ac3bf8ca24a5646cb34a116fcda00bf9a395eb2`
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
# Tue, 10 Oct 2023 23:49:32 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:49:33 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:49:33 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:49:33 GMT
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
	-	`sha256:7fdc94d8048f633eae2c9a75e6280b2a4bd6663d5672384d858a15ed85497f23`  
		Last Modified: Tue, 10 Oct 2023 23:53:02 GMT  
		Size: 103.6 MB (103585300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89369b261278d8b71ce7f3b7002318e00d3b9199d1de3068df5e4b4acb659cd2`  
		Last Modified: Tue, 10 Oct 2023 23:52:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40f43ad25335a237903209917e7381b9913ed75fdb7616b2591f85a052aa0b7`  
		Last Modified: Tue, 10 Oct 2023 23:52:52 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:83fb06e1ae4e9df2880fc7dd05578f0a0934ebcf37be5aa59a6678a2a6dc8434
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167110828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1333351b10c4ce2debb983f04deb8c7d9280764be033996f7811ed3d725a512a`
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
# Tue, 10 Oct 2023 23:51:08 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:51:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:51:10 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:51:10 GMT
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
	-	`sha256:6b6579ecaf28e9b0cb59b28d64bc081b13b160004c32ff7fa15f9f61287d84f4`  
		Last Modified: Tue, 10 Oct 2023 23:53:53 GMT  
		Size: 102.7 MB (102690771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c0c9204b6b81b9e33031b1d8c291abebfe3798a23b4f67925d43d4c9449f69`  
		Last Modified: Tue, 10 Oct 2023 23:53:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415253298694b2904d2ed0998093aaaab3f8a8b2316bd13b8625fbabd5c53131`  
		Last Modified: Tue, 10 Oct 2023 23:53:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1c7eadb3c3db4258044d0abe7c599a730246da6d8e99efa9eff0044e923ba759
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173778011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5a2d7c6ee28654d376500734c834cf04a66ca9e01856a712bcbe28607570b9`
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
# Tue, 10 Oct 2023 23:20:30 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:20:34 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 10 Oct 2023 23:20:34 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:20:35 GMT
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
	-	`sha256:c45953ebb13d176421e337329ec3c9e29061d51e3a75e3a69700d74d17ca7013`  
		Last Modified: Tue, 10 Oct 2023 23:23:55 GMT  
		Size: 101.0 MB (101044611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b092eae6922e0a6148234e155432bc44fd296f8004e81d1c1dbaef1dd041f7a8`  
		Last Modified: Tue, 10 Oct 2023 23:23:41 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1746230f0aea7e3c4773f927dd0f6588a3bb94841cfeafea038f32f5e1464540`  
		Last Modified: Tue, 10 Oct 2023 23:23:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
