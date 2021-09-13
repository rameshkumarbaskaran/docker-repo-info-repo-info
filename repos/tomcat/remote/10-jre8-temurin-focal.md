## `tomcat:10-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:06b20ee855efc563a982add396e201379b08e2fb79f968b0ac68ba115968df21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:10-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:a2b8870fd6828ec448921ff79faf3882bd86cace8b3bd201c23fcc813ec317a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99294484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7da88f8b48215a44609dff96e77b98add9a0dbf7472bdf5f1d051740105b94`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 03:31:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:31:24 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 31 Aug 2021 03:31:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 03:31:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 03:31:29 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 31 Aug 2021 20:46:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Aug 2021 20:46:38 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 20:46:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Aug 2021 20:46:39 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Aug 2021 20:46:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 20:46:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 20:46:40 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 31 Aug 2021 20:46:40 GMT
ENV TOMCAT_MAJOR=10
# Tue, 31 Aug 2021 20:46:41 GMT
ENV TOMCAT_VERSION=10.0.10
# Tue, 31 Aug 2021 20:46:41 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Mon, 13 Sep 2021 19:29:48 GMT
COPY dir:d79ec31db49248b789264b0a2c074df230b3947714a4674f7ff2948221e3a7b7 in /usr/local/tomcat 
# Mon, 13 Sep 2021 19:29:52 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 19:29:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Sep 2021 19:29:54 GMT
EXPOSE 8080
# Mon, 13 Sep 2021 19:29:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df1ad422e5a232e54d515fb2475eee78b57b25d905611bbceb50f364c0150c`  
		Last Modified: Tue, 31 Aug 2021 03:33:27 GMT  
		Size: 16.0 MB (16032853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb46219936bc211978885d2d8228192cde2547219658f31fac747332accbbb0b`  
		Last Modified: Tue, 31 Aug 2021 03:33:29 GMT  
		Size: 41.7 MB (41711956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6c8553572deee5a5a68b63b7f877418be1aa0e722442f97547b67a3b4aaec1`  
		Last Modified: Tue, 31 Aug 2021 03:33:24 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b3dc6145506c5bf51f1998f4482ef8ef4e6679d11e0bbbd8726a953bbf4c5`  
		Last Modified: Tue, 31 Aug 2021 21:44:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeef0d3a20e24a96b42337163cab601395da7f3dc609c7824db82690bbf5304`  
		Last Modified: Mon, 13 Sep 2021 19:50:29 GMT  
		Size: 12.5 MB (12533574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a6a6cc957095d1455a9634c4501cb005d8230579cd23810ddd09906996f846`  
		Last Modified: Mon, 13 Sep 2021 19:50:28 GMT  
		Size: 445.6 KB (445562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608243b12b717dd79dab3322ce6560279d79d629ba858d1a8c580cb12e90eb97`  
		Last Modified: Mon, 13 Sep 2021 19:50:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:07534e0f28331979ea264c7613a25f12e39f3ce35e046e7139b92f9eb911c145
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96811465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1388fba9722256831ebaeee852a14434165e6ecd2f8da61ac1e6199177447271`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 01:59:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:25:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:25:34 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 31 Aug 2021 02:25:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:25:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 02:25:39 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 01 Sep 2021 01:19:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 01 Sep 2021 01:19:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Sep 2021 01:19:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 01 Sep 2021 01:19:06 GMT
WORKDIR /usr/local/tomcat
# Wed, 01 Sep 2021 01:19:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 01 Sep 2021 01:19:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 01 Sep 2021 01:19:07 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 01 Sep 2021 01:19:07 GMT
ENV TOMCAT_MAJOR=10
# Wed, 01 Sep 2021 01:19:07 GMT
ENV TOMCAT_VERSION=10.0.10
# Wed, 01 Sep 2021 01:19:07 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Wed, 01 Sep 2021 01:19:08 GMT
COPY dir:7e442001c79f1acfd06d210cda097ea6f16dc0450f7545fbdcc5dfabb8e61eda in /usr/local/tomcat 
# Wed, 01 Sep 2021 01:19:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Sep 2021 01:19:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 01 Sep 2021 01:19:15 GMT
EXPOSE 8080
# Wed, 01 Sep 2021 01:19:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d8585069a0a852415434548e9df1c5314c6721293171b6ed14a607e76247d`  
		Last Modified: Tue, 31 Aug 2021 02:28:37 GMT  
		Size: 15.9 MB (15897608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be00a8d928ddbe13d7cbb1fc64e7c69e49cb7c11a808075d857972aa409d1a7d`  
		Last Modified: Tue, 31 Aug 2021 02:28:40 GMT  
		Size: 40.7 MB (40743716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4f192f0e6db1177bec5b029c96c4010f05051a4d7310d75984bcaed5eac419`  
		Last Modified: Tue, 31 Aug 2021 02:28:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e625078483edd199d16f9c533598452e728f030c944e3e3fcd9311370737d7e3`  
		Last Modified: Wed, 01 Sep 2021 02:28:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1d8c7741335aec892e85d5160c8ba38f4fc682e6a81765705bfd90736be6f`  
		Last Modified: Wed, 01 Sep 2021 02:28:03 GMT  
		Size: 12.6 MB (12550467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f555267adb01fd8d0425260439a3d5cf9b692a4d86a638f8935abb21aee507cb`  
		Last Modified: Wed, 01 Sep 2021 02:28:02 GMT  
		Size: 446.1 KB (446116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b4f241b81e8181ec6d793392894a13b0761ef38d759d19b76f92bfc5fd86e5`  
		Last Modified: Wed, 01 Sep 2021 02:28:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:1b9df995d4ad8a54e2adcb0717852056c1012c4284b92e84e6b78b29e3b741ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104681197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf402b17a1f813fa756963c643c2f96241679d998641191d390e0b921665936`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:40 GMT
ADD file:7e5ee5560faaa801aa10a76122190026f8c1da00c809f4fb6ff441751ba0c90f in / 
# Tue, 31 Aug 2021 02:10:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:31:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 05:45:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 05:45:47 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Tue, 31 Aug 2021 05:45:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9951a36430c14548f78569135956e929db2554bfc706bb3fe0bf9a14acd28055';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='0f242dc94b2c46f231e811427e30031cd1c7e5667979f8b403296008863d150e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|x86_64)          ESUM='a74e63657ad04151a8f95202071d2895f1cc9295c910ad3c361ff1cc27395107';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 05:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 05:46:10 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 31 Aug 2021 21:50:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Aug 2021 21:50:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 21:50:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Aug 2021 21:50:55 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Aug 2021 21:51:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 21:51:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 21:51:06 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 31 Aug 2021 21:51:07 GMT
ENV TOMCAT_MAJOR=10
# Tue, 31 Aug 2021 21:51:11 GMT
ENV TOMCAT_VERSION=10.0.10
# Tue, 31 Aug 2021 21:51:15 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Tue, 31 Aug 2021 21:51:17 GMT
COPY dir:710b0a5a296d39028ad178a6074f6984b34a80c0b3c7f1c885bfc169fcc26285 in /usr/local/tomcat 
# Tue, 31 Aug 2021 21:51:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 21:52:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Aug 2021 21:52:14 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 21:52:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:59390c695558464c51dc1fced64934b549770630192a1639ac6a90f59bd63b13`  
		Last Modified: Tue, 31 Aug 2021 02:14:21 GMT  
		Size: 33.3 MB (33291791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22897a482fa0e59d16e7302ee8b24736e577f4a14e821586507f289c961d84c9`  
		Last Modified: Tue, 31 Aug 2021 05:51:33 GMT  
		Size: 17.2 MB (17207875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecca0dae7238fce049f4be803709835981432da51c8a8783188b87945a97dd0`  
		Last Modified: Tue, 31 Aug 2021 05:51:36 GMT  
		Size: 41.1 MB (41136935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ad705fda28ad486de7bcef52bb4eb6ae0f6c6c8b99dce268677e4780dd5eac`  
		Last Modified: Tue, 31 Aug 2021 05:51:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242b1d1abd0f7ce5b3b0e88d6b27fcb45ab4b853efe3ee7c2babbc18876f7b7d`  
		Last Modified: Tue, 31 Aug 2021 22:34:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca13c66d3d92f0dee38967b3204edcf4a91e5d6fcaacaa43de4b3641748d582`  
		Last Modified: Tue, 31 Aug 2021 22:34:12 GMT  
		Size: 12.6 MB (12572802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18248c0c2e779715f5fb7eb68826371631a41a70920b5b56fa8c197255ddce01`  
		Last Modified: Tue, 31 Aug 2021 22:34:10 GMT  
		Size: 471.3 KB (471333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9754126f2f85ee36d4fb51247a1f4d6ddaf7cc69835608b6fe85bb6b9b33abda`  
		Last Modified: Tue, 31 Aug 2021 22:34:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
