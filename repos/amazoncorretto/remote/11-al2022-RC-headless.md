## `amazoncorretto:11-al2022-RC-headless`

```console
$ docker pull amazoncorretto@sha256:cce7a3f21860d1c348157f9bd23f4f0a86ffe8bf1e8e44624f2d59595d24e57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2022-RC-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e0cc9d87649ad1d109d659e5106faecadec60c0c7779c957c6ca99a01c9f0ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130719282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd17fa61710ab5a82345ef4ce5408e8b456938937e295c573fac2fde1adc1da3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Nov 2022 23:11:26 GMT
ADD file:541cbb916857290067c17f8f5718a02004fa3ade45da9cd68db6a3fbec9191a6 in / 
# Tue, 01 Nov 2022 23:11:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Nov 2022 01:38:06 GMT
ARG version=11.0.17.8-1
# Fri, 11 Nov 2022 01:38:45 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 11 Nov 2022 01:38:45 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:38:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b1f61030557f6b1b4adb79deb32494aecd38af05ed90a5d54900eea80eedc3bb`  
		Last Modified: Tue, 01 Nov 2022 23:12:19 GMT  
		Size: 57.7 MB (57657867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0203d9771217b9e68a7459290726f68de89105067c443eb8bbae6caf9243f6`  
		Last Modified: Fri, 11 Nov 2022 01:43:34 GMT  
		Size: 73.1 MB (73061415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2022-RC-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aee36e3476e7f35d61db3959983df3f4e3c734743374f0f984e05daa9490c5c5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129043403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6d3c70ae41036a65b01826b92158c30c04e2bd5208171e7e419bdc080f40ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:37 GMT
ADD file:ff147b37fd20344db08d3808c57eecb4baf220c236bdadf01d19a61f2dd6327e in / 
# Fri, 16 Dec 2022 00:41:38 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:59:47 GMT
ARG version=11.0.17.8-1
# Fri, 16 Dec 2022 01:00:18 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 16 Dec 2022 01:00:19 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:00:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f3bff8cbe57b20ad8a63095a2b0c5d31afccc39fd7fbaab9b0c483430b38429a`  
		Last Modified: Tue, 13 Dec 2022 16:26:02 GMT  
		Size: 56.7 MB (56712057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7adc2e2245babf2bdc76efb5712af5d84fc01167861fe28352c7269330f224`  
		Last Modified: Fri, 16 Dec 2022 01:04:28 GMT  
		Size: 72.3 MB (72331346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
