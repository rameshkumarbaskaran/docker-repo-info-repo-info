## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f3138f2ec359cb8745c26361d74d7ceb5c02fd708bdaabecf4b1efc8ba01b57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:742d59ec436790bb64d2ad885a823f420c04a5b20c9ce8463efa589e3520b8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128271639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91b8991257b33db45dac4aa6979b0b2676bb088890863b29439d0a78853c5d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:17 GMT
COPY dir:53a31edf8963d6fd2d947e72f41a518efb3266cde6711aa27f12fbd3bb05b5cc in / 
# Wed, 20 Dec 2023 08:49:17 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:27:14 GMT
ARG version=11.0.21.9-1
# Wed, 20 Dec 2023 09:27:59 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 09:28:00 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:28:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1db371c0a72a30b037eddab3bf3f6091c0226e7b6e3a122c8e0e27d2ea7e5432`  
		Last Modified: Mon, 18 Dec 2023 19:12:16 GMT  
		Size: 52.2 MB (52217769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7172b56cef6211a03e49f3459a7418c3062fd77259204edd988220ad9672ef29`  
		Last Modified: Wed, 20 Dec 2023 09:40:19 GMT  
		Size: 76.1 MB (76053870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6781498822319cb93ba5a1cc0f0d72fa641b8be00244b4312ee1adbc29447ccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126536474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f4b2c2747b95d2fca676930c6103d537e54ff7ff61bf43ec4cb113d57ca0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:07 GMT
COPY dir:d006faf7e50cd8429d93f8cf8ea807b50b60a3c38783c4d247b3e56de7d9a3dc in / 
# Wed, 20 Dec 2023 01:32:07 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 01:57:58 GMT
ARG version=11.0.21.9-1
# Wed, 20 Dec 2023 01:58:35 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 01:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 01:58:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:62dac1e13f9aa133cbec88aa21ded5df9ecd8a8ff67fc7ac9887cc25f3c387fb`  
		Last Modified: Mon, 18 Dec 2023 19:12:13 GMT  
		Size: 51.3 MB (51307984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa44ba3375c478dfbcc8ebd8b82262e406df2cfba33d0a33b5a198dfef20f9f`  
		Last Modified: Wed, 20 Dec 2023 02:08:15 GMT  
		Size: 75.2 MB (75228490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
