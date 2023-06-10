## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:c8d33671ab9a3deb40ad3543add1a9d6946a0c3fe7467abcc274755b42a17a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:9d409d3484336496bead6b69f267117560176afd3442bc024c0255600a3716be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.0 MB (591018402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c79839e23f278c7d131c2d53f628f9478659ab503f6756ddcca9a7073f3fd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 01:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:42:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Jun 2023 01:43:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:43:39 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Fri, 02 Jun 2023 01:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Jun 2023 01:44:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sun, 04 Jun 2023 16:55:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 04 Jun 2023 16:55:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 16:55:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 04 Jun 2023 16:55:35 GMT
WORKDIR /usr/local/tomcat
# Sun, 04 Jun 2023 16:55:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:55:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 04 Jun 2023 16:57:10 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sun, 04 Jun 2023 16:57:10 GMT
ENV TOMCAT_MAJOR=9
# Sat, 10 Jun 2023 00:37:37 GMT
ENV TOMCAT_VERSION=9.0.76
# Sat, 10 Jun 2023 00:37:38 GMT
ENV TOMCAT_SHA512=028163cbe15367f0ab60e086b0ebc8d774e62d126d82ae9152f863d4680e280b11c9503e3b51ee7089ca9bea1bfa5b535b244a727a3021e5fa72dd7e9569af9a
# Sat, 10 Jun 2023 00:37:38 GMT
COPY dir:f5743ecd98d7370b36812d144a58b18db659a92f2246413d17bb7f46eed37cf7 in /usr/local/tomcat 
# Sat, 10 Jun 2023 00:37:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Jun 2023 00:37:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 10 Jun 2023 00:37:44 GMT
EXPOSE 8080
# Sat, 10 Jun 2023 00:37:44 GMT
CMD ["catalina.sh" "run"]
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Sat, 10 Jun 2023 01:05:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Sat, 10 Jun 2023 01:06:56 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 10 Jun 2023 01:09:19 GMT
ENV XWIKI_VERSION=14.10.12
# Sat, 10 Jun 2023 01:09:19 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.12
# Sat, 10 Jun 2023 01:09:19 GMT
ENV XWIKI_DOWNLOAD_SHA256=45a7eb79eaf7c29094c7cb3fe97cb221f02509b6a8bdb8c382f34cc0d77eeb9c
# Sat, 10 Jun 2023 01:09:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 10 Jun 2023 01:10:57 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Sat, 10 Jun 2023 01:10:57 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Sat, 10 Jun 2023 01:10:57 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Sat, 10 Jun 2023 01:10:57 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Sat, 10 Jun 2023 01:10:57 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Sat, 10 Jun 2023 01:10:58 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Sat, 10 Jun 2023 01:10:58 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 10 Jun 2023 01:10:58 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 10 Jun 2023 01:10:58 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 10 Jun 2023 01:10:59 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 10 Jun 2023 01:10:59 GMT
VOLUME [/usr/local/xwiki]
# Sat, 10 Jun 2023 01:10:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 10 Jun 2023 01:10:59 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d1669123f28121211977ed38e663dca1a397c0c001e5386598b96c89b1b1cd51`  
		Last Modified: Mon, 22 May 2023 20:49:59 GMT  
		Size: 30.4 MB (30430275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7723b4ddeaefdff460e5e80fa453e1cc3a321b38d941490f9670da9ac646375b`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 12.5 MB (12493726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e8f29e341c2149d867915e16854b80377147f6a9051f61d5d926ccb70dbe17`  
		Last Modified: Fri, 02 Jun 2023 01:47:46 GMT  
		Size: 46.7 MB (46666187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e47f3a63c4e338b2efb84d399d9807797b5705ffb8ca8ce9c8214cff3e137`  
		Last Modified: Fri, 02 Jun 2023 01:47:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be4cbf958f0b2c2d0a7a700e3e5fc426dc018b5921f4dce4c3c2e05eb63c3d2`  
		Last Modified: Sun, 04 Jun 2023 17:04:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b91cbe0927f4b2ceb2b992bbdf934995afaa25ee50112bf7fae16106f4e8497`  
		Last Modified: Sat, 10 Jun 2023 00:45:50 GMT  
		Size: 12.3 MB (12269587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f620e68e7ae8dd7fa78c72bd2ac1ead80035fb84612fb65d520412aa49f51f5d`  
		Last Modified: Sat, 10 Jun 2023 00:45:50 GMT  
		Size: 3.0 MB (2966238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376fe98716bdf23a75dc54def95710cce46769b72f2f884575b6ce41b36f5d4`  
		Last Modified: Sat, 10 Jun 2023 00:45:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa37bcb786538d937cc96b88ac0bcf25b6fec71e052c5ab8f1006039ff2fac2`  
		Last Modified: Sat, 10 Jun 2023 01:11:46 GMT  
		Size: 178.3 MB (178333271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d0a11584db57f0257f8d90ccff4e5e6c3f880db5cd1f6449d9cbce9e0dde2`  
		Last Modified: Sat, 10 Jun 2023 01:13:35 GMT  
		Size: 307.3 MB (307251929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b286f7963448a112fd43a3c58b9c3f790687f018e06292ee00c63664b32742`  
		Last Modified: Sat, 10 Jun 2023 01:14:32 GMT  
		Size: 594.6 KB (594551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351607c95e7b5e0c26cde40728f48fd86bcec948963ebc7b9e8d5df64a2d3b53`  
		Last Modified: Sat, 10 Jun 2023 01:14:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469f3b85f6675d62d3a31a57e27817750124a3b7109b9a1b0d5b250982cdcae2`  
		Last Modified: Sat, 10 Jun 2023 01:14:32 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf94450b2dddda8fb5aef5339f39d2343b2066687329d65bd39990fd0fddf57`  
		Last Modified: Sat, 10 Jun 2023 01:14:33 GMT  
		Size: 6.0 KB (6016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed74d9433570e4b83e3530914efb2685c049e97f936b69eb07881e4e432fd15f`  
		Last Modified: Sat, 10 Jun 2023 01:14:32 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:742994fc2f4bdf73a930e6e51dc680737666751ca87ecd9794f736167ea5a047
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.1 MB (582108633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfde37b961ac711f2930f3656f739017e7c5748caa825088d9a59d9fbb7e03f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:18:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jun 2023 23:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jun 2023 23:18:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 01 Jun 2023 23:18:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:19:07 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 01 Jun 2023 23:19:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1fe4b20d808f393422610818711c728331992a4455eeeb061d3d05b45412771d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.19_7.tar.gz';          ;;        armhf|arm)          ESUM='cb754b055177381f9f6852b7e5469904a15edddd7f8e136043c28b1e33aee47c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.19_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8019d938e5525938ec8e68e2989c4413263b0d9b7b3f20fe0c45f6d967919cfb';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.19_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='058419435fe6212d1bc305a14f578c314f9ff9a2d96d523c178120e84231c733';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.19_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='32dcf760664f93531594b72ce9226e9216567de5705a23c9ff5a77c797948054';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.19%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.19_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 01 Jun 2023 23:19:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Jun 2023 01:57:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Jun 2023 01:57:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:57:48 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Jun 2023 01:57:48 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Jun 2023 01:57:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:57:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Jun 2023 01:59:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_VERSION=9.0.75
# Fri, 02 Jun 2023 01:59:05 GMT
ENV TOMCAT_SHA512=e29905e693598b64d958dd22b8d866590163917bdc6e1cfd363a8a06f97ecc89284b863b3ab2448f43903623564c3fd952c7a9bd33df8476d57f6873c2d463c7
# Fri, 02 Jun 2023 01:59:05 GMT
COPY dir:6772160db6f147cd31589cbb67d4cc64fba9465bcc14e4e3f07be9451759501e in /usr/local/tomcat 
# Fri, 02 Jun 2023 01:59:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:59:10 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jun 2023 01:59:10 GMT
EXPOSE 8080
# Fri, 02 Jun 2023 01:59:10 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 02 Jun 2023 03:24:00 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 02 Jun 2023 03:25:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Thu, 08 Jun 2023 17:48:08 GMT
ENV XWIKI_VERSION=14.10.12
# Thu, 08 Jun 2023 17:48:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.12
# Thu, 08 Jun 2023 17:48:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=45a7eb79eaf7c29094c7cb3fe97cb221f02509b6a8bdb8c382f34cc0d77eeb9c
# Thu, 08 Jun 2023 17:48:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 08 Jun 2023 17:49:44 GMT
ENV MARIADB_JDBC_VERSION=3.1.4
# Thu, 08 Jun 2023 17:49:44 GMT
ENV MARIADB_JDBC_SHA256=eb88b5d727d82e25117e2b6fabcec1daf734633b0a576456c73215884c189ad4
# Thu, 08 Jun 2023 17:49:44 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.1.4
# Thu, 08 Jun 2023 17:49:44 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.1.4.jar
# Thu, 08 Jun 2023 17:49:44 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.1.4.jar
# Thu, 08 Jun 2023 17:49:45 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Thu, 08 Jun 2023 17:49:45 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 08 Jun 2023 17:49:45 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 08 Jun 2023 17:49:46 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 08 Jun 2023 17:49:46 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 08 Jun 2023 17:49:46 GMT
VOLUME [/usr/local/xwiki]
# Thu, 08 Jun 2023 17:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jun 2023 17:49:46 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90f9c81eab3c275d75f3cf9f4840e195cfa7c5372d500bfeb5a040f3fc88262`  
		Last Modified: Thu, 01 Jun 2023 23:21:25 GMT  
		Size: 12.5 MB (12452855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fcc328ac0affca0471a6a1d24001fbf5d6927268b63108576c160df5647af7`  
		Last Modified: Thu, 01 Jun 2023 23:22:22 GMT  
		Size: 45.0 MB (45009479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5c29166d38f94500a3660aa3baef35070a8822a01cc0d45dd1ca1e9ace769`  
		Last Modified: Thu, 01 Jun 2023 23:22:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37df8cc9a991ed50f676003a7c9f6ebeeaa4b5b28a42b6126522c569938d544`  
		Last Modified: Fri, 02 Jun 2023 02:06:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e19b4e105eebc0ba47bb90c9ef63b8c9b604e0cee4eab1fb482a68b3664586`  
		Last Modified: Fri, 02 Jun 2023 02:07:50 GMT  
		Size: 12.2 MB (12242189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4850a1ed957a95b8a94a2957ccd1b4ed1227f7c8997a70eed6f9ff693b648e8e`  
		Last Modified: Fri, 02 Jun 2023 02:07:50 GMT  
		Size: 2.8 MB (2806582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c42a0a43520047ad78ac489284036db953e98cca2d1d4bd31b523bd0c6ba28`  
		Last Modified: Fri, 02 Jun 2023 02:07:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616eeb0d98e442348091228bd6eca84c2670b963a7ea7bd083875cb0d3a97862`  
		Last Modified: Fri, 02 Jun 2023 03:30:20 GMT  
		Size: 173.3 MB (173349470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a9d235961e06b85a663da4fd4b1ffb33d6241048c6bc8f5e0f2257a845adc`  
		Last Modified: Thu, 08 Jun 2023 17:50:27 GMT  
		Size: 307.3 MB (307251831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a387c34a2197a930fea6927746b161550aac6d1b2eaa7eeb9ca1b8f12df65f58`  
		Last Modified: Thu, 08 Jun 2023 17:51:26 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937fdb2f5eec9db9f8b2dd46222ac35054697c25a44c3a6a5b51957502da8090`  
		Last Modified: Thu, 08 Jun 2023 17:51:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe11a0d7154ff89ef3b72222fae6ee0d779c38c81fa3cba53b6f6ca9ee908ef3`  
		Last Modified: Thu, 08 Jun 2023 17:51:26 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bed3fcddf5bc845114eb6b30a63980acc58745d5116797d99fd3939a5dbd4a2`  
		Last Modified: Thu, 08 Jun 2023 17:51:26 GMT  
		Size: 6.0 KB (6014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa62be6c37d013ef98966c26cafd4fb2d973a0dfad9fe10fcdf8c8c52c11957`  
		Last Modified: Thu, 08 Jun 2023 17:51:26 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
