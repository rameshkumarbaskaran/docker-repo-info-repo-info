## `eclipse-temurin:20-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a374abe2a729ce6c742110a076a515ba47ca92c48491194a07002e54cf7e8e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:20-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bde2260802c94ed0a47b60ec8947984e70000a35833ea50c5e573759aece7fbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116009180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfc7ff54459b03ff74c631dec53c55374d552d125c3f742d78ceae1a07bd6e8`
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
# Tue, 10 Oct 2023 23:51:19 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Tue, 10 Oct 2023 23:51:45 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='63a730d5a3b6d21d31f7cba15dc44b019a8a4d8652e13acec45040f98584112c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e3592e86290c192804d9c6b5035d42cc32cf04141d1c0b9d1ecb67739826c8c5';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:51:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 10 Oct 2023 23:51:46 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:51:46 GMT
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
	-	`sha256:baaba4680d4f71ec4ae1cfd53e48cde615a33f8229da42c82c6017682ec1455f`  
		Last Modified: Tue, 10 Oct 2023 23:55:41 GMT  
		Size: 50.3 MB (50301294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b18c65309c191ade09cf711808a006945e677af1795964ba6d6e96206ed891a`  
		Last Modified: Tue, 10 Oct 2023 23:55:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992adb158aeec42e1bd5e1a8cad38e0a34a357c0c682604e6c494a6758cbe2a9`  
		Last Modified: Tue, 10 Oct 2023 23:55:33 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:92bd71c71bae3de7d8269265ab29ccd3159b4e07b586d1e8d27c6f927a4dbb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113928147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46502a1fcfded317d610faf07d78063e7b7d7f558b24a4f5c84c24ef2930f154`
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
# Tue, 10 Oct 2023 23:52:32 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Tue, 10 Oct 2023 23:52:53 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='63a730d5a3b6d21d31f7cba15dc44b019a8a4d8652e13acec45040f98584112c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e3592e86290c192804d9c6b5035d42cc32cf04141d1c0b9d1ecb67739826c8c5';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:52:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 10 Oct 2023 23:52:55 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:52:55 GMT
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
	-	`sha256:ade0dc3ddbfbd442524919ba30b098c12875e264a15b80f71ccc7c108e941233`  
		Last Modified: Tue, 10 Oct 2023 23:56:00 GMT  
		Size: 49.5 MB (49508088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1fba8ffefe7a698c1d6f9949691ae981a25f8fbed04ab298eb325d99c48dcc`  
		Last Modified: Tue, 10 Oct 2023 23:55:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c26e3ba373cb01b46d5f8f6cdce9c902c59c5919dfcb9f4d915c3e2db03a6d2`  
		Last Modified: Tue, 10 Oct 2023 23:55:54 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
