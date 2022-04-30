## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:5d6adcb064a9aa1dc9e447f643a0cd0fafecbb3527508e496ebce5f2657d060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:0c8fb3060604ec35a264994d6c2ee105757d3f81545ffd56a0f6b990f4a43d50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98059173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830cd8fd2525f5e769550411903a92f56df3c17af3e6792fde7b083f28718f83`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 29 Apr 2022 23:20:59 GMT
ADD file:7009ad0ee0bbe5ed7f381792e07347e260e6896aeee0d80597808065120fa96b in / 
# Fri, 29 Apr 2022 23:20:59 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:22:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:22:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:22:48 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 30 Apr 2022 00:23:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:23:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:23:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 30 Apr 2022 04:22:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Apr 2022 04:22:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 04:22:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Apr 2022 04:22:18 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Apr 2022 04:22:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 04:22:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 04:28:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 30 Apr 2022 04:28:53 GMT
ENV TOMCAT_MAJOR=8
# Sat, 30 Apr 2022 04:28:53 GMT
ENV TOMCAT_VERSION=8.5.78
# Sat, 30 Apr 2022 04:28:53 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Sat, 30 Apr 2022 04:28:53 GMT
COPY dir:1a89c25bff62e0eefa08b9eb1af640fd6ee93e3f4751eeedf47c0e3ef0f2d9ab in /usr/local/tomcat 
# Sat, 30 Apr 2022 04:28:58 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 04:28:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Apr 2022 04:28:59 GMT
EXPOSE 8080
# Sat, 30 Apr 2022 04:28:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d5fd17ec1767521cf97f61568096bfc9a7cd9c2d149576a7b43930c5a97062b0`  
		Last Modified: Thu, 28 Apr 2022 03:03:21 GMT  
		Size: 28.6 MB (28566230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e94d254f3c4d0b302d167dc31edd456d3f663ed337bc99fdd2fd0a21025340e`  
		Last Modified: Sat, 30 Apr 2022 00:26:11 GMT  
		Size: 16.0 MB (16030310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289804aac4b02bd751f57fbc5734a5ce46b1d944b336e1f2c4c001aca34befc1`  
		Last Modified: Sat, 30 Apr 2022 00:26:40 GMT  
		Size: 41.8 MB (41773817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ada27813977835bbe02975c6d7cdfee1509abf917af290f57e001801f661e19`  
		Last Modified: Sat, 30 Apr 2022 00:26:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7113c509e0a5798873e2b4ddfb3a7aa1025b8a07acc472eb76eea22d185f063`  
		Last Modified: Sat, 30 Apr 2022 04:42:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b324ede776597a66847cc9252a825cf89aae8e9a467db839dd2ab8b4e3b6094e`  
		Last Modified: Sat, 30 Apr 2022 04:48:11 GMT  
		Size: 11.2 MB (11243184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e729bed825690efccff9b4db94d7eeaff0008aeb5ba98550b99b9b09c22ab00`  
		Last Modified: Sat, 30 Apr 2022 04:48:11 GMT  
		Size: 445.2 KB (445172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4ba0f9c8b142d05c97634826af37c910aa2a85bfbb3611a667f0d2c27c5b38`  
		Last Modified: Sat, 30 Apr 2022 04:48:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:810eff4d61651077fe469f1adb05faed7b00e8775ba5397b7ed6ebccb954c143
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90103554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0768fdbd6e8348d5ebdcadc13425bf5c18a23e55e36391f176076b4a84d27b59`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:46 GMT
ADD file:5f12bea85a1ebe365907ca3979b0e31e6043dccfcb9a3cdf62be46e054494147 in / 
# Fri, 29 Apr 2022 22:58:47 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:56:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:56:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:56:46 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Fri, 29 Apr 2022 23:57:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:57:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:57:47 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 30 Apr 2022 03:15:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Apr 2022 03:15:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 03:15:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Apr 2022 03:15:04 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Apr 2022 03:15:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 03:15:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 03:28:10 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 30 Apr 2022 03:28:10 GMT
ENV TOMCAT_MAJOR=8
# Sat, 30 Apr 2022 03:28:10 GMT
ENV TOMCAT_VERSION=8.5.78
# Sat, 30 Apr 2022 03:28:11 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Sat, 30 Apr 2022 03:28:13 GMT
COPY dir:68714d711bfa56c9c26ec903ac695cfb8f01c535c717085b1cc1f00a26e8abc6 in /usr/local/tomcat 
# Sat, 30 Apr 2022 03:28:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 03:28:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Apr 2022 03:28:27 GMT
EXPOSE 8080
# Sat, 30 Apr 2022 03:28:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b20724a4297c7ca8b89f31d6ad53e7ead0c17c7908a4592871cdc97332193580`  
		Last Modified: Fri, 29 Apr 2022 23:03:00 GMT  
		Size: 24.1 MB (24073650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142d50dc2d1479b31402efb7588259cffeca2de60159fa16b540aa20dcf0cd3f`  
		Last Modified: Sat, 30 Apr 2022 00:04:04 GMT  
		Size: 14.9 MB (14901951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46e0c8dbb748dda220c94b17e28193da15491531c5c3dbf5f3e082b89a3433d`  
		Last Modified: Sat, 30 Apr 2022 00:05:14 GMT  
		Size: 39.5 MB (39508155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25393cba66b3d8a7eb0372cc2c279d197232cc1d45a50f07a83b740d66b7da9`  
		Last Modified: Sat, 30 Apr 2022 00:04:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747f31ff454862a60a52cd1a88448743059c96a5c964679f833fe0b42f45adb0`  
		Last Modified: Sat, 30 Apr 2022 03:45:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6866855952946b269390459839627d0efaabef86d69fad43572d68ba3acef734`  
		Last Modified: Sat, 30 Apr 2022 03:52:42 GMT  
		Size: 11.2 MB (11195965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d755d2fe618e700918c2cbf3343c6c326efb79697c6af2f7bdbccad1e1152c`  
		Last Modified: Sat, 30 Apr 2022 03:52:38 GMT  
		Size: 423.4 KB (423370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7115798c4f799b2027389ce55a698f01e8edf10a94d729790a2302a2b67ea55`  
		Last Modified: Sat, 30 Apr 2022 03:52:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b5f3d9d991a3eb852e670d93ee4e1748f943e179dba32b9e63d6be4a58f8a625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95306591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de68542934cad1c8c0faf07e13eea009af5594ddab9c81203ad1e0565457698f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:34 GMT
ADD file:ccdde790bb849fe101367f2b541f1062b3544d21f99a5acc535bf2b0884cc0eb in / 
# Fri, 29 Apr 2022 22:49:35 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:28:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 29 Apr 2022 23:28:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:28:53 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Fri, 29 Apr 2022 23:29:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 29 Apr 2022 23:29:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Apr 2022 23:29:20 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 30 Apr 2022 02:35:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Apr 2022 02:35:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 02:35:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Apr 2022 02:35:36 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Apr 2022 02:35:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 02:35:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 02:47:35 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 30 Apr 2022 02:47:35 GMT
ENV TOMCAT_MAJOR=8
# Sat, 30 Apr 2022 02:47:36 GMT
ENV TOMCAT_VERSION=8.5.78
# Sat, 30 Apr 2022 02:47:37 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Sat, 30 Apr 2022 02:47:39 GMT
COPY dir:1c766efb235e0b4181a1942d4c127d9dbfbc041c830097368449b2ed01d0722f in /usr/local/tomcat 
# Sat, 30 Apr 2022 02:47:45 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 02:47:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Apr 2022 02:47:48 GMT
EXPOSE 8080
# Sat, 30 Apr 2022 02:47:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d4ba87bb7858f0dd4a60003f011338f3a58b87d0add985652856007fe5ca5034`  
		Last Modified: Fri, 29 Apr 2022 22:51:32 GMT  
		Size: 27.2 MB (27169388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce33c7cb386794b97371bf23d6db512379e04036ae033b076a599f51f6416b6`  
		Last Modified: Fri, 29 Apr 2022 23:33:40 GMT  
		Size: 15.9 MB (15897301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73184a625fc89093837db22b6f5c26417cfcc4d7be02627a074b6ffab3db08b`  
		Last Modified: Fri, 29 Apr 2022 23:34:09 GMT  
		Size: 40.8 MB (40769839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7f5c35d2588ff5dd091c320ad1922046c42f2433c4032d975ad2e4a30c2755`  
		Last Modified: Fri, 29 Apr 2022 23:34:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab031cb18a4aa77bceb31175d7ae103a7eb85010d7dc8796fdc5d4e4490eb97`  
		Last Modified: Sat, 30 Apr 2022 03:12:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf480ef2b8d0bcb26518d8c0657868c02e01b1490ac2422ec7879479fd719c`  
		Last Modified: Sat, 30 Apr 2022 03:20:45 GMT  
		Size: 11.3 MB (11261542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732463f9f8d201df561bc0dda565c75aec663633ca230634533f26189843af58`  
		Last Modified: Sat, 30 Apr 2022 03:20:44 GMT  
		Size: 208.3 KB (208256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:e6d97954dab70fe2c73cd9000269e135d3de05bb8747ec19fd2e636b2559d201
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103412862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f426b818adcee168a8f170c13a61746456761d41de17fd9726177ac2b4d08`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 29 Apr 2022 23:22:28 GMT
ADD file:55691ac7d76af0fcfafc39ebd1e5a4f2d7018147d6db6f89812db33fbaffc2f9 in / 
# Fri, 29 Apr 2022 23:22:33 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:29:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Apr 2022 00:32:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:32:20 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Sat, 30 Apr 2022 00:33:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='22496d5e677aaccc5a85e90584d0a012c51a08898f0e09e259eabe67ed81da2b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u322b06.tar.gz';          ;;        armhf|arm)          ESUM='48181f17b85a13c0e2f260c8f4b39483e61664cf07ea00e6210a666fb5210492';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_arm_linux_hotspot_8u322b06.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='f15b536a97c27d114c0b59c86de07ca80a271d3979ed0aa056318ea329e31e5d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u322b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='9c4607cee01919a21c57a36e8c009a7aca7aefd63010c64d7a3023fe8590ebe1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Apr 2022 00:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 00:33:29 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 30 Apr 2022 03:51:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Apr 2022 03:51:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Apr 2022 03:52:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Apr 2022 03:52:02 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Apr 2022 03:52:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 03:52:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Apr 2022 04:18:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 30 Apr 2022 04:18:50 GMT
ENV TOMCAT_MAJOR=8
# Sat, 30 Apr 2022 04:18:52 GMT
ENV TOMCAT_VERSION=8.5.78
# Sat, 30 Apr 2022 04:18:55 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Sat, 30 Apr 2022 04:18:56 GMT
COPY dir:35e544878639fe591410251ec4a571879f894808758bff46b2e36e4fa9108464 in /usr/local/tomcat 
# Sat, 30 Apr 2022 04:19:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 04:19:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Apr 2022 04:19:25 GMT
EXPOSE 8080
# Sat, 30 Apr 2022 04:19:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e9c0a77cb9f0f7330e3fc62254e4c8ae89ed4bba21209fdc1088195250f950b9`  
		Last Modified: Fri, 29 Apr 2022 23:25:23 GMT  
		Size: 33.3 MB (33290661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a436aa11f9f1d03225e672ec1f60e82ddcff2d3b267d9904213f0f01ed5eeba5`  
		Last Modified: Sat, 30 Apr 2022 00:45:44 GMT  
		Size: 17.2 MB (17204116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d79cdfa11534f227af93a5add0a8f95910734701bd0ba373826b02d14fe32`  
		Last Modified: Sat, 30 Apr 2022 00:46:18 GMT  
		Size: 41.2 MB (41162301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5402cc8ea35997962a9c1be409af89e41e1aafbfb829c74cc367bd15700d0a`  
		Last Modified: Sat, 30 Apr 2022 00:46:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80e1113a6efc52e660377e7994956b66bcc0407fee16d6e450bda2656e8d035`  
		Last Modified: Sat, 30 Apr 2022 04:32:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a83607c9d448938050cc737893acf49181d930b538deb45ef508df801e8b624`  
		Last Modified: Sat, 30 Apr 2022 04:39:19 GMT  
		Size: 11.3 MB (11284065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91369d87a549fcf1e0c287fe89f534c9dfc554a9828baae4c4a712ee51a19042`  
		Last Modified: Sat, 30 Apr 2022 04:39:18 GMT  
		Size: 471.3 KB (471257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ff61e07888b028028843d9dc2f6e0d0bcf61c85a5e349c57d1282832e0f42a`  
		Last Modified: Sat, 30 Apr 2022 04:39:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
