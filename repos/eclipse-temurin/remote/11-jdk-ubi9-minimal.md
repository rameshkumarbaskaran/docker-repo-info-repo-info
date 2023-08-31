## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:26b671e7decb893fecb86dc4dbca129bf983873fd7c403afaa761eb6d2e887ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6d80f7920231342bc066c9b011dbf436b1f1dacd7cd6d4cb1062935f70ee0280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206976295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b832460992214ed4c44f90bef18ac182d4bdc8ed1977721cfac5b3bf80b701fe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jul 2023 14:57:46 GMT
ADD file:f3010bd586bc7794afba95160a7961e057f655d5b4f52d06b705e2a617017edd in / 
# Wed, 26 Jul 2023 14:57:47 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:57:47 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:57:48 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:57:48 GMT
ENV container oci
# Wed, 26 Jul 2023 14:57:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:57:48 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:57:50 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:b7b8ba930a63f130e5b521d20879b60b1bcaf936b24117776d0b51c2b48d2a4d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:b4ab85020f52e63c65078dbea52129cc08eeebd3d7249aa486338819331ac9f4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:57:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:57:52 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:57:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:57:55 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 01 Aug 2023 23:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 23:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 23:26:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Aug 2023 23:26:52 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 31 Aug 2023 20:22:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:22:45 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 31 Aug 2023 20:22:47 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:22:47 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:22:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:22:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:684e2f1d925d1b205883b677fc893b5275192cfc90efd1fa51a90e1da256c4e0`  
		Last Modified: Tue, 01 Aug 2023 12:07:07 GMT  
		Size: 37.8 MB (37822945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2828cc08e260989d3b1f2221bf07fc5e520511e23bc5b395498e083c91b1f6b`  
		Last Modified: Tue, 01 Aug 2023 23:30:20 GMT  
		Size: 27.9 MB (27866608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc04a999864ab696e92aef69b7184f6fa41b20ef705027ebb2f0f68f0636c1d`  
		Last Modified: Thu, 31 Aug 2023 20:28:29 GMT  
		Size: 141.3 MB (141285853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceeffd4c81c86591594b10e1c26ad08c09857021ce2196f6091bafb2e4774510`  
		Last Modified: Thu, 31 Aug 2023 20:28:18 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0699a8bedcf531baf83632b0fd2c07bbf9fd4d8ff0035e6918fd1219c532678f`  
		Last Modified: Thu, 31 Aug 2023 20:28:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:809700467e8ccbedbdb4af6b865f3d5d33719a146133f14342f7cc5e694a6b08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202454150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8052ed52f9dbf6bb7f690aaaac51d55802ac259c34ca32c0889ebc17f99f63`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jul 2023 14:58:04 GMT
ADD file:8d7c0f622c108d1e429ca4709a9dda0c55a5dd4cf1e5e2870676045dce7caeba in / 
# Wed, 26 Jul 2023 14:58:05 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:58:05 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:58:05 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:58:05 GMT
ENV container oci
# Wed, 26 Jul 2023 14:58:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:58:05 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:58:07 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:58:07 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:58:07 GMT
ADD file:14e3121d95013deb0e4913aeb325fcf7bbf604080f2fc69e396fcf1a88bc8897 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:58:07 GMT
ADD file:ba1f369d1b07d713c5215a52333de8398076c4ecb9e2b6628520422b2da2b65a in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:58:07 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:58:08 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:58:09 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:58:11 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 02 Aug 2023 00:03:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Aug 2023 00:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Aug 2023 00:03:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Aug 2023 00:03:52 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 31 Aug 2023 20:41:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:41:43 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 31 Aug 2023 20:41:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:41:46 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:41:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:41:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9624f58f605cb9332696a166f1617f4e6d7fb1060bba9b0ea2aac67daac0dc73`  
		Last Modified: Tue, 01 Aug 2023 12:07:13 GMT  
		Size: 36.1 MB (36130176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78179c51ffbc35adfff015fcabffcfccefa9d8913285f7c8e6fecba7de53d28b`  
		Last Modified: Wed, 02 Aug 2023 00:06:38 GMT  
		Size: 28.3 MB (28290560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af02303d1eb2b413f2a82bec97b598ca87ee7c4f229852baf80d51e1365063a`  
		Last Modified: Thu, 31 Aug 2023 20:45:46 GMT  
		Size: 138.0 MB (138032530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee1ed749a6aca2e082d538a4913bae0f6a8f561f5795bd7475f0f6ef8387703`  
		Last Modified: Thu, 31 Aug 2023 20:45:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f53b7ef8be1c57d7b2dea831b0381d26ab2164c8f39e520e301abf1ca40547`  
		Last Modified: Thu, 31 Aug 2023 20:45:37 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:fb73ee594ea858ce9b23bd68b81adac08a0030e23f4f6e74a1ac8e1db80c3478
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201199161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19471071e83ad221a10124ba4b075b7b8eb6ab42f196135070ef4d9c723188a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jul 2023 14:57:48 GMT
ADD file:0c441962aa29a3affc408ed5089865900d38e4b549824783248a665571d42ebf in / 
# Wed, 26 Jul 2023 14:57:50 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:57:50 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:57:50 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:57:50 GMT
ENV container oci
# Wed, 26 Jul 2023 14:57:50 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:57:50 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:57:51 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:57:51 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:a666bb3210193c7a955c3cec15b42d917e019faddf36ddc2545c81fc7f9ee928 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:57:52 GMT
ADD file:688393c03d435532347f62afef64019a0b40f85408be8040970afc31de6816e2 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:57:52 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:57:53 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:57:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:57:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 01 Aug 2023 23:16:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 23:16:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 23:16:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Aug 2023 23:18:28 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 31 Aug 2023 20:18:09 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 20:18:24 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 31 Aug 2023 20:18:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:18:30 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:18:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:18:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8458a49a58a9ceefce8feddf47e6c6d5ac3416b39eddb7e6a86407b47b94d1cb`  
		Last Modified: Tue, 01 Aug 2023 12:07:20 GMT  
		Size: 42.3 MB (42290376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2713fd75507be3000cb44286c34e36d1b211a49c77956a228a83323a08e1d`  
		Last Modified: Tue, 01 Aug 2023 23:26:03 GMT  
		Size: 30.4 MB (30421820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0c32957baefeaaab3b0de3fbf929faea6ae44dc6c8de8e3f7ba75d668fd54`  
		Last Modified: Thu, 31 Aug 2023 20:25:27 GMT  
		Size: 128.5 MB (128486076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0812dfba134ad48dfb0486426e9dea9be83980c7d0d777a352e71cf18af2d823`  
		Last Modified: Thu, 31 Aug 2023 20:25:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43539dc6c986cfd48e552766d33f932de806cf276b8d11a7a9b3033e737896e`  
		Last Modified: Thu, 31 Aug 2023 20:25:10 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b4ad2d505b3a41f8e59ec950ee69c1cc86d67bed126c352baafa77b511391860
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185621904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803aa1b0b9ecfa271a030b56cbc5cd05af4e567589e1b4113f1f8fc2b4e690ef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Jul 2023 14:57:52 GMT
ADD file:50c5df782f68dae0c892e7172130120932a58ce6adc6a40f2a32d7d564165254 in / 
# Wed, 26 Jul 2023 14:57:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:57:53 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:57:54 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:57:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:57:54 GMT
ENV container oci
# Wed, 26 Jul 2023 14:57:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:57:54 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:57:55 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:57:55 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:57:55 GMT
ADD file:0d7205c1b35756cf4b3cf99c1d6b2c557ec3210a870849364ad266a8e0f8d4c6 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:57:56 GMT
ADD file:11fe098cf4639d6f57b6bb2073606711b79ce6b364d3eeea4728668630edaa48 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:57:56 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:57:57 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:57:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:58:00 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 01 Aug 2023 21:44:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 21:44:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 21:44:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Aug 2023 21:44:20 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 31 Aug 2023 19:42:31 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 31 Aug 2023 19:42:39 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 31 Aug 2023 19:42:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 19:42:44 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 19:42:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 19:42:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38254e87d22384fb9d1de9b4ee962129b7559d571981b6433e1ce7e91d195ca1`  
		Last Modified: Tue, 01 Aug 2023 12:07:27 GMT  
		Size: 36.2 MB (36155872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2908851dfb78af9604539200130553a34f29efae9ee8b34aa0332fccc24fb7e4`  
		Last Modified: Tue, 01 Aug 2023 21:47:01 GMT  
		Size: 27.9 MB (27920214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeb39b8299118a0a3a3189d38d9b716ec6455b66bb0c89533f8bd66aba9b7c4`  
		Last Modified: Thu, 31 Aug 2023 19:46:19 GMT  
		Size: 121.5 MB (121544929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3b38b1d66ce68cbce8b89c79aa129240897f4acad52a0de74edbd7c183cfc9`  
		Last Modified: Thu, 31 Aug 2023 19:46:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7400f087a53f9979cda185e1b175b7bf7590e5f6dec58d13ce5c1559120d34`  
		Last Modified: Thu, 31 Aug 2023 19:46:10 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
