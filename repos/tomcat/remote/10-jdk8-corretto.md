## `tomcat:10-jdk8-corretto`

```console
$ docker pull tomcat@sha256:a7d7cfc7b742d0ede11963f87d3dde03728ca1714ee76239f141b8b3e239c339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:7e41d72a761c16637f6517a30059fe7d7254fa9289eaf1c2b43555012f9dcebf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152877325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9142735286ed064349e45089d778f62cb7412190eb0e6c0b2af0957550db1724`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:44:18 GMT
ARG version=1.8.0_292.b10-1
# Thu, 29 Apr 2021 22:44:40 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 29 Apr 2021 22:44:41 GMT
ENV LANG=C.UTF-8
# Thu, 29 Apr 2021 22:44:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 29 Apr 2021 23:19:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Apr 2021 23:19:06 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Apr 2021 23:19:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Apr 2021 23:19:07 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Apr 2021 23:19:08 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Apr 2021 23:19:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Apr 2021 23:19:08 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 29 Apr 2021 23:19:08 GMT
ENV TOMCAT_MAJOR=10
# Thu, 29 Apr 2021 23:19:08 GMT
ENV TOMCAT_VERSION=10.0.5
# Thu, 29 Apr 2021 23:19:08 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Thu, 29 Apr 2021 23:19:44 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 29 Apr 2021 23:19:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 29 Apr 2021 23:19:46 GMT
EXPOSE 8080
# Thu, 29 Apr 2021 23:19:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ad23f29e4f8b17962a57374d7f01c83b5b4aee098e0f7722fe45c1121a4e0f`  
		Last Modified: Thu, 29 Apr 2021 22:46:42 GMT  
		Size: 75.3 MB (75309606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194a88704b309722b3e4aa1f4f5a5d66e0f9a97eb434da9d1dd4c38986a22e83`  
		Last Modified: Thu, 29 Apr 2021 23:30:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb81488e76e4220e2230524e022740c7bab316077a3b0e7c3f1452d2edf303f`  
		Last Modified: Thu, 29 Apr 2021 23:30:50 GMT  
		Size: 15.6 MB (15620281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69553fba4f0c4b47cad70ed1f954c9c426755e2de0e4faa87aff8a51725b628c`  
		Last Modified: Thu, 29 Apr 2021 23:30:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9271375fe63eedd4164578c52cff68b8b1315ae3470e2bde6537d2c2a7987179
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138642267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8b9879c6f46c6f6668251d0fbda11121a287d684d3a0aee369ac79b2b05a0e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 29 Apr 2021 22:40:32 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 29 Apr 2021 22:40:37 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:58:29 GMT
ARG version=1.8.0_292.b10-1
# Thu, 29 Apr 2021 22:58:57 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 29 Apr 2021 22:58:59 GMT
ENV LANG=C.UTF-8
# Thu, 29 Apr 2021 22:58:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 29 Apr 2021 23:21:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 29 Apr 2021 23:21:48 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Apr 2021 23:21:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 29 Apr 2021 23:21:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 29 Apr 2021 23:21:52 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 29 Apr 2021 23:21:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 29 Apr 2021 23:21:54 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 29 Apr 2021 23:21:55 GMT
ENV TOMCAT_MAJOR=10
# Thu, 29 Apr 2021 23:21:56 GMT
ENV TOMCAT_VERSION=10.0.5
# Thu, 29 Apr 2021 23:21:57 GMT
ENV TOMCAT_SHA512=27271e17c8daf52503490c6657c992cc150cf2942e1b0179b738f34e9aa5e1aac3c7b947c67441d17294a8f1e772a00e38e30b2135372d6ee9d71207ac7261c3
# Thu, 29 Apr 2021 23:22:50 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 29 Apr 2021 23:22:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 29 Apr 2021 23:22:55 GMT
EXPOSE 8080
# Thu, 29 Apr 2021 23:22:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a33a1e1d6d4e2db68efcef0ab61a4e6e6292e0377438a5ef84ffbe0fcd44c0`  
		Last Modified: Thu, 29 Apr 2021 23:01:18 GMT  
		Size: 59.4 MB (59389877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe2e5190232c3a306e05401119ee8f86c18714717522c5497bddb550e919232`  
		Last Modified: Thu, 29 Apr 2021 23:36:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a4179e02ec979bd2e6bb2a86187fe98098c4c3ce5ad48f8efb326b51f1c4af`  
		Last Modified: Thu, 29 Apr 2021 23:36:11 GMT  
		Size: 15.6 MB (15592017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3556102a9905ee97aa88702cb592e55540d9485f2f2c76c9f32e3a0e6d8d7085`  
		Last Modified: Thu, 29 Apr 2021 23:36:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
