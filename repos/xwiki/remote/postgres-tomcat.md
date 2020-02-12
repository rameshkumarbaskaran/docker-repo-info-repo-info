## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:4dd50182dfa8f1aba7b6b63d58d5ae8f31dc076d72e1b62e18cd56adc7cbf55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f70802e99ad6172111d634b447d4518f63b046bab4db3848625939c0e297a595
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.1 MB (716076052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fbc06b6b7090716847ad4f6b3d88268574dcfe43a31daf3ee42cc899638b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Jan 2020 01:20:31 GMT
ADD file:08e718ed0796013f5957a1be7da3bef6225f3d82d8be0a86a7114e5caad50cbc in / 
# Thu, 16 Jan 2020 01:20:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 01:20:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:20:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:20:34 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 01:44:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2020 01:45:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Jan 2020 00:19:44 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Tue, 28 Jan 2020 00:19:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04b77f6754aed68528f39750c5cfd6a439190206aff216aa081d62a0e1a794fa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.6_10.tar.gz';          ;;        armhf)          ESUM='ab5b76203e54fe7a5221535f6f407efa43153de029a746f60af3cffb7cb5080b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.6_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9247f0271744188489b0dd628cab90e76ca1f22fa3bbcdebd9bfc4f140908df5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.6_10.tar.gz';          ;;        s390x)          ESUM='250fc79db2d6c70e655ff319e2db8ca205858bf82c9f30b040bda0c90cd9f583';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.6_10.tar.gz';          ;;        amd64|x86_64)          ESUM='330d19a2eaa07ed02757d7a785a77bab49f5ee710ea03b4ee2fa220ddd0feffc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 28 Jan 2020 00:19:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 00:19:56 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 02:10:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2020 02:10:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 02:10:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jan 2020 02:10:20 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2020 02:10:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:10:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2020 02:14:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 28 Jan 2020 02:14:03 GMT
ENV TOMCAT_MAJOR=8
# Tue, 11 Feb 2020 21:49:16 GMT
ENV TOMCAT_VERSION=8.5.51
# Tue, 11 Feb 2020 21:49:16 GMT
ENV TOMCAT_SHA512=bb9207d33d7b4408292186523f3556a3d1454ea172b4a6cde6e0028e2f7a5d9408615cb4ccf8d9fdb75a9f8ce227580f56f929a811eb24ef99e26f980e4bcb48
# Tue, 11 Feb 2020 21:49:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 11 Feb 2020 21:49:50 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Feb 2020 21:49:50 GMT
EXPOSE 8080
# Tue, 11 Feb 2020 21:49:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Feb 2020 22:18:38 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 11 Feb 2020 22:22:07 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Feb 2020 22:24:22 GMT
ENV XWIKI_VERSION=12.0
# Tue, 11 Feb 2020 22:24:22 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.0
# Tue, 11 Feb 2020 22:24:22 GMT
ENV XWIKI_DOWNLOAD_SHA256=da57110002c76001dc9ca16eb217ea0d6c81a2b4bd3d8ad26a6fc5efe96c776d
# Tue, 11 Feb 2020 22:25:08 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Feb 2020 22:25:09 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Feb 2020 22:25:09 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Feb 2020 22:25:09 GMT
COPY file:bd68ae28ec068b0f89a2e05a10b1098af3b375c97a69f9255831e8fa6e87f773 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Feb 2020 22:25:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Feb 2020 22:25:10 GMT
COPY file:1aeb90632849dc8f47315bba1c63b571b0f210b5f223333b3a494c471e4b9743 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Feb 2020 22:25:11 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Feb 2020 22:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2020 22:25:11 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5c939e3a4d1097af8d3292ad3a41d3caa846f6333b91f2dd22b972bc2d19c5b5`  
		Last Modified: Mon, 13 Jan 2020 13:21:09 GMT  
		Size: 26.7 MB (26690191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63719cdbe7ae254b453dba06fb446f583b503f2a2c15becc83f8c5bc7a705e0`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 35.4 KB (35366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a861ea6baff71b05cd577478984c3e62cf0177bf74468d0aca551f5fcb891c`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651c9d2d6c4f37c56a221259e033e7e2353b698139c2ff950623ca28d64a9837`  
		Last Modified: Thu, 16 Jan 2020 01:21:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e1a6e1ff3c935882f4005a6063541af139f9244769187488ef236e2052ce19`  
		Last Modified: Thu, 16 Jan 2020 01:48:24 GMT  
		Size: 13.3 MB (13323265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193adb2bcec5d5aa437d8a278e43e54ea30b31766030833d2d708455a20d5811`  
		Last Modified: Tue, 28 Jan 2020 00:23:13 GMT  
		Size: 198.1 MB (198075301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c211b413c8c6171e531907145d75543ba85753c7b3c1e9b010ef90f3e9cc18`  
		Last Modified: Tue, 28 Jan 2020 02:19:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2207fadffed2cc0b3e4d474f40da68393122d869440cec492504f35ae48ed169`  
		Last Modified: Tue, 11 Feb 2020 21:59:23 GMT  
		Size: 11.3 MB (11323546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13355fd0d2c11988f275950f00db94ccb268c8894444d728025f995e555d8d86`  
		Last Modified: Tue, 11 Feb 2020 21:59:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df456a6f976d7426d15d087afd3b6c680d1f0191c5745c2ce1d0adcfb2fcc8c`  
		Last Modified: Tue, 11 Feb 2020 22:26:39 GMT  
		Size: 179.6 MB (179562154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd260bd61bb85af272c9235d4168f3db6bfd74d9af2752f5212ee4ec74d4174`  
		Last Modified: Tue, 11 Feb 2020 22:27:32 GMT  
		Size: 286.4 MB (286435482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd31a8c8d043d4cdabf9d4e4481c9ac2948b8339457dd40dc3b351d9c28d895`  
		Last Modified: Tue, 11 Feb 2020 22:27:14 GMT  
		Size: 618.9 KB (618866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4249973ac5cedaf005abdaad940c8fb8cc9c7bd5c2b86066b75bb4a926ee0c29`  
		Last Modified: Tue, 11 Feb 2020 22:27:13 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7033f483d97b7bffba34071db3e415bfe7e8ecbcb8473e5678b7db896e172f2`  
		Last Modified: Tue, 11 Feb 2020 22:27:14 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cafe868b8babd62b00a5f327b389e6825101b43de588c517d3b73ac51110205`  
		Last Modified: Tue, 11 Feb 2020 22:27:13 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ce9a9a437bc37056dd90ba3628fc6045d85be0147551502108ffd96b67a4a1`  
		Last Modified: Tue, 11 Feb 2020 22:27:13 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:26560cfe4e476ede7f159df66113a16ae6de0cb29e42143904ffb5e118c2267a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.0 MB (706995909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6288f884c47722b28f12e89b05fe04a4c85214c6504d2ea4cd7e39f0b3cb8a19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Jan 2020 00:40:35 GMT
ADD file:868e3a7e9028dcf197b28fa33d45b368b95d6a4e98cceba6bc9cf2c85daa554a in / 
# Thu, 16 Jan 2020 00:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 16 Jan 2020 00:40:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 00:40:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 00:40:51 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 00:59:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Jan 2020 01:01:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Mon, 27 Jan 2020 23:40:14 GMT
ENV JAVA_VERSION=jdk-11.0.6+10
# Mon, 27 Jan 2020 23:40:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04b77f6754aed68528f39750c5cfd6a439190206aff216aa081d62a0e1a794fa';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.6_10.tar.gz';          ;;        armhf)          ESUM='ab5b76203e54fe7a5221535f6f407efa43153de029a746f60af3cffb7cb5080b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.6_10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9247f0271744188489b0dd628cab90e76ca1f22fa3bbcdebd9bfc4f140908df5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.6_10.tar.gz';          ;;        s390x)          ESUM='250fc79db2d6c70e655ff319e2db8ca205858bf82c9f30b040bda0c90cd9f583';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.6_10.tar.gz';          ;;        amd64|x86_64)          ESUM='330d19a2eaa07ed02757d7a785a77bab49f5ee710ea03b4ee2fa220ddd0feffc';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 27 Jan 2020 23:40:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Jan 2020 23:40:41 GMT
CMD ["jshell"]
# Wed, 29 Jan 2020 20:47:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Jan 2020 20:47:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2020 20:47:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Jan 2020 20:47:28 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Jan 2020 20:47:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Jan 2020 20:47:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Jan 2020 20:51:13 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 29 Jan 2020 20:51:14 GMT
ENV TOMCAT_MAJOR=8
# Tue, 11 Feb 2020 22:04:53 GMT
ENV TOMCAT_VERSION=8.5.51
# Tue, 11 Feb 2020 22:04:54 GMT
ENV TOMCAT_SHA512=bb9207d33d7b4408292186523f3556a3d1454ea172b4a6cde6e0028e2f7a5d9408615cb4ccf8d9fdb75a9f8ce227580f56f929a811eb24ef99e26f980e4bcb48
# Tue, 11 Feb 2020 22:05:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Tue, 11 Feb 2020 22:05:56 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 11 Feb 2020 22:05:57 GMT
EXPOSE 8080
# Tue, 11 Feb 2020 22:05:57 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Feb 2020 22:31:25 GMT
MAINTAINER Vincent Massol <vincent@massol.net>
# Tue, 11 Feb 2020 22:32:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Tue, 11 Feb 2020 22:33:56 GMT
ENV XWIKI_VERSION=12.0
# Tue, 11 Feb 2020 22:33:57 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/12.0
# Tue, 11 Feb 2020 22:33:57 GMT
ENV XWIKI_DOWNLOAD_SHA256=da57110002c76001dc9ca16eb217ea0d6c81a2b4bd3d8ad26a6fc5efe96c776d
# Tue, 11 Feb 2020 22:34:30 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Tue, 11 Feb 2020 22:34:33 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Tue, 11 Feb 2020 22:34:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Tue, 11 Feb 2020 22:34:34 GMT
COPY file:bd68ae28ec068b0f89a2e05a10b1098af3b375c97a69f9255831e8fa6e87f773 in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Tue, 11 Feb 2020 22:34:36 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Tue, 11 Feb 2020 22:34:36 GMT
COPY file:1aeb90632849dc8f47315bba1c63b571b0f210b5f223333b3a494c471e4b9743 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 11 Feb 2020 22:34:37 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Feb 2020 22:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2020 22:34:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:fbdcf4a939bd956d7cd2fd21e684e4e3ca5d9ef60886808b0345bbc2c3b6f18a`  
		Last Modified: Mon, 13 Jan 2020 15:33:17 GMT  
		Size: 23.7 MB (23719499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3463cc4abcf9c532fc6f5ad6b6780de967e7a0cadf865674d6dbbeefc9eb349`  
		Last Modified: Thu, 16 Jan 2020 00:43:21 GMT  
		Size: 35.2 KB (35201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf5b492942e45d969f49bd9465095c547ddfa152607f6b5ce9d924fe647f8f8`  
		Last Modified: Thu, 16 Jan 2020 00:43:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7799262edbd86d40847575d269f6f03068dba731519911195aa384ec02ae9702`  
		Last Modified: Thu, 16 Jan 2020 00:43:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd789495d7e9a60c135ebd6aebd36b8364d4f22c79d3a42a45be167c49cd2f09`  
		Last Modified: Thu, 16 Jan 2020 01:03:43 GMT  
		Size: 12.7 MB (12732288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4be551adfa9765e3a29fc6a9898b9fe0f2765b9d188522ec7d784b31e065c9`  
		Last Modified: Mon, 27 Jan 2020 23:43:24 GMT  
		Size: 196.3 MB (196252927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0214235fb98c31ed16218265e9b4a1f31c84c02cd25dbaa37f3ad023d2028e`  
		Last Modified: Wed, 29 Jan 2020 20:56:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08189549b3474fe1d82ed87336daa2434d0be937c3c9eb757930a8bff947b110`  
		Last Modified: Tue, 11 Feb 2020 22:15:15 GMT  
		Size: 11.3 MB (11328042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008fbab0067321b7b827f887a5e0851337c2ccb2d82f100a72787989b4ebd4d7`  
		Last Modified: Tue, 11 Feb 2020 22:15:13 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df09a586dda0faa4eafe4c2515e5af37aeeae51cc2ba653f7054d8b8970b1448`  
		Last Modified: Tue, 11 Feb 2020 22:35:38 GMT  
		Size: 175.9 MB (175861393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c2e7ddb138c28fb335f9edeba881c1526872c50776ec400cc67603aa044041`  
		Last Modified: Tue, 11 Feb 2020 22:36:23 GMT  
		Size: 286.4 MB (286435725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eacb544a05c4bb1418f8c70d7734e05b61f407e2e8c79437b36ad3690c1d83`  
		Last Modified: Tue, 11 Feb 2020 22:35:49 GMT  
		Size: 618.9 KB (618861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8011352fa9c3c97a5e483ba2dd1aee5d817e3821bb6bffb955c2504c96317ee`  
		Last Modified: Tue, 11 Feb 2020 22:35:49 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8f2535097b628047ff230b5ca1225fcd9418831556f7dab2fb182fdff6446e`  
		Last Modified: Tue, 11 Feb 2020 22:35:49 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbf327804a7c965ec346035350e669b9f42c06a9c0e064173e438f130deb623`  
		Last Modified: Tue, 11 Feb 2020 22:35:49 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129d7deba6cb55accc70465feed1dd6dd163387aca78a1e8f14e6969e10eb77f`  
		Last Modified: Tue, 11 Feb 2020 22:35:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
