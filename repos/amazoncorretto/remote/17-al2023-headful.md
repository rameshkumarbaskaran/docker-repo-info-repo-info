## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6ba44113dc134460f3b49b93bc8cb479915f817f8c4466a360dae790727fa76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:714b172c93a942f6fa392eea4af234b06a193866397c44e4400b9b3f0e033e1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135556674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b275f433609dbc14e6d000f976c08f279a08dc7c5827f02e517564c65c858d1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:46:18 GMT
ARG version=17.0.8.8-1
# Sat, 23 Sep 2023 00:46:18 GMT
ARG package_version=1
# Sat, 23 Sep 2023 00:47:22 GMT
# ARGS: package_version=1 version=17.0.8.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:47:23 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:47:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8a72337632b7aac323ac34ec29320058dfcbf8ef2425910cdad02a6e79ffe`  
		Last Modified: Sat, 23 Sep 2023 01:01:28 GMT  
		Size: 83.2 MB (83180592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:436fc3276aeb071d9e8db1c40ce08fb3f39a8e2d5ffe84a27f650111e44bf267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d3f1d1cb6164476687abc59ff03baf8d915bb17b2709429964b15a527b2395`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:31 GMT
COPY dir:03fe38cdd5cc2f8a990979b08efd5210e06e9c3897e52ada3c6c1600d3c4dd2a in / 
# Sat, 23 Sep 2023 00:39:32 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:17:12 GMT
ARG version=17.0.8.8-1
# Sat, 23 Sep 2023 01:17:12 GMT
ARG package_version=1
# Sat, 23 Sep 2023 01:18:09 GMT
# ARGS: package_version=1 version=17.0.8.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 01:18:10 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:18:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:154360ae54dfa1d6974917dc29086d4d678d1f640f9c2fe7a2152a2b7a62c6c1`  
		Last Modified: Thu, 21 Sep 2023 00:56:16 GMT  
		Size: 51.5 MB (51457152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f36a84f9c92851e2f8fbe058d8a69c1a307e174299ca6d055c2d521008fd8`  
		Last Modified: Sat, 23 Sep 2023 01:29:32 GMT  
		Size: 82.5 MB (82521166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
