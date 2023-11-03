## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7f88f37445781e1a1391573019252b3b4686ad10e40cfea1d5ffb3cd90e0884c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:22b99d0c1ed915946025148ea50e8cf5790cbf9ae9c550d039d18d8b5eb877c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141823334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe7dfbca0e78bd7d46d04ea7c3442d575d4635ff8f83ae929305127701e244a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:33 GMT
COPY dir:5b123379096b1f1bc8f9237baebbcbf1495f2f8d5cbcd36b1ee4414cae499dee in / 
# Fri, 03 Nov 2023 22:21:33 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:49:30 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 22:49:30 GMT
ARG package_version=2
# Fri, 03 Nov 2023 22:50:20 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 22:50:20 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:50:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a98bc98bb91a9e3ba206b37674c857456e1df8dd9fed29335a0441ffe4ba5869`  
		Last Modified: Tue, 31 Oct 2023 01:59:44 GMT  
		Size: 52.4 MB (52404740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fa25b8bd48ab40d88c38564b016e55a3ce024c8ce4df6887f74efb36a2af6a`  
		Last Modified: Fri, 03 Nov 2023 23:00:54 GMT  
		Size: 89.4 MB (89418594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f3b800feb17405a3310926b502951f20e2bcef0246c92b21ecc9025af01853a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139982398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30df41d545faee22a353f8c640189b08a039976b517f366f8b4ebe1e8213143`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:39:55 GMT
COPY dir:c10f7b11e978070d5aeb6ea4db7b31b48bfb2cb9b0062451e8bf9592fb61a2e4 in / 
# Fri, 03 Nov 2023 22:39:56 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:03:56 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 23:03:56 GMT
ARG package_version=2
# Fri, 03 Nov 2023 23:04:38 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 23:04:39 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:04:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:85509e5088985a7b5d6c9025cce59b920ce6ac3e2035241e3b24d9d86bfe0904`  
		Last Modified: Tue, 31 Oct 2023 01:59:43 GMT  
		Size: 51.5 MB (51484639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd58723a53c77a3eedf3eda90aebd9de943a36e38c60d3347fba09e3999bcf9`  
		Last Modified: Fri, 03 Nov 2023 23:14:00 GMT  
		Size: 88.5 MB (88497759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
