## `amazoncorretto:17-al2022-RC-headful`

```console
$ docker pull amazoncorretto@sha256:1e1437b2e96baf849044b0f11f30fe8b3cc1fa5044edce8dbba98f621f2b7e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2022-RC-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6842bd8c20342ecaa402827a6402a8b03530ce26e3456511598ef44e335bcfa8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139533819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b877550d6a4063bb8d226a222d8e395ffd6482c828594eb24ddfffa12f5696`
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
# Thu, 02 Feb 2023 20:39:59 GMT
# ARGS: package_version=1 version=17.0.6.10-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 02 Feb 2023 20:39:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 Feb 2023 20:39:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:044c2e2e5f7c74ee29fba14bd0c17aba2da682d4bb1f235b6efaeb7365c09814`  
		Last Modified: Thu, 02 Feb 2023 20:20:38 GMT  
		Size: 57.9 MB (57916237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a930770dbed33666a8d1380ef37ed84d8a86e1c939cdd437c56f9abc2aa6a4`  
		Last Modified: Thu, 02 Feb 2023 20:44:44 GMT  
		Size: 81.6 MB (81617582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2022-RC-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa33aba555f506f8ec986cb9dccb7189c1ca93de545d0eb6d421904452efe596
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137877877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b31e5b0f47f5764c7a517a8538737e4962793acf62089a5539697293e773e0`
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
# Thu, 02 Feb 2023 20:59:24 GMT
# ARGS: package_version=1 version=17.0.6.10-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2022.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2022.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 02 Feb 2023 20:59:25 GMT
ENV LANG=C.UTF-8
# Thu, 02 Feb 2023 20:59:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:838e33db41c437b283f45c5b41cf3cfe56026082e5c47e55eed49ec433af394c`  
		Last Modified: Tue, 31 Jan 2023 12:25:16 GMT  
		Size: 56.8 MB (56810570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e9ad75c50b98e272dfee0877745debe031583b9ef00c32735ed7fd9578a8d3`  
		Last Modified: Thu, 02 Feb 2023 21:02:15 GMT  
		Size: 81.1 MB (81067307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
