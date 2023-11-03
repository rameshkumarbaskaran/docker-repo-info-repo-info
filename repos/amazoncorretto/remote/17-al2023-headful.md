## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e5af46c909a5fd3e0f20c0b9633e8d5145082de36bee25f9c67099437bf8ce8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cf82380058444838319aab05c6fade9cf6887f24c2deab3fe970299685d1506b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135413338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cf34252b85d23bc388ff292e45e0b92616880f8fe0786f7f29801489e8f7e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:33 GMT
COPY dir:5b123379096b1f1bc8f9237baebbcbf1495f2f8d5cbcd36b1ee4414cae499dee in / 
# Fri, 03 Nov 2023 22:21:33 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 22:45:33 GMT
ARG version=17.0.9.8-1
# Fri, 03 Nov 2023 22:45:33 GMT
ARG package_version=1
# Fri, 03 Nov 2023 22:46:37 GMT
# ARGS: package_version=1 version=17.0.9.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 22:46:38 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 22:46:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a98bc98bb91a9e3ba206b37674c857456e1df8dd9fed29335a0441ffe4ba5869`  
		Last Modified: Tue, 31 Oct 2023 01:59:44 GMT  
		Size: 52.4 MB (52404740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a1697069cc0d1c3e38bb423e6908ef82e4a568fe7c14cc4d87a2a3f69940f0`  
		Last Modified: Fri, 03 Nov 2023 22:58:17 GMT  
		Size: 83.0 MB (83008598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef5a53a794b831a547d6ad163e5ec215099de20d0009e5589d0608f5a07a108a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133834668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c39eed57b6d1ab1feb3f28710672d5fb04a56a9d5d0b994bc40099a5c6ed4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:39:55 GMT
COPY dir:c10f7b11e978070d5aeb6ea4db7b31b48bfb2cb9b0062451e8bf9592fb61a2e4 in / 
# Fri, 03 Nov 2023 22:39:56 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:00:54 GMT
ARG version=17.0.9.8-1
# Fri, 03 Nov 2023 23:00:54 GMT
ARG package_version=1
# Fri, 03 Nov 2023 23:01:47 GMT
# ARGS: package_version=1 version=17.0.9.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 03 Nov 2023 23:01:48 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2023 23:01:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:85509e5088985a7b5d6c9025cce59b920ce6ac3e2035241e3b24d9d86bfe0904`  
		Last Modified: Tue, 31 Oct 2023 01:59:43 GMT  
		Size: 51.5 MB (51484639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907791dc31e398b00427a37bb482f6f6bb7de54ae3c5cf52e74fcb177c8c4ea4`  
		Last Modified: Fri, 03 Nov 2023 23:11:46 GMT  
		Size: 82.4 MB (82350029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
