## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:91c5fe52a474e55dbfd9636c9f266bdd0338dc9a24a2709e0e96e9747f976cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0a6fd13ebf5e2b06d9315b20ed7b8b1d4ed6d71f78ccdf3243dded7ff962a224
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154059425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba56ddf1266ad1a3bb51d650c22f3255623132e8f2e128da3603805ac338f7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:38:11 GMT
COPY dir:bba3c324992ed0e5d34f0f5796fe9c0e46ced00dc01939b98cad3bc355594b38 in / 
# Thu, 12 Oct 2023 22:38:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:09:52 GMT
ARG version=17.0.8.8-1
# Thu, 12 Oct 2023 23:13:18 GMT
# ARGS: version=17.0.8.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Thu, 12 Oct 2023 23:13:18 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:13:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2b92a4a464539d6c28ffd6b40875226086ace1e24d6598d771d8a65a6938acb1`  
		Last Modified: Fri, 29 Sep 2023 04:44:19 GMT  
		Size: 62.5 MB (62469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4dca372ae3395bdbf5dff02710b293113d7db39f985641331e9663ffbaa0b9`  
		Last Modified: Thu, 12 Oct 2023 23:26:08 GMT  
		Size: 91.6 MB (91589780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b5fff073b7d41980766d31be3df5ecb005a61575fde7f276f4abc118beb7acb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (146046610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed517f5fa17bbe1eed90226e0169ad394c70f26c801557ead52f3099b1b4fde8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:24:12 GMT
COPY dir:826b274d38ec470bf9beb46977486da92a3347aff5fcb970deb82f445fd7f20e in / 
# Thu, 12 Oct 2023 22:24:13 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:44:48 GMT
ARG version=17.0.9.8-1
# Thu, 19 Oct 2023 00:46:56 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Thu, 19 Oct 2023 00:46:57 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:46:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d503fbdb054df5fe68cd13e3abb40a519885fcda4fbaf301b0667ae8c1285f4f`  
		Last Modified: Tue, 03 Oct 2023 00:59:41 GMT  
		Size: 64.2 MB (64163711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab9e5579de6b5e8ef33e39072d6dfea277d82f3471e8e6a0e52701cb5a83672`  
		Last Modified: Thu, 19 Oct 2023 01:02:23 GMT  
		Size: 81.9 MB (81882899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
