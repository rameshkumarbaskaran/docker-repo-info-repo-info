## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:e818ef50ac2f8e6b149b4332abaa65b3382c204ff6771022e8c4c7330e2dc3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ead5989913e603d8d12b017caf2224b84f8d2ebccfc71aae0ca2bf8820bd55ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217298473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85f668c7770a92ca6a503a3732c967880ff3af2487074390663806f3562864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:40 GMT
COPY dir:7964ac201a93d838933b1631de52186ab9a9c98f572a75fd024299ea94e621fa in / 
# Wed, 20 Dec 2023 08:49:41 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:26:45 GMT
ARG version=11.0.21.9-1
# Wed, 20 Dec 2023 09:29:03 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 20 Dec 2023 09:29:03 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:29:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:99e9b04a7dc206f4a47a0937a2039102066a5273ce57a11fa6894d90fe3957bc`  
		Last Modified: Wed, 20 Dec 2023 08:50:39 GMT  
		Size: 62.6 MB (62645506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e02bedf0457617b3158b12f456b819b5d194e22e1de9912b98b41b716e3cfeb`  
		Last Modified: Wed, 20 Dec 2023 09:40:57 GMT  
		Size: 154.7 MB (154652967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7480861316bd8ff7b3f9838abfa6a743b26446e0ed4f82fcf8792238e25d0a0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211170609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff597cae0c89ede0aedd6a10b9c365a8cd723ecff345d0c7a5c30b2b4d7d853f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:23 GMT
COPY dir:380956fd469c5bff2cfd19545c66184d8301b431f1a3cd9c8338b2680a7f7a2b in / 
# Wed, 20 Dec 2023 01:32:24 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 01:57:35 GMT
ARG version=11.0.21.9-1
# Wed, 20 Dec 2023 01:59:19 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 20 Dec 2023 01:59:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 01:59:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1cdee3d784afc8dc3a31863ea6b75bfb24c3394d454dd5ca221d29fbd4c3f130`  
		Last Modified: Wed, 20 Dec 2023 01:32:56 GMT  
		Size: 64.4 MB (64445029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf02f60e524b64db03de2b2261e54aee02b0661850f5183fdf59f7d1acafd93d`  
		Last Modified: Wed, 20 Dec 2023 02:08:48 GMT  
		Size: 146.7 MB (146725580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
