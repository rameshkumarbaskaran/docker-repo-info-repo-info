## `tomcat:8-jre17-temurin-focal`

```console
$ docker pull tomcat@sha256:da0f44e5a1df32cdd6220a5b442409f2233760304ef1daa6941a95724dd9100d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:8-jre17-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:23dbe27226de07532f059273de47be304944f9745db4de71a0780a27dd47b80f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108771748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c482fec52e50fd0d7501b6db4901d548029f4519b8a8120f3fc36bc2de9c5b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:12:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:15:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:22:08 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:23:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d0fc84cb9627641d5a3c85aef9e7e26e4874e37524f9425112c6def5b12b7892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='6a559ec6186ae74c362115cab36057db40e0c6e9e50763f5b485240109a226ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a5d055cbdb1f8ef537afc66a6315e865646305420cb96ab08dc239074f88ad1d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a9f3193721ddea74e7a8aa8fe870bcef85cca6c5870835e8517bc61251f50a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='616b137b87fa84211ac2f5c23dfcf3a8c5df9d0fd7ea3c872a0bf394b2f6c464';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:23:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:23:01 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 19:09:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Jul 2022 19:09:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 19:09:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 28 Jul 2022 19:09:26 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Jul 2022 19:09:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 19:09:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 19:18:25 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 28 Jul 2022 19:18:25 GMT
ENV TOMCAT_MAJOR=8
# Thu, 28 Jul 2022 19:18:25 GMT
ENV TOMCAT_VERSION=8.5.81
# Thu, 28 Jul 2022 19:18:25 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Thu, 28 Jul 2022 19:18:25 GMT
COPY dir:d976053dfcce48a4698ff3f48f6d456c3f1c43b2a2093e255fb3e7a053fef70b in /usr/local/tomcat 
# Thu, 28 Jul 2022 19:18:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 19:18:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 28 Jul 2022 19:18:32 GMT
EXPOSE 8080
# Thu, 28 Jul 2022 19:18:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32598539a8f0b55be77078c6637866fc4128a4213ea59e9993662a310a2b711`  
		Last Modified: Tue, 07 Jun 2022 00:22:05 GMT  
		Size: 19.8 MB (19773881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33dae87d926696962d1edf6648739950f08788ba84ed28f8059c3359a861970e`  
		Last Modified: Thu, 28 Jul 2022 16:30:24 GMT  
		Size: 46.8 MB (46809114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f383e70a4ca356e88017e4add1069623cfc3ae0bf3373faf01a8d33b89344050`  
		Last Modified: Thu, 28 Jul 2022 16:30:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17307cd6ea79008e473e6b3bacc218a316f5bf9abb5dd22a9a8a221ce13705e3`  
		Last Modified: Thu, 28 Jul 2022 19:32:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05b0dc9281d620aed41fa8f341396481139bc543dc2f08af1b32f16bd80a503`  
		Last Modified: Thu, 28 Jul 2022 19:41:07 GMT  
		Size: 11.3 MB (11260498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9f63e5d98d2ee8630e8b713693b6a9f78f9ddf7cf88d3028132a6a0e0b9e43`  
		Last Modified: Thu, 28 Jul 2022 19:41:06 GMT  
		Size: 2.4 MB (2355160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab92a5de36cb18f9b231208454aabeccaa734838da895fe12ba1cd62e43263`  
		Last Modified: Thu, 28 Jul 2022 19:41:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:2f319faa4c45920112d21cdd29d75132d600657abb8fdb18e9bbdba34d73ee4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99756229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96df89913af90ebb41c19d0bdea1274aa32098825b8b32a09949a33ffaae7a14`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Sat, 30 Jul 2022 02:49:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Jul 2022 02:52:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 02:52:16 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Sat, 30 Jul 2022 02:53:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d0fc84cb9627641d5a3c85aef9e7e26e4874e37524f9425112c6def5b12b7892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='6a559ec6186ae74c362115cab36057db40e0c6e9e50763f5b485240109a226ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a5d055cbdb1f8ef537afc66a6315e865646305420cb96ab08dc239074f88ad1d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a9f3193721ddea74e7a8aa8fe870bcef85cca6c5870835e8517bc61251f50a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='616b137b87fa84211ac2f5c23dfcf3a8c5df9d0fd7ea3c872a0bf394b2f6c464';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jul 2022 02:53:23 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 02:53:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Sat, 30 Jul 2022 12:56:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Jul 2022 12:56:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 12:56:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Jul 2022 12:56:16 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Jul 2022 12:56:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 12:56:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 13:10:00 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 30 Jul 2022 13:10:00 GMT
ENV TOMCAT_MAJOR=8
# Sat, 30 Jul 2022 13:10:00 GMT
ENV TOMCAT_VERSION=8.5.81
# Sat, 30 Jul 2022 13:10:00 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Sat, 30 Jul 2022 13:10:01 GMT
COPY dir:28f320c93ddb65a40ce5606069fcfb435b106afd1508b6c8950fb677d2332577 in /usr/local/tomcat 
# Sat, 30 Jul 2022 13:10:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 13:10:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Jul 2022 13:10:09 GMT
EXPOSE 8080
# Sat, 30 Jul 2022 13:10:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916985a90d5d9c5f2a2e834acb83d3a31a527d90f6140d699201612fc01376a1`  
		Last Modified: Sat, 30 Jul 2022 02:59:50 GMT  
		Size: 19.2 MB (19191327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c2c4eaab643cfdee4f7f4029ecc1a660dcede822d686345ad7001969c0b305`  
		Last Modified: Sat, 30 Jul 2022 03:01:00 GMT  
		Size: 44.3 MB (44333367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91fb120e6e686154c3a69b29debbff122d7c38bad45be5fa618d94901c334d0`  
		Last Modified: Sat, 30 Jul 2022 03:00:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a222a7b0d9c6920d34127132f1d0e30bcdca0a000e0920adb741cb6fb5345e9`  
		Last Modified: Sat, 30 Jul 2022 13:30:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d508ab4ee0b71cc9c1e52f78a436b795a864b2de78c3253a8c1979d30cfb05e6`  
		Last Modified: Sat, 30 Jul 2022 13:42:16 GMT  
		Size: 11.2 MB (11213680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a358dfdd72a848329a3fccc2f305983d96bed22ff3b94aceaa8c8080168d8d`  
		Last Modified: Sat, 30 Jul 2022 13:42:15 GMT  
		Size: 424.7 KB (424749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64342230a190dd922c3569f5c25e4c369673f42c22b3c21a090f9a463c66318a`  
		Last Modified: Sat, 30 Jul 2022 13:42:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:646c941bc0a69fdd663639d3d5abf23244360c2d60796a4042c6087d39277ac8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105421019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f04f782fa688622af2e7d00ddc649eb183ad7127c61536b8b190f1c0970fcb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:50:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 17:54:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:54:11 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Tue, 02 Aug 2022 17:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d0fc84cb9627641d5a3c85aef9e7e26e4874e37524f9425112c6def5b12b7892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='6a559ec6186ae74c362115cab36057db40e0c6e9e50763f5b485240109a226ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a5d055cbdb1f8ef537afc66a6315e865646305420cb96ab08dc239074f88ad1d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a9f3193721ddea74e7a8aa8fe870bcef85cca6c5870835e8517bc61251f50a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='616b137b87fa84211ac2f5c23dfcf3a8c5df9d0fd7ea3c872a0bf394b2f6c464';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:55:19 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 03 Aug 2022 01:48:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:48:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:48:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:48:44 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:48:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:48:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:23:41 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 03 Aug 2022 02:23:41 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Aug 2022 02:23:42 GMT
ENV TOMCAT_VERSION=8.5.81
# Wed, 03 Aug 2022 02:23:43 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Wed, 03 Aug 2022 02:23:45 GMT
COPY dir:2a5692616dbfb19566a52b6077265bc543fcbbb1de36ad9de49be6bff8b0c383 in /usr/local/tomcat 
# Wed, 03 Aug 2022 02:23:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:23:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 02:23:56 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 02:23:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4b399269fa184aac3bbe66763d5b373c71d601c49266b8828e09b7fdd6789`  
		Last Modified: Tue, 02 Aug 2022 18:03:22 GMT  
		Size: 20.5 MB (20491864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca8d9252b438fb30affacbb9e7dfc3e8490002df425aa9726800d58476bffe9`  
		Last Modified: Tue, 02 Aug 2022 18:04:35 GMT  
		Size: 46.2 MB (46245603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0c4248876abb632b6eeb8e6f30ad92933c4cfaf445a88a9bb8215a922f00dc`  
		Last Modified: Tue, 02 Aug 2022 18:04:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49630b34e711b6d8e1bb201bb663ca547930bffbc3fe094224e7b7fa493837b7`  
		Last Modified: Wed, 03 Aug 2022 02:58:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa7fbb7601daca7b9f2291a1257079058a4c50c4cb0f0f2c726064d7d3823c6`  
		Last Modified: Wed, 03 Aug 2022 03:23:47 GMT  
		Size: 11.3 MB (11279436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1d61bde7f0a1b074326b5dad9896bd1087b4befbd2e29a9c67ef012d22925f`  
		Last Modified: Wed, 03 Aug 2022 03:23:45 GMT  
		Size: 212.0 KB (212047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:9313be1a62c41ec99b8204d756563692a571a81ff1e82afafa98f0f1ca62ac5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113386375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f80b0f9e1f745567c84d5838ea688033337bf0db9fffe6cc0aefc7b11da5b1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:02 GMT
ADD file:86506a94b834ba2b6f10dc0d1955bee539be1cf565e4ccc2c4bc074e0375f115 in / 
# Tue, 07 Jun 2022 05:46:06 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 00:33:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:41:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 16:19:37 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 28 Jul 2022 16:21:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d0fc84cb9627641d5a3c85aef9e7e26e4874e37524f9425112c6def5b12b7892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='6a559ec6186ae74c362115cab36057db40e0c6e9e50763f5b485240109a226ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a5d055cbdb1f8ef537afc66a6315e865646305420cb96ab08dc239074f88ad1d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a9f3193721ddea74e7a8aa8fe870bcef85cca6c5870835e8517bc61251f50a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='616b137b87fa84211ac2f5c23dfcf3a8c5df9d0fd7ea3c872a0bf394b2f6c464';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 28 Jul 2022 16:21:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 16:21:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Thu, 28 Jul 2022 17:26:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Jul 2022 17:26:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Jul 2022 17:26:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 28 Jul 2022 17:26:14 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Jul 2022 17:26:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:26:15 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Jul 2022 17:39:20 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 28 Jul 2022 17:39:21 GMT
ENV TOMCAT_MAJOR=8
# Thu, 28 Jul 2022 17:39:21 GMT
ENV TOMCAT_VERSION=8.5.81
# Thu, 28 Jul 2022 17:39:21 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Thu, 28 Jul 2022 17:39:22 GMT
COPY dir:de6628d4ea77eb57ac6631eb2b96dac2ceedc412279a5db135add987cda65b19 in /usr/local/tomcat 
# Thu, 28 Jul 2022 17:39:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 28 Jul 2022 17:39:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 28 Jul 2022 17:39:32 GMT
EXPOSE 8080
# Thu, 28 Jul 2022 17:39:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3f52d061d2d3fdde0d3a099bbeae64080476c9650e9f3ba05de898d5bb5f03e8`  
		Last Modified: Tue, 07 Jun 2022 05:49:10 GMT  
		Size: 33.3 MB (33294345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff6ca525e26e65e4f33725ff2f731fb66f9fa21452fe1cff1f1d65d9860921`  
		Last Modified: Wed, 27 Jul 2022 00:55:32 GMT  
		Size: 21.7 MB (21686416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae9e6235c682933e61f641392a3d8726a09893869af9c0dcd597a14a24ef949`  
		Last Modified: Thu, 28 Jul 2022 16:30:24 GMT  
		Size: 46.6 MB (46628635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f46e9fc6ec150dd218b5ba02d3367929ce66570793d254a0f1372177990c61`  
		Last Modified: Thu, 28 Jul 2022 16:30:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34607299a652066242678a7bf9ff55cb7eb7941a2ed7c1a630548ef970b917f3`  
		Last Modified: Thu, 28 Jul 2022 17:57:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ec604fbebd7671066fc8e0900ae117046d22367f785fef413fb54b50ac029`  
		Last Modified: Thu, 28 Jul 2022 18:07:30 GMT  
		Size: 11.3 MB (11302549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793fcbcc2254f6b8223c68be1332a959835803c6a269701f7b476fbebaf7bf34`  
		Last Modified: Thu, 28 Jul 2022 18:07:29 GMT  
		Size: 474.0 KB (473966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c802c4974225127e799b6c04c4009334ad4dbb176aa905e4f16e1c2694fe4a2a`  
		Last Modified: Thu, 28 Jul 2022 18:07:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre17-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:a4936c058e4c2a54170f3eb5d55b1133ca24c505063ec18ce83b7fa5dc27e89d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101687594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e112edfa2f4923279fe9c54941a45343ae57c9b393393fa5b201c7384322554a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:41:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 12:49:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:04:47 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Tue, 02 Aug 2022 13:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d0fc84cb9627641d5a3c85aef9e7e26e4874e37524f9425112c6def5b12b7892';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='6a559ec6186ae74c362115cab36057db40e0c6e9e50763f5b485240109a226ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a5d055cbdb1f8ef537afc66a6315e865646305420cb96ab08dc239074f88ad1d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='79a9f3193721ddea74e7a8aa8fe870bcef85cca6c5870835e8517bc61251f50a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='616b137b87fa84211ac2f5c23dfcf3a8c5df9d0fd7ea3c872a0bf394b2f6c464';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jre_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 13:06:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 13:06:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 03 Aug 2022 01:49:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:49:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:49:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:49:59 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:49:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:49:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:56:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 03 Aug 2022 01:56:14 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Aug 2022 01:56:14 GMT
ENV TOMCAT_VERSION=8.5.81
# Wed, 03 Aug 2022 01:56:14 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Wed, 03 Aug 2022 01:56:15 GMT
COPY dir:3180284b65a315a4411a84973acaa69d192cd40554d5d7931dbfc5c4f3eba009 in /usr/local/tomcat 
# Wed, 03 Aug 2022 01:56:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 01:56:19 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 01:56:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 01:56:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b48d17296789cbed49100fd665aec2330de5c27d57190835247afb1fa0799b`  
		Last Modified: Tue, 02 Aug 2022 12:54:34 GMT  
		Size: 19.2 MB (19224154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab655fe85e08c6c9bcfa9aeadd6c54613abd08101dee9380adee17e050c11231`  
		Last Modified: Tue, 02 Aug 2022 13:11:00 GMT  
		Size: 43.7 MB (43692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb37e9e27abd33e13adf8fd7fe4448d96ebd3aaa277815985adb218997b823`  
		Last Modified: Tue, 02 Aug 2022 13:10:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d7ad8f0f7e1766ec99130b160c0a590a1bf6cfec10ce7e7924ec0b1f2a8c3b`  
		Last Modified: Wed, 03 Aug 2022 02:07:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d195d918d501ff0ecdf12632ed1beab0d2d38bf4ea89d07f61d3a40ea84efd42`  
		Last Modified: Wed, 03 Aug 2022 02:12:00 GMT  
		Size: 11.3 MB (11274474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87d4fca596ee07178b76d6c9e2dab49fc3d75f7e58cc55c4b8298929b224eb`  
		Last Modified: Wed, 03 Aug 2022 02:12:00 GMT  
		Size: 450.5 KB (450529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd4df5faea29b1e1629f75a71ca3ec1ba7634572984c57a2a464531a73b3e46`  
		Last Modified: Wed, 03 Aug 2022 02:12:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
