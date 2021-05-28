## `tomcat:10-jdk8-corretto`

```console
$ docker pull tomcat@sha256:1f31c2ccfe069a95961fb47a08bae456463c8bcb93e96c4a8873e819fab9a63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jdk8-corretto` - linux; amd64

```console
$ docker pull tomcat@sha256:e6811b90a2ce118e28de6e9c993f1ca67d7eed1ade9db2c57842f2b77305ed17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152872759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fddb42569edaf89d3f6aa2a7dd261f48fd01921727f01140fa8abd975f6c9e`
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
# Thu, 13 May 2021 18:35:47 GMT
ENV TOMCAT_VERSION=10.0.6
# Thu, 13 May 2021 18:35:47 GMT
ENV TOMCAT_SHA512=3d39b086b6fec86e354aa4837b1b55e6c16bfd5ec985a82a5dd71f928e3fab5370b2964a5a1098cfe05ca63d031f198773b18b1f8c7c6cdee6c90aa0644fb2f2
# Thu, 13 May 2021 18:36:21 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 13 May 2021 18:36:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 13 May 2021 18:36:24 GMT
EXPOSE 8080
# Thu, 13 May 2021 18:36:24 GMT
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
	-	`sha256:a1a6fa94ab8ac8b38d23baf991ee4f43df398025714b633416da711fe594bbfe`  
		Last Modified: Thu, 13 May 2021 19:03:05 GMT  
		Size: 15.6 MB (15615717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3391df184bdb333d138de3b3c8222776ae2a72a25ae3de65a0c3818fe89e23`  
		Last Modified: Thu, 13 May 2021 19:03:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3922ce8cccf46df05d292516e8825787cc8e9609eeeffa97e1f1b425814fede8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147358122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949961e0dc6fe7d1ccbfd8315d55703f86848cedb4a951fcca9fc17c77dac323`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 29 Apr 2021 22:40:32 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 29 Apr 2021 22:40:37 GMT
CMD ["/bin/bash"]
# Fri, 28 May 2021 12:43:12 GMT
ARG version=1.8.0_292.b10-1
# Fri, 28 May 2021 12:43:32 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 28 May 2021 12:43:32 GMT
ENV LANG=C.UTF-8
# Fri, 28 May 2021 12:43:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 28 May 2021 14:28:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 28 May 2021 14:28:02 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 14:28:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 28 May 2021 14:28:03 GMT
WORKDIR /usr/local/tomcat
# Fri, 28 May 2021 14:28:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 28 May 2021 14:28:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 28 May 2021 14:28:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 28 May 2021 14:28:04 GMT
ENV TOMCAT_MAJOR=10
# Fri, 28 May 2021 14:28:04 GMT
ENV TOMCAT_VERSION=10.0.6
# Fri, 28 May 2021 14:28:04 GMT
ENV TOMCAT_SHA512=3d39b086b6fec86e354aa4837b1b55e6c16bfd5ec985a82a5dd71f928e3fab5370b2964a5a1098cfe05ca63d031f198773b18b1f8c7c6cdee6c90aa0644fb2f2
# Fri, 28 May 2021 14:28:38 GMT
RUN set -eux; 		if ! command -v yumdb > /dev/null; then 		yum install -y yum-utils; 		yumdb set reason dep yum-utils; 	fi; 	if [ -f /etc/oracle-release ]; then 		yumdb set reason user filesystem; 	fi; 	_yum_install_temporary() { ( set -eu +x; 		local pkg todo=''; 		for pkg; do 			if ! rpm --query "$pkg" > /dev/null 2>&1; then 				todo="$todo $pkg"; 			fi; 		done; 		if [ -n "$todo" ]; then 			set -x; 			yum install -y $todo; 			yumdb set reason dep $todo; 		fi; 	) }; 	_yum_install_temporary gzip tar; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	_yum_install_temporary 		apr-devel 		gcc 		make 		openssl-devel 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		deps="$( 		find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 			| awk '/=>/ && $(NF-1) != "=>" { print $(NF-1) }' 			| xargs -rt readlink -e 			| sort -u 			| xargs -rt rpm --query --whatprovides 			| sort -u 	)"; 	[ -z "$deps" ] || yumdb set reason user $deps; 		yum autoremove -y; 	yum clean all; 	rm -rf /var/cache/yum; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Fri, 28 May 2021 14:28:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 28 May 2021 14:28:40 GMT
EXPOSE 8080
# Fri, 28 May 2021 14:28:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9de775f47e3020f7c8c1f5ef652acb5fdec9f3217fc42bd8b1116d4d9815f7`  
		Last Modified: Fri, 28 May 2021 12:45:29 GMT  
		Size: 59.4 MB (59390200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e668514db233fd5aa9178507f44192470b26d8ac977207e47e64a318d83d17bd`  
		Last Modified: Fri, 28 May 2021 14:56:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0198d3d0e3f6962a0c0c62126c913ba840e0a636e488de348e77ed98d15414d`  
		Last Modified: Fri, 28 May 2021 14:56:11 GMT  
		Size: 24.3 MB (24307550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c0f2325070d0f0a8a51fbd8d93af57c2bb3ee7d80f38fc2691dd60dc69a92a`  
		Last Modified: Fri, 28 May 2021 14:56:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
