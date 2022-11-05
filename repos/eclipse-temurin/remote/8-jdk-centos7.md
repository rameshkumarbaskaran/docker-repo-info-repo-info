## `eclipse-temurin:8-jdk-centos7`

```console
$ docker pull eclipse-temurin@sha256:80b0419ba72e9c2d6e2b24283d0ebbe5c56a1a7fef645b2289d45f1c12810cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jdk-centos7` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4e08f467e71abf1bac93c63787819c26278c288305ffec77240510e3fb5af241
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193417713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f153824984c06f4e1617df2eba3e2a16d174cdb2de9b0f41a2e90a2deb7652c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 11 Aug 2022 19:21:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:21:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:21:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:21:19 GMT
RUN yum install -y tzdata openssl curl wget ca-certificates fontconfig gzip tar     && yum clean all
# Fri, 04 Nov 2022 23:20:18 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:23 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:20:25 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e946c336ceae859cd4d70967ac63af2f5351aed0dfe146fa12e896157d2c035`  
		Last Modified: Fri, 12 Aug 2022 17:28:51 GMT  
		Size: 13.8 MB (13789720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf3584f28a3d61a792e174749f8021c7e1cce2d3a4acf6ea8cf28c9f324624`  
		Last Modified: Fri, 04 Nov 2022 23:25:56 GMT  
		Size: 103.5 MB (103530677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a804dffe300b9b5af422f0f04336929e5307562f48fe913454613c40b5e5934c`  
		Last Modified: Fri, 04 Nov 2022 23:25:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:700dddadba1d71a1159b33787a577db165dae1c328c775a57dc2fb73f7f43544
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225385508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dd3684489d22cbd42340b6eb4a9c2c59038a8d14de27c99328808f9a54bda9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 01:09:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 01:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:09:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:09:36 GMT
RUN yum install -y tzdata openssl curl wget ca-certificates fontconfig gzip tar     && yum clean all
# Fri, 04 Nov 2022 22:39:58 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:07 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 22:40:09 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda7f1658b00328097c595ebc985d4147ed732e13a6abb6228f5db45ea35f873`  
		Last Modified: Wed, 26 Oct 2022 01:16:54 GMT  
		Size: 14.4 MB (14383757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73637542047de9f21a5d5671a731c0551c35459b8a4b6c3319de524d4fce2b`  
		Last Modified: Fri, 04 Nov 2022 22:44:20 GMT  
		Size: 102.6 MB (102626644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b108fbc0dae6b5e0065fcbc32b7409d5b6a4f9848e159ff51885dc43b8e6d35`  
		Last Modified: Fri, 04 Nov 2022 22:44:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jdk-centos7` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:78a2ee83c3282937ad9e3f01c5439928c5ff8d43914f3d95c348754161ba7da2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195270623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c464bb634fc396cac54ffca5e691b57ebdf5efe35a5b25da0de8319569a7613e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Thu, 11 Aug 2022 19:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:19:39 GMT
RUN yum install -y tzdata openssl curl wget ca-certificates fontconfig gzip tar     && yum clean all
# Fri, 04 Nov 2022 23:17:41 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:17:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:17:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0867462d675122ef191a9c60cfd06321372590626128884857fb78457b40b2a5`  
		Last Modified: Fri, 12 Aug 2022 17:33:43 GMT  
		Size: 13.7 MB (13725244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a2146693be8bc865d76cd05854da17be16c7080095071826634df0dedeb723`  
		Last Modified: Fri, 04 Nov 2022 23:25:54 GMT  
		Size: 101.0 MB (101028759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d2c9c6e6e4bcf9aaddd1fdc445aa40967e594d9cebf0bc50d035c3702a6e14`  
		Last Modified: Fri, 04 Nov 2022 23:25:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
