## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:69f62752484258dcabdc38d68e504b2a3bf9d4948b0f89b80c7380f6df61971c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c422d4fbe301eb6ddc37423f290891a20bd50336b4fefd0b590012baa752dbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142525691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420ac7e276058fb877bf2e8fef726ad479f4c603b297d7bd0520386497369bc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:33 GMT
COPY dir:5b123379096b1f1bc8f9237baebbcbf1495f2f8d5cbcd36b1ee4414cae499dee in / 
# Fri, 03 Nov 2023 22:21:33 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:49:30 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 22:49:30 GMT
ARG package_version=2
# Fri, 03 Nov 2023 22:50:41 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 22:50:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:50:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a98bc98bb91a9e3ba206b37674c857456e1df8dd9fed29335a0441ffe4ba5869`  
		Last Modified: Tue, 31 Oct 2023 01:59:44 GMT  
		Size: 52.4 MB (52404740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274290f14cc6f8174dc053ac1845bbecbc4f40b3b0c4b29b26d999d8cdccf35e`  
		Last Modified: Fri, 03 Nov 2023 23:01:13 GMT  
		Size: 90.1 MB (90120951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6b66f4a6fa9c3b95a0cfd60807b194f58a5fe8271be57a46287a72df0c729bc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140700434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53ce4b4385cb4a7e3ef4b6fcc6edd06a815ba0aa8f10496354512f7019a4094`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:39:55 GMT
COPY dir:c10f7b11e978070d5aeb6ea4db7b31b48bfb2cb9b0062451e8bf9592fb61a2e4 in / 
# Fri, 03 Nov 2023 22:39:56 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:03:56 GMT
ARG version=21.0.1.12-1
# Fri, 03 Nov 2023 23:03:56 GMT
ARG package_version=2
# Fri, 03 Nov 2023 23:04:58 GMT
# ARGS: package_version=2 version=21.0.1.12-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 23:04:59 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:04:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:85509e5088985a7b5d6c9025cce59b920ce6ac3e2035241e3b24d9d86bfe0904`  
		Last Modified: Tue, 31 Oct 2023 01:59:43 GMT  
		Size: 51.5 MB (51484639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8077f865070a1c9b04ef90d33d9bc7670b999baeb0f0affe2a685e22c6c4e8a`  
		Last Modified: Fri, 03 Nov 2023 23:14:17 GMT  
		Size: 89.2 MB (89215795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
