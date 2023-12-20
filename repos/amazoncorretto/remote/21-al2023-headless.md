## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a8045bcdc6fd6d714bb5c7e42b97f127733e320c24d439365822c52c649f517f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce25a3bb3d3d208209c8d433fdbfb42aebab5d815243c798cae1d76d69240c29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141632965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4b6e06f90a34909695b6e9b521811bd25dc94a189ee8e372fe0a39b3877c26`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:17 GMT
COPY dir:53a31edf8963d6fd2d947e72f41a518efb3266cde6711aa27f12fbd3bb05b5cc in / 
# Wed, 20 Dec 2023 08:49:17 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:34:50 GMT
ARG version=21.0.1.12-1
# Wed, 20 Dec 2023 09:34:50 GMT
ARG package_version=2
# Wed, 20 Dec 2023 09:35:40 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 09:35:41 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:35:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1db371c0a72a30b037eddab3bf3f6091c0226e7b6e3a122c8e0e27d2ea7e5432`  
		Last Modified: Mon, 18 Dec 2023 19:12:16 GMT  
		Size: 52.2 MB (52217769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3287a0082ec2fcde2651856e86a7dd0c685d21d59022b47641ed9f3910d72775`  
		Last Modified: Wed, 20 Dec 2023 09:45:18 GMT  
		Size: 89.4 MB (89415196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:74a2c876fbd1e43fff5be797e1deb028f91502ce037d697ad574b7cebb24008e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139802413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827b7af94bce0a63943399c04a5d6bd725cc7f0f1d5e8e0252a841a4f41c1ff9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:07 GMT
COPY dir:d006faf7e50cd8429d93f8cf8ea807b50b60a3c38783c4d247b3e56de7d9a3dc in / 
# Wed, 20 Dec 2023 01:32:07 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 02:03:41 GMT
ARG version=21.0.1.12-1
# Wed, 20 Dec 2023 02:03:41 GMT
ARG package_version=2
# Wed, 20 Dec 2023 02:04:18 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 20 Dec 2023 02:04:19 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:04:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:62dac1e13f9aa133cbec88aa21ded5df9ecd8a8ff67fc7ac9887cc25f3c387fb`  
		Last Modified: Mon, 18 Dec 2023 19:12:13 GMT  
		Size: 51.3 MB (51307984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613d48017ea08b79e2ca27662a98b1b267818273d18c12d5ab8e10d5c53becaa`  
		Last Modified: Wed, 20 Dec 2023 02:12:43 GMT  
		Size: 88.5 MB (88494429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
