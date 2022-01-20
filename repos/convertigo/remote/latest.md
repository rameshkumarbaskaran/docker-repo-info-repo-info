## `convertigo:latest`

```console
$ docker pull convertigo@sha256:5701f787c7c7f886a7f333e965518d602613e058ab5f87ff88c8cdd11daa7baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:a9897f38143ede610c349f9d11f96031d2ffe30b00c8414cf8007b1adebe3fd6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.0 MB (439985959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98c9e5abffbe0c391506a2eac19dd2372a095a2c45dc22233b29a396764045`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:32 GMT
ADD file:c03517c5ddbed4053165bfdf984b27a006fb5f533ca80b5798232d96df221440 in / 
# Tue, 21 Dec 2021 01:22:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:51:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:51:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 23:00:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 23:00:34 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 23:00:34 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 20:43:18 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 19 Jan 2022 20:43:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 19 Jan 2022 20:43:35 GMT
CMD ["jshell"]
# Thu, 20 Jan 2022 00:50:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 20 Jan 2022 00:50:33 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Jan 2022 00:50:34 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 20 Jan 2022 00:50:34 GMT
WORKDIR /usr/local/tomcat
# Thu, 20 Jan 2022 00:50:34 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 00:50:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 20 Jan 2022 01:01:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 20 Jan 2022 01:01:03 GMT
ENV TOMCAT_MAJOR=9
# Thu, 20 Jan 2022 01:01:03 GMT
ENV TOMCAT_VERSION=9.0.56
# Thu, 20 Jan 2022 01:01:03 GMT
ENV TOMCAT_SHA512=b4c2c85891e84f0fbd8fec889ef0890d68a2bfa53eb31d4d39fcf5758aa483694af7ac27533ea4bc3fc3fdae56f2fa9c018d4acf872574c0ec5e37bb443599ce
# Thu, 20 Jan 2022 01:01:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Thu, 20 Jan 2022 01:01:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 20 Jan 2022 01:01:29 GMT
EXPOSE 8080
# Thu, 20 Jan 2022 01:01:29 GMT
CMD ["catalina.sh" "run"]
# Thu, 20 Jan 2022 05:25:44 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 20 Jan 2022 05:25:44 GMT
ENV SWT_GTK3=0
# Thu, 20 Jan 2022 05:25:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 20 Jan 2022 05:25:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 20 Jan 2022 05:25:45 GMT
WORKDIR /usr/local/tomcat
# Thu, 20 Jan 2022 05:25:58 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     unzip   && rm -rf /var/lib/apt/lists/*
# Thu, 20 Jan 2022 05:25:58 GMT
ENV GOSU_VERSION=1.12
# Thu, 20 Jan 2022 05:25:59 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 20 Jan 2022 05:25:59 GMT
ENV TINI_VERSION=0.19.0
# Thu, 20 Jan 2022 05:25:59 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Thu, 20 Jan 2022 05:26:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture | awk -F- '{ print $NF }')"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture | awk -F- '{ print $NF }').asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture | awk -F- '{ print $NF }')"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture | awk -F- '{ print $NF }').asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Thu, 20 Jan 2022 05:26:13 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo
# Thu, 20 Jan 2022 05:26:14 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Thu, 20 Jan 2022 05:26:14 GMT
ENV CONVERTIGO_VERSION=7.9.7
# Thu, 20 Jan 2022 05:26:14 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.9.7/convertigo-7.9.7.war
# Thu, 20 Jan 2022 05:26:14 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 20 Jan 2022 05:26:27 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Thu, 20 Jan 2022 05:26:27 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Thu, 20 Jan 2022 05:26:27 GMT
COPY file:ba6487fa7ec71ffccfe3babd0fb02dea602edf66ffef39f9ab084bdb887562ab in / 
# Thu, 20 Jan 2022 05:26:27 GMT
WORKDIR /workspace
# Thu, 20 Jan 2022 05:26:28 GMT
VOLUME [/workspace]
# Thu, 20 Jan 2022 05:26:28 GMT
EXPOSE 28080
# Thu, 20 Jan 2022 05:26:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 20 Jan 2022 05:26:28 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:0e29546d541cdbd309281d21a73a9d1db78665c1b95b74f32b009e0b77a6e1e3`  
		Last Modified: Tue, 21 Dec 2021 01:27:20 GMT  
		Size: 54.9 MB (54919034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b829c73b52b92b97d5c07a54fb0f3e921995a296c714b53a32ae67d19231fcd`  
		Last Modified: Tue, 21 Dec 2021 02:01:26 GMT  
		Size: 5.2 MB (5152816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5b7ae361722f070eca53f35823ed21baa85d61d5d95cd5a95ab53d740cdd56`  
		Last Modified: Tue, 21 Dec 2021 02:01:26 GMT  
		Size: 10.9 MB (10871868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6494e4811622b31c027ccac322ca463937fd805f569a93e6f15c01aade718793`  
		Last Modified: Tue, 21 Dec 2021 02:01:49 GMT  
		Size: 54.6 MB (54566215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b102718924c67af431330a4eae288cb9c4236caa5c79864e71c8aa3be8808138`  
		Last Modified: Tue, 21 Dec 2021 23:14:04 GMT  
		Size: 14.1 MB (14071715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc138796d3229007379558fe6ca5122933ecb27f5b49912b45b5272c81674b`  
		Last Modified: Wed, 19 Jan 2022 21:00:08 GMT  
		Size: 187.6 MB (187628533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeb79502525353a03599166316a6e50dab715b1a73943662e61843607b0351c`  
		Last Modified: Thu, 20 Jan 2022 01:24:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bca49c3abe99ad023560d5687950b4c0fc7c6c5ed3fb1f2ef00c525a16e3db`  
		Last Modified: Thu, 20 Jan 2022 01:34:23 GMT  
		Size: 12.5 MB (12527225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642796def18af5ea61acac0f0f4ce6e87de6d5f6689a6ce5121409a30c26015d`  
		Last Modified: Thu, 20 Jan 2022 01:34:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb5a6ebd6b78d0ef4c2af8b2691ecf960dc27fbb5befc02ad8c1aa44f8c0c06`  
		Last Modified: Thu, 20 Jan 2022 05:26:48 GMT  
		Size: 2.3 MB (2254028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831a321fa30ab307c77bd09bda4ef7d9ef733f40c07b6432315c2aab5502d2e8`  
		Last Modified: Thu, 20 Jan 2022 05:26:47 GMT  
		Size: 970.4 KB (970370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33de10c1af5b34146c018991289ac11ef65ec174523ffd32b4fb28857e2ffa61`  
		Last Modified: Thu, 20 Jan 2022 05:26:43 GMT  
		Size: 4.4 KB (4422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27455fdbfe94b41feba92e9c4bf8c9fc6a879685edfb9f567e12da0e4f0b6c66`  
		Last Modified: Thu, 20 Jan 2022 05:26:43 GMT  
		Size: 27.5 KB (27485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26211c23f7eb0a0cbffa767b46561f343bf712376f97672d6e8465a436be7906`  
		Last Modified: Thu, 20 Jan 2022 05:26:48 GMT  
		Size: 97.0 MB (96990062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af574fb9d0040de3202549b0b6c1525a095b07475c7bdf3f9cb7beb5e116954`  
		Last Modified: Thu, 20 Jan 2022 05:26:43 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638e7f29572e13343b39eeebe2040715af9db974a1807dd7765e2c7404982388`  
		Last Modified: Thu, 20 Jan 2022 05:26:43 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
