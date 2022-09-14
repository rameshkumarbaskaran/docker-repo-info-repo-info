## `eclipse-temurin:18-jre`

```console
$ docker pull eclipse-temurin@sha256:76246c2bef9e0876aa139a441e08fd7013921d34276326290d9c0f2c3b6f78d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `eclipse-temurin:18-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0d503e979d1b0c61d122a26985e23e42e87741198fd967c0c1efeefbd240ff95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94091435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39473b6fc06af035f8670c6dcaf44dc572693bae11b61bc424d4a46468846fae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 05:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 05:22:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 05:24:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:25:56 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Fri, 02 Sep 2022 05:26:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e11e00438c2f6f79f86ff1ca2b015913b0e16bd9491953a082d5c786402cb50a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='0ae7281fa883de0d39a75b39bfbbcec1d2a5f8ed8691af12226962ce1a761cd7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2298504c99b4c15f620f70415215e481766d2b2f784d066206eed8c583922f8f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='52bc6f5420ae46e8b9868c63c1d9b5af77d21ef5bda413617b2ad3fbb6b6c64a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74f602ab5abaa554859a5e92a65e5bb6e23c2d4165228299c7f54ed56dbc5959';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:26:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a58ffb4a943ab9205ec8ee456a88a4993ebcd34fca832aa0c3b0162cd79480`  
		Last Modified: Fri, 02 Sep 2022 05:31:23 GMT  
		Size: 17.0 MB (16985308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312b85e06e660e5be2915e474f238649b9d82009d49a15b0f29e29ec2654487`  
		Last Modified: Fri, 02 Sep 2022 05:33:39 GMT  
		Size: 46.7 MB (46679261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f41b780441d3b26a8d21852c7f9aa0477fa6c195d26905e693cd8833dc9e54a`  
		Last Modified: Fri, 02 Sep 2022 05:33:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:9413b271ac80b5857cca4d589e72ce8bff98a1517514f163072ca3eb23ec5885
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88459990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb42b9fc3642d013f6b0946c1c7ea95fccdaffe3c1aa8927e4606246a5736d9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:32 GMT
ADD file:8b109e7521f26505639a07128de43f93636fcc05ecf26c6358f893f22df38acd in / 
# Fri, 02 Sep 2022 06:08:32 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 09:45:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 09:45:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 09:45:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 09:48:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:49:51 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Fri, 02 Sep 2022 09:50:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e11e00438c2f6f79f86ff1ca2b015913b0e16bd9491953a082d5c786402cb50a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='0ae7281fa883de0d39a75b39bfbbcec1d2a5f8ed8691af12226962ce1a761cd7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2298504c99b4c15f620f70415215e481766d2b2f784d066206eed8c583922f8f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='52bc6f5420ae46e8b9868c63c1d9b5af77d21ef5bda413617b2ad3fbb6b6c64a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74f602ab5abaa554859a5e92a65e5bb6e23c2d4165228299c7f54ed56dbc5959';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 09:50:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:af25ea170fdc3ef953710312fcb7b9706eae0149cf05cd81c8281f1c511208bb`  
		Last Modified: Fri, 02 Sep 2022 06:10:34 GMT  
		Size: 27.0 MB (27016783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a174d21dfcc6012ca278ff8288f06ad5bbcf153a41bb1ad9f2d81bbffb133`  
		Last Modified: Fri, 02 Sep 2022 09:56:19 GMT  
		Size: 17.1 MB (17105870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9227c26e2e40f9e0083a2f7e70313b2581f093f4768c5d9fec03696d8d099c52`  
		Last Modified: Fri, 02 Sep 2022 09:58:53 GMT  
		Size: 44.3 MB (44337178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c289d342a8c1e1a2698399852b639f7e49258ebced6b18f385bd848850679c`  
		Last Modified: Fri, 02 Sep 2022 09:58:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:07f3fa500184c79c85b17cb00acf17b2f02490aab2070b039d9f3e3c985df3dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92971064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8014f123e124e9ba45ee6291ba397f00db88a5612289659e681355077ac6b53`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:56:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:56:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:56:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:59:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:51 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Fri, 02 Sep 2022 05:01:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e11e00438c2f6f79f86ff1ca2b015913b0e16bd9491953a082d5c786402cb50a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='0ae7281fa883de0d39a75b39bfbbcec1d2a5f8ed8691af12226962ce1a761cd7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2298504c99b4c15f620f70415215e481766d2b2f784d066206eed8c583922f8f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='52bc6f5420ae46e8b9868c63c1d9b5af77d21ef5bda413617b2ad3fbb6b6c64a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74f602ab5abaa554859a5e92a65e5bb6e23c2d4165228299c7f54ed56dbc5959';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:01:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948ed504bea9f0b27111de5ca0d2086e160f6df8abc460af1a3b7be67def00da`  
		Last Modified: Fri, 02 Sep 2022 05:07:45 GMT  
		Size: 18.4 MB (18417910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c90ec9b056586d3c10a1aff61fe123130b0ed2f3d0caf6b4917d427d50fe6ec`  
		Last Modified: Fri, 02 Sep 2022 05:10:23 GMT  
		Size: 46.2 MB (46171657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaaabe6b00885f8bd0b1e42e1637f8f9e03ec2eae2acc1719c52ba6835a002a`  
		Last Modified: Fri, 02 Sep 2022 05:10:16 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a92b72c6e295b01fff5cd6b64d885e30b42269ece3e5d935883ba5265bd1953b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100486858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe2e39ac7a34f66feb62784c7b40e5a60c9c59e30c728fcd2b755665b1c4d61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:50:09 GMT
ADD file:39b6fa94f6e1300a6fc4b6094e8250c22ecaa6e7c9f934841765d45b919402c5 in / 
# Thu, 01 Sep 2022 23:50:11 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:01:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 04:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:01:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:06:38 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:08:41 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Fri, 02 Sep 2022 04:09:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e11e00438c2f6f79f86ff1ca2b015913b0e16bd9491953a082d5c786402cb50a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='0ae7281fa883de0d39a75b39bfbbcec1d2a5f8ed8691af12226962ce1a761cd7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2298504c99b4c15f620f70415215e481766d2b2f784d066206eed8c583922f8f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='52bc6f5420ae46e8b9868c63c1d9b5af77d21ef5bda413617b2ad3fbb6b6c64a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74f602ab5abaa554859a5e92a65e5bb6e23c2d4165228299c7f54ed56dbc5959';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:09:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9ef77d5e46df05bf9f34e5871097fd038295a2aa5e29f1806ac3a96aa2545b5f`  
		Last Modified: Thu, 01 Sep 2022 23:52:34 GMT  
		Size: 35.7 MB (35721187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85977b7295954c6e2da6bc787d829a272b82f21a297819241fc4c76ae09fc1e`  
		Last Modified: Fri, 02 Sep 2022 04:17:02 GMT  
		Size: 18.3 MB (18267419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9728edb18a60dc4d6fd7d6db1035e9281593f7656e842c88e0603ef4cad6213`  
		Last Modified: Fri, 02 Sep 2022 04:20:27 GMT  
		Size: 46.5 MB (46498092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f165f0cb32cd7d6be5fcc97d216e29929bae42843110f4150c6bcf06cf2a3986`  
		Last Modified: Fri, 02 Sep 2022 04:20:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:089fd5f58420e210200cde79ba9f2b0ef4d85f5e52f56fb66bed4304e4961237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88882384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53cae19f5edf88e9939fb0fb3017bfff838d9d7bf194d7807aaafad2f8acdc5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:25 GMT
ADD file:aabc057fd7b1b1f9b4b729222b6dc90e98f846a65bfee1ee57cc899b6cee5a10 in / 
# Fri, 02 Sep 2022 01:03:28 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 01:22:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Sep 2022 01:22:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 01:22:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 01:24:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:26:20 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Fri, 02 Sep 2022 01:26:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e11e00438c2f6f79f86ff1ca2b015913b0e16bd9491953a082d5c786402cb50a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='0ae7281fa883de0d39a75b39bfbbcec1d2a5f8ed8691af12226962ce1a761cd7';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='2298504c99b4c15f620f70415215e481766d2b2f784d066206eed8c583922f8f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='52bc6f5420ae46e8b9868c63c1d9b5af77d21ef5bda413617b2ad3fbb6b6c64a';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='74f602ab5abaa554859a5e92a65e5bb6e23c2d4165228299c7f54ed56dbc5959';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 01:27:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a32e6a15a6635185097921b9d08997d505b6b6500b6c142ad8e718d87c45ffad`  
		Last Modified: Fri, 02 Sep 2022 01:05:01 GMT  
		Size: 28.6 MB (28643161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d6cf4ff256fd1049dace9d5ac1af95d347b696965a0296a5e6aee3c03bb52`  
		Last Modified: Fri, 02 Sep 2022 01:30:04 GMT  
		Size: 16.8 MB (16765672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446140f4571f07052d805549b4dc06fd1360e0e3014e8ca84214d273b0064a06`  
		Last Modified: Fri, 02 Sep 2022 01:31:49 GMT  
		Size: 43.5 MB (43473391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e3342ac32fc3efd63a9b38414d758bf3141a38ad9418558e46f0ef0e7bb095`  
		Last Modified: Fri, 02 Sep 2022 01:31:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - windows version 10.0.20348.1006; amd64

```console
$ docker pull eclipse-temurin@sha256:89081094738c37d46deab5cb9c0b7312aefaf9dd3b6357893a1bc6c58e38322a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2422019687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb5602ecde02d6b3527e295bfee39d41b61eb4b1e3f57254f8d553181f73581`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:26:32 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:34:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ;     Write-Host ('Verifying sha256 (1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:34:55 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5b521ee82dff3a1edca26df6b02fa9c803362e173a6a27332ce7aaf59c045`  
		Last Modified: Wed, 14 Sep 2022 16:54:24 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e5a9351e38dde5dee2f9ecdaee608d42b5713d9e857333aa27c5d88cccb4be`  
		Last Modified: Wed, 14 Sep 2022 16:56:36 GMT  
		Size: 74.5 MB (74530081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08f57849c29d61c77e4a6a31758e9b0639c09985809c73b4d7cf7b7d77502c3`  
		Last Modified: Wed, 14 Sep 2022 16:56:26 GMT  
		Size: 537.2 KB (537247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-jre` - windows version 10.0.17763.3406; amd64

```console
$ docker pull eclipse-temurin@sha256:9482c61e08b0d2850a2644573259b959e5493227845628e149f05953a647ff83
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2781070247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757a017eba725ebb6c04f019e6b2cb7bd1dde03b41eef8b70c3ff2d42e8d54f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 16:28:15 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Wed, 14 Sep 2022 16:36:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jre_x64_windows_hotspot_18.0.2.1_1.msi ;     Write-Host ('Verifying sha256 (1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e726c0ea2a8b25c2c75a8174df173dd54c98caa0235ef49d84a03292f152bfc') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-18' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Sep 2022 16:37:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a1bcd319e0d0b53c51f704f4020596a76b923e111317f26a7c9ceb586b8ce0`  
		Last Modified: Wed, 14 Sep 2022 16:55:08 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a114aa678560d5145019847839648c3843c88edddb1e4edc905ae8e4cf52fd1`  
		Last Modified: Wed, 14 Sep 2022 16:56:57 GMT  
		Size: 74.3 MB (74323833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e682d2b308248b8e4e67204cf3aea73c0223aff21df2b2c7d8a934aa5c2a55bd`  
		Last Modified: Wed, 14 Sep 2022 16:56:48 GMT  
		Size: 3.2 MB (3178882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
