## `xwiki:13-postgres-tomcat`

```console
$ docker pull xwiki@sha256:7108f61f3a3527176aca019cbc4e870f02f328959c9ddbbbbd95980d2e0cbcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:13-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:de8edf22f5abc67dd53f4b9d4f188e2b5b00ee885baea44f441e84a6dd0083b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.3 MB (724343333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a9a7db81d792d01c6e438b1d2b8b7b1df642c715fa964ee753c41bb38a4d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 23:23:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 10 May 2021 18:19:40 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Mon, 10 May 2021 18:19:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 10 May 2021 18:19:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 May 2021 18:19:51 GMT
CMD ["jshell"]
# Tue, 11 May 2021 01:58:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 11 May 2021 01:58:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 May 2021 01:58:49 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 11 May 2021 01:58:49 GMT
WORKDIR /usr/local/tomcat
# Tue, 11 May 2021 01:58:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 11 May 2021 01:58:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 17 Jun 2021 00:44:12 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 17 Jun 2021 00:44:12 GMT
ENV TOMCAT_MAJOR=8
# Thu, 17 Jun 2021 00:44:12 GMT
ENV TOMCAT_VERSION=8.5.68
# Thu, 17 Jun 2021 00:44:12 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Thu, 17 Jun 2021 00:44:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:44:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:44:51 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:44:52 GMT
CMD ["catalina.sh" "run"]
# Thu, 17 Jun 2021 01:27:10 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 17 Jun 2021 01:30:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 01:30:55 GMT
ENV XWIKI_VERSION=13.4
# Thu, 17 Jun 2021 01:30:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4
# Thu, 17 Jun 2021 01:30:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=b9fcf40879203b6237fa1e88a45cec8cd681e5b1bf11949f03daa19b762d5765
# Thu, 17 Jun 2021 01:31:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 17 Jun 2021 01:31:36 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 17 Jun 2021 01:31:36 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 17 Jun 2021 01:31:36 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 17 Jun 2021 01:31:37 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 17 Jun 2021 01:31:37 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Jun 2021 01:31:38 GMT
VOLUME [/usr/local/xwiki]
# Thu, 17 Jun 2021 01:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 01:31:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ec2d7c1370aca6ef48ee1d20fbb3a4c148db400adc5dc575778c681f5dba0`  
		Last Modified: Fri, 23 Apr 2021 23:32:39 GMT  
		Size: 16.0 MB (16034099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0a2410aba2adb3fc36d0afef53fdb794de060dfa24ff52424735d165af5ee9`  
		Last Modified: Mon, 10 May 2021 18:28:28 GMT  
		Size: 193.7 MB (193651089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267948abfc47d400ccf2e9273d7a6ce5eeceea00dbb0d2c27d250e2200954da`  
		Last Modified: Tue, 11 May 2021 02:13:50 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef386518669b975afd0559f6275909cb85331cb09fa6d085656b0c0142777a7`  
		Last Modified: Thu, 17 Jun 2021 01:05:46 GMT  
		Size: 13.6 MB (13592027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a990e3fbcd5734444bef8a437f6c4ca161834a7fbc2a4355342355847a4296`  
		Last Modified: Thu, 17 Jun 2021 01:05:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe45a89eb6f07543f1ff668fa91c72c336b799aa7b0aff01b8d9b0ab8401dc1`  
		Last Modified: Thu, 17 Jun 2021 01:35:37 GMT  
		Size: 168.3 MB (168251991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca582ebd1d79ef6b35e4858873f29ce7d2562f4acb56bddd5503b1370e98a94`  
		Last Modified: Thu, 17 Jun 2021 01:35:31 GMT  
		Size: 303.5 MB (303466279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9084e246f243c38145c9252fbda7cdc46713726a30ba65b46a16119429be1fa`  
		Last Modified: Thu, 17 Jun 2021 01:35:09 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220bc23f84be4f8cffee2a77734ff340f1d1a8ce4cc335b9ad81bc65bcfaaeaa`  
		Last Modified: Thu, 17 Jun 2021 01:35:09 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35fa38c2992aa80a23eaf0f1f5b740b193964a0a8b76cd2f3ef747a63cb212d`  
		Last Modified: Thu, 17 Jun 2021 01:35:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfb8e9eea56a60dce35e661ec9d6be9a5211c4b6915281fde16390300e31d92`  
		Last Modified: Thu, 17 Jun 2021 01:35:09 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba68e410edf68de2a23ac8c721b08e24e85ae355f4f61c0913919d222c5cfd43`  
		Last Modified: Thu, 17 Jun 2021 01:35:09 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:13-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0345f95555444435746967d0a089afa383708685b33f4fd7bf0ab46d4ade6370
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.8 MB (713769219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e891c3a958287ab974c20629c3c873868a9e1312a42571b41e24ff08a2e93bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 May 2021 12:29:57 GMT
ADD file:57e6f432b1329c286e596ded8065bebdfc70a87fae91dd79bd805363ef008e5d in / 
# Thu, 27 May 2021 12:29:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:59 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:00 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:31:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 May 2021 20:31:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:32:20 GMT
ENV JAVA_VERSION=jdk-11.0.11+9
# Thu, 27 May 2021 20:32:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4966b0df9406b7041e14316e04c9579806832fafa02c5d3bd1842163b7f2353a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.11_9.tar.gz';          ;;        armhf|armv7l)          ESUM='2d7aba0b9ea287145ad437d4b3035fc84f7508e78c6fec99be4ff59fe1b6fc0d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.11_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='945b114bd0a617d742653ac1ae89d35384bf89389046a44681109cf8e4f4af91';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.11_9.tar.gz';          ;;        s390x)          ESUM='5d81979d27d9d8b3ed5bca1a91fc899cbbfb3d907f445ee7329628105e92f52c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.11_9.tar.gz';          ;;        amd64|x86_64)          ESUM='e99b98f851541202ab64401594901e583b764e368814320eba442095251e78cb';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 27 May 2021 20:32:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 20:32:29 GMT
CMD ["jshell"]
# Fri, 28 May 2021 14:25:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 28 May 2021 14:25:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 14:25:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 28 May 2021 14:25:01 GMT
WORKDIR /usr/local/tomcat
# Fri, 28 May 2021 14:25:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 28 May 2021 14:25:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 17 Jun 2021 00:25:18 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 17 Jun 2021 00:25:18 GMT
ENV TOMCAT_MAJOR=8
# Thu, 17 Jun 2021 00:25:19 GMT
ENV TOMCAT_VERSION=8.5.68
# Thu, 17 Jun 2021 00:25:19 GMT
ENV TOMCAT_SHA512=673f8d295d6f6b8e53b30c9c81989a3586341f9660f00e61a131153f54f0ce9d41bf8f49960ef477d3ec81610e1c75c1684c8676e9ebe5015486334c443d82e5
# Thu, 17 Jun 2021 00:25:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if wget -O "$f" "$distUrl" --progress=dot:giga && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 17 Jun 2021 00:25:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 17 Jun 2021 00:25:53 GMT
EXPOSE 8080
# Thu, 17 Jun 2021 00:25:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 17 Jun 2021 01:20:27 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Thu, 17 Jun 2021 01:21:00 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 01:21:01 GMT
ENV XWIKI_VERSION=13.4
# Thu, 17 Jun 2021 01:21:01 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/13.4
# Thu, 17 Jun 2021 01:21:01 GMT
ENV XWIKI_DOWNLOAD_SHA256=b9fcf40879203b6237fa1e88a45cec8cd681e5b1bf11949f03daa19b762d5765
# Thu, 17 Jun 2021 01:21:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Thu, 17 Jun 2021 01:21:41 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Thu, 17 Jun 2021 01:21:41 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Thu, 17 Jun 2021 01:21:41 GMT
COPY file:0ea4aba0ba32585cf3bff474898c52efb2cc5e16d470bc0badff3e2d86f04c8d in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Thu, 17 Jun 2021 01:21:42 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Thu, 17 Jun 2021 01:21:42 GMT
COPY file:a47c4dcd87c9dad97aff38c49188357e6193bcad50757e516cfb08a60d4de611 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Jun 2021 01:21:43 GMT
VOLUME [/usr/local/xwiki]
# Thu, 17 Jun 2021 01:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 01:21:43 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:80bc30679ac1fd798f3241208c14accd6a364cb8a6224d1127dfb1577d10554f`  
		Last Modified: Fri, 16 Apr 2021 08:25:26 GMT  
		Size: 27.1 MB (27144417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c937c19c2d76950fb80c27261cfc3ba1515cd1d701bf7c5b570ce4d14a7b9688`  
		Last Modified: Thu, 27 May 2021 12:31:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4ad27543765699a5feb74058f25dff93de058fe2ccca9bd8f3f419d4c3d0bd`  
		Last Modified: Thu, 27 May 2021 12:31:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3605b52bdc11515ca48a75175687bc98f47b3754856ca0a1e75b63d84e81a4`  
		Last Modified: Thu, 27 May 2021 20:35:28 GMT  
		Size: 15.9 MB (15893911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a437d042d396233fba393139d8eb134355745501d71e02e839fa0146b8fd81`  
		Last Modified: Thu, 27 May 2021 20:36:26 GMT  
		Size: 190.4 MB (190379266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba92a69b6e22a4dfa769567103669eaafab2341d320be49a6f811179dcce7200`  
		Last Modified: Fri, 28 May 2021 14:54:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd295ac56b42d1baad18fe6ca539d5bd9501a0f8236ba8305bc6c06d2c79d68`  
		Last Modified: Thu, 17 Jun 2021 00:50:53 GMT  
		Size: 11.7 MB (11705310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38b39dadbe83c56497d3132c518dec152e28334e70445306695927f5a685bc`  
		Last Modified: Thu, 17 Jun 2021 00:50:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af4a403b8ce07d4fd8a258b533a2b1d49bb402d3145cbe233539e85e5f7c01c`  
		Last Modified: Thu, 17 Jun 2021 01:23:40 GMT  
		Size: 164.4 MB (164371777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d438f7ccdcbfb4d3cf5c57aa26819738d1e13556a3ecb7a4310137c6188df3fa`  
		Last Modified: Thu, 17 Jun 2021 01:23:36 GMT  
		Size: 303.5 MB (303466291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d53b8e5abfc40b138ae726dce5382c9eb999838716307dc68e366cb0f04defd`  
		Last Modified: Thu, 17 Jun 2021 01:23:12 GMT  
		Size: 795.4 KB (795416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8d50c04ba03317363dbad40158e542a670985bfdc0572d1c1f1d4432c5d51d`  
		Last Modified: Thu, 17 Jun 2021 01:23:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3963f35ef065960df3e093521e0b0a4f08d66b6af9216783ac2ca307cbb979`  
		Last Modified: Thu, 17 Jun 2021 01:23:12 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099dc7aa7b3e98cb6783ca32b7e880e6a109dc923e305603340754ee7df211e7`  
		Last Modified: Thu, 17 Jun 2021 01:23:12 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25c293ba5d3d11445a6c55418a54f004dace163105f41ba9c08f66e5ea1fca5`  
		Last Modified: Thu, 17 Jun 2021 01:23:12 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
