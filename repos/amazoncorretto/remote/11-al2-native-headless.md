## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:bebcede4b7170f429589558a3decfee2849a8f228f654bb71185c36840df9ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b27fc2729574d60fd02e57c624d3947f6dd824668f86bf7543600f115a64c449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (217048567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6183f8ca9b6523f6f9bbb83b160ebbeae18c556f4e95109774f4b2870e9a925c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:38:11 GMT
COPY dir:bba3c324992ed0e5d34f0f5796fe9c0e46ced00dc01939b98cad3bc355594b38 in / 
# Thu, 12 Oct 2023 22:38:11 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 23:05:49 GMT
ARG version=11.0.20.9-1
# Thu, 12 Oct 2023 23:08:23 GMT
# ARGS: version=11.0.20.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Thu, 12 Oct 2023 23:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 23:08:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2b92a4a464539d6c28ffd6b40875226086ace1e24d6598d771d8a65a6938acb1`  
		Last Modified: Fri, 29 Sep 2023 04:44:19 GMT  
		Size: 62.5 MB (62469645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff095920737e7d69e854d2f08c543a246b4c441087cf7608891fddcfa85df794`  
		Last Modified: Thu, 12 Oct 2023 23:23:24 GMT  
		Size: 154.6 MB (154578922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:077e12394100642bd99b36b34dee78eb8709ada525f7a842f24a1a3c93b673ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210892987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85866cc751d16e22767bf14a48396fd0188ea50c4a2789073c7541fefd30ed01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Oct 2023 22:24:12 GMT
COPY dir:826b274d38ec470bf9beb46977486da92a3347aff5fcb970deb82f445fd7f20e in / 
# Thu, 12 Oct 2023 22:24:13 GMT
CMD ["/bin/bash"]
# Thu, 19 Oct 2023 00:41:35 GMT
ARG version=11.0.21.9-1
# Thu, 19 Oct 2023 00:43:25 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Thu, 19 Oct 2023 00:43:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Oct 2023 00:43:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d503fbdb054df5fe68cd13e3abb40a519885fcda4fbaf301b0667ae8c1285f4f`  
		Last Modified: Tue, 03 Oct 2023 00:59:41 GMT  
		Size: 64.2 MB (64163711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9341e58160db5fec49cb666842ddce327b4496a002746af6f3d40d1fa96c816c`  
		Last Modified: Thu, 19 Oct 2023 00:58:03 GMT  
		Size: 146.7 MB (146729276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
