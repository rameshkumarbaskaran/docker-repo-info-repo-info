## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:41640b4547eca3bcf553ead39f4ca04a367d90cd77ee8a77d36194b093a9960e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6ab42072a9d5d3bc71a4e39ef3e49f5f9e552086fe15d57be24a3a36c03777d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112747615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef348d441b0a364c29655b51ddf6f93624eb0b1e761edfbfeb1b4e017c2a0271`
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
# Wed, 10 May 2023 01:18:37 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 10 May 2023 01:18:58 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:18:59 GMT
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
	-	`sha256:b49aef449e128b3547d84ff3a0c6fe94365803f054e0567471f3653265a18297`  
		Last Modified: Wed, 10 May 2023 01:22:00 GMT  
		Size: 47.0 MB (47001374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d01351a4ba3a606a16bbab91f306cccde64c3e23555fd7c9b5c1e2f7dcc114`  
		Last Modified: Wed, 10 May 2023 01:21:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aedebbc74f13325bb1e52ce3c2ee7b25a730cf518e95409e285764d5bf5d9711
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110977426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959540a00a09fb54c9f259d1fb829340d3645943ee513fe633321a28734ea7aa`
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
# Wed, 10 May 2023 01:12:15 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 10 May 2023 01:12:35 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:12:36 GMT
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
	-	`sha256:066ad83fdc75c4d177ffdaf4bd126efe8b37d8103c1dcc26e5f65782f2b8158e`  
		Last Modified: Wed, 10 May 2023 01:15:16 GMT  
		Size: 46.5 MB (46485242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c702303176138029c99a7484bffbdfeecdee4719c4169211fe64e88386124321`  
		Last Modified: Wed, 10 May 2023 01:15:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1e89a70293a97a1f57f63f8d76aeebe9008e52d536992b6a4aec556af9d8a029
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119620710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1893f7bcd58e37145c6c9165bba86764d174b9416902b32a6cf1217454e201fc`
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
# Wed, 10 May 2023 01:22:13 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 10 May 2023 01:22:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:22:58 GMT
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
	-	`sha256:139b619bc5b8ebde189b7ac84848fe299e525f27655380318f5af7caa0d84052`  
		Last Modified: Wed, 10 May 2023 01:26:13 GMT  
		Size: 46.9 MB (46877465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1c9ddb3133d6edb65ac645412da193c38d0621b5cc89f835db0ecabf5d1f86`  
		Last Modified: Wed, 10 May 2023 01:26:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:37c1d96b132fedb02477f5378d6c172134b3e6ac6dcb952a8fca385b5c77fec2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107926769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717b655f5c14ad02ec7cc6d1d57c59f3767195111f2f904fddb62b02be6c6835`
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
# Wed, 10 May 2023 01:00:08 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Wed, 10 May 2023 01:00:37 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:00:39 GMT
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
	-	`sha256:8741c074d985d9eece0baf8cb28e1e38f06f6793799644a017f6542390fa1eb0`  
		Last Modified: Wed, 10 May 2023 01:02:11 GMT  
		Size: 43.8 MB (43764446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfae51985d3af8db94f525f854028bbbfde90c6a97ada224974804897827faac`  
		Last Modified: Wed, 10 May 2023 01:02:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
