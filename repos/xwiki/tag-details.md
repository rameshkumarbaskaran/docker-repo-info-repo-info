<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `xwiki`

-	[`xwiki:12`](#xwiki12)
-	[`xwiki:12.10`](#xwiki1210)
-	[`xwiki:12.10.4`](#xwiki12104)
-	[`xwiki:12.10.4-mysql-tomcat`](#xwiki12104-mysql-tomcat)
-	[`xwiki:12.10.4-postgres-tomcat`](#xwiki12104-postgres-tomcat)
-	[`xwiki:12.10-mysql-tomcat`](#xwiki1210-mysql-tomcat)
-	[`xwiki:12.10-postgres-tomcat`](#xwiki1210-postgres-tomcat)
-	[`xwiki:12.6`](#xwiki126)
-	[`xwiki:12.6.8`](#xwiki1268)
-	[`xwiki:12.6.8-mysql-tomcat`](#xwiki1268-mysql-tomcat)
-	[`xwiki:12.6.8-postgres-tomcat`](#xwiki1268-postgres-tomcat)
-	[`xwiki:12.6-mysql-tomcat`](#xwiki126-mysql-tomcat)
-	[`xwiki:12.6-postgres-tomcat`](#xwiki126-postgres-tomcat)
-	[`xwiki:12-mysql-tomcat`](#xwiki12-mysql-tomcat)
-	[`xwiki:12-postgres-tomcat`](#xwiki12-postgres-tomcat)
-	[`xwiki:13`](#xwiki13)
-	[`xwiki:13.1`](#xwiki131)
-	[`xwiki:13.1.0`](#xwiki1310)
-	[`xwiki:13.1.0-mysql-tomcat`](#xwiki1310-mysql-tomcat)
-	[`xwiki:13.1.0-postgres-tomcat`](#xwiki1310-postgres-tomcat)
-	[`xwiki:13.1-mysql-tomcat`](#xwiki131-mysql-tomcat)
-	[`xwiki:13.1-postgres-tomcat`](#xwiki131-postgres-tomcat)
-	[`xwiki:13-mysql-tomcat`](#xwiki13-mysql-tomcat)
-	[`xwiki:13-postgres-tomcat`](#xwiki13-postgres-tomcat)
-	[`xwiki:latest`](#xwikilatest)
-	[`xwiki:lts`](#xwikilts)
-	[`xwiki:lts-mysql`](#xwikilts-mysql)
-	[`xwiki:lts-mysql-tomcat`](#xwikilts-mysql-tomcat)
-	[`xwiki:lts-postgres`](#xwikilts-postgres)
-	[`xwiki:lts-postgres-tomcat`](#xwikilts-postgres-tomcat)
-	[`xwiki:mysql-tomcat`](#xwikimysql-tomcat)
-	[`xwiki:postgres-tomcat`](#xwikipostgres-tomcat)
-	[`xwiki:stable`](#xwikistable)
-	[`xwiki:stable-mysql`](#xwikistable-mysql)
-	[`xwiki:stable-mysql-tomcat`](#xwikistable-mysql-tomcat)
-	[`xwiki:stable-postgres`](#xwikistable-postgres)
-	[`xwiki:stable-postgres-tomcat`](#xwikistable-postgres-tomcat)

## `xwiki:12`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.4`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10.4` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.4-mysql-tomcat`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10.4-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10.4-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4bba8e05de493ea77a9639720d3247d73f22184138dfd5ecc9cbb7a411a1a640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10.4-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bbd762c295026a307f84c514d8ee89f2ac8f5c2bcf0d157eebcad1002c0e7c3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 MB (723200388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece3b21a2d50ff4f905a40cf9f7f57544d0a67260020cd3df73fc572054edd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:25:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:25:23 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:25:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:25:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:25:25 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3e182a1e1fe2a5a0e3cbc73980b1713eec68cac84635f362643befaeb21e2e`  
		Last Modified: Sat, 06 Mar 2021 01:31:31 GMT  
		Size: 297.1 MB (297074044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab955d8c75eb3b4dec5ef01e4509b47fa4bc7db17bdc27965665a1b1819542`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12385ef41a13baf05bb1108dee9d7aaf94cbfe8412007210f9bff7df1eeb127a`  
		Last Modified: Sat, 06 Mar 2021 01:31:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20d2f8186b85818fc4cad9367dcfd050f6a978afb58a063f3d074fe690bda7`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303348ab2ffe0002d31e08cb230189ff94165084fa640222a68b3233f664d6a`  
		Last Modified: Sat, 06 Mar 2021 01:31:10 GMT  
		Size: 5.2 KB (5208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3337b73c272b945610f6afe19f485cf9c0775627d2673b0d23c7cb550621c8e`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10.4-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:af347d9a03e4fb1c797cd001c673f77e14cbe2f801ff0d08686c57379ab2bc10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.4 MB (713364301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8f099f9d37b8d844f68c64e58e498061cd8a53247283a7cc53ef713e773fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 00:42:39 GMT
ENV XWIKI_VERSION=12.10.4
# Fri, 12 Feb 2021 00:42:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Fri, 12 Feb 2021 00:42:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Fri, 12 Feb 2021 00:43:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 12 Feb 2021 00:43:18 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 12 Feb 2021 00:43:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 12 Feb 2021 00:43:20 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 12 Feb 2021 00:43:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 12 Feb 2021 00:43:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Feb 2021 00:43:23 GMT
VOLUME [/usr/local/xwiki]
# Fri, 12 Feb 2021 00:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 00:43:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b00e087d75653a43a9f8df514dd63ffaed9bee3120fe11d4b10b4dcf55be397`  
		Last Modified: Fri, 12 Feb 2021 00:44:27 GMT  
		Size: 297.1 MB (297074025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d166dda5a19b4353e5a17d709f6bd96f9045429232b4215b76458a8f648ba`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1981c8a7c8089b760985c8f4755c6ed90906b6360d66a40eae6879a80fbaa6`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b11cabf69fed2021cf819bdcdae8b3f110db333e3da680f6c73b38e3dbfcb5`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf26f7c87347b3c59ba07669208c06b0535bfce947234f19e89d49153a77c7d`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c15d461a60564e28b182709cd17aa4badd11e2dba8a0090fe50fbfaffbfbaf`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-mysql-tomcat`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.10-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.10-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4bba8e05de493ea77a9639720d3247d73f22184138dfd5ecc9cbb7a411a1a640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.10-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bbd762c295026a307f84c514d8ee89f2ac8f5c2bcf0d157eebcad1002c0e7c3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 MB (723200388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece3b21a2d50ff4f905a40cf9f7f57544d0a67260020cd3df73fc572054edd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:25:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:25:23 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:25:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:25:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:25:25 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3e182a1e1fe2a5a0e3cbc73980b1713eec68cac84635f362643befaeb21e2e`  
		Last Modified: Sat, 06 Mar 2021 01:31:31 GMT  
		Size: 297.1 MB (297074044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab955d8c75eb3b4dec5ef01e4509b47fa4bc7db17bdc27965665a1b1819542`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12385ef41a13baf05bb1108dee9d7aaf94cbfe8412007210f9bff7df1eeb127a`  
		Last Modified: Sat, 06 Mar 2021 01:31:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20d2f8186b85818fc4cad9367dcfd050f6a978afb58a063f3d074fe690bda7`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303348ab2ffe0002d31e08cb230189ff94165084fa640222a68b3233f664d6a`  
		Last Modified: Sat, 06 Mar 2021 01:31:10 GMT  
		Size: 5.2 KB (5208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3337b73c272b945610f6afe19f485cf9c0775627d2673b0d23c7cb550621c8e`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.10-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:af347d9a03e4fb1c797cd001c673f77e14cbe2f801ff0d08686c57379ab2bc10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.4 MB (713364301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8f099f9d37b8d844f68c64e58e498061cd8a53247283a7cc53ef713e773fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 00:42:39 GMT
ENV XWIKI_VERSION=12.10.4
# Fri, 12 Feb 2021 00:42:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Fri, 12 Feb 2021 00:42:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Fri, 12 Feb 2021 00:43:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 12 Feb 2021 00:43:18 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 12 Feb 2021 00:43:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 12 Feb 2021 00:43:20 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 12 Feb 2021 00:43:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 12 Feb 2021 00:43:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Feb 2021 00:43:23 GMT
VOLUME [/usr/local/xwiki]
# Fri, 12 Feb 2021 00:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 00:43:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b00e087d75653a43a9f8df514dd63ffaed9bee3120fe11d4b10b4dcf55be397`  
		Last Modified: Fri, 12 Feb 2021 00:44:27 GMT  
		Size: 297.1 MB (297074025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d166dda5a19b4353e5a17d709f6bd96f9045429232b4215b76458a8f648ba`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1981c8a7c8089b760985c8f4755c6ed90906b6360d66a40eae6879a80fbaa6`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b11cabf69fed2021cf819bdcdae8b3f110db333e3da680f6c73b38e3dbfcb5`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf26f7c87347b3c59ba07669208c06b0535bfce947234f19e89d49153a77c7d`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c15d461a60564e28b182709cd17aa4badd11e2dba8a0090fe50fbfaffbfbaf`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6`

```console
$ docker pull xwiki@sha256:45e95dd76b5cf6b2eab35e5c86600f2660cf9e02c597767e23694892596b5cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.6` - linux; amd64

```console
$ docker pull xwiki@sha256:5fa5216a3fcaaa8341535088fff11b3046860a437a48e3b0e170e6f41b3099e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.8 MB (710793286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3aadd26226e8ed30e00baccc1f8122d16f336d728ca83437b045835c9a425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:26:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_VERSION=8.0.21
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_SHA256=2f62d886270a75ebc8e8fd89127d4a30ccc711f02256ade2cfb7090817132003
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.21
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:26:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:26:15 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:26:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:26:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:26:16 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:26:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:26:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c74f410e3b91e5412d6fcc510e18860aca33f6674c8baa5caf4ea9ade87064`  
		Last Modified: Sat, 06 Mar 2021 01:32:18 GMT  
		Size: 284.0 MB (283997253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698b34c2e8091b8ad6d20a5b81fee49079cd2ec1264912e6538fb35e4b15560e`  
		Last Modified: Sat, 06 Mar 2021 01:31:58 GMT  
		Size: 2.3 MB (2265141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a3f083857b97c37bd2b8f9b61322cf5b64ae0b669c4e3758a8cd330a4b79c`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15687794f585e0a93f6c51e9fd6143a92de6a3f0a52ee8c8040ddda354e586a2`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a946195f77b7d4b6e3a41aa6a0de0826ca731d2a0ded85672dca445484f028`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b9bef7a39024cb7e4dfdb29fb4550b1b17e57daaa6e8225f2c0e292aa86cf`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6.8`

```console
$ docker pull xwiki@sha256:45e95dd76b5cf6b2eab35e5c86600f2660cf9e02c597767e23694892596b5cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.6.8` - linux; amd64

```console
$ docker pull xwiki@sha256:5fa5216a3fcaaa8341535088fff11b3046860a437a48e3b0e170e6f41b3099e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.8 MB (710793286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3aadd26226e8ed30e00baccc1f8122d16f336d728ca83437b045835c9a425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:26:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_VERSION=8.0.21
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_SHA256=2f62d886270a75ebc8e8fd89127d4a30ccc711f02256ade2cfb7090817132003
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.21
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:26:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:26:15 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:26:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:26:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:26:16 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:26:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:26:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c74f410e3b91e5412d6fcc510e18860aca33f6674c8baa5caf4ea9ade87064`  
		Last Modified: Sat, 06 Mar 2021 01:32:18 GMT  
		Size: 284.0 MB (283997253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698b34c2e8091b8ad6d20a5b81fee49079cd2ec1264912e6538fb35e4b15560e`  
		Last Modified: Sat, 06 Mar 2021 01:31:58 GMT  
		Size: 2.3 MB (2265141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a3f083857b97c37bd2b8f9b61322cf5b64ae0b669c4e3758a8cd330a4b79c`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15687794f585e0a93f6c51e9fd6143a92de6a3f0a52ee8c8040ddda354e586a2`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a946195f77b7d4b6e3a41aa6a0de0826ca731d2a0ded85672dca445484f028`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b9bef7a39024cb7e4dfdb29fb4550b1b17e57daaa6e8225f2c0e292aa86cf`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6.8-mysql-tomcat`

```console
$ docker pull xwiki@sha256:45e95dd76b5cf6b2eab35e5c86600f2660cf9e02c597767e23694892596b5cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.6.8-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5fa5216a3fcaaa8341535088fff11b3046860a437a48e3b0e170e6f41b3099e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.8 MB (710793286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3aadd26226e8ed30e00baccc1f8122d16f336d728ca83437b045835c9a425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:26:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_VERSION=8.0.21
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_SHA256=2f62d886270a75ebc8e8fd89127d4a30ccc711f02256ade2cfb7090817132003
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.21
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:26:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:26:15 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:26:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:26:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:26:16 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:26:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:26:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c74f410e3b91e5412d6fcc510e18860aca33f6674c8baa5caf4ea9ade87064`  
		Last Modified: Sat, 06 Mar 2021 01:32:18 GMT  
		Size: 284.0 MB (283997253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698b34c2e8091b8ad6d20a5b81fee49079cd2ec1264912e6538fb35e4b15560e`  
		Last Modified: Sat, 06 Mar 2021 01:31:58 GMT  
		Size: 2.3 MB (2265141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a3f083857b97c37bd2b8f9b61322cf5b64ae0b669c4e3758a8cd330a4b79c`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15687794f585e0a93f6c51e9fd6143a92de6a3f0a52ee8c8040ddda354e586a2`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a946195f77b7d4b6e3a41aa6a0de0826ca731d2a0ded85672dca445484f028`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b9bef7a39024cb7e4dfdb29fb4550b1b17e57daaa6e8225f2c0e292aa86cf`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6.8-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4918e74023258629381cd8fe1810c31fdbbea8fb4059fcafb4c975a146404a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.6.8-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:64cdee7dc21d1252fb4a2aa81d19da07b9e59cb0a54b73261c297d15c151963c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.1 MB (710123386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7382dcc782fc7f579ae5cb043ab7e9e2f2e84bb343d4ea9b09977915b7b86020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:26:24 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:26:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:26:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:27:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:27:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:27:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:27:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:27:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:27:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:27:05 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:27:05 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed7cbc8b58d7413337f46a2ec0a4348f07d0c5f55e9a096b883c7309904cbe6`  
		Last Modified: Sat, 06 Mar 2021 01:32:58 GMT  
		Size: 284.0 MB (283997225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdb0ca5fd0c9362db0e789eabe0581ef8f088859d5caf7e416cefa679b9d258`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233aa47d6ed7a4126a4e93d82fec04310eb0e47052197c7ab6da5cb0fcccf219`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa91d5816a199347331740c1133265a880e84968010fd714273ef26356dfad`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f1aeb1fa3058ed62c77b49477c75eee6f7f714180dc89093850317edf11cb3`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d9095e58e3511945ce2a4273d32e6883832b41d14cf0906746a28a99be95`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.6.8-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:7618d7577a6c7689461899d746fae2cb0ad2aba4fe25315e760594d1bffd686b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700287447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e1c12a3a0453192b5a4614410dde0565ebb24ebdbfc38dfcb6133599a6fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 20:38:50 GMT
ENV XWIKI_VERSION=12.6.8
# Thu, 04 Mar 2021 20:38:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Thu, 04 Mar 2021 20:38:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Thu, 04 Mar 2021 20:39:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 04 Mar 2021 20:39:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 04 Mar 2021 20:39:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 04 Mar 2021 20:39:22 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 04 Mar 2021 20:39:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 04 Mar 2021 20:39:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 04 Mar 2021 20:39:26 GMT
VOLUME [/usr/local/xwiki]
# Thu, 04 Mar 2021 20:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 20:39:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c09077af2fdf82498b6e48d3d3710acb3b398d8dbb3cd98f273bc0b38af712`  
		Last Modified: Thu, 04 Mar 2021 20:40:26 GMT  
		Size: 284.0 MB (283997328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b5d2c9aede80efaaf935de8b13bcb83e61950841c4722cf13afcac9d2b1671`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 795.4 KB (795425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043d9d6e34e399cd9384a4250a1fb70b3911d02962ce81e14086422c4545db5f`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3704f146f69d4fb42dee718e485a6b56c741571b45f7a7e554872104178bf271`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98068aaeca6c91cc75d6ae37b11c0ad264df7703691a8e18395c1c58722fd2b8`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 5.0 KB (5044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155f0edb09e9c634ded79f2ef719078974f7ae4270729039f422dc4272b68753`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6-mysql-tomcat`

```console
$ docker pull xwiki@sha256:45e95dd76b5cf6b2eab35e5c86600f2660cf9e02c597767e23694892596b5cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12.6-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5fa5216a3fcaaa8341535088fff11b3046860a437a48e3b0e170e6f41b3099e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.8 MB (710793286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec3aadd26226e8ed30e00baccc1f8122d16f336d728ca83437b045835c9a425`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:25:34 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:26:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_VERSION=8.0.21
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_SHA256=2f62d886270a75ebc8e8fd89127d4a30ccc711f02256ade2cfb7090817132003
# Sat, 06 Mar 2021 01:26:12 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.21
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:13 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.21.jar
# Sat, 06 Mar 2021 01:26:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:26:14 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:26:15 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:26:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:26:16 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:26:16 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:26:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:26:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c74f410e3b91e5412d6fcc510e18860aca33f6674c8baa5caf4ea9ade87064`  
		Last Modified: Sat, 06 Mar 2021 01:32:18 GMT  
		Size: 284.0 MB (283997253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698b34c2e8091b8ad6d20a5b81fee49079cd2ec1264912e6538fb35e4b15560e`  
		Last Modified: Sat, 06 Mar 2021 01:31:58 GMT  
		Size: 2.3 MB (2265141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a3f083857b97c37bd2b8f9b61322cf5b64ae0b669c4e3758a8cd330a4b79c`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15687794f585e0a93f6c51e9fd6143a92de6a3f0a52ee8c8040ddda354e586a2`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a946195f77b7d4b6e3a41aa6a0de0826ca731d2a0ded85672dca445484f028`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b9bef7a39024cb7e4dfdb29fb4550b1b17e57daaa6e8225f2c0e292aa86cf`  
		Last Modified: Sat, 06 Mar 2021 01:31:57 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12.6-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4918e74023258629381cd8fe1810c31fdbbea8fb4059fcafb4c975a146404a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12.6-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:64cdee7dc21d1252fb4a2aa81d19da07b9e59cb0a54b73261c297d15c151963c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.1 MB (710123386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7382dcc782fc7f579ae5cb043ab7e9e2f2e84bb343d4ea9b09977915b7b86020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:26:24 GMT
ENV XWIKI_VERSION=12.6.8
# Sat, 06 Mar 2021 01:26:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Sat, 06 Mar 2021 01:26:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Sat, 06 Mar 2021 01:27:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:27:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:27:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:27:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:27:05 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:27:05 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:27:05 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:27:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:27:05 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed7cbc8b58d7413337f46a2ec0a4348f07d0c5f55e9a096b883c7309904cbe6`  
		Last Modified: Sat, 06 Mar 2021 01:32:58 GMT  
		Size: 284.0 MB (283997225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdb0ca5fd0c9362db0e789eabe0581ef8f088859d5caf7e416cefa679b9d258`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233aa47d6ed7a4126a4e93d82fec04310eb0e47052197c7ab6da5cb0fcccf219`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa91d5816a199347331740c1133265a880e84968010fd714273ef26356dfad`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f1aeb1fa3058ed62c77b49477c75eee6f7f714180dc89093850317edf11cb3`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 5.0 KB (5040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c1d9095e58e3511945ce2a4273d32e6883832b41d14cf0906746a28a99be95`  
		Last Modified: Sat, 06 Mar 2021 01:32:39 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12.6-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:7618d7577a6c7689461899d746fae2cb0ad2aba4fe25315e760594d1bffd686b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700287447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e1c12a3a0453192b5a4614410dde0565ebb24ebdbfc38dfcb6133599a6fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 20:38:50 GMT
ENV XWIKI_VERSION=12.6.8
# Thu, 04 Mar 2021 20:38:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.6.8
# Thu, 04 Mar 2021 20:38:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=86ddfd5eca8af848866fe04fdf75f03572810a51a07c44e6f3597fef17c07574
# Thu, 04 Mar 2021 20:39:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 04 Mar 2021 20:39:21 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 04 Mar 2021 20:39:21 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 04 Mar 2021 20:39:22 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 04 Mar 2021 20:39:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 04 Mar 2021 20:39:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 04 Mar 2021 20:39:26 GMT
VOLUME [/usr/local/xwiki]
# Thu, 04 Mar 2021 20:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 20:39:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c09077af2fdf82498b6e48d3d3710acb3b398d8dbb3cd98f273bc0b38af712`  
		Last Modified: Thu, 04 Mar 2021 20:40:26 GMT  
		Size: 284.0 MB (283997328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b5d2c9aede80efaaf935de8b13bcb83e61950841c4722cf13afcac9d2b1671`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 795.4 KB (795425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043d9d6e34e399cd9384a4250a1fb70b3911d02962ce81e14086422c4545db5f`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3704f146f69d4fb42dee718e485a6b56c741571b45f7a7e554872104178bf271`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98068aaeca6c91cc75d6ae37b11c0ad264df7703691a8e18395c1c58722fd2b8`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 5.0 KB (5044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155f0edb09e9c634ded79f2ef719078974f7ae4270729039f422dc4272b68753`  
		Last Modified: Thu, 04 Mar 2021 20:39:57 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-mysql-tomcat`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:12-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:12-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4bba8e05de493ea77a9639720d3247d73f22184138dfd5ecc9cbb7a411a1a640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:12-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bbd762c295026a307f84c514d8ee89f2ac8f5c2bcf0d157eebcad1002c0e7c3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 MB (723200388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece3b21a2d50ff4f905a40cf9f7f57544d0a67260020cd3df73fc572054edd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:25:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:25:23 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:25:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:25:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:25:25 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3e182a1e1fe2a5a0e3cbc73980b1713eec68cac84635f362643befaeb21e2e`  
		Last Modified: Sat, 06 Mar 2021 01:31:31 GMT  
		Size: 297.1 MB (297074044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab955d8c75eb3b4dec5ef01e4509b47fa4bc7db17bdc27965665a1b1819542`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12385ef41a13baf05bb1108dee9d7aaf94cbfe8412007210f9bff7df1eeb127a`  
		Last Modified: Sat, 06 Mar 2021 01:31:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20d2f8186b85818fc4cad9367dcfd050f6a978afb58a063f3d074fe690bda7`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303348ab2ffe0002d31e08cb230189ff94165084fa640222a68b3233f664d6a`  
		Last Modified: Sat, 06 Mar 2021 01:31:10 GMT  
		Size: 5.2 KB (5208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3337b73c272b945610f6afe19f485cf9c0775627d2673b0d23c7cb550621c8e`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:12-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:af347d9a03e4fb1c797cd001c673f77e14cbe2f801ff0d08686c57379ab2bc10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.4 MB (713364301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8f099f9d37b8d844f68c64e58e498061cd8a53247283a7cc53ef713e773fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 00:42:39 GMT
ENV XWIKI_VERSION=12.10.4
# Fri, 12 Feb 2021 00:42:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Fri, 12 Feb 2021 00:42:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Fri, 12 Feb 2021 00:43:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 12 Feb 2021 00:43:18 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 12 Feb 2021 00:43:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 12 Feb 2021 00:43:20 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 12 Feb 2021 00:43:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 12 Feb 2021 00:43:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Feb 2021 00:43:23 GMT
VOLUME [/usr/local/xwiki]
# Fri, 12 Feb 2021 00:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 00:43:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b00e087d75653a43a9f8df514dd63ffaed9bee3120fe11d4b10b4dcf55be397`  
		Last Modified: Fri, 12 Feb 2021 00:44:27 GMT  
		Size: 297.1 MB (297074025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d166dda5a19b4353e5a17d709f6bd96f9045429232b4215b76458a8f648ba`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1981c8a7c8089b760985c8f4755c6ed90906b6360d66a40eae6879a80fbaa6`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b11cabf69fed2021cf819bdcdae8b3f110db333e3da680f6c73b38e3dbfcb5`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf26f7c87347b3c59ba07669208c06b0535bfce947234f19e89d49153a77c7d`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c15d461a60564e28b182709cd17aa4badd11e2dba8a0090fe50fbfaffbfbaf`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.1` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1.0`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.1.0` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1.0-mysql-tomcat`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.1.0-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1.0-postgres-tomcat`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.1.0-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.1.0-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1-mysql-tomcat`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13.1-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13.1-postgres-tomcat`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13.1-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13.1-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-mysql-tomcat`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:13-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:latest`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:latest` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:331f2c86def49a1772778325240b08fc673b85212145c29717fc796cbe819e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:603c9d4ba7e0d48a5ef8c93a53b4eef0d04968b5525494f1b798b67f8d1f1789
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.9 MB (723862928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea48fffc7dceda55511034a5d691b7e73bcf068a8adcbeec6b3e0cfccdbdbec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:23:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:24:31 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:24:32 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:33 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:24:34 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:24:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:24:35 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:24:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:24:36 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:24:36 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:24:36 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0535a96f7904c0afd93395916ca2b6a7e7896a9f596d360788b9d1074d126b8a`  
		Last Modified: Sat, 06 Mar 2021 01:30:35 GMT  
		Size: 297.1 MB (297074038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e290cb249666e0d0945d27633a35b62bd6c34f05e063d7c48796efe55584593`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 MB (2257827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21ccaef6e649c5071111c94664867a67085a50a7c3942b4ce9044b2533db5b5`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb270bdb0eb20f8dae808e30534b00062663617cf521ca2f0f8964ef8591652`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135433beb017403056fe925bcf4bdbddcf0a30a10ce063b05bcc05b0e36668b3`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb44dcb671a7b1873fe2be04b0578b278975a24b026ac271c9b34b64915fe4d`  
		Last Modified: Sat, 06 Mar 2021 01:30:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:4bba8e05de493ea77a9639720d3247d73f22184138dfd5ecc9cbb7a411a1a640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:bbd762c295026a307f84c514d8ee89f2ac8f5c2bcf0d157eebcad1002c0e7c3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 MB (723200388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece3b21a2d50ff4f905a40cf9f7f57544d0a67260020cd3df73fc572054edd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:25:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:25:23 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:25:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:25:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:25:25 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3e182a1e1fe2a5a0e3cbc73980b1713eec68cac84635f362643befaeb21e2e`  
		Last Modified: Sat, 06 Mar 2021 01:31:31 GMT  
		Size: 297.1 MB (297074044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab955d8c75eb3b4dec5ef01e4509b47fa4bc7db17bdc27965665a1b1819542`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12385ef41a13baf05bb1108dee9d7aaf94cbfe8412007210f9bff7df1eeb127a`  
		Last Modified: Sat, 06 Mar 2021 01:31:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20d2f8186b85818fc4cad9367dcfd050f6a978afb58a063f3d074fe690bda7`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303348ab2ffe0002d31e08cb230189ff94165084fa640222a68b3233f664d6a`  
		Last Modified: Sat, 06 Mar 2021 01:31:10 GMT  
		Size: 5.2 KB (5208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3337b73c272b945610f6afe19f485cf9c0775627d2673b0d23c7cb550621c8e`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:af347d9a03e4fb1c797cd001c673f77e14cbe2f801ff0d08686c57379ab2bc10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.4 MB (713364301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8f099f9d37b8d844f68c64e58e498061cd8a53247283a7cc53ef713e773fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 00:42:39 GMT
ENV XWIKI_VERSION=12.10.4
# Fri, 12 Feb 2021 00:42:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Fri, 12 Feb 2021 00:42:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Fri, 12 Feb 2021 00:43:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 12 Feb 2021 00:43:18 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 12 Feb 2021 00:43:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 12 Feb 2021 00:43:20 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 12 Feb 2021 00:43:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 12 Feb 2021 00:43:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Feb 2021 00:43:23 GMT
VOLUME [/usr/local/xwiki]
# Fri, 12 Feb 2021 00:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 00:43:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b00e087d75653a43a9f8df514dd63ffaed9bee3120fe11d4b10b4dcf55be397`  
		Last Modified: Fri, 12 Feb 2021 00:44:27 GMT  
		Size: 297.1 MB (297074025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d166dda5a19b4353e5a17d709f6bd96f9045429232b4215b76458a8f648ba`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1981c8a7c8089b760985c8f4755c6ed90906b6360d66a40eae6879a80fbaa6`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b11cabf69fed2021cf819bdcdae8b3f110db333e3da680f6c73b38e3dbfcb5`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf26f7c87347b3c59ba07669208c06b0535bfce947234f19e89d49153a77c7d`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c15d461a60564e28b182709cd17aa4badd11e2dba8a0090fe50fbfaffbfbaf`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:4bba8e05de493ea77a9639720d3247d73f22184138dfd5ecc9cbb7a411a1a640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bbd762c295026a307f84c514d8ee89f2ac8f5c2bcf0d157eebcad1002c0e7c3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.2 MB (723200388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ece3b21a2d50ff4f905a40cf9f7f57544d0a67260020cd3df73fc572054edd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_VERSION=12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Sat, 06 Mar 2021 01:24:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Sat, 06 Mar 2021 01:25:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:25:23 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:25:24 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:25:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:25:25 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:25:25 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:25:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:25:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3e182a1e1fe2a5a0e3cbc73980b1713eec68cac84635f362643befaeb21e2e`  
		Last Modified: Sat, 06 Mar 2021 01:31:31 GMT  
		Size: 297.1 MB (297074044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab955d8c75eb3b4dec5ef01e4509b47fa4bc7db17bdc27965665a1b1819542`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 795.4 KB (795424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12385ef41a13baf05bb1108dee9d7aaf94cbfe8412007210f9bff7df1eeb127a`  
		Last Modified: Sat, 06 Mar 2021 01:31:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf20d2f8186b85818fc4cad9367dcfd050f6a978afb58a063f3d074fe690bda7`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2303348ab2ffe0002d31e08cb230189ff94165084fa640222a68b3233f664d6a`  
		Last Modified: Sat, 06 Mar 2021 01:31:10 GMT  
		Size: 5.2 KB (5208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3337b73c272b945610f6afe19f485cf9c0775627d2673b0d23c7cb550621c8e`  
		Last Modified: Sat, 06 Mar 2021 01:31:11 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:af347d9a03e4fb1c797cd001c673f77e14cbe2f801ff0d08686c57379ab2bc10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.4 MB (713364301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e8f099f9d37b8d844f68c64e58e498061cd8a53247283a7cc53ef713e773fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 00:42:39 GMT
ENV XWIKI_VERSION=12.10.4
# Fri, 12 Feb 2021 00:42:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.10.4
# Fri, 12 Feb 2021 00:42:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=fd213ff52d575cfec4c7f0c2c1e20312075d131fbc08285cc7d3b1234437eaa4
# Fri, 12 Feb 2021 00:43:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Fri, 12 Feb 2021 00:43:18 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Fri, 12 Feb 2021 00:43:19 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Fri, 12 Feb 2021 00:43:20 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Fri, 12 Feb 2021 00:43:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Fri, 12 Feb 2021 00:43:22 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Feb 2021 00:43:23 GMT
VOLUME [/usr/local/xwiki]
# Fri, 12 Feb 2021 00:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 00:43:24 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b00e087d75653a43a9f8df514dd63ffaed9bee3120fe11d4b10b4dcf55be397`  
		Last Modified: Fri, 12 Feb 2021 00:44:27 GMT  
		Size: 297.1 MB (297074025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d166dda5a19b4353e5a17d709f6bd96f9045429232b4215b76458a8f648ba`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 795.4 KB (795418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1981c8a7c8089b760985c8f4755c6ed90906b6360d66a40eae6879a80fbaa6`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b11cabf69fed2021cf819bdcdae8b3f110db333e3da680f6c73b38e3dbfcb5`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf26f7c87347b3c59ba07669208c06b0535bfce947234f19e89d49153a77c7d`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 5.2 KB (5205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c15d461a60564e28b182709cd17aa4badd11e2dba8a0090fe50fbfaffbfbaf`  
		Last Modified: Fri, 12 Feb 2021 00:43:56 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:073ec9eabe9a4bce444aea509b0135630cb1e46aae99898c51472b69beb08b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d29f1e29c7745313230e800c2311445046b45dac647c65d43ebb374817bb5349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.8 MB (726757561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c913ed057d3848da0aac0967b3db2a0933bd85d0cad05117e27147748251c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:21:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:21:31 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:22:09 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_VERSION=8.0.22
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_SHA256=5019defbd12316295e97a6e88f2a9b07f118345a4e982710bba232e499b22f4f
# Sat, 06 Mar 2021 01:22:10 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.22
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:11 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-java-8.0.22.jar
# Sat, 06 Mar 2021 01:22:12 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c -
# Sat, 06 Mar 2021 01:22:12 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:22:13 GMT
COPY file:2ddb14ac28e30d814fb2fc4772408aeb1bad06733f2b02f99ac544ada515f776 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:22:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:22:14 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:22:14 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:22:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:22:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952df188119ca82a55ecd70806eae1c26aa817d145898d0e65cc54996b1ace53`  
		Last Modified: Sat, 06 Mar 2021 01:28:30 GMT  
		Size: 167.7 MB (167665983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb1935f6672c23cac39a83b9065cd5808a64547203af9a71354ca13f726107b`  
		Last Modified: Sat, 06 Mar 2021 01:28:23 GMT  
		Size: 300.0 MB (299968673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96c7698beb12497278763c4c2f406acf861931a64be904540278701637f4032`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.3 MB (2257826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bd942f5940e94b8edaed2d3e1cd7fa15b6f1f469d937c1399fc404a0a64b28`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30bf67af58d1bad5bb895d24abffd7e38c9bdb9183eca67d9676205b7ab64dc`  
		Last Modified: Sat, 06 Mar 2021 01:27:58 GMT  
		Size: 2.3 KB (2318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512ebf1c8df78c20f6bb89bb78239de045bbebcc9467794d61090402990e5cd`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 5.2 KB (5199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d0b237baa91eacf62e829801cac4ce7d1da53171b9e18fcbb08b343c60b34`  
		Last Modified: Sat, 06 Mar 2021 01:27:59 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:25dbad77c8ba993b21c1705c4aafec33a2e565f5e11ed8161dd4b09fe64aaf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7799170b6a8d41c6f5b84c173be2dec3f78a396df675276e9fe0ef31b336ee7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726094994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ed8819514ff8f8396d4a3c51e6c76df4595c316cc643e3060d645a1684786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 07:11:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 07:11:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 01:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 01:20:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 01:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 01:20:10 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 23:15:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 23:15:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:15:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 23:15:08 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 23:15:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:15:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 23:35:08 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 23:35:08 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:44:50 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:49:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:49:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:50:00 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:50:00 GMT
CMD ["catalina.sh" "run"]
# Sat, 06 Mar 2021 01:19:01 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Sat, 06 Mar 2021 01:23:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_VERSION=13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Sat, 06 Mar 2021 01:23:02 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Sat, 06 Mar 2021 01:23:41 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Sat, 06 Mar 2021 01:23:43 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Sat, 06 Mar 2021 01:23:43 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Sat, 06 Mar 2021 01:23:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Sat, 06 Mar 2021 01:23:45 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:23:45 GMT
VOLUME [/usr/local/xwiki]
# Sat, 06 Mar 2021 01:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:23:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a2f9af18be145e109b6ad9ca1c120bb9df3c4a67baae7d20e2fabb19fe484`  
		Last Modified: Thu, 21 Jan 2021 07:30:04 GMT  
		Size: 16.0 MB (16037697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db220d7462e6b1f852486b374b1a06c9363454e1fb03750ee5c8070f6325013`  
		Last Modified: Sat, 30 Jan 2021 01:29:47 GMT  
		Size: 195.0 MB (194975417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f210b945a160f6b043ee123d9d73306b1e2f9221cdc8026a26195bc378252`  
		Last Modified: Mon, 01 Feb 2021 23:46:25 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20d214ae4c092a4f4bd218dab7cf76732bc9f0255dcbb5c173d010b94a3c38`  
		Last Modified: Wed, 03 Feb 2021 21:37:52 GMT  
		Size: 17.3 MB (17273429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b7b0745a0090d86dbc53e2c23b7dba47d6af283c7dcf0d8e80529127c1ea6`  
		Last Modified: Wed, 03 Feb 2021 21:37:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73658126fbe236436f88ff14180a165e5820eaa5ad26f0a87f68e9eb70c0a6ef`  
		Last Modified: Sat, 06 Mar 2021 01:29:43 GMT  
		Size: 168.5 MB (168465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bb49786c00fd99ebe002513cf43ee2e4fe66b1ac2ba64200162cf85a3570c5`  
		Last Modified: Sat, 06 Mar 2021 01:29:37 GMT  
		Size: 300.0 MB (299968666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a3f45b47af6520d9ab9bb69d339e956ae90d0cc473b865ae3ae6e1308a6a3`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eac6c6b683e497fbea8a8366681e0c94f44de5b8c6c7f3aad52bbc8afb1a6b`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31320219d87342c0d630108e1fd5a75d7440e73231749bae438665b6d9cc9ff`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df54ecdf25a736f2737be49933cb206b3287e30bcf1218d279eec9d076fdee41`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 5.2 KB (5196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e2eb36105bd7c0d893980653614bb81a3809463b772218243f41394b4475eb`  
		Last Modified: Sat, 06 Mar 2021 01:29:13 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:631126b7f4747415c1b5526c737703d3f456bdfd1ad64fc7b53902e6a68e2191
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.3 MB (716258938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af3be82331b18ff3fd5b295d876fadfbf4dbaa47b1dd9ad82fe434a0ad06832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:16:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 05:16:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jan 2021 00:39:39 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Sat, 30 Jan 2021 00:39:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='420c5d1e5dc66b2ed7dedd30a7bdf94bfaed10d5e1b07dc579722bf60a8114a9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.10_9.tar.gz';          ;;        armhf|armv7l)          ESUM='34908da9c200f5ef71b8766398b79fd166f8be44d87f97510667698b456c8d44';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.10_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1d130a284f0881893711f17df83198d320c16f807de823c788407af019b356b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.10_9.tar.gz';          ;;        s390x)          ESUM='b55e5d774bcec96b7e6ffc8178a17914ab151414f7048abab3afe3c2febb9a20';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.10_9.tar.gz';          ;;        amd64|x86_64)          ESUM='ae78aa45f84642545c01e8ef786dfd700d2226f8b12881c844d6a1f71789cb99';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.10_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jan 2021 00:39:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jan 2021 00:39:56 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 22:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 01 Feb 2021 22:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 22:03:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 01 Feb 2021 22:03:43 GMT
WORKDIR /usr/local/tomcat
# Mon, 01 Feb 2021 22:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 01 Feb 2021 22:21:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 01 Feb 2021 22:21:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Feb 2021 20:38:15 GMT
ENV TOMCAT_VERSION=8.5.63
# Wed, 03 Feb 2021 20:38:16 GMT
ENV TOMCAT_SHA512=f6379373fa688a6a6a49b47589fe02b753dbb639cd85e5deeb9481651343172fbbcc2944e0d3975cce471ca0dcf8f906b7bdab908253d685f588dcafe99de880
# Wed, 03 Feb 2021 20:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Wed, 03 Feb 2021 20:41:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Feb 2021 20:41:40 GMT
EXPOSE 8080
# Wed, 03 Feb 2021 20:41:41 GMT
CMD ["catalina.sh" "run"]
# Wed, 03 Feb 2021 21:21:17 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Wed, 03 Feb 2021 21:22:19 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 24 Feb 2021 19:32:31 GMT
ENV XWIKI_VERSION=13.1
# Wed, 24 Feb 2021 19:32:32 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.1
# Wed, 24 Feb 2021 19:32:33 GMT
ENV XWIKI_DOWNLOAD_SHA256=885e41640d11cf8a3bb86333f0eb9c7836c138f346a632029402e388694dfa94
# Wed, 24 Feb 2021 19:32:59 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 24 Feb 2021 19:33:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 24 Feb 2021 19:33:03 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 24 Feb 2021 19:33:04 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 24 Feb 2021 19:33:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 24 Feb 2021 19:33:07 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 19:33:08 GMT
VOLUME [/usr/local/xwiki]
# Wed, 24 Feb 2021 19:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 19:33:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0287722270ce37abd490501ab7da0fe067f73ee79fae79a93f5ef3e4dd27d6a`  
		Last Modified: Thu, 21 Jan 2021 05:20:27 GMT  
		Size: 15.9 MB (15905058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f85373fce2014607f5841cc337b69041d63ebb6a913cc295ff410f10cb6cbe2`  
		Last Modified: Sat, 30 Jan 2021 00:48:13 GMT  
		Size: 191.7 MB (191730034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a879dbf2c8b4b9e45d2ef8619354e41478cf7beccb2a10aa6cd2e2bafa21df`  
		Last Modified: Mon, 01 Feb 2021 22:27:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ec778ffc808f8da2f87efc3c3051c06d6849063bbe0c119d7cbe27f0c0939`  
		Last Modified: Wed, 03 Feb 2021 21:04:59 GMT  
		Size: 16.4 MB (16370042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52648dd3b9c00ee26b403b31bdcb3207e0a3efb03d4d8a968e23829534f7fba0`  
		Last Modified: Wed, 03 Feb 2021 21:04:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca724e15d81e47b381bfdae4debbc77f0aec7dd0ebab2abedbe20a966994917a`  
		Last Modified: Wed, 03 Feb 2021 21:26:02 GMT  
		Size: 164.3 MB (164303931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edd58d4a0c8784c5cb5b4dd10f2fd823198fcf49ff77a162b04333b494b5232`  
		Last Modified: Wed, 24 Feb 2021 19:34:24 GMT  
		Size: 300.0 MB (299968668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c9255e52110066601ee497daa98fdf3d761dd4dd624d817f28e439e970a33e`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 795.4 KB (795422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8058b56736f0df90b93aef3b0969843ce945b903f537363edfc54627ec593d`  
		Last Modified: Wed, 24 Feb 2021 19:33:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7cf07a3bba23afd273d4e7da77a7106e48c95aa648d37eb6d5f6121450d1b9`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fab76d57df46bc791184bf340457765046d3aa7b508255bd07fd8edc8a0f3b4`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 5.2 KB (5198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84659c5a9139915209b4269166720043ad51ced6cfaf70427c6635f98628b3b6`  
		Last Modified: Wed, 24 Feb 2021 19:33:46 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
