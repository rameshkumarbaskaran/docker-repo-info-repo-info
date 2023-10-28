## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:52f588cff3d9e0b828ace9020d6310fd2d42c45d087e0dc018b3dc97f286e2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:1b7ccf2a520a33e8e6e28536cbc173203fa59dd78726974cb34b63f08307cc0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.1 MB (806139821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a1cca9b050bea5650f572936a08353d0b82e3a1ab84898fee7c4026f7f4074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Oct 2023 11:43:01 GMT
ADD file:ac79b39564366abf518db1877bec9e7decc48d98d62df0901810df3f6551517c in / 
# Wed, 18 Oct 2023 11:43:02 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 11:43:02 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 11:43:03 GMT
ADD multi:12e0f830418c4a74b6b1be700d93192adbe117072dc2de691398011ca651d375 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 11:43:03 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 18 Oct 2023 11:43:03 GMT
ENV container oci
# Wed, 18 Oct 2023 11:43:03 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 11:43:03 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 11:43:03 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 11:43:04 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 18 Oct 2023 11:43:04 GMT
ADD file:c8a182b1e2945588635709f7de8e002d33cd9a632a6470d85cb8501d7a8192c8 in /root/buildinfo/content_manifests/ubi9-container-9.2-755.1697625012.json 
# Wed, 18 Oct 2023 11:43:05 GMT
ADD file:5c7256801438a54a3366c233fa64ceb409db6c2e818388725faaa238ad398a00 in /root/buildinfo/Dockerfile-ubi9-9.2-755.1697625012 
# Wed, 18 Oct 2023 11:43:05 GMT
LABEL "release"="755.1697625012" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:30:28" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-755.1697625012"
# Wed, 18 Oct 2023 11:43:06 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460167-244af.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 18 Oct 2023 11:43:06 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 11:43:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:20:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 28 Oct 2023 00:20:45 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 28 Oct 2023 00:21:00 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Sat, 28 Oct 2023 00:21:00 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 28 Oct 2023 00:21:01 GMT
ARG SWIFT_PLATFORM=ubi9
# Sat, 28 Oct 2023 00:21:01 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Sat, 28 Oct 2023 00:21:01 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Sat, 28 Oct 2023 00:21:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 28 Oct 2023 00:21:01 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 28 Oct 2023 00:21:51 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 28 Oct 2023 00:21:57 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:cc7c08d56aada5b55c0b4a8ecc515a2fa2dc25a96479425437ff8fefa387cc20`  
		Last Modified: Thu, 19 Oct 2023 00:53:46 GMT  
		Size: 78.1 MB (78066310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeef0e8321022948e607c53324f196dda586b6802e67a0d425689b8824ffaa7`  
		Last Modified: Sat, 28 Oct 2023 00:28:07 GMT  
		Size: 120.9 MB (120949633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527bd29277a6bb10a09530efdbf9c1207eed853d7c8189fb0f694352e8b049f`  
		Last Modified: Sat, 28 Oct 2023 00:29:13 GMT  
		Size: 607.1 MB (607123680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b87a3945adcc45e4b830496b60459909ed4c58b74d8994a83dd4824187a5f00`  
		Last Modified: Sat, 28 Oct 2023 00:27:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:622c21c7e84fd599170680fd32310b5227afb4b4815b4ac251c0226dcd4328c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **792.6 MB (792619702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90948ee6a8dd26aa874e43ed3f4ac2d15608e7de0639f3a2681fa3a4416be201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Oct 2023 11:43:00 GMT
ADD file:25cb472a1cb6204a2d2fe11696cbbc1bc8d4796bec550d6c69dd19f0482769f9 in / 
# Wed, 18 Oct 2023 11:43:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 11:43:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 11:43:01 GMT
ADD multi:12e0f830418c4a74b6b1be700d93192adbe117072dc2de691398011ca651d375 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 11:43:01 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 18 Oct 2023 11:43:01 GMT
ENV container oci
# Wed, 18 Oct 2023 11:43:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 11:43:01 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 11:43:03 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 11:43:04 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 18 Oct 2023 11:43:04 GMT
ADD file:22c68d8978210e6d1b513f22f8e5360b9997ba70a5944a0adafd1b92a41de019 in /root/buildinfo/content_manifests/ubi9-container-9.2-755.1697625012.json 
# Wed, 18 Oct 2023 11:43:04 GMT
ADD file:cac24251905b5f4d6edc6ade55bca32660ccba335705157865a761c52443b781 in /root/buildinfo/Dockerfile-ubi9-9.2-755.1697625012 
# Wed, 18 Oct 2023 11:43:04 GMT
LABEL "release"="755.1697625012" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:30:28" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-755.1697625012"
# Wed, 18 Oct 2023 11:43:05 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460167-244af.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 18 Oct 2023 11:43:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 11:43:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 28 Oct 2023 00:17:06 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 28 Oct 2023 00:17:18 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Sat, 28 Oct 2023 00:17:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 28 Oct 2023 00:17:19 GMT
ARG SWIFT_PLATFORM=ubi9
# Sat, 28 Oct 2023 00:17:19 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Sat, 28 Oct 2023 00:17:19 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Sat, 28 Oct 2023 00:17:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 28 Oct 2023 00:17:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 28 Oct 2023 00:17:58 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 28 Oct 2023 00:18:10 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:dfd70797773c6a771805ef340c4276c82be1f572dd4784998b2013ff4c558f3f`  
		Last Modified: Thu, 19 Oct 2023 00:57:34 GMT  
		Size: 75.8 MB (75821852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c36c513ff7e83d9f3cc5b25f549ec065a01ebb2f6c6e6e464bd1fc57ef42a06`  
		Last Modified: Sat, 28 Oct 2023 00:21:50 GMT  
		Size: 115.1 MB (115094611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6db4c16a68d90460b22c744e44346b62ffacbd5c61dc6e3285ddbb51ebe845`  
		Last Modified: Sat, 28 Oct 2023 00:22:39 GMT  
		Size: 601.7 MB (601703040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d6ce6ddac033a358a2da7ead43f9bd03319aef8def90944593f3870151af99`  
		Last Modified: Sat, 28 Oct 2023 00:21:40 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
