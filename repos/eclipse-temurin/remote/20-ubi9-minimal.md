## `eclipse-temurin:20-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:95199b55931838a1ed833027747629b84c80c2084d246cf58818382d5b3d4589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:20-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5dba234b043141f4dcf18f1c7d2277688b1c7ef3a80ea46f9c167acfb1292338
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268567371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b2a9690f995f061cda492051d45479039692084486a6ec37eb3659bd4d479b`
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
# Wed, 10 May 2023 01:19:04 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Wed, 10 May 2023 01:19:13 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='b16c0271899de1f0e277dc0398bfff11b54511765f104fa938929ac484dc926d';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.1_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43ad054f135a7894dc87ad5d10ad45d8e82846186515892acdbc17c2c5cd27e4';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:19:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 01:19:16 GMT
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
	-	`sha256:28b67f34195549647f10a482e8afd47c6ac3909ec039f6525de8e44bd990564c`  
		Last Modified: Wed, 10 May 2023 01:22:24 GMT  
		Size: 202.8 MB (202821112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15f2866ed2b416a03753bff4db03a19b81ac0ebc615e9d8f5398de45274d4a4`  
		Last Modified: Wed, 10 May 2023 01:22:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:844a5edb047de627ce4d0ee13bffba7d29526e6199494133b5e541f59da4aa00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265655998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed2c21b66e3c47fef5285e936f6999160eef1b1fec06ed60eec72c13752e73`
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
# Wed, 10 May 2023 01:12:39 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Wed, 10 May 2023 01:12:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='b16c0271899de1f0e277dc0398bfff11b54511765f104fa938929ac484dc926d';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.1_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='43ad054f135a7894dc87ad5d10ad45d8e82846186515892acdbc17c2c5cd27e4';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 10 May 2023 01:12:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 May 2023 01:12:51 GMT
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
	-	`sha256:3b622a120b0f603c09a7c54a4c41848b3fbe17dc30b55a5ab4f7c75ef89b4fa3`  
		Last Modified: Wed, 10 May 2023 01:15:37 GMT  
		Size: 201.2 MB (201163797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296e3aee46640455b34faa8687414ec051d69a58b1c84f2d72861ba5ff783d56`  
		Last Modified: Wed, 10 May 2023 01:15:25 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
