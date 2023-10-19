## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b764010b3ded3a1970c720947cb573bc7168a006c97ff8d3bedcad2d51063555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4955db935319cd87d0b5b1cf0e614fd9a48eeeebc5fafe5060cf96a32c884a11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142510578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd552001e3e9dfd5c104b4f8a2716193c2e6ce31a2edaa1b9e83aae1d895ddb9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:37:51 GMT
COPY dir:73a08d9acd2707b5f429ab7e4f26f6f5880d94265654591f74d7102f20954c66 in / 
# Thu, 12 Oct 2023 22:37:52 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:16:51 GMT
ARG version=21.0.0.35-1
# Thu, 12 Oct 2023 23:16:51 GMT
ARG package_version=1
# Thu, 12 Oct 2023 23:17:55 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 12 Oct 2023 23:17:56 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:17:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:860bcbd64bf9485a06bc1858b0de975763ffab4b4fb53fb19b66b42536e48fe7`  
		Last Modified: Wed, 11 Oct 2023 21:33:29 GMT  
		Size: 52.4 MB (52395746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd1f85d5b8442f0d831acf803f1f91078a20c8804e54b38f7ae4b1b23b0a1f9`  
		Last Modified: Thu, 12 Oct 2023 23:29:25 GMT  
		Size: 90.1 MB (90114832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9ea13b0242e7ce4d3147420c8b005d80b4a0613cc48d4395f5257d4345a8e9f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140694751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01137ce2a10f8cf9b30c9dd40a74f0252b4c613418a0d22b7f3cf26a691dcf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:23:51 GMT
COPY dir:23c4f526fba599c79c471bcc9a859c715cfebcd3d79aabf95868c2189962dde3 in / 
# Thu, 12 Oct 2023 22:23:51 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:48:41 GMT
ARG version=21.0.1.12-1
# Thu, 19 Oct 2023 00:48:41 GMT
ARG package_version=1
# Thu, 19 Oct 2023 00:49:34 GMT
# ARGS: package_version=1 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 19 Oct 2023 00:49:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:49:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d726870119c530d3b141cccd8b55693be0fc259a674ed2bc3bcf5999ff1434d3`  
		Last Modified: Thu, 12 Oct 2023 01:34:33 GMT  
		Size: 51.5 MB (51474358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96159d03ea79364a115a0a0ec6877b1d7b2953cd03a30d6581cf068329bc75b6`  
		Last Modified: Thu, 19 Oct 2023 01:06:28 GMT  
		Size: 89.2 MB (89220393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
