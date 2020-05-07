## `maven:3-ibmjava-8-alpine`

```console
$ docker pull maven@sha256:05ca682d48dd0acd6cd6d4da916b6df9941083af729f61cf7283010e1a13e779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-ibmjava-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:36a4440196f2adbff4154abdfcfa329ae1c683e3f40553dfeffae1f74ed3a5be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187080661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cf8a984cec00395382338de648082ff69a4c66440ac51bf07c53899d9c6b42`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:39:22 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:22 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 24 Apr 2020 14:40:42 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 06 May 2020 17:22:59 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:26:41 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1a330b630b173fcecaeb730494612c1a28f7b73ea6a9b7eb41f29a9136ef3863';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='94ea289890f9953f62d2f82cd8cfe4c69f8914c2b136e9bfe244b93f16a66ccd';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ea99ab28dd300b08940882d178247e99aafe5a998b1621cf288dfb247394e067';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='25dcbae84e3a8e4a0cc30b5c6fcf985886e59fcaf450149a3f724ece8745f967';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='85685deb69e377e63a26c33fe913dd206d70d1b40a25f44ac991abfe45a35dc2';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 06 May 2020 17:26:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:54:08 GMT
RUN apk add --no-cache curl tar bash procps
# Wed, 06 May 2020 18:54:09 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 06 May 2020 18:54:09 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 May 2020 18:54:09 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 06 May 2020 18:54:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 06 May 2020 18:54:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 May 2020 18:54:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 May 2020 18:54:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 May 2020 18:54:19 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 May 2020 18:54:19 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 May 2020 18:54:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 May 2020 18:54:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369d0408c211add55834354d71f8ff4d7f799ecaf4472b93c21ac4d9ac29b7b4`  
		Last Modified: Wed, 29 Apr 2020 03:28:28 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3289c53f301de0b6c28151df7a81b40d0ef1afa8399da07e02bcf6a86e8136fe`  
		Last Modified: Wed, 29 Apr 2020 03:28:30 GMT  
		Size: 5.6 MB (5565680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cbe773ac95a7aa4719d3ccfaea671e656497c7a20ab40a85986a10bba2f97`  
		Last Modified: Wed, 06 May 2020 18:35:09 GMT  
		Size: 167.5 MB (167475558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f691a612501921495878061a477d57b0914539596f884b8ae991b440cd8cf433`  
		Last Modified: Thu, 07 May 2020 21:24:59 GMT  
		Size: 1.7 MB (1660860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0179205eee4dbde6377240f2a3f6dc10457c59476cca49f44d48e1803f6f91`  
		Last Modified: Thu, 07 May 2020 21:25:00 GMT  
		Size: 9.6 MB (9581232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740066de9faf9b1194a350a819cfd6efeb993f124713a4569eabfb4a541c3c4c`  
		Last Modified: Thu, 07 May 2020 21:24:59 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f09307801ab23dfc3a68899d02073bd1309c6c99839e8387361bfc7ca92cb96`  
		Last Modified: Thu, 07 May 2020 21:24:59 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
