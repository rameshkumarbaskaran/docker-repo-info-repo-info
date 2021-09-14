## `convertigo:latest`

```console
$ docker pull convertigo@sha256:1be1851b347e81076ca5c15b39a588a403fc50f73837a444ff783915070ae7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:8a54f060567ee33fef38bfdbb7fe1713414df41736bd010f10eec25b672dbad6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.2 MB (437211886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a3048df5b87674129b93a1d04fbc56f0e328087f4190fd20d1cb7efbc8a9cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:07 GMT
ADD file:1fedf68870782f1b44cd50691444aab4061cc0c70f24e5fabe9c562cc46eb9af in / 
# Fri, 03 Sep 2021 01:21:08 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:31:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:31:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 06:31:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:35:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Fri, 03 Sep 2021 08:35:12 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 08:35:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:35:12 GMT
ENV JAVA_VERSION=16.0.2
# Fri, 03 Sep 2021 08:35:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 03 Sep 2021 08:35:23 GMT
CMD ["jshell"]
# Sat, 04 Sep 2021 13:10:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 04 Sep 2021 13:10:49 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Sep 2021 13:10:50 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 04 Sep 2021 13:10:50 GMT
WORKDIR /usr/local/tomcat
# Sat, 04 Sep 2021 13:10:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 04 Sep 2021 13:10:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 04 Sep 2021 13:26:24 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 04 Sep 2021 13:26:24 GMT
ENV TOMCAT_MAJOR=9
# Tue, 14 Sep 2021 17:45:23 GMT
ENV TOMCAT_VERSION=9.0.53
# Tue, 14 Sep 2021 17:45:24 GMT
ENV TOMCAT_SHA512=ee731b2d0c3ab7e14fa924dcb8d598707cedf714c9ce1f2c2d907a1fd51e26f7eec1343c3dc39e240ff64dac2e0213f154d23e5f94a430f429165b5df51f786f
# Tue, 14 Sep 2021 17:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		dirmngr 		gnupg 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local mvnFile="${1:-}"; 		local success=; 		local distUrl=; 		for distUrl in 			"https://www.apache.org/dyn/closer.cgi?action=download&filename=$distFile" 			"https://downloads.apache.org/$distFile" 			"https://www-us.apache.org/dist/$distFile" 			"https://www.apache.org/dist/$distFile" 			"https://archive.apache.org/dist/$distFile" 			${mvnFile:+"https://repo1.maven.org/maven2/org/apache/tomcat/tomcat/$mvnFile"} 		; do 			if curl -fL -o "$f" "$distUrl" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc" "$TOMCAT_VERSION/tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes 		; 		nproc="$(nproc)"; 		make -j "$nproc"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| xargs -rt readlink -e 		| sort -u 		| xargs -rt dpkg-query --search 		| cut -d: -f1 		| sort -u 		| tee "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt" 		| xargs -r apt-mark manual 	; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work; 		catalina.sh version
# Tue, 14 Sep 2021 17:45:50 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 14 Sep 2021 17:45:50 GMT
EXPOSE 8080
# Tue, 14 Sep 2021 17:45:50 GMT
CMD ["catalina.sh" "run"]
# Tue, 14 Sep 2021 19:21:24 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Tue, 14 Sep 2021 19:21:24 GMT
ENV SWT_GTK3=0
# Tue, 14 Sep 2021 19:21:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 14 Sep 2021 19:21:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 14 Sep 2021 19:21:25 GMT
WORKDIR /usr/local/tomcat
# Tue, 14 Sep 2021 19:21:29 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     sudo     unzip   && rm -rf /var/lib/apt/lists/*
# Tue, 14 Sep 2021 19:21:29 GMT
ENV GOSU_VERSION=1.12
# Tue, 14 Sep 2021 19:21:29 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Tue, 14 Sep 2021 19:21:29 GMT
ENV TINI_VERSION=0.19.0
# Tue, 14 Sep 2021 19:21:30 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Tue, 14 Sep 2021 19:21:42 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture | awk -F- '{ print $NF }')"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture | awk -F- '{ print $NF }').asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture | awk -F- '{ print $NF }')"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture | awk -F- '{ print $NF }').asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Tue, 14 Sep 2021 19:21:43 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace     && echo "convertigo ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/convertigo     && chmod 0440 /etc/sudoers.d/convertigo
# Tue, 14 Sep 2021 19:21:43 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         -e 's,</Context>,<Manager pathname="" /><CookieProcessor sameSiteCookies="unset" /></Context>,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Tue, 14 Sep 2021 19:21:44 GMT
ENV CONVERTIGO_VERSION=7.9.4
# Tue, 14 Sep 2021 19:21:44 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.9.4/convertigo-7.9.4.war
# Tue, 14 Sep 2021 19:21:44 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Tue, 14 Sep 2021 19:21:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Tue, 14 Sep 2021 19:21:50 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Tue, 14 Sep 2021 19:21:50 GMT
COPY file:ba6487fa7ec71ffccfe3babd0fb02dea602edf66ffef39f9ab084bdb887562ab in / 
# Tue, 14 Sep 2021 19:21:51 GMT
WORKDIR /workspace
# Tue, 14 Sep 2021 19:21:51 GMT
VOLUME [/workspace]
# Tue, 14 Sep 2021 19:21:51 GMT
EXPOSE 28080
# Tue, 14 Sep 2021 19:21:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 14 Sep 2021 19:21:51 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:955615a668ce169f8a1443fc6b6e6215f43fe0babfb4790712a2d3171f34d366`  
		Last Modified: Fri, 03 Sep 2021 01:26:55 GMT  
		Size: 54.9 MB (54926871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2756ef5f69a5190f4308619e0f446d95f5515eef4a814dbad0bcebbbbc7b25a8`  
		Last Modified: Fri, 03 Sep 2021 06:39:22 GMT  
		Size: 5.2 MB (5153100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911ea9f2bd51e53a455297e0631e18a72a86d7e2c8e1807176e80f991bde5d64`  
		Last Modified: Fri, 03 Sep 2021 06:39:23 GMT  
		Size: 10.9 MB (10871687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b0a22ee906271a6ce9ddd1754fdd7d3b59078e0b57b6cc054c7ed7ac301587`  
		Last Modified: Fri, 03 Sep 2021 06:39:45 GMT  
		Size: 54.6 MB (54566834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79c82cab03ddf5fc88cf1ab0550217980b866ec12c52b0f16751bc45be87b6`  
		Last Modified: Fri, 03 Sep 2021 08:48:24 GMT  
		Size: 14.1 MB (14071678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c965e8fb8dc18667119f0e6e2bf13db24c86078a1ab58e95b4bc0279e63314`  
		Last Modified: Fri, 03 Sep 2021 08:54:10 GMT  
		Size: 184.9 MB (184917708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415db3c8b51e3f2fe5cdb326f459ed204450903d06983ca758569c339fb50a72`  
		Last Modified: Sat, 04 Sep 2021 13:54:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37810e320a231dfa1e8dbfd39066e8e51c355332ab8ab8f52ff760bf600e0d4d`  
		Last Modified: Tue, 14 Sep 2021 18:37:41 GMT  
		Size: 12.5 MB (12518833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8b7444c8f158d7b260e9959374d4d6204d60f1343f6c2e788175ed3dd969f0`  
		Last Modified: Tue, 14 Sep 2021 18:37:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4acc4cd8074266b5aa9fa3b5953e4c0a9e40123bf03505296363297ba92e180`  
		Last Modified: Tue, 14 Sep 2021 19:22:05 GMT  
		Size: 2.3 MB (2253900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c2d6e43a8b41e26023b6e6f9798c23179c267f711f41e06e8a56e4ad7fe2ce`  
		Last Modified: Tue, 14 Sep 2021 19:22:05 GMT  
		Size: 970.4 KB (970352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30a6a7dc561995e367861386d46ca558a39f477d61e4f9221e1e794d9ea3cd5`  
		Last Modified: Tue, 14 Sep 2021 19:22:02 GMT  
		Size: 4.4 KB (4422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb279a8de32815898dceababf6856bd963f5044c89ba5ded89d62a34d5b8c9e3`  
		Last Modified: Tue, 14 Sep 2021 19:22:02 GMT  
		Size: 27.5 KB (27503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261e8c825d196d20ec6f8861b47aec340e62554bcde0469a932a4f95309516b`  
		Last Modified: Tue, 14 Sep 2021 19:22:08 GMT  
		Size: 96.9 MB (96926815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673f7b60dae1bfa1076c943bd918f84f3f6923a22944865f78cb031e5aa0ce0a`  
		Last Modified: Tue, 14 Sep 2021 19:22:02 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67fdafc8491b5be32c5e88c928e6df8a1c90a89c7237d9f7aaa2664db38bcce`  
		Last Modified: Tue, 14 Sep 2021 19:22:02 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
