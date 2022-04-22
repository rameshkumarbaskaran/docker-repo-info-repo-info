## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:af13c67e1115f33d2b40c7be1ec024c5e54675c574c01f373ab5751015da6cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:bc3ce7c75655f9760ec6f98b5ffcf4208a9747cc52348c63bc583ab6049bde32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98058859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8aa11901e5d1d5d4df912c7b49543bc5a1fb0fecfbd285dad90b563282ca04`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:04:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:04:35 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Fri, 22 Apr 2022 02:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:04:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 22 Apr 2022 05:36:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Apr 2022 05:36:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 05:36:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Apr 2022 05:36:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Apr 2022 05:36:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:36:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:47:45 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 22 Apr 2022 05:47:45 GMT
ENV TOMCAT_MAJOR=8
# Fri, 22 Apr 2022 05:47:45 GMT
ENV TOMCAT_VERSION=8.5.78
# Fri, 22 Apr 2022 05:47:45 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Fri, 22 Apr 2022 05:47:45 GMT
COPY dir:5ad30b42d178c0dd858fd1e8e05a356dfb479f10b0f2c14bf710e6fe9c1215f8 in /usr/local/tomcat 
# Fri, 22 Apr 2022 05:47:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 05:47:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Apr 2022 05:47:51 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 05:47:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11e2aa9202b3c11a943dfa8adc2bef4462ab2165124b84051d10250faff2a0`  
		Last Modified: Fri, 22 Apr 2022 02:08:16 GMT  
		Size: 16.0 MB (16030117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65b1157d6084a2ea36096688a243ea6d05fc59b44b2331626849535196db689`  
		Last Modified: Fri, 22 Apr 2022 02:08:41 GMT  
		Size: 41.8 MB (41773808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94201e8045a2b75849b87376763eb19cd1ec004669a3d4821923f64259838bf`  
		Last Modified: Fri, 22 Apr 2022 02:08:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c423511f8e89fd1b7706b5cb42ef0ac5fd54fb9315dc19b64ccfce9723e7af85`  
		Last Modified: Fri, 22 Apr 2022 07:43:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2edf8bd0b8acc06e8087c9703a4b580fddc0b6f60620f227f55971ce603b4c`  
		Last Modified: Fri, 22 Apr 2022 07:50:55 GMT  
		Size: 11.2 MB (11243327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0926be208af940fb8b3c28f2c5c575a276256a842880c8f605e71389baf5a`  
		Last Modified: Fri, 22 Apr 2022 07:50:54 GMT  
		Size: 445.1 KB (445147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab895d432bbf73d11b6d61318013199fba816ebaa41fb5beadd54b009af1967d`  
		Last Modified: Fri, 22 Apr 2022 07:50:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:e83c8cc166e610f704dce4feca5a8f727d1e1933582b9ede68690ce61f0d0058
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90100910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d639dd69a86800cea1956ef2e226a9b10f451cda8374518d148ba95d0aa7027c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:03:58 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:04:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:04:57 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 08:07:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Apr 2022 08:07:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 08:07:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Apr 2022 08:07:19 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Apr 2022 08:07:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 08:07:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 08:22:41 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 06 Apr 2022 08:22:42 GMT
ENV TOMCAT_MAJOR=8
# Wed, 06 Apr 2022 08:22:42 GMT
ENV TOMCAT_VERSION=8.5.78
# Wed, 06 Apr 2022 08:22:42 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Wed, 06 Apr 2022 08:22:45 GMT
COPY dir:847e7737bbc210a1b0f5f992b1801f2f8a531873e19add8f86ed059253cac1da in /usr/local/tomcat 
# Wed, 06 Apr 2022 08:22:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 08:22:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Apr 2022 08:22:58 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 08:22:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5571d75f300668becfcd40e9fafe6bbce8567722d68f30aeb98dc329d4823191`  
		Last Modified: Wed, 06 Apr 2022 04:13:25 GMT  
		Size: 39.5 MB (39507446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5ed2119a1c0ba32f14c24749a783945a7e212b84bcdbd71e3c4aacd2065f03`  
		Last Modified: Wed, 06 Apr 2022 04:13:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f047e2338b22ca955025c035543f36bc6301e0d49c0fb991f6b94dbb9ffa5347`  
		Last Modified: Wed, 06 Apr 2022 10:21:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda2228250fdf8c0ef42fb00cae9af6f427a1be28d7b1974be99500dabf59391`  
		Last Modified: Wed, 06 Apr 2022 10:29:20 GMT  
		Size: 11.2 MB (11196068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288fa6e8fd5d660ee40da27b1cbd479ce743a19085191b55a5ed14b3c488cd31`  
		Last Modified: Wed, 06 Apr 2022 10:29:15 GMT  
		Size: 422.6 KB (422597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b895ff9cb638f317db006f5f60a623c33e911f01cf0b8778a7ce8d260640269`  
		Last Modified: Wed, 06 Apr 2022 10:29:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b09bbbabc57e1f1179dce489167574c2d71463dcaae715101bf089d62a36e20a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95304931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff3405c85ece784dd6a6e3a8f43ffa7796c586e5521d73883df3e2294546733`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 22 Apr 2022 00:54:11 GMT
ADD file:6ca4a270cea388f6267a1c7739fd787a34793f48bf8480740a383b5e73299af2 in / 
# Fri, 22 Apr 2022 00:54:11 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:56:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:56:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:56:47 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Fri, 22 Apr 2022 02:57:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:57:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:57:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 22 Apr 2022 05:39:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Apr 2022 05:39:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 05:39:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Apr 2022 05:39:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Apr 2022 05:39:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:39:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:55:35 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 22 Apr 2022 05:55:36 GMT
ENV TOMCAT_MAJOR=8
# Fri, 22 Apr 2022 05:55:37 GMT
ENV TOMCAT_VERSION=8.5.78
# Fri, 22 Apr 2022 05:55:38 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Fri, 22 Apr 2022 05:55:40 GMT
COPY dir:4fc356f4886756f7a85fdfd1429b61b54b96deb682baa735cb02b17016c79aa0 in /usr/local/tomcat 
# Fri, 22 Apr 2022 05:55:46 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 05:55:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Apr 2022 05:55:49 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 05:55:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:61e1864f78be077e322819a4ce1e09da9389c8119cf552629dc048b713a3f42b`  
		Last Modified: Tue, 19 Apr 2022 13:13:57 GMT  
		Size: 27.2 MB (27169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89015ff109b922c48ff7f1847b2e63f33dc54bd022e11f479dbed2eb7fb5da0`  
		Last Modified: Fri, 22 Apr 2022 03:02:05 GMT  
		Size: 15.9 MB (15895876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1241f218f4a9078a7dcbfc6fd6ed6877e46407b06b6221bc6206fab8af4c590b`  
		Last Modified: Fri, 22 Apr 2022 03:02:34 GMT  
		Size: 40.8 MB (40769834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3678ae378db153e8948d4ba589775345c50a90226740a49251dc8d98ee1ee6`  
		Last Modified: Fri, 22 Apr 2022 03:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84180625906a5b274f118064c51574aee1fe77f526e1183d6359365bbcbc3e59`  
		Last Modified: Fri, 22 Apr 2022 08:02:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcd067edc0975ad067f1320bfb311530b610a36906c22f909767704c1e96e9a`  
		Last Modified: Fri, 22 Apr 2022 08:12:09 GMT  
		Size: 11.3 MB (11261438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02a645f28c5d4d8596e77174c6b5dae5fde734e5cf00511963978fd04996127`  
		Last Modified: Fri, 22 Apr 2022 08:12:07 GMT  
		Size: 208.4 KB (208375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:e3f87dd3e0eadcf0389ea42046349cffbca721f5d52fc6525c637d84634b2afe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103413856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495849a5b0526fa5d52b3419388f595235584d3d682262866e08d7c381de9011`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:53:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:55:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:55:16 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Wed, 06 Apr 2022 04:56:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:56:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:56:58 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 06 Apr 2022 09:26:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Apr 2022 09:26:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 09:26:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Apr 2022 09:26:39 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Apr 2022 09:26:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 09:26:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 10:08:46 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 06 Apr 2022 10:08:49 GMT
ENV TOMCAT_MAJOR=8
# Wed, 06 Apr 2022 10:08:51 GMT
ENV TOMCAT_VERSION=8.5.78
# Wed, 06 Apr 2022 10:08:54 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Wed, 06 Apr 2022 10:08:56 GMT
COPY dir:87eee75f73c8228af4914272e67f32d67cc5ab4bd966e25a52d83ac14cca6381 in /usr/local/tomcat 
# Wed, 06 Apr 2022 10:09:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 10:09:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Apr 2022 10:09:44 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 10:09:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51134a7a9e0d0b603ce41f6ef7aa0f9d1a77696cb80e63a1e73b539ff51023b0`  
		Last Modified: Wed, 06 Apr 2022 05:08:30 GMT  
		Size: 17.2 MB (17204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d01fde6e0529762cce89295c75440cad9885812f7a745288f87ae078f446db`  
		Last Modified: Wed, 06 Apr 2022 05:09:04 GMT  
		Size: 41.2 MB (41162303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b67bd659ecdc333c82a200f1da0f4c7ab807ed333272bb5eb662d38420f3564`  
		Last Modified: Wed, 06 Apr 2022 05:08:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef7a91d6220dadd37720542f8bae036a3662b5724075ef429e966855acfad5`  
		Last Modified: Wed, 06 Apr 2022 10:22:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed99ea0442b162dc2555aaab376274b8c065aee2372763b276560624a4d1abf`  
		Last Modified: Wed, 06 Apr 2022 10:29:11 GMT  
		Size: 11.3 MB (11284010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975272ae2cd6b7f8ac86e250b78506bd79cf9870691dd189c4edabdcd8889a0b`  
		Last Modified: Wed, 06 Apr 2022 10:29:10 GMT  
		Size: 471.0 KB (471021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e182ed7cd958af8d18621efa9a57c35d0120ba88cdd75d065e883d4691adc7e`  
		Last Modified: Wed, 06 Apr 2022 10:29:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
