## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5f46e284aa6e3580ec3a0946e5ea669be2f27dabe253b741edd43b0e1d1f984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdaf55bef2bfdde322afa7943485f582eabad12c9cdccc77b50c43b977485fcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142491867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0d2cc4355d5cb8e569a25078a8358944161554c442859fe7bb4ecd8efde70b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:52:39 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 00:52:39 GMT
ARG package_version=1
# Sat, 23 Sep 2023 00:53:44 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:53:45 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:53:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4ad18100b10d1c14fafe1b3405bd1e0fc7a8a680708b60cb93a5317a29c3f`  
		Last Modified: Sat, 23 Sep 2023 01:05:30 GMT  
		Size: 90.1 MB (90115785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:179beca7166398fbd26ef8503b04b02c8605c87e39e9d3d5a3ddc205995cc8ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140533855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786ad07333411fbe5030f31acd7afdd25a98398c0c4c5b8f2a41d8e6f7d63327`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:40:45 GMT
COPY dir:0004a2667b3e5dc5080ba46954457d05835caf07f7030d94b953f1c3cede9b0c in / 
# Tue, 29 Aug 2023 18:40:47 GMT
CMD ["/bin/bash"]
# Fri, 22 Sep 2023 00:42:29 GMT
ARG version=21.0.0.35-1
# Fri, 22 Sep 2023 00:42:29 GMT
ARG package_version=1
# Fri, 22 Sep 2023 00:43:22 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 22 Sep 2023 00:43:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 Sep 2023 00:43:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8e2acd49419010bc77a61e38a85963f09e403f004635f24c436d177a08df1040`  
		Last Modified: Sat, 26 Aug 2023 03:06:10 GMT  
		Size: 51.3 MB (51324150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ceac8e14f5315545234988f4cb72b67062cfa833340ace09f50706944b9895`  
		Last Modified: Fri, 22 Sep 2023 00:47:43 GMT  
		Size: 89.2 MB (89209705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
