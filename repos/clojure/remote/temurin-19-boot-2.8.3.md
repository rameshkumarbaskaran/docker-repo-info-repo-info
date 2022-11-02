## `clojure:temurin-19-boot-2.8.3`

```console
$ docker pull clojure@sha256:be95aaf6763c8a954cbb97ff84c0a9c2d8c7a173d377ae4d2ec51fd4e640fa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:e90625de5299ec8670ed2820f32f5eaeda41f8d90ed9369ea30829d83cfe629b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307424437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4479830998155bb064a4fc94accc4473412ea40c8248728d057420ac3520f65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 02 Nov 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:46:23 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 18:46:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 18:46:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 18:46:40 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:18:29 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:18:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:18:29 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:18:34 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:18:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:18:52 GMT
RUN boot
# Wed, 02 Nov 2022 20:18:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:18:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:18:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fa72e018dd1c616d4bdb23d6fbb735820db9a943b470a787973556d4ee24e`  
		Last Modified: Wed, 02 Nov 2022 18:50:22 GMT  
		Size: 17.0 MB (16986189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be68af618289efb6a189cb5adf042aeb201cc90dc568832de1d22bf09c28239`  
		Last Modified: Wed, 02 Nov 2022 18:51:22 GMT  
		Size: 200.9 MB (200852998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe61642fd50a00b1e64bb99d83f68065ea661478fb56e5b682b868401aeda8`  
		Last Modified: Wed, 02 Nov 2022 18:51:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae7f71b5f41ac059260ff3d91be4fd55b589180a64a0ef87d7743429ff81422`  
		Last Modified: Wed, 02 Nov 2022 20:30:38 GMT  
		Size: 338.6 KB (338619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8730a4d1099822466c8bce3d9deead02ecf0b6dc068b7fa8ae73acd49be3ba2b`  
		Last Modified: Wed, 02 Nov 2022 20:30:41 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a085a8d7571293ac7f2b5399d4223c00a99d24a72c75877bf4832f5d4c8657a2`  
		Last Modified: Wed, 02 Nov 2022 20:30:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f40089ea497d4bcd5f95eef6a28db033f0f906a868aca13e73da6d3f8a480cba
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305547934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c906926508156f7ca79142fda62c0b74c7c92fcb6f66a30995515fa131471e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 02 Nov 2022 19:45:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:46:27 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 19:46:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 19:46:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 19:46:44 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:53:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:53:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:53:19 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:53:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:53:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:53:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:53:40 GMT
RUN boot
# Wed, 02 Nov 2022 20:53:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:53:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:53:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d9c230ad7b20621780183623ce76b7c296e1db90d16a51deeb03f19e2493c`  
		Last Modified: Wed, 02 Nov 2022 19:49:51 GMT  
		Size: 18.4 MB (18416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad0c2cd6437a19e827e089c26dc673cb9b759584447394ca75a59d7262cbbc`  
		Last Modified: Wed, 02 Nov 2022 19:50:48 GMT  
		Size: 199.6 MB (199589982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7bc6d25e82c611ff8eda9d3d6ce3092c1680a8f792973b0f5a9b5d1775da39`  
		Last Modified: Wed, 02 Nov 2022 19:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502cd8028a83bf5e97f51a5f3fad43dfe2d86d75fdb4a18d62f88238e361fb0`  
		Last Modified: Wed, 02 Nov 2022 21:04:18 GMT  
		Size: 338.7 KB (338674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d47b87b495c516433789f7d996af04e502f23095215c1c87162b31293afbcf0`  
		Last Modified: Wed, 02 Nov 2022 21:04:20 GMT  
		Size: 58.8 MB (58820373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c552151eec0d1434f7ea7f2dfb8bf44dbe0767b1d1c3b7bd46fc6a359174a3`  
		Last Modified: Wed, 02 Nov 2022 21:04:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
