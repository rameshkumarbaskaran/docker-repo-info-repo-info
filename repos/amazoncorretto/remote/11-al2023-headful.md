## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7c4bf817b3253fc0237c6fbd936ca1861ee9fff79c2eb1c22735b5be78db4896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:649db8ca18c8a5d30591c8b571767285e1ecbe3791fb02231ecbec06d20f27ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129168327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579a7df10d4609add3c4784206b09e80bb68c5cf85d0d7351116a3bb170ae049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:33 GMT
COPY dir:5b123379096b1f1bc8f9237baebbcbf1495f2f8d5cbcd36b1ee4414cae499dee in / 
# Fri, 03 Nov 2023 22:21:33 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:42:14 GMT
ARG version=11.0.21.9-1
# Fri, 03 Nov 2023 22:43:14 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 22:43:15 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:43:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a98bc98bb91a9e3ba206b37674c857456e1df8dd9fed29335a0441ffe4ba5869`  
		Last Modified: Tue, 31 Oct 2023 01:59:44 GMT  
		Size: 52.4 MB (52404740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc2569857680db2c879bc0ed1556f09090bcff67641905aa457b13003ee2600`  
		Last Modified: Fri, 03 Nov 2023 22:55:42 GMT  
		Size: 76.8 MB (76763587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b29c1ba63e34a0167ec9ccd74290c0045026d950dd80f401367fdb3ffe7f7c5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127417613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5631e1f296bd54202df6a8a218619291fb918c13897d4ab4b774f3f244bd3245`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:39:55 GMT
COPY dir:c10f7b11e978070d5aeb6ea4db7b31b48bfb2cb9b0062451e8bf9592fb61a2e4 in / 
# Fri, 03 Nov 2023 22:39:56 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:58:16 GMT
ARG version=11.0.21.9-1
# Fri, 03 Nov 2023 22:59:09 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 22:59:10 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:59:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:85509e5088985a7b5d6c9025cce59b920ce6ac3e2035241e3b24d9d86bfe0904`  
		Last Modified: Tue, 31 Oct 2023 01:59:43 GMT  
		Size: 51.5 MB (51484639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7df2598228ddd1b58be82abd4836e02fdd705571ef59aa13c5294228abbf12`  
		Last Modified: Fri, 03 Nov 2023 23:09:33 GMT  
		Size: 75.9 MB (75932974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
