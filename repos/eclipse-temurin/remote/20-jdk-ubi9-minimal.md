## `eclipse-temurin:20-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:4afc9ef181559b3b77fe078f3ae328c044a39d01e5a7a1744f07cd5cdb8ab9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:20-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:da54b240d48fba33c0bf74c41829e7fed5c110e0c35563c270d7cdde42d0e61c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219529545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf8edcd9297aef0fb03712fd47cd92ba48a087d1462bc31f0f213544602381d`
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
# Wed, 13 Sep 2023 00:14:14 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 00:14:24 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='b475bcc23db0bd618c815bb8f11d8e084dc58288ea3bcdf4e7f389ed41c89f56';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d91842e9c172967ac397076523249d05a82ead51b0006838f5f0315ad52222c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:14:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:14:26 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:14:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:14:26 GMT
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
	-	`sha256:9cb86257bb0a7c4614655aeee6cca65ded50d16694fed501ce6f2c9eb36743a9`  
		Last Modified: Wed, 13 Sep 2023 00:18:27 GMT  
		Size: 153.8 MB (153797105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbf67c0a0b2444c3405a475903accf18a77ae1cada5725eb263cdcaf5540089`  
		Last Modified: Wed, 13 Sep 2023 00:18:14 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5d1de79bf0260b9b06f7eebe5512f39501856565cf2ccf60ad0c9b0c01f134`  
		Last Modified: Wed, 13 Sep 2023 00:18:14 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f3c869ce92eb69ceb93e0016df382bf13bfd663fed3cb473184014ed358d2085
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216563400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eef46ecdd8ed49a89ebe5267db77ab834744389241a72c610f9779ab0f7ca4`
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
# Wed, 13 Sep 2023 00:52:00 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 00:52:10 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='b475bcc23db0bd618c815bb8f11d8e084dc58288ea3bcdf4e7f389ed41c89f56';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3d91842e9c172967ac397076523249d05a82ead51b0006838f5f0315ad52222c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 13 Sep 2023 00:52:13 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 00:52:13 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Wed, 13 Sep 2023 00:52:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 Sep 2023 00:52:13 GMT
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
	-	`sha256:b9eb3207fa9f0448e873974793021a4fe6cae3bfba18a1a6199537efc107a9cd`  
		Last Modified: Wed, 13 Sep 2023 00:55:36 GMT  
		Size: 152.1 MB (152125700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd8624c53ea9607146784510f0cfb644d6e3f5a9bebcb18791ed3fa13d034f6`  
		Last Modified: Wed, 13 Sep 2023 00:55:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf41e55517af4bdd82de479bd4f90bd4e7020ddcb3740d44308581adaab5ca30`  
		Last Modified: Wed, 13 Sep 2023 00:55:26 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
