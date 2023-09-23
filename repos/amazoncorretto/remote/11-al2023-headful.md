## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:60a80dfb08f0e103baa2094422a100b096aa468bb78d643349b028dd087ccada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:00617d61672e1ab70059b968655354bc3ea1449791ffc33cb374903c287bdb0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129098055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daff6ffa54964c3677c12ca210bf068300df54a0e15abb38112845198e573fdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:05 GMT
COPY dir:7e612c093d3db43a33d50cdcf8cc724368fe38043e469a8331439a51adfd0468 in / 
# Sat, 23 Sep 2023 00:20:05 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:42:10 GMT
ARG version=11.0.20.9-1
# Sat, 23 Sep 2023 00:43:14 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:43:15 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:43:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2ba6900c23f81b30a87d2b3f0df394dae38059e1edf2492b11d4192b740a2e`  
		Last Modified: Sat, 23 Sep 2023 00:59:01 GMT  
		Size: 76.7 MB (76721973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a2101a20fa585a1dd273aca8e8d3bf6418646cb2e4484d70c8d5df149a746e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127200868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ab2e037bf327daebdb4dd616f5c4991e33a7520a81cc69feae008f342ed111`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:40:45 GMT
COPY dir:0004a2667b3e5dc5080ba46954457d05835caf07f7030d94b953f1c3cede9b0c in / 
# Tue, 29 Aug 2023 18:40:47 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:42:39 GMT
ARG version=11.0.20.9-1
# Fri, 08 Sep 2023 21:43:32 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 08 Sep 2023 21:43:33 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:43:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8e2acd49419010bc77a61e38a85963f09e403f004635f24c436d177a08df1040`  
		Last Modified: Sat, 26 Aug 2023 03:06:10 GMT  
		Size: 51.3 MB (51324150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1967ccb94a2a0d6239bf7a3b1d4c9bba02d09342b2e4e37d1dac2fc07c647c`  
		Last Modified: Fri, 08 Sep 2023 21:53:10 GMT  
		Size: 75.9 MB (75876718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
