## `clojure:temurin-18-boot`

```console
$ docker pull clojure@sha256:d37e08dce71e746f39ea797afb6445896ff72a731ebc579693684267b404c141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-boot` - linux; amd64

```console
$ docker pull clojure@sha256:10ce2646e64088d455ecaa031be77954b8a7cba84945e17514f06907c13e7858
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300159177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039d044f11df4ecef292102dcc27e7c2055d0dae6ca22912bd6783968fb1c154`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:20:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:23:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Aug 2022 18:28:09 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:28:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='262be608e266fd76d7496af83b2832be853c3aaf7460d6a4da198cd40db74553';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='4cd49b92d13847bfad7b3bf635cca349e2c89c7641748c5288bc40d612cdbbd6';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='030261a2189a8f773fda543a85ab9beb4c430bf81ca5be37cf6cb970b5ccbb03';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='06d0f71e59b0d7112303a2eb95b1c3701054c868100837e642c6204ea71c0e2f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7d6beba8cfc0a8347f278f7414351191a95a707d46b6586e9a786f2669af0f8b';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Aug 2022 18:28:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:28:22 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 18:53:57 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 29 Aug 2022 18:53:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 29 Aug 2022 18:53:57 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 18:54:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 29 Aug 2022 18:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 29 Aug 2022 18:54:03 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 29 Aug 2022 18:54:21 GMT
RUN boot
# Mon, 29 Aug 2022 18:54:21 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 18:54:21 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 18:54:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ffabbc7d493a0023d83d0a6b1e82866abef587a22c60708a4f07dda563de6a`  
		Last Modified: Fri, 12 Aug 2022 17:32:48 GMT  
		Size: 17.0 MB (17001621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dfd3c955c87cc4f481decbed8d811ef68d88cd6f8161c17bc1a5a28214f2a8`  
		Last Modified: Mon, 29 Aug 2022 18:33:39 GMT  
		Size: 193.6 MB (193572386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa48bd4c65a5e9df5d3382230e8da11fae1429ab96f3caf14ce71a77704c2ba7`  
		Last Modified: Mon, 29 Aug 2022 18:33:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed84c7213abb3cc45e1ed7e875618b946696e7a47a3f25115fa1c7f9c1a901`  
		Last Modified: Mon, 29 Aug 2022 18:59:57 GMT  
		Size: 338.1 KB (338089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13274103eff1401cbdffcd7b87990abd610bc4234b1285090c5b6f3fcd1d7ce4`  
		Last Modified: Mon, 29 Aug 2022 19:00:00 GMT  
		Size: 58.8 MB (58820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a554630b852fc88ec1d25c524f20c1bcd7b6661f6d43d208303ac03bb17c58`  
		Last Modified: Mon, 29 Aug 2022 18:59:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f940237a0d3e38a716accd61affcee5cf752e67e20ca3a0e019e1677638697d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298143540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5bd5532858569315f3dbe572d553dd1fc52926e64837656e05eecf331cafc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:40:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 17:45:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 29 Aug 2022 18:41:46 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:41:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='262be608e266fd76d7496af83b2832be853c3aaf7460d6a4da198cd40db74553';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        armhf|arm)          ESUM='4cd49b92d13847bfad7b3bf635cca349e2c89c7641748c5288bc40d612cdbbd6';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='030261a2189a8f773fda543a85ab9beb4c430bf81ca5be37cf6cb970b5ccbb03';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='06d0f71e59b0d7112303a2eb95b1c3701054c868100837e642c6204ea71c0e2f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7d6beba8cfc0a8347f278f7414351191a95a707d46b6586e9a786f2669af0f8b';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Aug 2022 18:41:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:41:59 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 20:46:46 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 29 Aug 2022 20:46:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 29 Aug 2022 20:46:48 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 20:46:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 29 Aug 2022 20:46:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 29 Aug 2022 20:46:57 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 29 Aug 2022 20:47:10 GMT
RUN boot
# Mon, 29 Aug 2022 20:47:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 20:47:11 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 20:47:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3daf49bfff4711ea3e9c4de6d7bb8d1733d4b962c4d277384d83f2d8d98f367`  
		Last Modified: Fri, 12 Aug 2022 17:56:05 GMT  
		Size: 18.4 MB (18434264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5461e37007336e3ed01592a5dbea1d3424f3ee87a0c73731cbd9fb26c38eeaed`  
		Last Modified: Mon, 29 Aug 2022 18:46:50 GMT  
		Size: 192.4 MB (192410499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759425cc88e4fb9d5eae8a2b555c126108ddff9740dd1d6ee3c1c57c9dbc9fa6`  
		Last Modified: Mon, 29 Aug 2022 18:46:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ac8a35af548ba8f0e19c3975bcfa5afb5609a9ba659eaf4dbe33824b28467e`  
		Last Modified: Mon, 29 Aug 2022 20:53:39 GMT  
		Size: 101.2 KB (101205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b8c3bd51e1f8b6f1720bd6e51f67c98935aa2d64aa427f74ba80ecf8231007`  
		Last Modified: Mon, 29 Aug 2022 20:53:43 GMT  
		Size: 58.8 MB (58815856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7c89233253f52a9d31477bab515ba972cb195d360b9f7aeb925d545bbb8cfb`  
		Last Modified: Mon, 29 Aug 2022 20:53:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
