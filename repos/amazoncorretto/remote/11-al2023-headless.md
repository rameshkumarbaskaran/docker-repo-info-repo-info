## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:9a1e5127681a0a5ff583973989adf66cf3ea08dbdbb9af3c6812ea07f7778381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:578bbf21ab48d0c7c33d8883e37b95eaed594e9aad1c17323526cf77c75ae217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128406428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39044925adb21103929af411f1382d8d2a481ab5722f19b3be32933e3c8a2829`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:37:51 GMT
COPY dir:73a08d9acd2707b5f429ab7e4f26f6f5880d94265654591f74d7102f20954c66 in / 
# Thu, 12 Oct 2023 22:37:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:06:30 GMT
ARG version=11.0.20.9-1
# Thu, 12 Oct 2023 23:07:09 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 12 Oct 2023 23:07:09 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:07:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:860bcbd64bf9485a06bc1858b0de975763ffab4b4fb53fb19b66b42536e48fe7`  
		Last Modified: Wed, 11 Oct 2023 21:33:29 GMT  
		Size: 52.4 MB (52395746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c690597fa389df20167347538189204130ef9fbb2d89708aa39e6af20c3029e7`  
		Last Modified: Thu, 12 Oct 2023 23:22:46 GMT  
		Size: 76.0 MB (76010682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:25b1a1e12b35ce3607b4f3debd3ca290b114fe9cde58f992f8e4d1dd42ab26e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126697227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2534b1dccacf66cf54d9a814eb1ef32d31197480e97467779b279f2fd66199b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:23:51 GMT
COPY dir:23c4f526fba599c79c471bcc9a859c715cfebcd3d79aabf95868c2189962dde3 in / 
# Thu, 12 Oct 2023 22:23:51 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:41:58 GMT
ARG version=11.0.21.9-1
# Thu, 19 Oct 2023 00:42:34 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 19 Oct 2023 00:42:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:42:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d726870119c530d3b141cccd8b55693be0fc259a674ed2bc3bcf5999ff1434d3`  
		Last Modified: Thu, 12 Oct 2023 01:34:33 GMT  
		Size: 51.5 MB (51474358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b13c29756785c39604007e605da0e86835436825e1392e489ba9996eb6d880`  
		Last Modified: Thu, 19 Oct 2023 00:57:27 GMT  
		Size: 75.2 MB (75222869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
