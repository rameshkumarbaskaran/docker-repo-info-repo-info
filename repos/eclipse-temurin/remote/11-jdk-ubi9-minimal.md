## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:979a1a5e213aee0f3566abdf6579b662a7afbaed7a8a6620796685147bf3a8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:12884d4d977f2c40d6b5476afa1bb70654564c48c82be5173d8c375fef79ecda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207335216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9939c32def015766fd7186debfb5ef69554e31f23f9ce34578a39f2cc428275c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 17 Nov 2023 04:10:54 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Fri, 17 Nov 2023 04:11:01 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c3146035b99c55ab26a2982f4b9abd2bf600582361cf9c732539f713d271faf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='60ea98daa09834fdd3162ca91ddc8d92a155ab3121204f6f643176ee0c2d0d5e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='262ff98d6d88a7c7cc522cb4ec4129491a0eb04f5b17dcca0da57cfcdcf3830d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bc67f79fb82c4131d9dcea32649c540a16aa380a9726306b9a67c5ec9690c492';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 04:11:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 17 Nov 2023 04:11:04 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 04:11:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Nov 2023 04:11:04 GMT
CMD ["jshell"]
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
	-	`sha256:6bd7d80b23b002de91f76ca039c7b3a03db11c9af2c112942f3b8c8bfc6495f1`  
		Last Modified: Fri, 17 Nov 2023 04:14:29 GMT  
		Size: 141.7 MB (141731227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a701bba2e92b54fdfffb2b2bfc681cf62611d7ed3450d75471f28663fb0d925b`  
		Last Modified: Fri, 17 Nov 2023 04:14:18 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275172df8cd670688006b9037ad3111432cb0c3d74dfe082f7241263e023b0b5`  
		Last Modified: Fri, 17 Nov 2023 04:14:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e0c0a782ea0bea2cc7356d3d3b05a7b9024d812515ce83f6bb4f7c7eb2ebbf2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202801269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37ea8ad785805afe7b06999b81ffa4e4a2b2e4d969fb9e61d0316e9335703f4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 17 Nov 2023 03:27:30 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Fri, 17 Nov 2023 03:27:37 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c3146035b99c55ab26a2982f4b9abd2bf600582361cf9c732539f713d271faf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='60ea98daa09834fdd3162ca91ddc8d92a155ab3121204f6f643176ee0c2d0d5e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='262ff98d6d88a7c7cc522cb4ec4129491a0eb04f5b17dcca0da57cfcdcf3830d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bc67f79fb82c4131d9dcea32649c540a16aa380a9726306b9a67c5ec9690c492';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 03:27:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 17 Nov 2023 03:27:40 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 03:27:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Nov 2023 03:27:40 GMT
CMD ["jshell"]
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
	-	`sha256:950fc8d528af84417589d43ee97d3cc9a5c7c837f49ba7313abf6d2e98e072f6`  
		Last Modified: Fri, 17 Nov 2023 03:30:23 GMT  
		Size: 138.5 MB (138467355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28024df1b2982761ee2b141cd097fc6d3b3144db003996cafcd719d24999a9f4`  
		Last Modified: Fri, 17 Nov 2023 03:30:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74179f6fb7488d31f1fe672eebd587d5cbff7f603f4b83c4efc7479b73497cc`  
		Last Modified: Fri, 17 Nov 2023 03:30:12 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8bdf2f20cde9ad37bd8bb0f0e00cee29e86dd70b55ab222bb0670bc71dc491d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201437245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c95dbcf3bbbf97b40cce07a531a2f875d06d295e2c1069228cdcb7303dadd8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Fri, 17 Nov 2023 03:48:26 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Fri, 17 Nov 2023 03:48:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c3146035b99c55ab26a2982f4b9abd2bf600582361cf9c732539f713d271faf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='60ea98daa09834fdd3162ca91ddc8d92a155ab3121204f6f643176ee0c2d0d5e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='262ff98d6d88a7c7cc522cb4ec4129491a0eb04f5b17dcca0da57cfcdcf3830d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bc67f79fb82c4131d9dcea32649c540a16aa380a9726306b9a67c5ec9690c492';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 03:48:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 17 Nov 2023 03:48:52 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 03:48:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Nov 2023 03:48:53 GMT
CMD ["jshell"]
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
	-	`sha256:5b013d2fb294dfd4fdbf006d5cdb5c2f56c361942d2a9317f061c430bcb7214b`  
		Last Modified: Fri, 17 Nov 2023 03:54:02 GMT  
		Size: 128.9 MB (128903366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0d3fcd341811280019c418096fbbf660980e152fee0e22e1b74366c67bec49`  
		Last Modified: Fri, 17 Nov 2023 03:53:51 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294fae3accb3cf7903078cdd4337de3275b45c544b2a75a6a39f550909126b19`  
		Last Modified: Fri, 17 Nov 2023 03:53:50 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f3ed5ed05ef631ef16d23e795faff519ce8fa8da3536724d401add94e15bad13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b882fa28b0fbdc2bb203d9e40a6e8ce3c85916dea98cd5fe78175ab1b58e6eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Nov 2023 16:53:45 GMT
ADD file:95f6aad3eab79a5d9bde68a70bcaa0743b97fface89a95dfff736c2d40842c30 in / 
# Thu, 09 Nov 2023 16:53:47 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:53:47 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:53:48 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:53:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Nov 2023 16:53:48 GMT
ENV container oci
# Thu, 09 Nov 2023 16:53:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:53:48 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:53:49 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:53:50 GMT
ADD file:e8c6090ad37e0d55fd43ba23141df14b3e21dc9e9a6c478674ba7cfe3ce3a092 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1361.1699548032.json 
# Thu, 09 Nov 2023 16:53:50 GMT
ADD file:2aa97e2f3da535bb1c68e20c3dfe01d0be179495a42dc7f013ddb7677cca2310 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1361.1699548032 
# Thu, 09 Nov 2023 16:53:50 GMT
LABEL "release"="1361.1699548032" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:47" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1361.1699548032"
# Thu, 09 Nov 2023 16:53:51 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:53:53 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:53:54 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:49:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Nov 2023 03:49:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 17 Nov 2023 03:49:23 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Fri, 17 Nov 2023 03:49:31 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c3146035b99c55ab26a2982f4b9abd2bf600582361cf9c732539f713d271faf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.21_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='60ea98daa09834fdd3162ca91ddc8d92a155ab3121204f6f643176ee0c2d0d5e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.21_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='262ff98d6d88a7c7cc522cb4ec4129491a0eb04f5b17dcca0da57cfcdcf3830d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.21_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bc67f79fb82c4131d9dcea32649c540a16aa380a9726306b9a67c5ec9690c492';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 17 Nov 2023 03:49:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 17 Nov 2023 03:49:37 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Fri, 17 Nov 2023 03:49:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Nov 2023 03:49:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c5602414fe6a5d98e900c61aaab466a759c5f1eb279f0e29f8f5287547466c8`  
		Last Modified: Wed, 15 Nov 2023 12:10:25 GMT  
		Size: 36.0 MB (36023178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375b232debe50fd1a1dc141906098d31c68d92d50cd42311b3fc59c7666bd28b`  
		Last Modified: Fri, 17 Nov 2023 03:51:55 GMT  
		Size: 27.9 MB (27926997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f36fee453fb2a14dc914a5f1a253ea258abc379cb26019d2a2dbb64ffc9cf3`  
		Last Modified: Fri, 17 Nov 2023 03:52:00 GMT  
		Size: 121.8 MB (121806704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5da9e0a8538dc2a4f9ece8dfc49159c417f352ce5404286ce0f61a04ffdc151`  
		Last Modified: Fri, 17 Nov 2023 03:51:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73551bf4bd1f31b2e416924cc60e736dd872c6ffe83c267338efe0e0da9a7ea`  
		Last Modified: Fri, 17 Nov 2023 03:51:51 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
