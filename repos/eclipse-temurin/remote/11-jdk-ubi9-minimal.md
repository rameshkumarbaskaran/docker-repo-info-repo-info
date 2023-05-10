## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ce9d48e572ab1bd3bd7c7f47aaaef157a9544a38576a8df03a419d90d2593130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1394362f5bb63a9fa1e78ddc826dba921a83559646a80a4f332dcb5bacf6f5ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260772089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d9f1b798bf4a64c7a999ac08356e419dc1c279ffe47b6e39bf86c06c8548e6`
-	Default Command: `["jshell"]`

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
# Wed, 10 May 2023 01:18:13 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:18:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 01:18:15 GMT
CMD ["jshell"]
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
	-	`sha256:d34e75d13aee12657018cd5314b5bf54dbf378d88e3ea0365cdb7ded7681989d`  
		Last Modified: Wed, 10 May 2023 01:20:57 GMT  
		Size: 195.0 MB (195025830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ad56f1f5c783abf39a4fc2141401777af8781aa776c8ceac6d605c9a2ce2c0`  
		Last Modified: Wed, 10 May 2023 01:20:44 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2db8a712820eb64b307403ac803f379e24015799cca6e8df02b225653f6f078d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256290329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315044df6fc6e087c249aef58d3187bdb2bbfb8ce2d6dff1eab52f6b50374d85`
-	Default Command: `["jshell"]`

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
# Wed, 10 May 2023 01:11:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:11:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 01:11:56 GMT
CMD ["jshell"]
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
	-	`sha256:f259a714883b9145233d5e4afa6947f340413efe6a1623e748ff4b8c1e30ae3d`  
		Last Modified: Wed, 10 May 2023 01:14:20 GMT  
		Size: 191.8 MB (191798128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543677696351a261bbf4e90689991533b005fe5416f76a8a0013ae339c4e11d7`  
		Last Modified: Wed, 10 May 2023 01:14:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:91c22ed0d0a86378602e9a50647a503f250b3312e4b0f77c1528957404608dd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249795574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639b0ae938a09710b4dd036b50091bad795c4bb7066683e8edb47c34ebb4f22e`
-	Default Command: `["jshell"]`

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
# Wed, 10 May 2023 01:21:26 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:21:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 01:21:33 GMT
CMD ["jshell"]
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
	-	`sha256:dd061460c707299f316d6e75012b0ec4b26867cb186579e2bbe4933871363edb`  
		Last Modified: Wed, 10 May 2023 01:24:48 GMT  
		Size: 177.1 MB (177052311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c9d80eaf40f23a34928eab5525d002da4b51f7df6c5374cc1d79adb25efdd5`  
		Last Modified: Wed, 10 May 2023 01:24:26 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f82a3670a5e66d56948826a250d7ddb92f509a4c59c02dcd720583929c6daf2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232582500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f208acf2ffe2e1d18ee82329c3ce8f6e0b44d40c1378ef7c4303789d8b888c`
-	Default Command: `["jshell"]`

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
# Wed, 10 May 2023 00:59:28 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0c7763a19b4af4ef5fbae831781b5184e988d6f131d264482399eeaf51b6e254';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1e3704c8e155f8f894953c2a6708a52e6f449bbf5a85450be6fbb2ec76581700';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a21e2c30e48df0b7238691833316c008167cbedd4e2f1e677bcb81638420d273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5f19fb28aea3e28fcc402b73ce72f62b602992d48769502effe81c52ca39a581';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 00:59:32 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 00:59:33 GMT
CMD ["jshell"]
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
	-	`sha256:0fd2e117a3cb9f4bc9532311649d810e682aa27d3406e46c3c7b8609ea8566b1`  
		Last Modified: Wed, 10 May 2023 01:01:23 GMT  
		Size: 168.4 MB (168420159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704d96095abe1ad852ee523da7466dd8f8575d416f5fb3821088dcc506d64eb7`  
		Last Modified: Wed, 10 May 2023 01:01:13 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
