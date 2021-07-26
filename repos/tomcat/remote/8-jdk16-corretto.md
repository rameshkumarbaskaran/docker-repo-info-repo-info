## `tomcat:8-jdk16-corretto`

```console
$ docker pull tomcat@sha256:270d190ed2ecf16b1e46dd7831594c9841759a7e0bddf81eafe7f8acd35f6b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jdk16-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:e9d2e56400c0159cc39f57eefca0cdfd077437148866e0d43210d71e3902bea5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237904312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136e11356a4f6ff32020366c5fc973b3a92c535328cf315434d786e9b89763f6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Jul 2021 18:19:40 GMT
ARG version=16.0.2.7-1
# Mon, 26 Jul 2021 18:20:02 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Jul 2021 18:20:03 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:20:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 26 Jul 2021 18:59:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Jul 2021 18:59:58 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:59:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Jul 2021 18:59:59 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Jul 2021 18:59:59 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Jul 2021 18:59:59 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Jul 2021 19:03:05 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 26 Jul 2021 19:03:05 GMT
ENV TOMCAT_MAJOR=8
# Mon, 26 Jul 2021 19:03:06 GMT
ENV TOMCAT_VERSION=8.5.69
# Mon, 26 Jul 2021 19:03:06 GMT
ENV TOMCAT_SHA512=3ce092c7b89a12904681f23c9c8a2517c13305b4beb783f7b1e85e947aaba4d2bfe8f954f9cefbe009f678557eeb552995f214d9e98c3f1be395822eb2582a1c
# Mon, 26 Jul 2021 19:03:56 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 26 Jul 2021 19:03:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Jul 2021 19:03:58 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 19:03:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aed8a232bf7a40fe973a4cd182928ebe6b7e9c09023452fcf7803138da37056`  
		Last Modified: Mon, 26 Jul 2021 18:21:41 GMT  
		Size: 160.0 MB (159978571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1c1a55d23c9787c2fb8b7df8072278df41d502873a23c338e68d5eb9bc0909`  
		Last Modified: Mon, 26 Jul 2021 19:08:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350643307fe8a0f99411dd1609ae7b15878c14d441f36b158b977463b0118ac1`  
		Last Modified: Mon, 26 Jul 2021 19:09:41 GMT  
		Size: 16.0 MB (15959433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85f8aa8d8922e991ea6dd00b05e35249efab7650f4c4c6bb3aec9fde98cc820`  
		Last Modified: Mon, 26 Jul 2021 19:09:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jdk16-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6db8726dc31aae2721973646d09e4491f8b8e329c4628a7336b180758f457c67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239427874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4fcec0c3265493bdfc3fef4a4317235fa97509158669a7ad09f805ff098a8d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Mon, 26 Jul 2021 17:39:46 GMT
ARG version=16.0.2.7-1
# Mon, 26 Jul 2021 17:40:14 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Jul 2021 17:40:14 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 17:40:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
# Mon, 26 Jul 2021 18:19:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Jul 2021 18:19:35 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:19:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Jul 2021 18:19:36 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Jul 2021 18:19:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Jul 2021 18:19:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Jul 2021 18:23:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 8B46CA49EF4837B8C7F292DAA54AD08EA7A0233C 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 26 Jul 2021 18:23:29 GMT
ENV TOMCAT_MAJOR=8
# Mon, 26 Jul 2021 18:23:30 GMT
ENV TOMCAT_VERSION=8.5.69
# Mon, 26 Jul 2021 18:23:30 GMT
ENV TOMCAT_SHA512=3ce092c7b89a12904681f23c9c8a2517c13305b4beb783f7b1e85e947aaba4d2bfe8f954f9cefbe009f678557eeb552995f214d9e98c3f1be395822eb2582a1c
# Mon, 26 Jul 2021 18:24:10 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Mon, 26 Jul 2021 18:24:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Jul 2021 18:24:12 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 18:24:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d6c00fa286044c267ce902d9051a1210ba685bdeb2e004a2325ab4b854a22e`  
		Last Modified: Mon, 26 Jul 2021 17:41:26 GMT  
		Size: 159.9 MB (159942469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff43604698c5634e177f2b1ac2e501e92e2f033b42b3666fb6ede96d14749e47`  
		Last Modified: Mon, 26 Jul 2021 18:32:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baee5aea98b7d9933284eeb151241befaaa6e050a5a8d2581d95fa9d7dfb7e7`  
		Last Modified: Mon, 26 Jul 2021 18:34:47 GMT  
		Size: 15.9 MB (15917210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3259517fc2ae6a326270fe2dd8354e067eedc78cbf53ab1b80a1922aa815f744`  
		Last Modified: Mon, 26 Jul 2021 18:34:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
