## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:5aaec5ee613a16591f491bd3ed3b31c758f9671a927fceb38cb5feac4bc5d964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:70303315f8f190751e71e877f0137ac452d34da691cb666136041dfdfb1b4c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165661181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730b498ad17247d096f2555422316ff25ba155159cd19d3bec4bbd0562eeae24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Aug 2023 05:58:49 GMT
ADD file:c3c0082ae3828a568a202df86877cc3e70b4ae0e5925dc424cedcac06d77be73 in / 
# Wed, 23 Aug 2023 05:58:50 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 23 Aug 2023 05:59:10 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 23 Aug 2023 05:59:11 GMT
ADD multi:b0ab630b23847a4e725e0c4d6cd6a39aae310b05fedbc72c4f87de94f2a843c8 in /etc/yum.repos.d/ 
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Aug 2023 05:59:11 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 23 Aug 2023 05:59:11 GMT
ENV container oci
# Wed, 23 Aug 2023 05:59:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 05:59:11 GMT
CMD ["/bin/bash"]
# Wed, 23 Aug 2023 05:59:11 GMT
RUN rm -rf /var/log/*
# Wed, 23 Aug 2023 05:59:12 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 23 Aug 2023 05:59:12 GMT
ADD file:fde3c80d4331562816fd0d1060cddad838534b2ab71f844391948713ce482e5c in /root/buildinfo/content_manifests/ubi9-container-9.2-722.1692769367.json 
# Wed, 23 Aug 2023 05:59:12 GMT
ADD file:e4818bdd48eca78e43e660f779acaab019cf192dd4c55c619f38f266ce8fc000 in /root/buildinfo/Dockerfile-ubi9-9.2-722.1692769367 
# Wed, 23 Aug 2023 05:59:12 GMT
LABEL "release"="722.1692769367" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-08-23T05:46:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-722.1692769367"
# Wed, 23 Aug 2023 05:59:13 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2294296-4190f.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Wed, 23 Aug 2023 05:59:14 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 23 Aug 2023 05:59:17 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 26 Aug 2023 03:41:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 26 Aug 2023 03:41:44 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 26 Aug 2023 03:42:54 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 26 Aug 2023 03:42:54 GMT
ARG SWIFT_PLATFORM=ubi9
# Sat, 26 Aug 2023 03:42:54 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Sat, 26 Aug 2023 03:42:54 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Sat, 26 Aug 2023 03:42:54 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:42:54 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:43:23 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:1041e80416766a3be14610bcf1b1d9181ea2996dee351a9a2d10e8d370d43dea`  
		Last Modified: Thu, 24 Aug 2023 18:05:56 GMT  
		Size: 78.1 MB (78091972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acefde54edcb23dadce46daedcca8e0fd200d59430d978eed6a78f09b384d640`  
		Last Modified: Sat, 26 Aug 2023 03:49:29 GMT  
		Size: 87.6 MB (87569209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8a17427558765543e2e71f99a4fb0ae71d100624a16926c019ff8cca8252bb6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161381544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019af1b38cd32d6de8a2e9af47d50cde6cce5505d05cf6d0d5e81c30b049c7cf`
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
# Sat, 26 Aug 2023 03:55:15 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 26 Aug 2023 03:55:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Sat, 26 Aug 2023 03:55:15 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Sat, 26 Aug 2023 03:55:15 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Sat, 26 Aug 2023 03:55:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:55:15 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 26 Aug 2023 03:55:39 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:a648050271282e5ecbb419ccdf8c226f33a2f1e3d678a76b7efd596771326813`  
		Last Modified: Thu, 24 Aug 2023 18:06:04 GMT  
		Size: 75.8 MB (75803668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97fbe1b7fb005ad774337c95ab8af6bc4db5620853a57b068ffd916b4a73dc`  
		Last Modified: Sat, 26 Aug 2023 03:57:38 GMT  
		Size: 85.6 MB (85577876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
