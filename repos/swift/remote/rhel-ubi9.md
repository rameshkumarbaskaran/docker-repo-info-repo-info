## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:828fa2657ba0023778a5c901246e61bcd53a909352cf493f50a5b7b5d47414d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:de5692ab4d8566ad609f3f6028246f4508382013c7dcb658edd12cf71a25deae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.3 MB (756260714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57e12e075d1c9aa492c21d8c7ca17283cd676b946e4938df8d3ec37d4641ebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 05 Sep 2023 09:12:58 GMT
ADD file:23767f338b8937e3b109b7fdcb0bd8089e6d4d5101f347c2fa71aff03067f04e in / 
# Tue, 05 Sep 2023 09:12:59 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 05 Sep 2023 09:12:59 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 05 Sep 2023 09:12:59 GMT
ADD multi:724ed0e3f3beae9b8bce7fd72262ce34617b5e89ed2a1257879bb55c22d53483 in /etc/yum.repos.d/ 
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 05 Sep 2023 09:12:59 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 05 Sep 2023 09:12:59 GMT
ENV container oci
# Tue, 05 Sep 2023 09:12:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Sep 2023 09:12:59 GMT
CMD ["/bin/bash"]
# Tue, 05 Sep 2023 09:13:00 GMT
RUN rm -rf /var/log/*
# Tue, 05 Sep 2023 09:13:00 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 05 Sep 2023 09:13:00 GMT
LABEL release=755
# Tue, 05 Sep 2023 09:13:01 GMT
ADD file:166857615ef4c89f9f1fbf2c5b9d936738e86cd40ed5b9e3bf7d54cd2719727c in /root/buildinfo/content_manifests/ubi9-container-9.2-755.json 
# Tue, 05 Sep 2023 09:13:01 GMT
ADD file:c90f7bbcedb8bccb78e2d2ac0b760812d6024cdd06f02e621a204668c03e8feb in /root/buildinfo/Dockerfile-ubi9-9.2-755 
# Tue, 05 Sep 2023 09:13:01 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-09-05T09:00:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-755"
# Tue, 05 Sep 2023 09:13:02 GMT
RUN rm -f '/etc/yum.repos.d/repo-f8785.repo' '/etc/yum.repos.d/repo-08a34.repo'
# Tue, 05 Sep 2023 09:13:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 05 Sep 2023 09:13:05 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 13 Sep 2023 00:20:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 Sep 2023 00:20:11 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 Sep 2023 00:20:26 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Wed, 13 Sep 2023 00:20:27 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 13 Sep 2023 00:20:27 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 13 Sep 2023 00:20:27 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Wed, 13 Sep 2023 00:20:27 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Wed, 13 Sep 2023 00:20:27 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 Sep 2023 00:20:28 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 Sep 2023 00:21:02 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 13 Sep 2023 00:21:08 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:3b7adf049118244599c2f433c32bb40ea46462b457d9ca01ab066462c5f38561`  
		Last Modified: Tue, 12 Sep 2023 17:36:15 GMT  
		Size: 78.0 MB (78045460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca3909d1d1774e2ec99ed5806b6b9f216baf22b209f07c6f5f30d43883acce2`  
		Last Modified: Wed, 13 Sep 2023 00:28:28 GMT  
		Size: 121.0 MB (120960490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26958c5866abd4f8efef0fdd860d489c7bdd80d3ee946de3f0e543df78f814c6`  
		Last Modified: Wed, 13 Sep 2023 00:29:29 GMT  
		Size: 557.3 MB (557254541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd63b2a370e00ce6d4672c6886985494258e56f2281b44a842bd3e739f25ac0`  
		Last Modified: Wed, 13 Sep 2023 00:28:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:676b5e9d0c7fc96c48cc1c9713b5444b181d0743102f2d9c3bdc5eb91c21a905
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.6 MB (738609041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9162b7fc0338134536621dabf2e0b552b19a79c882ad54c5dd63dc736708293b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Aug 2023 05:58:46 GMT
ADD file:d3d17472fc7b2a62ee571d602a59dd1d140ab241b6a6058886bd46dd7cbdca36 in / 
# Wed, 23 Aug 2023 05:58:48 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 23 Aug 2023 05:58:48 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 23 Aug 2023 05:58:48 GMT
ADD multi:b0ab630b23847a4e725e0c4d6cd6a39aae310b05fedbc72c4f87de94f2a843c8 in /etc/yum.repos.d/ 
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Aug 2023 05:58:48 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 23 Aug 2023 05:58:48 GMT
ENV container oci
# Wed, 23 Aug 2023 05:58:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 05:58:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Aug 2023 05:58:49 GMT
RUN rm -rf /var/log/*
# Wed, 23 Aug 2023 05:58:51 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 23 Aug 2023 05:58:51 GMT
ADD file:1b62caa8d5a495de181819d9d04d125a26b8968e37dc980509a3dfe4b9ba125f in /root/buildinfo/content_manifests/ubi9-container-9.2-722.1692769367.json 
# Wed, 23 Aug 2023 05:58:51 GMT
ADD file:c091b07d0e8609d9ff02c22bee0851a7e145fca9d28895c249bdf8a42f1c56dc in /root/buildinfo/Dockerfile-ubi9-9.2-722.1692769367 
# Wed, 23 Aug 2023 05:58:51 GMT
LABEL "release"="722.1692769367" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-08-23T05:46:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-722.1692769367"
# Wed, 23 Aug 2023 05:58:52 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2294296-4190f.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 23 Aug 2023 05:58:53 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 23 Aug 2023 05:58:55 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 26 Aug 2023 03:54:07 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 26 Aug 2023 03:54:07 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 26 Aug 2023 03:54:20 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Sat, 26 Aug 2023 03:54:22 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 26 Aug 2023 03:54:22 GMT
ARG SWIFT_PLATFORM=ubi9
# Sat, 26 Aug 2023 03:54:22 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Sat, 26 Aug 2023 03:54:22 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Sat, 26 Aug 2023 03:54:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:54:22 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:54:57 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 26 Aug 2023 03:55:08 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:a648050271282e5ecbb419ccdf8c226f33a2f1e3d678a76b7efd596771326813`  
		Last Modified: Thu, 24 Aug 2023 18:06:04 GMT  
		Size: 75.8 MB (75803668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf8ca574113d65bc0f587dd4a969b972865c9e70513a3f2a2c1ef4fcfa38d47`  
		Last Modified: Sat, 26 Aug 2023 03:56:37 GMT  
		Size: 115.1 MB (115089533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4002a5a927a7c9f891d1da71fd72abf4335402ce3d1db536467e4287b769731`  
		Last Modified: Sat, 26 Aug 2023 03:57:20 GMT  
		Size: 547.7 MB (547715612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30b4dcaf6d4e73f73af2b4140955451c9ea6c368c2bf98fea55307e3171cb61`  
		Last Modified: Sat, 26 Aug 2023 03:56:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
