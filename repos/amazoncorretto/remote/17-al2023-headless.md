## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:75cf2b6197b0622e22872abf9b6856cc06b6896cb7c57812ddf1dbce27cf78d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:88b3373d2223f290053dae98280fe65361cf47421e81d02ef478db92e6d67150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134548310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1eddd756f5ddb5b199efa1fa2d4661a680f74b88f11cb1f29bf5e00a0cac698`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:19:52 GMT
COPY dir:1ca4a277361366916e6a16164366bcbcd71ed199d0a9f09b06f0dce102ed17c8 in / 
# Mon, 05 Jun 2023 19:19:53 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:40:49 GMT
ARG version=17.0.7.7-1
# Mon, 05 Jun 2023 19:40:49 GMT
ARG package_version=1
# Mon, 05 Jun 2023 19:41:26 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 05 Jun 2023 19:41:27 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:41:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e94ab5e30a70253c20abbca50c15f312ade187b3787505f9772f9d14bf28b26d`  
		Last Modified: Wed, 24 May 2023 23:13:56 GMT  
		Size: 52.3 MB (52264123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5331bd59a96a88156459c5f4edc0733ea66d3112173ab3444e90cbe4102811c5`  
		Last Modified: Mon, 05 Jun 2023 19:46:54 GMT  
		Size: 82.3 MB (82284187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6655c21863788a96ea0b7b21732d616df4813fbf46a8582c3ea37ab3ac8728a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132900163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ee00d93be837e2e7e82d02a4d42e28a60d6d5018c6131978c1732efb289163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 19:39:31 GMT
COPY dir:fb039c7f3fc033175c2cd9eb4c7b7245aa6d97fbdbadf7109eb1444417c92581 in / 
# Mon, 05 Jun 2023 19:39:32 GMT
CMD ["/bin/bash"]
# Mon, 05 Jun 2023 19:58:11 GMT
ARG version=17.0.7.7-1
# Mon, 05 Jun 2023 19:58:11 GMT
ARG package_version=1
# Mon, 05 Jun 2023 19:58:43 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 05 Jun 2023 19:58:44 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jun 2023 19:58:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2f034b348d769e8ab686a03d3713c98068a3c410e983985412e28004eabd1336`  
		Last Modified: Thu, 25 May 2023 03:06:05 GMT  
		Size: 51.3 MB (51300330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e56725b929dd4c5f18556e4abb9a636db706e16a87783f6df80c76448ba329`  
		Last Modified: Mon, 05 Jun 2023 20:03:33 GMT  
		Size: 81.6 MB (81599833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
