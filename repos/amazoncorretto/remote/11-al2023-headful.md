## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e53f4c82f6bfab79ca8b94d0a06c57c5e99a782dd06b9f51ddbc75bf9dcc2243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd7a2263ebe6ade55ad5c9f85497aab06d4681fdcbd2d990903cb4476e2058db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128810918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6040faa2b42d3c3140c9dd3b06c0e87541aed5120ddd897d36f6fe9f75f7145a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:19:52 GMT
COPY dir:1ca4a277361366916e6a16164366bcbcd71ed199d0a9f09b06f0dce102ed17c8 in / 
# Mon, 05 Jun 2023 19:19:53 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:39:13 GMT
ARG version=11.0.19.7-1
# Mon, 05 Jun 2023 19:40:07 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 05 Jun 2023 19:40:08 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:40:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:e94ab5e30a70253c20abbca50c15f312ade187b3787505f9772f9d14bf28b26d`  
		Last Modified: Wed, 24 May 2023 23:13:56 GMT  
		Size: 52.3 MB (52264123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37e7135dd7d77d33ff8a57c6c3c6574b895a4cbd3a1a0eb3682b290c4f7adcc`  
		Last Modified: Mon, 05 Jun 2023 19:45:39 GMT  
		Size: 76.5 MB (76546795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a203bbd14b98036a3770a61735f3c1f111ac92c2f2a79d7a8df533ea3d1d9b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02ece92cfb8cddc37af22a7b7c50ca492d2979e01acd06a0280075303e0dfaf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:39:31 GMT
COPY dir:fb039c7f3fc033175c2cd9eb4c7b7245aa6d97fbdbadf7109eb1444417c92581 in / 
# Mon, 05 Jun 2023 19:39:32 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:56:47 GMT
ARG version=11.0.19.7-1
# Mon, 05 Jun 2023 19:57:39 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 05 Jun 2023 19:57:40 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:57:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2f034b348d769e8ab686a03d3713c98068a3c410e983985412e28004eabd1336`  
		Last Modified: Thu, 25 May 2023 03:06:05 GMT  
		Size: 51.3 MB (51300330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1e934f9ac99525a3f8d489724455a41859fb2a0a240067dfb84bea23204760`  
		Last Modified: Mon, 05 Jun 2023 20:02:25 GMT  
		Size: 75.7 MB (75712351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
