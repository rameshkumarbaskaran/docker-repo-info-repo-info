## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4688fba9f5225ee53e71e9c74027615eda298768fb3d811b34c141d20c126a50
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
$ docker pull amazoncorretto@sha256:e665b0ec73ab5799ff23b49ebfde169c776a94213a0a78bcde85a8f1c8d57e26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126501449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155d58c445f2554be307ef499c9a94d303861e1e7ec1778173d9f69a0be8018c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:40:45 GMT
COPY dir:0004a2667b3e5dc5080ba46954457d05835caf07f7030d94b953f1c3cede9b0c in / 
# Tue, 29 Aug 2023 18:40:47 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:42:39 GMT
ARG version=11.0.20.9-1
# Fri, 08 Sep 2023 21:43:15 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 08 Sep 2023 21:43:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:43:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8e2acd49419010bc77a61e38a85963f09e403f004635f24c436d177a08df1040`  
		Last Modified: Sat, 26 Aug 2023 03:06:10 GMT  
		Size: 51.3 MB (51324150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c257b638508b75fd2a3dad33651ef0dfff9071fc998bedb3fc7fac36acfb7860`  
		Last Modified: Fri, 08 Sep 2023 21:52:54 GMT  
		Size: 75.2 MB (75177299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
