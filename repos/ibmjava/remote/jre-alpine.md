## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:aabd2f1b130c0e787dea6fe6220179b9749a1289ee1fae75b4c5b2e86c0a3dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:195182957c7eb930b7419eb2e3a8ead0d88bfc21039eff07418531b546e8a142
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137166626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcc2307ba9aec21621d33db8092ebe74af64608b6f54d956966a72cbb4e5741`
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
# Wed, 23 Feb 2022 18:20:53 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e2036ff825599773d0da7ca65e526ef4653e8060b787e5f9a4967fa73756cb56';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='f4639c53ae366cda315db5f504bf7596a9757d7dccb4be66cce6e447613672cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='0961aedeaab4801cadb3d7a327344e66ef5d7f982f9269d5a0e447e4699feee7';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2469075243605203690306e9022150b86da5e9b5c563bba7ae1c3413c65b9cbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='71abbc456c06850a3f557465e988b73ecf66a22d9fd7d8a57a03dc56849f06a4';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 23 Feb 2022 18:20:54 GMT
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
	-	`sha256:5970cdd91e499919232464640d391812b957c91161e892ef2c76cbbf3f1b79b1`  
		Last Modified: Wed, 23 Feb 2022 18:25:10 GMT  
		Size: 128.8 MB (128816714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
