## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2e087f0efc2c62f8a66040d602c7ad4fc9e64e7de6095883a4cb0139126a56c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f50bf4df51568cd72284542763f753fcf6083ad884c2cf4ef4f71449cd9584bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141778734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3afffdc54d05e1545948341f7549de999221588d6a37f87f0d46a0ae9a7c391`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:52:39 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 00:52:39 GMT
ARG package_version=1
# Sat, 23 Sep 2023 00:53:24 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:53:24 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:53:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de258ffec2821d250f8296183675d8bccd6781f8c3745f10384638331ce7dbda`  
		Last Modified: Sat, 23 Sep 2023 01:05:11 GMT  
		Size: 89.4 MB (89402652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:914a98ee0b171dd35bfc08b09bf5943eabafb2e9aedcc1e6ab169b6c969f7616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139939821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223e1a298314bc3eaa9bde01abf2603a3b801d84855a3b455cc820ab1cbcbdea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:31 GMT
COPY dir:03fe38cdd5cc2f8a990979b08efd5210e06e9c3897e52ada3c6c1600d3c4dd2a in / 
# Sat, 23 Sep 2023 00:39:32 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:22:02 GMT
ARG version=21.0.0.35-1
# Sat, 23 Sep 2023 01:22:02 GMT
ARG package_version=1
# Sat, 23 Sep 2023 01:22:43 GMT
# ARGS: package_version=1 version=21.0.0.35-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 01:22:44 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:22:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:154360ae54dfa1d6974917dc29086d4d678d1f640f9c2fe7a2152a2b7a62c6c1`  
		Last Modified: Thu, 21 Sep 2023 00:56:16 GMT  
		Size: 51.5 MB (51457152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dea34d0c3b3a0de51590e4fd51ebcae0f8ce6c8abf389ca066d225b5152da7`  
		Last Modified: Sat, 23 Sep 2023 01:32:43 GMT  
		Size: 88.5 MB (88482669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
