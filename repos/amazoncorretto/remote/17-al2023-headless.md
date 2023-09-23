## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:df5e0173550b20b2c20bb15311e1238b6025c1d9fbb1dbbf6ca1cd9d259a5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ba477f195549337ee9deee30c1bbc79fafa3dfc3f10d6d8f0d16969f28495f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134880321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f46d2aca3890483e37bb315aa777b0e6f58de62cbe43ec91f6c01ec689953`
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
# Sat, 23 Sep 2023 00:47:01 GMT
# ARGS: package_version=1 version=17.0.8.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 00:47:02 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:47:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6a2bb1614d2d1379c623b77632496b4317697cf85ad3ccd300ce6e7f95a0176e`  
		Last Modified: Thu, 21 Sep 2023 00:56:18 GMT  
		Size: 52.4 MB (52376082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91004c311475b884307e8cda9c329f2b45ac12ac42f1792fbb7a0655b3cc74e`  
		Last Modified: Sat, 23 Sep 2023 01:01:10 GMT  
		Size: 82.5 MB (82504239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:66024068eeb4fc856465309b5574520edfcf49a27e56a2c87fb231b53bc6c58f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133284416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efcc05d137e7710f430be5aa41bcaf14acc888bfce84f0b06e69a95a5712d58`
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
# Sat, 23 Sep 2023 01:17:53 GMT
# ARGS: package_version=1 version=17.0.8.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 23 Sep 2023 01:17:54 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:17:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:154360ae54dfa1d6974917dc29086d4d678d1f640f9c2fe7a2152a2b7a62c6c1`  
		Last Modified: Thu, 21 Sep 2023 00:56:16 GMT  
		Size: 51.5 MB (51457152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2283f0ef0291343d6540d059b391b8795fb8ba3b480b47ae364f13d3ff99011a`  
		Last Modified: Sat, 23 Sep 2023 01:29:15 GMT  
		Size: 81.8 MB (81827264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
