## `amazoncorretto:17-al2022-RC-headless`

```console
$ docker pull amazoncorretto@sha256:cf61d3c926a9b470e14be6a0f1080a9200913450a5c55cab375b98d5423f0493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2022-RC-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c1545672336e871f95df351d595a9c54652b0a4a9d7deaed80909c924eee0636
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137432462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691747e693c5ef1f679a5298b3c12a2186ec1dc0be732e9e4bdf72510c83f878`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 20:19:36 GMT
ADD file:98ef92cdf32a39d761092e3dbc916e083179c438c365e21a2ea68b801a3f595d in / 
# Thu, 02 Feb 2023 20:19:37 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 20:38:59 GMT
ARG version=17.0.6.10-1
# Thu, 02 Feb 2023 20:38:59 GMT
ARG package_version=1
# Thu, 02 Feb 2023 20:39:38 GMT
# ARGS: package_version=1 version=17.0.6.10-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 02 Feb 2023 20:39:39 GMT
ENV LANG=C.UTF-8
# Thu, 02 Feb 2023 20:39:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:044c2e2e5f7c74ee29fba14bd0c17aba2da682d4bb1f235b6efaeb7365c09814`  
		Last Modified: Thu, 02 Feb 2023 20:20:38 GMT  
		Size: 57.9 MB (57916237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23aef8afef81d0cc48d7966877e6d9567b934822ff94a08d467571a29d44467`  
		Last Modified: Thu, 02 Feb 2023 20:44:26 GMT  
		Size: 79.5 MB (79516225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2022-RC-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1ea338ad512e6ffa056383ff71f45d43ac3b1801268a4f751fb624803aded9e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135763469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186db607aec1af7c54a0c52ccef1874ed0901fde08838c5ff311215a33f0d3ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 20:39:44 GMT
ADD file:9f05ba021fffd82beb2a9d0ea647b83648b1bfd0e607557faab2356c813fb362 in / 
# Thu, 02 Feb 2023 20:39:44 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 20:58:35 GMT
ARG version=17.0.6.10-1
# Thu, 02 Feb 2023 20:58:35 GMT
ARG package_version=1
# Thu, 02 Feb 2023 20:59:07 GMT
# ARGS: package_version=1 version=17.0.6.10-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 02 Feb 2023 20:59:08 GMT
ENV LANG=C.UTF-8
# Thu, 02 Feb 2023 20:59:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:838e33db41c437b283f45c5b41cf3cfe56026082e5c47e55eed49ec433af394c`  
		Last Modified: Tue, 31 Jan 2023 12:25:16 GMT  
		Size: 56.8 MB (56810570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2956a45eb29cda327917ce51d4a940cb530ea4309b4a9bf61643ad288ab42a`  
		Last Modified: Thu, 02 Feb 2023 21:01:58 GMT  
		Size: 79.0 MB (78952899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
