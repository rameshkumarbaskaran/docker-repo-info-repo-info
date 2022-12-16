## `amazoncorretto:17-al2022-RC-headful`

```console
$ docker pull amazoncorretto@sha256:ef9da8ca524c29dae8d9602fd9431e8945e81b1cb38b31d1be5fb0465a0d0601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2022-RC-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ebe49230e1b03f82a30a8598dc025a55647f49942b987ed3455072472b53be7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137130455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0d4edab68591f157076ac464c4738781f7248fc0b6bfe0c713489fd6edd2cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Nov 2022 01:39:23 GMT
ARG version=17.0.5.8-1
# Fri, 11 Nov 2022 01:39:23 GMT
ARG package_version=1
# Fri, 11 Nov 2022 01:39:59 GMT
# ARGS: package_version=1 version=17.0.5.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 11 Nov 2022 01:39:59 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:39:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df04607be2835ea2cc5d105df890bdc2e024011f143581578771fec96cbb325`  
		Last Modified: Fri, 11 Nov 2022 01:44:42 GMT  
		Size: 79.5 MB (79472588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2022-RC-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:49533933768f7fd5209e60771d598bfce5acf692e476fc7c1a1b0158bf9cafd9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135610464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494c773b92d263912e003ceb66e3a52a50439ece5b9bd05cca474958d7494d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:37 GMT
ADD file:ff147b37fd20344db08d3808c57eecb4baf220c236bdadf01d19a61f2dd6327e in / 
# Fri, 16 Dec 2022 00:41:38 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 01:01:02 GMT
ARG version=17.0.5.8-1
# Fri, 16 Dec 2022 01:01:02 GMT
ARG package_version=1
# Fri, 16 Dec 2022 01:01:33 GMT
# ARGS: package_version=1 version=17.0.5.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 16 Dec 2022 01:01:34 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:01:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f3bff8cbe57b20ad8a63095a2b0c5d31afccc39fd7fbaab9b0c483430b38429a`  
		Last Modified: Tue, 13 Dec 2022 16:26:02 GMT  
		Size: 56.7 MB (56712057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1461c762e0f41e382028d92bdb316aa1dbe88800403803e97a917d8583c1c6`  
		Last Modified: Fri, 16 Dec 2022 01:05:47 GMT  
		Size: 78.9 MB (78898407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
