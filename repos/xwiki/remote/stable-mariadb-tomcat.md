## `xwiki:stable-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:f6b98e6e775097757810c29d5a388d8100c4adf51e69d5fd513a2115fc6b9244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f98365d8b5c11b8b939dba9e22b8042742c01d0559d5f0a78684f074a130fe04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581271955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e78699e845c6c4b21eb863e4b7c6013f5e1baaf05a0b66cbd77f47b012821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Fri, 02 Sep 2022 05:22:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:23:32 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 05:24:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 05:24:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 10:35:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 10:35:58 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 10:35:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 10:35:59 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 10:35:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:35:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 10:43:14 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 10:43:14 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Sep 2022 10:43:14 GMT
ENV TOMCAT_VERSION=9.0.65
# Fri, 02 Sep 2022 10:43:14 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Fri, 02 Sep 2022 10:43:14 GMT
COPY dir:5b8e3bd6b1bb211fe27b422f100cba55faf61405b1e89ba08b5dfa0acdbfc74f in /usr/local/tomcat 
# Fri, 02 Sep 2022 10:43:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 10:43:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Sep 2022 10:43:20 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 10:43:20 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 02 Sep 2022 12:14:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 02 Sep 2022 12:15:58 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:16:00 GMT
ENV XWIKI_VERSION=14.7
# Fri, 02 Sep 2022 12:16:00 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.7
# Fri, 02 Sep 2022 12:16:00 GMT
ENV XWIKI_DOWNLOAD_SHA256=3de00089af3af64929ccb39f5f36486d44dbb0e1181c42dc046f6db19c8a20f5
# Fri, 02 Sep 2022 12:16:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Sep 2022 12:18:13 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Fri, 02 Sep 2022 12:18:13 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Fri, 02 Sep 2022 12:18:13 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Fri, 02 Sep 2022 12:18:13 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Fri, 02 Sep 2022 12:18:13 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Fri, 02 Sep 2022 12:18:14 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Sep 2022 12:18:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Sep 2022 12:18:14 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Sep 2022 12:18:15 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Sep 2022 12:18:15 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Sep 2022 12:18:15 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Sep 2022 12:18:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Sep 2022 12:18:15 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca45fc4c4ca4ea0526871f8fe0527c23dbb2d24df2aff307d5b41e7b5ebc3fe`  
		Last Modified: Fri, 02 Sep 2022 05:28:37 GMT  
		Size: 12.4 MB (12441851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522d9aa14d93cbdfa4eac0048d607d396eea10c1bfe2da9eafd0ee8b562d5c45`  
		Last Modified: Fri, 02 Sep 2022 05:30:43 GMT  
		Size: 46.5 MB (46498618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a19e0a4285757e7a688613e8c01972397948c470b96c5e1a9eef9c1acb847e3`  
		Last Modified: Fri, 02 Sep 2022 05:30:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee310b06f35a03f98596c215dcbed87e02dc080494393a5b0a49ad322f2cd5`  
		Last Modified: Fri, 02 Sep 2022 10:57:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6339556a0cdabcb4506355753818227f43eafb07382fd802972a64cc13a52243`  
		Last Modified: Fri, 02 Sep 2022 11:05:07 GMT  
		Size: 12.2 MB (12185040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0176dbb87b70aed4ecd1c3e21e692599d24fc88f03f436da28bf480532ac5b0a`  
		Last Modified: Fri, 02 Sep 2022 11:05:07 GMT  
		Size: 452.2 KB (452197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90b87a434c90d249f4254739d844d2cbf474d83a1f36c68807b0b0aa8a9b038`  
		Last Modified: Fri, 02 Sep 2022 11:05:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfc8c2e3627eed9a1f83b30e9784ec2fa2f9d2778a8f608b4808b4fa4db84ce`  
		Last Modified: Fri, 02 Sep 2022 12:22:58 GMT  
		Size: 178.3 MB (178335459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fbc42a7db67f315e847bced0121b5ee943860f5a9a591980aacb2bb1d0c9cb`  
		Last Modified: Fri, 02 Sep 2022 12:22:51 GMT  
		Size: 300.4 MB (300375649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6511684737118dcc9cf188c5fb793c39d36f30fcda47a2905ee47cddde76b1`  
		Last Modified: Fri, 02 Sep 2022 12:24:25 GMT  
		Size: 543.9 KB (543935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338cb7dc40ae98051bbf0de5f68e87146f5dbbbf2e07fa095181f17c49f4ccd3`  
		Last Modified: Fri, 02 Sep 2022 12:24:25 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913daf6c0e33f412af4565ffe096a14f4c040556ff6143215e0778176cb1ccf5`  
		Last Modified: Fri, 02 Sep 2022 12:24:25 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063758653d7880556f50db160ef20d7683647370c2541af59d75ea0b2b43a60`  
		Last Modified: Fri, 02 Sep 2022 12:24:25 GMT  
		Size: 5.9 KB (5875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0efed64d7e534895349481c28b93361d7947fe679c6e1a664743738e8d8cc65`  
		Last Modified: Fri, 02 Sep 2022 12:24:25 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f49375b7b99887e5a1301a131ec0f48648c1175e89eb62fd50fa943e4b0285a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.3 MB (572288018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7048ebe9926ff6398fb9a7055fa1d17d18e9c9065db4f0ed50cc4fc4cb0f5e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

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
# Fri, 02 Sep 2022 04:56:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:57:37 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 02 Sep 2022 04:58:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b6607f28fa2906d612d517f0babe4f0f895aa1c3f901edcddb493e33c1e27364';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        armhf|arm)          ESUM='2ee7fe636a6a57e4718dfe597e8097b93ef8d976e4b05384433777c9f0526f5a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f76b64b201b64ff37f77f73ead546ebcf2af9862b7cd1a1f4e0e5628e3f6a7fc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='bf01489459135ab0ce1ad346a56f0dfeb2d6fe4e59854ef76a6bb989ac403f91';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1ffe1a682e8179e35238bf3f93aba0cb185850e202c676f41d38cb0561883eda';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 02 Sep 2022 04:58:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 02 Sep 2022 09:16:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 02 Sep 2022 09:16:15 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 09:16:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 02 Sep 2022 09:16:17 GMT
WORKDIR /usr/local/tomcat
# Fri, 02 Sep 2022 09:16:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:16:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 02 Sep 2022 09:28:21 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 02 Sep 2022 09:28:21 GMT
ENV TOMCAT_MAJOR=9
# Fri, 02 Sep 2022 09:28:22 GMT
ENV TOMCAT_VERSION=9.0.65
# Fri, 02 Sep 2022 09:28:23 GMT
ENV TOMCAT_SHA512=2ae846848b8436856be11cfa18d9c62caa06ca7d3134012b2e10cbf6078753c4af20cc5d37f7dc75f1779f5c59d7c033850b8626534c3ce7e389641a67963cf6
# Fri, 02 Sep 2022 09:28:25 GMT
COPY dir:9c4391ce573391ca3db965376ee6ab48ed05f3e68677ca4f56a01c9018f54474 in /usr/local/tomcat 
# Fri, 02 Sep 2022 09:28:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:28:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Sep 2022 09:28:34 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 09:28:35 GMT
CMD ["catalina.sh" "run"]
# Fri, 02 Sep 2022 12:48:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 02 Sep 2022 12:48:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 02 Sep 2022 12:48:41 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 02 Sep 2022 12:48:42 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 02 Sep 2022 12:48:43 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 02 Sep 2022 12:48:44 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 02 Sep 2022 12:49:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 12:49:25 GMT
ENV XWIKI_VERSION=14.7
# Fri, 02 Sep 2022 12:49:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.7
# Fri, 02 Sep 2022 12:49:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=3de00089af3af64929ccb39f5f36486d44dbb0e1181c42dc046f6db19c8a20f5
# Fri, 02 Sep 2022 12:50:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 02 Sep 2022 12:52:18 GMT
ENV MARIADB_JDBC_VERSION=3.0.7
# Fri, 02 Sep 2022 12:52:19 GMT
ENV MARIADB_JDBC_SHA256=96c7bb2e6228ccbdf88dd4b071346979fa1216196a24aca3d1fb9e4199698bef
# Fri, 02 Sep 2022 12:52:19 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.0.7
# Fri, 02 Sep 2022 12:52:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.0.7.jar
# Fri, 02 Sep 2022 12:52:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.0.7.jar
# Fri, 02 Sep 2022 12:52:23 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c -
# Fri, 02 Sep 2022 12:52:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 02 Sep 2022 12:52:25 GMT
COPY file:0e237c3876eeb3b5f3473a064d3e507da2df6c228ca714687930b34e3b687601 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 02 Sep 2022 12:52:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 02 Sep 2022 12:52:27 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Sep 2022 12:52:27 GMT
VOLUME [/usr/local/xwiki]
# Fri, 02 Sep 2022 12:52:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Sep 2022 12:52:29 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdb549d469a383cfda4a1db7a2dd57a269b1b7a2325cbf0e9d8f5c604a72eed`  
		Last Modified: Fri, 02 Sep 2022 05:04:20 GMT  
		Size: 12.4 MB (12397459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e2de83fd0832584ab1379ffe8c12ed166b2406e60b5e297487e5df856f4c9`  
		Last Modified: Fri, 02 Sep 2022 05:07:00 GMT  
		Size: 44.8 MB (44824448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3970fa7bb851d635c04498eaedd0112cf0274c4b699bb547b26e4538cb06b5`  
		Last Modified: Fri, 02 Sep 2022 05:06:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c016dc02a28329c1d799871b3ae0d29c9cf580c2ad6e371006e19b93bb7eb80`  
		Last Modified: Fri, 02 Sep 2022 09:52:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c121e617e4bd1844a5498c6069f15e8e56fcfe89af8c321b82577b8e05743ef5`  
		Last Modified: Fri, 02 Sep 2022 10:02:03 GMT  
		Size: 12.2 MB (12191541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccac1cb7586a3d849fa335bf3b6e8302e23c5137c986754440ff08657c5300e`  
		Last Modified: Fri, 02 Sep 2022 10:02:02 GMT  
		Size: 214.2 KB (214189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b649f6f924cb33b97c7af1e5c6b5f90660c1167a556e22041d21076b816cbb6`  
		Last Modified: Fri, 02 Sep 2022 12:58:50 GMT  
		Size: 173.3 MB (173347037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822961d8a02dddd1e19c6c9e7397f66feec63b33bc5ed083d3c77780de708364`  
		Last Modified: Fri, 02 Sep 2022 12:58:48 GMT  
		Size: 300.4 MB (300375727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5579678a15a6ce2266d4df792fe4555c7b38b21777dd75631222697455cbc8e`  
		Last Modified: Fri, 02 Sep 2022 13:00:27 GMT  
		Size: 543.9 KB (543935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9bee35285f81c6a3df77fb3a2624e9e01bf452c227889907beefefe15adc6b`  
		Last Modified: Fri, 02 Sep 2022 13:00:27 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5d7168aaf660a2fb794db5228cf885d3c0cb9f76e1067262192721af1adaf4`  
		Last Modified: Fri, 02 Sep 2022 13:00:27 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbbb7a0ba84dda33042dbec537656bd12dec025a5d339c4c20d48ab8bed546c`  
		Last Modified: Fri, 02 Sep 2022 13:00:27 GMT  
		Size: 5.9 KB (5880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e43c0f5968e6f8bcda7fa25f6d988f9f82a0789386da2c2a5c709e38cd24ff`  
		Last Modified: Fri, 02 Sep 2022 13:00:27 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
