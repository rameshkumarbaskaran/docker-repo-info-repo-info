## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:b49126e615b3ce49faab37b2d32d5e29bcdb550441b40e621ee6bde650ed27ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a263442866e3a3b9fd89f12ab0c7566414a073f7c25afbbc3f26ca74b2ab402b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210514194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3399caee86b4355ff594cade56e035a11fd73d36a534639c62813d0c7d66cc11`
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
# Wed, 13 Sep 2023 00:13:38 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 00:13:46 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:13:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:13:48 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:13:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:13:48 GMT
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
	-	`sha256:1e47199250c4b185f39de1ca0739409e3ca564728fde072596683a83b8fb336f`  
		Last Modified: Wed, 13 Sep 2023 00:17:41 GMT  
		Size: 144.8 MB (144781754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973e0b7c1c00f1d0e65d19ab1fb8eb0a263bffd159ca8f01c1dc101704981c85`  
		Last Modified: Wed, 13 Sep 2023 00:17:29 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09f4f3e1b515cbabf64b80b23353ba477b0b3a20c2de4d52f49b81681a1ba2`  
		Last Modified: Wed, 13 Sep 2023 00:17:29 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ebdc7e550e01e626ad9b79d1c8d1478d75cab33176f62e86fd62cae3a615d4a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207986604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36220f29e02966ef186aa8acb388b4876d792bf8507ac89ea38b7255737500a`
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
# Wed, 13 Sep 2023 00:51:31 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 00:51:41 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:51:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:51:44 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:51:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:51:44 GMT
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
	-	`sha256:d5b6f4b5d57703df3ff812bc78e545e95e36f49ae04f007b85e56328d88e8990`  
		Last Modified: Wed, 13 Sep 2023 00:54:51 GMT  
		Size: 143.5 MB (143548907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaedb8dd94df54c683e05acbad8f5713fae9ef812238f7c40cb0a77314a98a1e`  
		Last Modified: Wed, 13 Sep 2023 00:54:41 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5984a8c440bf6e474b2c04c5c4a96a69700bd52bed5c70e1bb25c4d6b2f4863f`  
		Last Modified: Wed, 13 Sep 2023 00:54:41 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:bdaea3b07fdb7011696ba5f4eb10485f93264ac3bbe1324dfa6d8f4376665001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217212881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90b9b1d527bebb764f1f78bd991e9b523fa80ece463e6c7f10eb08b8879f7d9`
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
# Wed, 13 Sep 2023 00:22:18 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 00:22:35 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:22:42 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:22:42 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:22:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:22:43 GMT
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
	-	`sha256:b3d074c5ab1ca0ecb7e2a9b4dd98d1259c47d5503488214a92df9c7d55b8376c`  
		Last Modified: Wed, 13 Sep 2023 00:25:58 GMT  
		Size: 144.5 MB (144512759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322608cadac5c019ef8f03cbaa47e8b0e860e8da452472e13b5a00cd9041406a`  
		Last Modified: Wed, 13 Sep 2023 00:25:38 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e21fc76e56fe44504452def549de8cd3c15e64b8b9185530edf8732127f8c9`  
		Last Modified: Wed, 13 Sep 2023 00:25:38 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:95ca4a4407f886f1b285f6efacf5a68c050cd5e454482584e7802b2592ea4dde
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198244273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8400247c8f70b9e1790c66aadb4750bfd8717b17ea14d31d0ad830f3f2f78a`
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
# Tue, 12 Sep 2023 23:59:08 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 12 Sep 2023 23:59:16 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 12 Sep 2023 23:59:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Sep 2023 23:59:22 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 12 Sep 2023 23:59:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 Sep 2023 23:59:22 GMT
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
	-	`sha256:db9206730268155909a560c4f77b28fc2904bdb66b0775f7ec0d7aefa89e41f3`  
		Last Modified: Wed, 13 Sep 2023 00:01:19 GMT  
		Size: 134.2 MB (134215617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6600f40c13175c225b7238e4e9003b0cc3ec7ab8468affa11c791e29c2e615f`  
		Last Modified: Wed, 13 Sep 2023 00:01:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94e86f8fff2decd238a238e5240b47f05ed801904618a5a7661652bcba29d13`  
		Last Modified: Wed, 13 Sep 2023 00:01:09 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
