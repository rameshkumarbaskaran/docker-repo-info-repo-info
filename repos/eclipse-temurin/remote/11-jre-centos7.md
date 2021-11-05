## `eclipse-temurin:11-jre-centos7`

```console
$ docker pull eclipse-temurin@sha256:a07658b10962a289cf90f3c991766eb932b230ef40e5c86c43fd607a0169fbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:11-jre-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d17e551028b5dda33af2eb59492064cc00bf8024e4b36320d21e8672e40e4c3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132004583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204ea2721d3d2b183c59ee020673e0a9d98c540ccf882fa39efdc70d981dac10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:51:48 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 27 Oct 2021 00:21:44 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Fri, 05 Nov 2021 19:20:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:20:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6893209e3a4a16d453c0b998ba34f62067ad6099b971afc4f30040eb1467d`  
		Last Modified: Wed, 15 Sep 2021 18:54:13 GMT  
		Size: 12.7 MB (12706445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6e13031a3cfa5bf8c8321430d7e8b7edd5bac27e35648a68347b33e77c4ea1`  
		Last Modified: Fri, 05 Nov 2021 19:24:29 GMT  
		Size: 43.2 MB (43200822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18494434a2f4ebf028cebf378f9482675dcdf85d0a93e4795199929ec7d9607`  
		Last Modified: Fri, 05 Nov 2021 19:24:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9d4a19dc644479e2f14073ded8b8a8862bef8754965aad9fa6330df86ab06012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162961360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64027dd1670c041846a1cdbccdf03326ca7e0c2de53bab7c2bdcf0bf0028f811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Oct 2021 03:25:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 03:26:24 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 27 Oct 2021 00:59:42 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Fri, 05 Nov 2021 19:41:00 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='76f7da05d905b5f9de8de1a34c1a206744f7589bf0eed876cd9069cb1d913806';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.13_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f267876675dac3da3f4ceccd44d812b57098505eeec5fb1688d54bdeffcd1da';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.13_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fb0a27e6e1f26a1ee79daa92e4cfe3ec0d676acfe114d99dd84b3414f056e8a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:41:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:41:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed710eb0a2f63323ad5c292c7cfd48094b0fee69aa1c789341819797baca66`  
		Last Modified: Sat, 16 Oct 2021 03:32:08 GMT  
		Size: 13.1 MB (13066395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fec0c896b10ea3ef1257390459175f4322385b9bd20f659285f325c3ff190fb`  
		Last Modified: Fri, 05 Nov 2021 19:45:06 GMT  
		Size: 41.5 MB (41519894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d88ea0bbb4b79014f6b6e0946e230599e083035efe0c6e8c7de7f4ac5b7ac8`  
		Last Modified: Fri, 05 Nov 2021 19:45:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b675968910c2b9bc1d86c634d4bc2c12461f10f26b47a88c9f1e366d2586b156
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131758630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39224dd0043275a3bc19cb1b93aa5a0ca06183ee5a961b002f80276d8794541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 21:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 21:29:19 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Wed, 15 Sep 2021 21:31:55 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Thu, 07 Oct 2021 19:26:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eebf9b6b515fd139d45410ea4a0e7c18f015acba41e677cd7a57d1fe7a553681';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.12_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='21129821a148503333dcc9868f04f3c971290c75f07ca384b1ab5d906901ea80';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.12_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e813e270b7ea0a13f9c400ce5abd4cb811aacbd536b8909e6c7f0e346f78348c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 07 Oct 2021 19:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 19:27:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f502386ff4e2195af1b6b4432c6ccd0fabc7a63dd38550f635eacaa707c74a`  
		Last Modified: Wed, 15 Sep 2021 21:38:40 GMT  
		Size: 12.6 MB (12616024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcc91dcb5659e6ccde72fcc595c645676b8118a92cdf2b01f85420e0acd79f1`  
		Last Modified: Thu, 07 Oct 2021 19:31:56 GMT  
		Size: 38.6 MB (38625986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa1c745c5a6d57546efea2a057925c1e5cd0df9f9d6607dcf7123ce4fa1150b`  
		Last Modified: Thu, 07 Oct 2021 19:31:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
