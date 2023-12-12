## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:3b20ade5b4bba72969f7f673e94a990f17a1af778390955590666095245b2d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:1bb27411b1aa1f39ed1455b421e7fd380b936c10b43fe90c0afbee0afa9b6d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124204684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8668dcce90a36d839f664178658911d4a216715e498a75560139c53865d265f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Nov 2023 16:57:21 GMT
ADD file:51365bf81ffef571b9cae6537437d1cb9578bf45d8b6a353848d4bbc24583ace in / 
# Thu, 09 Nov 2023 16:57:22 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:57:22 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:57:23 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:57:23 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 09 Nov 2023 16:57:23 GMT
ENV container oci
# Thu, 09 Nov 2023 16:57:23 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:57:23 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:57:23 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:57:24 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 09 Nov 2023 16:57:24 GMT
ADD file:b21f5a973eb1a7e7cede8eb88bab4f034175bf01de661263540b4722655ec4b1 in /root/buildinfo/content_manifests/ubi9-container-9.3-1361.1699548029.json 
# Thu, 09 Nov 2023 16:57:25 GMT
ADD file:81c5ce84fbc74763cd36dea9ef0064ee0c92125a77a579cfbb4a026beeb7be4f in /root/buildinfo/Dockerfile-ubi9-9.3-1361.1699548029 
# Thu, 09 Nov 2023 16:57:25 GMT
LABEL "release"="1361.1699548029" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:44" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1361.1699548029"
# Thu, 09 Nov 2023 16:57:26 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:57:27 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:57:29 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:17:31 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 17 Nov 2023 04:17:32 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 17 Nov 2023 04:18:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 17 Nov 2023 04:18:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 12 Dec 2023 00:32:26 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Tue, 12 Dec 2023 00:32:26 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Tue, 12 Dec 2023 00:32:26 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Dec 2023 00:32:26 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Dec 2023 00:33:00 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:b824f4b30c465e487e640bdc22e46bafd6983e4e0eabf30085cacf945c261160`  
		Last Modified: Wed, 15 Nov 2023 11:22:54 GMT  
		Size: 78.8 MB (78771519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cefbf1f6c554f310e1ac1aeebb94e837f27148ee48e944c3910bc713cb94e0c`  
		Last Modified: Tue, 12 Dec 2023 00:45:49 GMT  
		Size: 45.4 MB (45433165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:521fe23f7916ae6bfe5ab6ca3e4aa487c9f56cccef75f37b942aabe6ba8aa826
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120557966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a3abaaa9b3e68f529524ccfc1adf8885886bc34794148eb62ee88955b9e5bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Nov 2023 16:57:17 GMT
ADD file:205960a3d0706f085c18728490f06b5e7fd7a132ab6b07a95a4ed18f00e126f4 in / 
# Thu, 09 Nov 2023 16:57:18 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 09 Nov 2023 16:57:18 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 09 Nov 2023 16:57:18 GMT
ADD multi:af962ebf871d89c5885926949add253d557f4af2063b876a12e675ae0ac48a6d in /etc/yum.repos.d/ 
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Nov 2023 16:57:18 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 09 Nov 2023 16:57:18 GMT
ENV container oci
# Thu, 09 Nov 2023 16:57:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Nov 2023 16:57:18 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 16:57:19 GMT
RUN rm -rf /var/log/*
# Thu, 09 Nov 2023 16:57:20 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 09 Nov 2023 16:57:20 GMT
ADD file:0b626ed84dc2ce267bf6b274208582760edaf2c022f3194ac8260153cafce9d1 in /root/buildinfo/content_manifests/ubi9-container-9.3-1361.1699548029.json 
# Thu, 09 Nov 2023 16:57:21 GMT
ADD file:a85c30847dff015a401ef205805a5a71cc706ae037b798d7b69c0465edec50a7 in /root/buildinfo/Dockerfile-ubi9-9.3-1361.1699548029 
# Thu, 09 Nov 2023 16:57:21 GMT
LABEL "release"="1361.1699548029" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-09T16:40:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1361.1699548029"
# Thu, 09 Nov 2023 16:57:22 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2540020-1b8c0.repo' '/etc/yum.repos.d/gitweb-15c2e.repo'
# Thu, 09 Nov 2023 16:57:23 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 09 Nov 2023 16:57:25 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:33:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 17 Nov 2023 03:33:06 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 17 Nov 2023 03:34:28 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 17 Nov 2023 03:34:28 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 11 Dec 2023 23:57:35 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Mon, 11 Dec 2023 23:57:35 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Mon, 11 Dec 2023 23:57:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 11 Dec 2023 23:57:35 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 11 Dec 2023 23:58:10 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:19dd821b7a83bf1ad388914394494ea983308667df914c57a315c52e312eb2c4`  
		Last Modified: Wed, 15 Nov 2023 11:22:52 GMT  
		Size: 76.5 MB (76512185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63f7339aaa9db9cf4b4ae30e725cada44458101493943d958b40d83ee5acb31`  
		Last Modified: Tue, 12 Dec 2023 00:05:22 GMT  
		Size: 44.0 MB (44045781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
