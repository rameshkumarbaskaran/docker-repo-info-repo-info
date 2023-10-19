## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c3ba1cb8ec497b63d9b343f348fcd0c4875f54c00edd4c46e75e8b64d701d033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a1b06432efa09b976f64f7e7909fce1c1f90d33f46a4187146e4e31a45237b5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129113497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06e9d70cb7932504fb7ce2939210a811ac737efd631dc5cf90264c9820f263f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:37:51 GMT
COPY dir:73a08d9acd2707b5f429ab7e4f26f6f5880d94265654591f74d7102f20954c66 in / 
# Thu, 12 Oct 2023 22:37:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:06:30 GMT
ARG version=11.0.20.9-1
# Thu, 12 Oct 2023 23:07:30 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 12 Oct 2023 23:07:30 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:07:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:860bcbd64bf9485a06bc1858b0de975763ffab4b4fb53fb19b66b42536e48fe7`  
		Last Modified: Wed, 11 Oct 2023 21:33:29 GMT  
		Size: 52.4 MB (52395746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be729f46a436d5e7c200829d31eef4ecfbf97698daa9179b27c6ad31e8d0b943`  
		Last Modified: Thu, 12 Oct 2023 23:23:03 GMT  
		Size: 76.7 MB (76717751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a2873350ecd2739ee4ede9e74da32ca3c95e9788bdc993fefcf6081bc1b4166b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127392271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013df157e4142178e2445f5aceec2971661bf4ec5ee764bcf6c2babcd57ed3aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:23:51 GMT
COPY dir:23c4f526fba599c79c471bcc9a859c715cfebcd3d79aabf95868c2189962dde3 in / 
# Thu, 12 Oct 2023 22:23:51 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:41:58 GMT
ARG version=11.0.21.9-1
# Thu, 19 Oct 2023 00:42:51 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 19 Oct 2023 00:42:52 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:42:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d726870119c530d3b141cccd8b55693be0fc259a674ed2bc3bcf5999ff1434d3`  
		Last Modified: Thu, 12 Oct 2023 01:34:33 GMT  
		Size: 51.5 MB (51474358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a920ab0280a6806e6f1a1f251be5d428cb112c544a3d303661cff212e03c597f`  
		Last Modified: Thu, 19 Oct 2023 00:57:43 GMT  
		Size: 75.9 MB (75917913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
