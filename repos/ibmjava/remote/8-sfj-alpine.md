## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:58993c2c2608a1b2d17701553f26b0c164929a357f892257ba33db4c5c68147c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:8e1c08a89939ee68722b3f9e06925f4cc66487a9cc044e73135a8e357ab61d46
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72944821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508f54e13ec75e0ef13055b18fd95cccd9e14b2bd86e5c7a76978b2919e74fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 02:05:30 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 13 Nov 2021 02:05:31 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Sat, 13 Nov 2021 02:05:43 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 23 Feb 2022 18:20:21 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 23 Feb 2022 18:22:01 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 23 Feb 2022 18:22:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f8e3b09ebf8884133e8275541ed6d97df1dd1eac0c812e8981e6349756802a`  
		Last Modified: Sat, 13 Nov 2021 02:08:48 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0922b8d703a3bb90cd16ccf998a2ae91a50f98987dada91b7fa4d8bc26f2e4`  
		Last Modified: Sat, 13 Nov 2021 02:08:49 GMT  
		Size: 5.5 MB (5539897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da58960b0bf88434600a2281b0c46d2ce8d5986940b8a747d0785273775fb2d`  
		Last Modified: Wed, 23 Feb 2022 18:26:42 GMT  
		Size: 64.6 MB (64594909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
