## `amazoncorretto:8u382-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:80f28a6b5fdb17b011a97b5c77872bb3b5792951b5ef1dd8c43dc84513d4868e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8u382-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a14d4816a8a636c44e69a41ca6ec3c0cbcc56d90cacfc540f8c6828a748b6a83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067d2fedeaab1a5706a0740838e7603266d5b8730d0dd08b944eff72e217861c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:20:25 GMT
COPY dir:a2da562c67b011c1b42effadc6ff06b6f82996c9f8d8c5778282cf441aac39a5 in / 
# Sat, 23 Sep 2023 00:20:25 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 00:37:40 GMT
ARG version=1.8.0_382.b05-1
# Sat, 23 Sep 2023 00:41:01 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Sat, 23 Sep 2023 00:41:01 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 00:41:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9aa850931a9d85a578215adaccd39361fe6ec5a8c81ead1837d4c5d43415b66b`  
		Last Modified: Mon, 18 Sep 2023 18:32:31 GMT  
		Size: 62.5 MB (62469678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6652cf381703a98d022b1144568d15e87a0160d1470f905669bfe72d107eb636`  
		Last Modified: Sat, 23 Sep 2023 00:57:19 GMT  
		Size: 125.6 MB (125556108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8u382-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:eecc4ce6c7cc648dcd5ba90db6d2d54d27b6ca42a03f158d3641c1210f5f3fd5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131605757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc435b0958cb63c0191eeb5734ae8726746e8359af22b1d2dd1eb97afd0bd65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 23 Sep 2023 00:39:47 GMT
COPY dir:5885a696cc03fd82c0c021dd701725b8b1bc11902dc8789780147154a555ba2a in / 
# Sat, 23 Sep 2023 00:39:48 GMT
CMD ["/bin/bash"]
# Sat, 23 Sep 2023 01:11:19 GMT
ARG version=1.8.0_382.b05-1
# Sat, 23 Sep 2023 01:13:15 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Sat, 23 Sep 2023 01:13:16 GMT
ENV LANG=C.UTF-8
# Sat, 23 Sep 2023 01:13:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0cd473df417d2282c9d0586281fb9293e3faf1fb6481fa584bac46295844f59e`  
		Last Modified: Mon, 18 Sep 2023 18:32:30 GMT  
		Size: 64.2 MB (64161861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0a6e393fa7dfa7d9fc0d054232558efed8da58a4050cd79f6637c3cea5d32`  
		Last Modified: Sat, 23 Sep 2023 01:25:51 GMT  
		Size: 67.4 MB (67443896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
