## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:02c0a803a3c7b3b8076f3f2e31825efdca4373d45164983609f15c6e86c2a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:43f99cfb3622512301c416a6d92a03f2de93624e92a075fa7a0eb4497b325912
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134889876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b7e4561b9ecd401c139afc99b68cafa00b654f800f904ca7a55b562ee89ad5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:37:51 GMT
COPY dir:73a08d9acd2707b5f429ab7e4f26f6f5880d94265654591f74d7102f20954c66 in / 
# Thu, 12 Oct 2023 22:37:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:10:33 GMT
ARG version=17.0.8.8-1
# Thu, 12 Oct 2023 23:10:33 GMT
ARG package_version=1
# Thu, 12 Oct 2023 23:11:12 GMT
# ARGS: package_version=1 version=17.0.8.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 12 Oct 2023 23:11:13 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:860bcbd64bf9485a06bc1858b0de975763ffab4b4fb53fb19b66b42536e48fe7`  
		Last Modified: Wed, 11 Oct 2023 21:33:29 GMT  
		Size: 52.4 MB (52395746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e7d2b16d81c8be4660b9d3dac9d0470ebb080e15a24bbfd722bffb2e34e269`  
		Last Modified: Thu, 12 Oct 2023 23:25:11 GMT  
		Size: 82.5 MB (82494130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d171af33a4fea2f951e064558e90ec95e71815307e8f4647ca24e33d24b759f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133124242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b42e97816dafa63724b4bae5c867af9d592d8b0eb01f6e2aa3f66d4667c528`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:23:51 GMT
COPY dir:23c4f526fba599c79c471bcc9a859c715cfebcd3d79aabf95868c2189962dde3 in / 
# Thu, 12 Oct 2023 22:23:51 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:45:11 GMT
ARG version=17.0.9.8-1
# Thu, 19 Oct 2023 00:45:12 GMT
ARG package_version=1
# Thu, 19 Oct 2023 00:45:48 GMT
# ARGS: package_version=1 version=17.0.9.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 19 Oct 2023 00:45:49 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:45:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d726870119c530d3b141cccd8b55693be0fc259a674ed2bc3bcf5999ff1434d3`  
		Last Modified: Thu, 12 Oct 2023 01:34:33 GMT  
		Size: 51.5 MB (51474358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4434537d1f4d65fb6f2bb5a236f31c4fdb4afe6b437efc02932f6de28c0f90b5`  
		Last Modified: Thu, 19 Oct 2023 01:01:28 GMT  
		Size: 81.6 MB (81649884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
