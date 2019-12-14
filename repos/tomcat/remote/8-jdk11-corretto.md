## `tomcat:8-jdk11-corretto`

```console
$ docker pull tomcat@sha256:f8fc6058f0ea5e2e0c3d8c5a05f4a2566aa77582dbf03e44f57bd5c61d350fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jdk11-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:2013f2ccd663b0bf43f8a9a200166d0d9ff0cb12b3688819c22f4a61a6c1e2ca
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282458491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba875cbbde3be9fd05232df645aa7ece28eadaa300c5c5b07b43b6f8add5c530`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 22 Oct 2019 01:28:31 GMT
ADD file:7b0629b865f6a424605580d655d74b7e23b2f3518177b7df4559597a1a87a4c7 in / 
# Tue, 22 Oct 2019 01:28:31 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2019 01:47:15 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Tue, 22 Oct 2019 01:47:15 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Tue, 22 Oct 2019 01:47:15 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Tue, 22 Oct 2019 01:47:15 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Tue, 22 Oct 2019 01:47:16 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Tue, 22 Oct 2019 01:47:16 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Tue, 22 Oct 2019 01:47:41 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 22 Oct 2019 01:47:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 22 Oct 2019 02:06:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Oct 2019 02:06:55 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2019 02:06:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Oct 2019 02:06:56 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Oct 2019 02:06:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Oct 2019 02:06:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Oct 2019 02:12:17 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Oct 2019 02:12:17 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Dec 2019 23:50:31 GMT
ENV TOMCAT_VERSION=8.5.50
# Fri, 13 Dec 2019 23:50:32 GMT
ENV TOMCAT_SHA512=ffca86027d298ba107c7d01c779318c05b61ba48767cc5967ee6ce5a88271bb6ec8eed60708d45453f30eeedddcaedd1a369d6df1b49eea2cd14fa40832cfb90
# Fri, 13 Dec 2019 23:52:14 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Fri, 13 Dec 2019 23:52:17 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Dec 2019 23:52:17 GMT
EXPOSE 8080
# Fri, 13 Dec 2019 23:52:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:17282fad1a5eb72a6f1f7a05102a1e3474fd2193cd013d44845d43c013cd594b`  
		Last Modified: Tue, 22 Oct 2019 01:30:07 GMT  
		Size: 61.7 MB (61659797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2ecadfcc76dac14ddf0377e0339d89d93b357bf384289513a8f446943005ec`  
		Last Modified: Tue, 22 Oct 2019 01:48:47 GMT  
		Size: 197.2 MB (197209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbdff1975716e19e94153a2d73563fb191b206ec60c480ad42769d6a71db34`  
		Last Modified: Tue, 22 Oct 2019 02:21:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4269002c1bdb50e0a44f0660fc10c58f9b5302def1e65c0bd7485da39e73e623`  
		Last Modified: Sat, 14 Dec 2019 00:00:01 GMT  
		Size: 23.6 MB (23589180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe8b597f63b75b6a060b1499e526c38e86bfc898815d5ea5b4833718472a024`  
		Last Modified: Fri, 13 Dec 2019 23:59:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:d7970a7d3fb41eb4fd377ea72849dea1ed4a422a30188fe7c8cabd5842528407
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282196538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b942ac69bc71266d6cbee6cc80974c5de4c8342ef5d0b0249032c62637fcff7c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 22 Oct 2019 01:09:30 GMT
ADD file:01531581542d07e40e72ce8cd4e0ec4407d5fda4da394ac63e13b78513b8dbe8 in / 
# Tue, 22 Oct 2019 01:09:33 GMT
CMD ["/bin/bash"]
# Tue, 22 Oct 2019 01:27:13 GMT
ARG rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
# Tue, 22 Oct 2019 01:27:14 GMT
ARG path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Tue, 22 Oct 2019 01:27:15 GMT
ARG key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Tue, 22 Oct 2019 01:27:17 GMT
ARG rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm
# Tue, 22 Oct 2019 01:27:19 GMT
ARG path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1
# Tue, 22 Oct 2019 01:27:20 GMT
ARG key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0
# Tue, 22 Oct 2019 01:27:51 GMT
# ARGS: key_aarch64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 key_x64=13817E35D6AA26BB2D85267712EABAC5209DDBC0 path_aarch64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 path_x64=https://d3pxv6yz143wms.cloudfront.net/11.0.5.10.1 rpm_aarch64=java-11-amazon-corretto-devel-11.0.5.10-1.aarch64.rpm rpm_x64=java-11-amazon-corretto-devel-11.0.5.10-1.x86_64.rpm
RUN set -eux;     case "$(uname -p)" in         x86_64) rpm=$rpm_x64; path=$path_x64; key=$key_x64 ;;         aarch64) rpm=$rpm_aarch64; path=$path_aarch64; key=$key_aarch64 ;;         *) echo >&2 "Unsupported architecture $(uname -p)."; exit 1 ;;     esac;         curl -O $path/$rpm     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key     && gpg --armor --export $key > corretto.asc     && rpm --import corretto.asc     && rpm -K $rpm     && rpm -i $rpm     && rm -r $GNUPGHOME corretto.asc $rpm     && yum install -y fontconfig     && yum clean all
# Tue, 22 Oct 2019 01:27:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 22 Oct 2019 01:48:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 22 Oct 2019 01:48:37 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 22 Oct 2019 01:48:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 22 Oct 2019 01:48:40 GMT
WORKDIR /usr/local/tomcat
# Tue, 22 Oct 2019 01:48:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 22 Oct 2019 01:48:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 22 Oct 2019 01:53:04 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Tue, 22 Oct 2019 01:53:05 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Dec 2019 23:59:50 GMT
ENV TOMCAT_VERSION=8.5.50
# Fri, 13 Dec 2019 23:59:51 GMT
ENV TOMCAT_SHA512=ffca86027d298ba107c7d01c779318c05b61ba48767cc5967ee6ce5a88271bb6ec8eed60708d45453f30eeedddcaedd1a369d6df1b49eea2cd14fa40832cfb90
# Sat, 14 Dec 2019 00:01:38 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if curl -fL -o "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| sort -u 			| xargs -r rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Sat, 14 Dec 2019 00:01:44 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 14 Dec 2019 00:01:45 GMT
EXPOSE 8080
# Sat, 14 Dec 2019 00:01:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:502dfb788f6ca3e66517bd9090f7b27b9bd7e455e2ce1e6b1df693451492d769`  
		Last Modified: Tue, 22 Oct 2019 01:10:26 GMT  
		Size: 62.8 MB (62831385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8ed3b958887637d4a889f96a4f6869df0f96a66e942aec7b35b74cc78ec8f`  
		Last Modified: Tue, 22 Oct 2019 01:29:08 GMT  
		Size: 195.4 MB (195447181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0a6542ee927d1044c9015e631786ab86eb5f4b7813b9d703d1499a14cc6dcb`  
		Last Modified: Tue, 22 Oct 2019 01:58:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72c55e7d1a5da194bc43a87e5ff3078e2640e7b063d99c62d4d8f445a96be70`  
		Last Modified: Sat, 14 Dec 2019 00:05:54 GMT  
		Size: 23.9 MB (23917637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73cf89d9e5838df9e833e06ce744f26f393c5be50774da66c631806d74e954`  
		Last Modified: Sat, 14 Dec 2019 00:05:48 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
