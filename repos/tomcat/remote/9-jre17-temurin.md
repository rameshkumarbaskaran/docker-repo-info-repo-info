## `tomcat:9-jre17-temurin`

```console
$ docker pull tomcat@sha256:ff85721f23eeb694bd2be0c8a464ad997d6f9c0f546bec33bf69169025f1e22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:32faa6f18c923f69cae768945d50a63c4ecd87f99fd21a2964a2d25740336429
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106864711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34ebfb9ebe154b5f0991061856fa6744db9d226449242b099bf33714e08d46`
-	Default Command: `["catalina.sh","run"]`

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
# Fri, 02 Sep 2022 05:24:55 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:25:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e4137529319cd7935f74e1289025b7b4c794c0fb47a3d138adffbd1bbc0ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b63f532cb8b30e4d0bd18d52f08c1933e3cf66aeb373180d002274b6d94b4a25';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='02947997297742ac5a7064fc5414042071fb96d0260d3756100abb281eff3cde';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f594458bbf42d1d43f7fb5880d0b09d5f9ac11e8eea0de8756419228a823d21c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e96814ee145a599397d91e16831d2dddc3c6b8e8517a8527e28e727649aaa2d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:25:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:35:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 10:35:12 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:35:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 10:35:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 10:35:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:35:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:41:37 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 10:41:37 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 00:44:50 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 00:44:50 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 00:44:51 GMT
COPY dir:f6ad66b2c9389953a597282f3f87e65a6ed58d9c9019d4913262d54d8456d4b5 in /usr/local/tomcat 
# Tue, 27 Sep 2022 00:44:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 00:44:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 00:44:56 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 00:44:56 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:89d66e37a1bafafaeaec8b2eeab06e70e4fc71c6bc00282701d4e36bc65d04f1`  
		Last Modified: Fri, 02 Sep 2022 05:32:10 GMT  
		Size: 46.8 MB (46806032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88abbee52af5c71a32880d2d96c4dfc6bc24d2035b92719a2f53a10cc6df898b`  
		Last Modified: Fri, 02 Sep 2022 05:32:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91860fe182ba9e919e734f5cc2821fad62b451338f2d1117f4ec1b7cb3e9c6a7`  
		Last Modified: Fri, 02 Sep 2022 10:56:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94ccecf5249b1cf90aca7b7b777ad4e5ed79feaea0ad54ea29015e508c8cb04`  
		Last Modified: Tue, 27 Sep 2022 01:11:25 GMT  
		Size: 12.2 MB (12190967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0714807ce0ced93cfb4f33a478648def176e969a8a193a88b404eeef81d5b5ca`  
		Last Modified: Tue, 27 Sep 2022 01:11:24 GMT  
		Size: 455.2 KB (455236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b21eacda2047ea88a7251f2db4dd6810cf0f2731e0b2a3668628a440134b397`  
		Last Modified: Tue, 27 Sep 2022 01:11:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:9632becc13e24b89ba09dd70fa4139af339e3968cfe39d77a7d356b0cb8f6656
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101018953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399b4f0611cfe7436fb1f34e87df56bd45df149c9bbb4410d53692c36f3a7080`
-	Default Command: `["catalina.sh","run"]`

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
# Fri, 02 Sep 2022 09:48:41 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 09:49:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e4137529319cd7935f74e1289025b7b4c794c0fb47a3d138adffbd1bbc0ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b63f532cb8b30e4d0bd18d52f08c1933e3cf66aeb373180d002274b6d94b4a25';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='02947997297742ac5a7064fc5414042071fb96d0260d3756100abb281eff3cde';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f594458bbf42d1d43f7fb5880d0b09d5f9ac11e8eea0de8756419228a823d21c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e96814ee145a599397d91e16831d2dddc3c6b8e8517a8527e28e727649aaa2d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 09:49:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 18:44:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 18:44:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 18:44:12 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 18:44:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 18:44:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 18:44:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 18:53:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 18:53:24 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 10:47:34 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 10:47:34 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 10:47:35 GMT
COPY dir:17e7227c8dc33c894183b914b8148e692a5f8736c1debb6d6772ac129662e589 in /usr/local/tomcat 
# Tue, 27 Sep 2022 10:47:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 10:47:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 10:47:47 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 10:47:47 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:13f14851f3004ac1e836b8fd67a2951420d29c2522b76d36d83c51e9ea3827e2`  
		Last Modified: Fri, 02 Sep 2022 09:57:13 GMT  
		Size: 44.3 MB (44341131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a418544103d978f0722a0a71f89ad30a5c420525ff2c1ec918132bf1dabe5c8`  
		Last Modified: Fri, 02 Sep 2022 09:57:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cba65bf8a2527a8104c558cc2f077b28ce086ed51e78dee6c17f634503cfbd`  
		Last Modified: Fri, 02 Sep 2022 19:17:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e336f6218a3ab8d1ffaa595dcfe783252b7cf7d3e1eb91c60a9c5c2e027f0`  
		Last Modified: Tue, 27 Sep 2022 11:15:19 GMT  
		Size: 12.1 MB (12125555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4008df2df82ab28ee251e282a2df1cf66c6fe0e9441f12ce2a4bd209695a8923`  
		Last Modified: Tue, 27 Sep 2022 11:15:17 GMT  
		Size: 429.1 KB (429150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddba07e6eb87428e604c1836bab7bfdb064367e659a1efa3d6f80cd8c17ef66f`  
		Last Modified: Tue, 27 Sep 2022 11:15:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:df3c20e7f79ea66c2bafa204c8de95efedd3f26b4a018d023bdc4c6a82f614ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105461801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b668447f1b759793d7a093a454e7c3d7ab749e59dbbe8521f4a49d7a3e5a6aeb`
-	Default Command: `["catalina.sh","run"]`

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
# Fri, 02 Sep 2022 04:59:28 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 05:00:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e4137529319cd7935f74e1289025b7b4c794c0fb47a3d138adffbd1bbc0ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b63f532cb8b30e4d0bd18d52f08c1933e3cf66aeb373180d002274b6d94b4a25';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='02947997297742ac5a7064fc5414042071fb96d0260d3756100abb281eff3cde';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f594458bbf42d1d43f7fb5880d0b09d5f9ac11e8eea0de8756419228a823d21c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e96814ee145a599397d91e16831d2dddc3c6b8e8517a8527e28e727649aaa2d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:00:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 09:14:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 09:14:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 09:14:49 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 09:14:50 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 09:14:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:14:52 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:25:52 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 09:25:53 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 01:11:58 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 01:11:58 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 01:12:00 GMT
COPY dir:e253992f11454fc7c9c6036b101a59899bf3570e98e088d7a400653c4fd3c58d in /usr/local/tomcat 
# Tue, 27 Sep 2022 01:12:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 01:12:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 01:12:10 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 01:12:11 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:7f0ecd5da9e82be7865fb237fbab11da50546b977db6264c943e31a327b8462a`  
		Last Modified: Fri, 02 Sep 2022 05:08:41 GMT  
		Size: 46.2 MB (46246807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8631aa4afee3e67c3dbf3273098a4ba92f732f41f01d1ea9831b6f5b7515d614`  
		Last Modified: Fri, 02 Sep 2022 05:08:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148698c9517e720e40fd72a273222686be3d87ea26e74962fdd85232f1000c7b`  
		Last Modified: Fri, 02 Sep 2022 09:51:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e6bb9ad14072fe17cc003f10b7b42ebc21383de925553e8846ccffb4f0751`  
		Last Modified: Tue, 27 Sep 2022 01:33:45 GMT  
		Size: 12.2 MB (12198630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80d5999a52e7c0a4aa9b81ae77f08585f8122be1dd34307c2e2520dc68c7c1e`  
		Last Modified: Tue, 27 Sep 2022 01:33:44 GMT  
		Size: 216.8 KB (216815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6c5f639c70f87b39343d13072cc7fa38608161e1ad3a5e707d96208fb8970378
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113315281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5e3d3f24799f4fd36b68a424e7736bd4b4b91c6d3447193d39a450a4b23f11`
-	Default Command: `["catalina.sh","run"]`

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
# Fri, 02 Sep 2022 04:06:39 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Fri, 02 Sep 2022 04:07:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e4137529319cd7935f74e1289025b7b4c794c0fb47a3d138adffbd1bbc0ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b63f532cb8b30e4d0bd18d52f08c1933e3cf66aeb373180d002274b6d94b4a25';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='02947997297742ac5a7064fc5414042071fb96d0260d3756100abb281eff3cde';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f594458bbf42d1d43f7fb5880d0b09d5f9ac11e8eea0de8756419228a823d21c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e96814ee145a599397d91e16831d2dddc3c6b8e8517a8527e28e727649aaa2d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:07:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 07:01:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 07:01:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 07:01:46 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 07:01:46 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 07:01:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 07:01:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 07:14:58 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 07:14:58 GMT
ENV TOMCAT_MAJOR=9
# Tue, 27 Sep 2022 01:44:47 GMT
ENV TOMCAT_VERSION=9.0.67
# Tue, 27 Sep 2022 01:44:47 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Tue, 27 Sep 2022 01:44:48 GMT
COPY dir:daa01cf8119baa5030a3c7ec78f1f384933b3577cffb9e9acac9d15edc2fdd62 in /usr/local/tomcat 
# Tue, 27 Sep 2022 01:44:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2022 01:44:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 27 Sep 2022 01:44:58 GMT
EXPOSE 8080
# Tue, 27 Sep 2022 01:44:59 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:7e17a61ad61a7f9359ae9fd7cdae67fe31d9c944666e253a7b41d68e9721a6f1`  
		Last Modified: Fri, 02 Sep 2022 04:18:14 GMT  
		Size: 46.6 MB (46620325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217f44725f902a3b4fa165ba09e3bef5b95a2b52846851283f37f65d788739af`  
		Last Modified: Fri, 02 Sep 2022 04:18:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e082032ff47438142f76a056f130d1c63769b4a11a2e064562f444e8f0cab4f`  
		Last Modified: Fri, 02 Sep 2022 07:43:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c433d88e57e48740f84c554f9c2b3dc301197be35bacbaefb90510e47bac2e31`  
		Last Modified: Tue, 27 Sep 2022 02:07:18 GMT  
		Size: 12.2 MB (12219601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877d06bb7c1b727ba96b4825c119c58c00d650bdab7eb05349bd4d91cf252a8b`  
		Last Modified: Tue, 27 Sep 2022 02:07:17 GMT  
		Size: 486.3 KB (486284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fbedfac88f78bc85ff70a62ea7900b6083b664b93a1a6c5eee0303822a05ac`  
		Last Modified: Tue, 27 Sep 2022 02:07:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:73c2c7ea913b2a592495340ff79cb2e649af427e766fc6f517d426c992df27e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101749987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c900c1f318264406236061f4cb15af0b57b9e9102fe6681709584235c6ac10fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 04 Oct 2022 23:52:57 GMT
ADD file:b1fcc8690fce8195995c8eab6b853225d65017d69692537273760bf84bfb72ec in / 
# Tue, 04 Oct 2022 23:52:59 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 07:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 07:55:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 07:57:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 07:57:57 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1
# Wed, 05 Oct 2022 07:59:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2e4137529319cd7935f74e1289025b7b4c794c0fb47a3d138adffbd1bbc0ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        armhf|arm)          ESUM='b63f532cb8b30e4d0bd18d52f08c1933e3cf66aeb373180d002274b6d94b4a25';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='02947997297742ac5a7064fc5414042071fb96d0260d3756100abb281eff3cde';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f594458bbf42d1d43f7fb5880d0b09d5f9ac11e8eea0de8756419228a823d21c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e96814ee145a599397d91e16831d2dddc3c6b8e8517a8527e28e727649aaa2d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.4.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 05 Oct 2022 07:59:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Wed, 05 Oct 2022 18:06:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Oct 2022 18:06:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 18:06:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Oct 2022 18:06:55 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Oct 2022 18:06:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Oct 2022 18:06:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Oct 2022 18:11:41 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Oct 2022 18:11:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 05 Oct 2022 18:11:41 GMT
ENV TOMCAT_VERSION=9.0.67
# Wed, 05 Oct 2022 18:11:41 GMT
ENV TOMCAT_SHA512=f3c4841754640a21842de9d8ec4674b1a072d42f3ba9d1accea143a61ac4f77b06c789fbcc395c23ed2154ec7e7cd76e6d39743e544f7c6f2022967e8a2334d5
# Wed, 05 Oct 2022 18:11:42 GMT
COPY dir:da39e8d4e0104badfb83c6083d682f7131af0270516a065aeda87a8f070c6e54 in /usr/local/tomcat 
# Wed, 05 Oct 2022 18:11:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 18:11:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Oct 2022 18:11:46 GMT
EXPOSE 8080
# Wed, 05 Oct 2022 18:11:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:29c30188ad5f0c76a8b336bfa488a1bdf199dc8127ed81e4051c1c71d4da8f87`  
		Last Modified: Tue, 04 Oct 2022 23:54:34 GMT  
		Size: 28.6 MB (28643466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52739390b60a09956a7447b4a5e03687f23ee651c092732ffdc1b69a0764dd8`  
		Last Modified: Wed, 05 Oct 2022 08:04:28 GMT  
		Size: 16.8 MB (16766125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f9991fc19bb3c35655b342ac496229e68c7d56ad3790ea0e51d556505d1c7c`  
		Last Modified: Wed, 05 Oct 2022 08:05:07 GMT  
		Size: 43.7 MB (43693934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b96185e649756765f3b8af58d879adc6ccc38533cea5cb868b47a00ff8b2eea`  
		Last Modified: Wed, 05 Oct 2022 08:05:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69345bc0c9e822f306533a3d4030409a94caa0005dcae359f6b8c94d27d4272d`  
		Last Modified: Wed, 05 Oct 2022 18:23:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299bb9266b3856e834318fec6730ab63775cf6601bd709d0db93e110be66d74a`  
		Last Modified: Wed, 05 Oct 2022 18:27:16 GMT  
		Size: 12.2 MB (12189019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f1a72d42c8d5e501e66fc8ccee4d4b4b1c4c0c15716e44e55d2995aa9788ad`  
		Last Modified: Wed, 05 Oct 2022 18:27:16 GMT  
		Size: 457.0 KB (456981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916b02db4d01ade9c7ebe2a0f4eeccd29a814097924b193d3e45dbdaee41115`  
		Last Modified: Wed, 05 Oct 2022 18:27:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
