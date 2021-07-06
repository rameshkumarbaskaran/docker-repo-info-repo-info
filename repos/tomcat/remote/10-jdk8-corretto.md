## `tomcat:10-jdk8-corretto`

```console
$ docker pull tomcat@sha256:59687c84df0c5484773e06cf7213567fb8aa13c8f79438faf8ee675f92f74f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:4789ab1969d43f30c2d9f7222d89c9703eb70f4626d4c6140c795e6c948e86ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163431136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5c1cd10c572354388586f923cbc57c289e180ce49ec6e28bd381c31f3ffa78`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 25 Jun 2021 17:19:49 GMT
ADD file:dc851f79dbfc66e08196951041e8c856c41a3cc24b8bc27e66722210d51e87cf in / 
# Fri, 25 Jun 2021 17:19:50 GMT
CMD ["/bin/bash"]
# Fri, 25 Jun 2021 18:02:23 GMT
ARG version=1.8.0_292.b10-1
# Fri, 25 Jun 2021 18:02:42 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 25 Jun 2021 18:02:42 GMT
ENV LANG=C.UTF-8
# Fri, 25 Jun 2021 18:02:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 25 Jun 2021 18:29:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 25 Jun 2021 18:29:05 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Jun 2021 18:29:06 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 25 Jun 2021 18:29:07 GMT
WORKDIR /usr/local/tomcat
# Fri, 25 Jun 2021 18:29:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 25 Jun 2021 18:29:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 25 Jun 2021 18:29:07 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 25 Jun 2021 18:29:07 GMT
ENV TOMCAT_MAJOR=10
# Fri, 02 Jul 2021 19:55:36 GMT
ENV TOMCAT_VERSION=10.0.8
# Fri, 02 Jul 2021 19:55:36 GMT
ENV TOMCAT_SHA512=188fb84f86ae5f5b88ddbe6f38c8dec6ec733a5ef166c5875e1c6728701e49f9d01f494a419186fd8da80ab21576e0a056382d59f7fe17695c4ec63aaf543897
# Tue, 06 Jul 2021 20:28:59 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl11-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 06 Jul 2021 20:29:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 06 Jul 2021 20:29:01 GMT
EXPOSE 8080
# Tue, 06 Jul 2021 20:29:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:85ee02fe1a09b50ffaacc1e7482fdbb3e80c577256420503196fc549b9e4ef29`  
		Last Modified: Fri, 25 Jun 2021 00:50:03 GMT  
		Size: 61.9 MB (61940054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f840dce53cea5e67f9e53e509a2e79ca3ffe6d479594453d85db9940e7634b7e`  
		Last Modified: Fri, 25 Jun 2021 18:04:34 GMT  
		Size: 75.3 MB (75279963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80adf2308340f879f657f59608105636355f0f845909bd899d27010d2e1c7874`  
		Last Modified: Fri, 25 Jun 2021 18:44:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cef6922ff0bc5ec5bc34d38541e6b585e8457e6b026afe53db5617f0f61cbd`  
		Last Modified: Tue, 06 Jul 2021 20:41:30 GMT  
		Size: 26.2 MB (26210814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5f14b600678e819f93e531f8c95465957033cde822e84a77b2e14e117b882`  
		Last Modified: Tue, 06 Jul 2021 20:41:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cd43122e98f77b3647d7b6c98a94f5f8ed7ae53ec4206808c52d685e17959d6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148086644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbea2d7f2ea8d202ffc78a0676404c7e32335d65b7646ab4b01cfe336b49fee9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 25 Jun 2021 17:39:34 GMT
ADD file:d4d6f883cd1ba97522a617c6f7b0125b0a82e12101c702ca57ac48063f0e3707 in / 
# Fri, 25 Jun 2021 17:39:35 GMT
CMD ["/bin/bash"]
# Fri, 25 Jun 2021 17:56:52 GMT
ARG version=1.8.0_292.b10-1
# Fri, 25 Jun 2021 17:57:09 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && if [[ `arch` == 'aarch64' ]]; then version=1.8.0_292.b10-2; fi     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 25 Jun 2021 17:57:10 GMT
ENV LANG=C.UTF-8
# Fri, 25 Jun 2021 17:57:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 25 Jun 2021 18:19:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 25 Jun 2021 18:19:02 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Jun 2021 18:19:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 25 Jun 2021 18:19:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 25 Jun 2021 18:19:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 25 Jun 2021 18:19:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 25 Jun 2021 18:19:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 25 Jun 2021 18:19:04 GMT
ENV TOMCAT_MAJOR=10
# Fri, 02 Jul 2021 20:00:58 GMT
ENV TOMCAT_VERSION=10.0.8
# Fri, 02 Jul 2021 20:00:58 GMT
ENV TOMCAT_SHA512=188fb84f86ae5f5b88ddbe6f38c8dec6ec733a5ef166c5875e1c6728701e49f9d01f494a419186fd8da80ab21576e0a056382d59f7fe17695c4ec63aaf543897
# Fri, 02 Jul 2021 20:01:34 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 02 Jul 2021 20:01:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 02 Jul 2021 20:01:36 GMT
EXPOSE 8080
# Fri, 02 Jul 2021 20:01:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b19e557e673ca4274c5ee576b0d897c535e4329a596ac20b3ff70225b734a125`  
		Last Modified: Fri, 25 Jun 2021 00:50:31 GMT  
		Size: 63.6 MB (63564395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b327425bd466dbcb48303d6037d16224d314f717ad03a2f37dbc70ee8147222a`  
		Last Modified: Fri, 25 Jun 2021 17:59:07 GMT  
		Size: 59.4 MB (59398104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25b085de6d961682a9c48f60cd8b6104d5082a394c91730acadfc695d67554e`  
		Last Modified: Fri, 25 Jun 2021 18:37:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f857d4a55fdb9fb84eee943179beae6a9f1469d9fcf76cd4156083589f493`  
		Last Modified: Fri, 02 Jul 2021 20:34:35 GMT  
		Size: 25.1 MB (25123842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82273b5f853f95594614adfeb6e4a198675a4377ecca686c13164fc58e345d3`  
		Last Modified: Fri, 02 Jul 2021 20:34:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
