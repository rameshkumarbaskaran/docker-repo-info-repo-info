## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:cc82ba733fdf6fab990cf226b88a0164dc9077f26737a9666659b22ebc9248de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a4a354c75ff3ae3f91c0ce6acb9a5238af8ce4d484a64a98c338def8281d1e3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134534969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56023c41adaa4af523736d5b8230bc305231a7af1382a8dbbbc152bff290be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:17 GMT
COPY dir:53a31edf8963d6fd2d947e72f41a518efb3266cde6711aa27f12fbd3bb05b5cc in / 
# Wed, 20 Dec 2023 08:49:17 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:30:38 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 09:30:38 GMT
ARG package_version=1
# Wed, 20 Dec 2023 09:31:23 GMT
# ARGS: package_version=1 version=17.0.9.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 09:31:23 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:31:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1db371c0a72a30b037eddab3bf3f6091c0226e7b6e3a122c8e0e27d2ea7e5432`  
		Last Modified: Mon, 18 Dec 2023 19:12:16 GMT  
		Size: 52.2 MB (52217769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0657a6970516d92981ea7f3b45a588914ab066544fbb578435bd66d5c8af0e2`  
		Last Modified: Wed, 20 Dec 2023 09:42:37 GMT  
		Size: 82.3 MB (82317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dc4c864397b1a0a7b03b09e1d1dc14a286a1c9b0a7a6ac7fdc50ee06b7c954f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132965636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51ee6a96a43c1463af463c93cf1b7a6c83cf8931ca2f377bbcf9169517eeb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:07 GMT
COPY dir:d006faf7e50cd8429d93f8cf8ea807b50b60a3c38783c4d247b3e56de7d9a3dc in / 
# Wed, 20 Dec 2023 01:32:07 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 02:00:30 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 02:00:30 GMT
ARG package_version=1
# Wed, 20 Dec 2023 02:01:12 GMT
# ARGS: package_version=1 version=17.0.9.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 02:01:13 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:01:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:62dac1e13f9aa133cbec88aa21ded5df9ecd8a8ff67fc7ac9887cc25f3c387fb`  
		Last Modified: Mon, 18 Dec 2023 19:12:13 GMT  
		Size: 51.3 MB (51307984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a71cdcf5f5882f9e8510a2e32c3816a8cea91e06c061cc805d9ab308245b9`  
		Last Modified: Wed, 20 Dec 2023 02:10:20 GMT  
		Size: 81.7 MB (81657652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
