## `eclipse-temurin:8-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:6e14341e883e29095ed127a074c09c7c4643d4f70713b0ebae863cb786d40848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:169c1a5c2500344adf8d4f5ebc58c3d961ecda62be8a87f036e010b418d23292
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84683436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d33b5c1b6e743f087853a785d780ac4b2f360581cbbdf28b4d6779cadf3463c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:44:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:20:09 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ced2591451da3a02e2b6bb44752b9e3f00d77789921be4df5082fb9f9880ad0`  
		Last Modified: Wed, 02 Nov 2022 18:48:43 GMT  
		Size: 12.4 MB (12439006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f23febae705afcbe0e1dbd31533557d90db42220fbf7e3d6a2c0732453318f`  
		Last Modified: Fri, 04 Nov 2022 23:26:42 GMT  
		Size: 41.8 MB (41818664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccbf47c061fb68ae0fb6b21e0e050d8ca99437b6abade62732747de2c9fb0d4`  
		Last Modified: Fri, 04 Nov 2022 23:26:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:c448956147ebdc3fc8de8f282697a694272d235ab5e2f5ac65bba8324a1c7c52
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78575672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de166e53d81609097a2ec8c05d9605940645d55c9ec4f66cf6092f03d1b478a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 17:58:54 GMT
ADD file:3acaa98e676fc52121edd2feea0fc71a60614dbf081f3db61809aab25af42a8c in / 
# Wed, 02 Nov 2022 17:58:54 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:35:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:35:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:35:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:35:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:58:15 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:59:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:59:08 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c3a947801223d5dd57236bed8663245ffddcbb4700ba3aec7edc7865fd8cd9d7`  
		Last Modified: Wed, 02 Nov 2022 18:00:26 GMT  
		Size: 27.0 MB (27020159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0829db637b9792b59814837768853e2024fa2d0f3ed5e36053294ccab7a0dd6`  
		Last Modified: Wed, 02 Nov 2022 18:45:01 GMT  
		Size: 12.0 MB (12012626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064e271d2360704d4839e1b892ac7121bfd35579980379557f6eb248fceb3346`  
		Last Modified: Fri, 04 Nov 2022 23:05:03 GMT  
		Size: 39.5 MB (39542760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433df5ff31ea4843c8939a0e9745c6af9c11ada0eece853f2912545e4e627b04`  
		Last Modified: Fri, 04 Nov 2022 23:04:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b51970023e900a7b063e0c245c18b89b2fff45f216c3f90b4f4c90d34cd7e6c0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81585991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181019742499f7c31ce21fa4ff76ba2cbcd25fab335c6f84c655e34b08812e82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 22:39:49 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 22:40:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 22:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a1af2bcd98f5f0d2f5e4da1a0e7bbe07a2c548e2662f7d37dce5ae1df46c`  
		Last Modified: Wed, 02 Nov 2022 19:48:28 GMT  
		Size: 12.4 MB (12396330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd66203f631549955cf8c4f71f60bc148efa34d467138bc7406e9b20cfd155c1`  
		Last Modified: Fri, 04 Nov 2022 22:44:50 GMT  
		Size: 40.8 MB (40807347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c8761d4b12ec391f3de7086ce2d5554b3a25b4073842d4d4c2b52f617a52d`  
		Last Modified: Fri, 04 Nov 2022 22:44:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5a3574f006f30aa2e7eaf8763df813213c390f326a4838d1d3dc026c00003a0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90187647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cf59aae8208845f6ffe1cb81f004f523839fbc470442106bdcef4fb90be255`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:55:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:56:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Nov 2022 23:17:18 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:18:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        armhf|arm)          ESUM='d5ef8ced672a1b391e7949190b8d24db16290e06f257816d5bd0969aed593852';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_arm_linux_hotspot_8u352b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Fri, 04 Nov 2022 23:18:26 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03873e196fa2aab86a981e0b5a73ace2c40cf4cd3da88abc4c2a4ce980ef6bc`  
		Last Modified: Wed, 02 Nov 2022 19:03:58 GMT  
		Size: 13.3 MB (13263240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77caf72d771e3770bb4b742ba76794160bc2a415a266012f4b3f48678e33dacd`  
		Last Modified: Fri, 04 Nov 2022 23:26:36 GMT  
		Size: 41.2 MB (41216665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12044dfe27fa028727095dd29c6e5fcda09571dd556c7beb6f09dfac06b7cb1`  
		Last Modified: Fri, 04 Nov 2022 23:26:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
