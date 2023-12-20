## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:241f8f44472a44e45e27fec6f4eb3c35c42d5fae89e3ed88330ef62e09f9b28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f39df3d37323f060537f088a7b96dcebc637a1cfb304ab201a73d6d0031072ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150332334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277a70d6ec709bbeb7caca8371efbe956d53b4a2aa163319b324ecbb386600dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 08:49:40 GMT
COPY dir:7964ac201a93d838933b1631de52186ab9a9c98f572a75fd024299ea94e621fa in / 
# Wed, 20 Dec 2023 08:49:41 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 09:30:09 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 09:32:19 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 20 Dec 2023 09:32:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 09:32:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:99e9b04a7dc206f4a47a0937a2039102066a5273ce57a11fa6894d90fe3957bc`  
		Last Modified: Wed, 20 Dec 2023 08:50:39 GMT  
		Size: 62.6 MB (62645506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8289f26f6722c152555ab8049f9bb7ca99818ab608c9e4918232928970d5a905`  
		Last Modified: Wed, 20 Dec 2023 09:43:14 GMT  
		Size: 87.7 MB (87686828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e613dce4ac79809151e10af02b4cb0217513f74210a3126b7366424fff69c78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144187137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34444ad20be94866b6ea2d14f4750e3f5a62d3ef54cb6320b7932fb183062d3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 Dec 2023 01:32:23 GMT
COPY dir:380956fd469c5bff2cfd19545c66184d8301b431f1a3cd9c8338b2680a7f7a2b in / 
# Wed, 20 Dec 2023 01:32:24 GMT
CMD ["/bin/bash"]
# Wed, 20 Dec 2023 02:00:07 GMT
ARG version=17.0.9.8-1
# Wed, 20 Dec 2023 02:01:52 GMT
# ARGS: version=17.0.9.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 20 Dec 2023 02:01:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 Dec 2023 02:01:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1cdee3d784afc8dc3a31863ea6b75bfb24c3394d454dd5ca221d29fbd4c3f130`  
		Last Modified: Wed, 20 Dec 2023 01:32:56 GMT  
		Size: 64.4 MB (64445029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536ba57c2f85c75d3fd9bd9056fac5b0feda5a2e01899099ee28689344ffbef9`  
		Last Modified: Wed, 20 Dec 2023 02:10:53 GMT  
		Size: 79.7 MB (79742108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
