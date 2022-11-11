## `amazoncorretto:11-al2022-RC-headful`

```console
$ docker pull amazoncorretto@sha256:a7bf85cb428099b00e35e2119400dbdcc1f338debf738a41eb33fb9806b00022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2022-RC-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a71c9df6aed791463ee4b9429bb8a9bd4ffd3d95ffad7fc2db9a074a875d6520
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132833209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246ae6f34ac404296b798c22143b4b8e5324f1d9f149a2786daa757d487bebc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Nov 2022 01:38:06 GMT
ARG version=11.0.17.8-1
# Fri, 11 Nov 2022 01:39:06 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 11 Nov 2022 01:39:06 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3e19463f7f76dd6501192b2b9b43f74f15ff205d3eb4a82c004014aa1ca681`  
		Last Modified: Fri, 11 Nov 2022 01:43:52 GMT  
		Size: 75.2 MB (75175342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2022-RC-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8bb7055578f6d3a2302796e7b27f44159b43cca5b402a0ca76fdb2d2e1e07b13
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130956120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7f95f7ca6435dcd6065eb6e6f60017c1bf419072dbfa2d5b7e264ec3078cc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:12 GMT
ADD file:a96a24d7338f7e441a7666f0001096f24674170b376588f39095734b91d9dfed in / 
# Tue, 01 Nov 2022 23:11:13 GMT
CMD ["/bin/bash"]
# Fri, 11 Nov 2022 11:56:12 GMT
ARG version=11.0.17.8-1
# Fri, 11 Nov 2022 11:57:05 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 11 Nov 2022 11:57:06 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9f53c5402c7b18b2658ebb93a03c882a5ca1212112c795f5d4a3c561ea6fcd2f`  
		Last Modified: Tue, 01 Nov 2022 23:12:05 GMT  
		Size: 56.5 MB (56505867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0010be5b236353b303bad8facd40d9cd15c2e73d087bf5ebedffd85f44fa7a1e`  
		Last Modified: Fri, 11 Nov 2022 11:59:36 GMT  
		Size: 74.5 MB (74450253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
