## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a83cf4bef6f3cc16be94552ef6718fe6c6671a0b83bd95f89307a0503af2796b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ddd0d2729e559dace9c76652c7b4519c3ff19ed3961b43feb9c54010fbb2adb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128392994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1fda3a6b0f8a1b734f2271eaf4d6b888678349f39060ef5eceee9dfbf37f42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:42:10 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 00:42:54 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:42:54 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:42:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216c6284dc34d39958abe051782cb7592c862abb352f539ec60a8e40ae5d02ce`  
		Last Modified: Sat, 23 Sep 2023 00:58:44 GMT  
		Size: 76.0 MB (76016912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1ccbbcf8b07bf2176d3d6136576bfe4bd81b3c02496e383b4b2da5517319f0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126633167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d7b6718d1b72b0b781b333fff48e0d21e8549377a18e4f25aeeb28d54facaf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:31 GMT
COPY dir:03fe38cdd5cc2f8a990979b08efd5210e06e9c3897e52ada3c6c1600d3c4dd2a in / 
# Sat, 23 Sep 2023 00:39:32 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:14:09 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 01:14:45 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 01:14:46 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:14:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:154360ae54dfa1d6974917dc29086d4d678d1f640f9c2fe7a2152a2b7a62c6c1`  
		Last Modified: Thu, 21 Sep 2023 00:56:16 GMT  
		Size: 51.5 MB (51457152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a234adb7b6f661cf7541d3a12ba7710c7abff0f535de32296a15575c512fba5`  
		Last Modified: Sat, 23 Sep 2023 01:27:08 GMT  
		Size: 75.2 MB (75176015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
