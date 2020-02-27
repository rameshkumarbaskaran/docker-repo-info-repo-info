<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `convertigo`

-	[`convertigo:7.7`](#convertigo77)
-	[`convertigo:7.7.0`](#convertigo770)
-	[`convertigo:latest`](#convertigolatest)

## `convertigo:7.7`

```console
$ docker pull convertigo@sha256:6db1323afc63a061b5bbb0702d7c68ea525859940d535f5b51ec4dc85a295685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:7.7` - linux; amd64

```console
$ docker pull convertigo@sha256:ce4e8c24714f40393855c7cfce3c744c4b1275763aed1418dd3859c46b175a5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429028205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5076bfe973ca402023959ac79c1e25b373af1072c831e6a7ffbe9cad540d8cbf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:01 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:20:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:20:13 GMT
CMD ["jshell"]
# Thu, 27 Feb 2020 07:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 07:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 07:50:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 07:50:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_VERSION=9.0.31
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_SHA512=75045ce54ad1b6ea66fd112e8b2ffa32a0740c018ab9392c7217a6dd6b829e8645b6810ab4b28dd186c12ce6045c1eb18ed19743c5d4b22c9e613e76294f22f5
# Thu, 27 Feb 2020 07:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Thu, 27 Feb 2020 07:51:03 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Feb 2020 07:51:03 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 07:51:04 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Feb 2020 08:17:51 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 27 Feb 2020 08:17:51 GMT
ENV SWT_GTK3=0
# Thu, 27 Feb 2020 08:17:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 08:17:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 08:17:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 08:17:56 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Thu, 27 Feb 2020 08:17:59 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Thu, 27 Feb 2020 08:18:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Thu, 27 Feb 2020 08:18:01 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_VERSION=7.7.0
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.7.0/convertigo-7.7.0.war
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 27 Feb 2020 08:18:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Thu, 27 Feb 2020 08:18:06 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Thu, 27 Feb 2020 08:18:07 GMT
COPY file:50df0fa3f88bad82c9cf37b6054755b485e39ccdd9250b2906dc40869fcdd4e8 in / 
# Thu, 27 Feb 2020 08:18:07 GMT
WORKDIR /workspace
# Thu, 27 Feb 2020 08:18:07 GMT
VOLUME [/workspace]
# Thu, 27 Feb 2020 08:18:07 GMT
EXPOSE 28080
# Thu, 27 Feb 2020 08:18:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:18:07 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27ce2095ec233759347c30234b114a10cfdd9871c8338738025aba71fe11701`  
		Last Modified: Wed, 26 Feb 2020 20:26:23 GMT  
		Size: 5.3 MB (5284596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0840c2dae09d9afc27fd6c13c1851b96bd7f67831c3bcb66b28fe6eb76c15`  
		Last Modified: Wed, 26 Feb 2020 20:26:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491685d1af8ca17764fc8afe31ba7a2ff5e16c75290f3384d1439490c167f887`  
		Last Modified: Wed, 26 Feb 2020 20:26:42 GMT  
		Size: 196.1 MB (196068101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de47a376c9911077d087ef470748945e84c6647573288318f15af887278f0aa`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9e610cf044965dad454d528d42c1b6b2f1f8c84c34c2bfdb7d43db2118132e`  
		Last Modified: Thu, 27 Feb 2020 08:01:08 GMT  
		Size: 12.1 MB (12064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bfb13107a1423c768882ce6678fb70e0fe3e44ef0595fbacf6b548812f782d`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa76b063b521176e55f1bdf36a44cef3079df128ddeb2fb0eef33b184cc770ab`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1a970e2088fe97afeed274c6031518c9012b863564cd830deb06a4d783c99b`  
		Last Modified: Thu, 27 Feb 2020 08:18:16 GMT  
		Size: 910.1 KB (910073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8013fed710adbaba97f2b9d0892e40aace7392ec55a7c7b9db9d2ba3389240`  
		Last Modified: Thu, 27 Feb 2020 08:18:14 GMT  
		Size: 4.3 KB (4288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c990a7e40b6c86f21ea4cf7d60ca20021dce638b4684f1543beee814dea57`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 27.3 KB (27280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58b28ba1bac6cbe949dfc613ed08197985c6feaf851b1577372003d8daa151d`  
		Last Modified: Thu, 27 Feb 2020 08:18:22 GMT  
		Size: 94.7 MB (94685737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec80d9d83c2df61a029c9fca884dacae161e9a0b1feb634d1d5f522d9718cca3`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706118d77efe08fc3596458027f71b71941bb683fd58861d4796b268a0c6386`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `convertigo:7.7.0`

```console
$ docker pull convertigo@sha256:6db1323afc63a061b5bbb0702d7c68ea525859940d535f5b51ec4dc85a295685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:7.7.0` - linux; amd64

```console
$ docker pull convertigo@sha256:ce4e8c24714f40393855c7cfce3c744c4b1275763aed1418dd3859c46b175a5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429028205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5076bfe973ca402023959ac79c1e25b373af1072c831e6a7ffbe9cad540d8cbf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:01 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:20:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:20:13 GMT
CMD ["jshell"]
# Thu, 27 Feb 2020 07:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 07:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 07:50:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 07:50:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_VERSION=9.0.31
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_SHA512=75045ce54ad1b6ea66fd112e8b2ffa32a0740c018ab9392c7217a6dd6b829e8645b6810ab4b28dd186c12ce6045c1eb18ed19743c5d4b22c9e613e76294f22f5
# Thu, 27 Feb 2020 07:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Thu, 27 Feb 2020 07:51:03 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Feb 2020 07:51:03 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 07:51:04 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Feb 2020 08:17:51 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 27 Feb 2020 08:17:51 GMT
ENV SWT_GTK3=0
# Thu, 27 Feb 2020 08:17:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 08:17:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 08:17:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 08:17:56 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Thu, 27 Feb 2020 08:17:59 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Thu, 27 Feb 2020 08:18:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Thu, 27 Feb 2020 08:18:01 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_VERSION=7.7.0
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.7.0/convertigo-7.7.0.war
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 27 Feb 2020 08:18:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Thu, 27 Feb 2020 08:18:06 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Thu, 27 Feb 2020 08:18:07 GMT
COPY file:50df0fa3f88bad82c9cf37b6054755b485e39ccdd9250b2906dc40869fcdd4e8 in / 
# Thu, 27 Feb 2020 08:18:07 GMT
WORKDIR /workspace
# Thu, 27 Feb 2020 08:18:07 GMT
VOLUME [/workspace]
# Thu, 27 Feb 2020 08:18:07 GMT
EXPOSE 28080
# Thu, 27 Feb 2020 08:18:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:18:07 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27ce2095ec233759347c30234b114a10cfdd9871c8338738025aba71fe11701`  
		Last Modified: Wed, 26 Feb 2020 20:26:23 GMT  
		Size: 5.3 MB (5284596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0840c2dae09d9afc27fd6c13c1851b96bd7f67831c3bcb66b28fe6eb76c15`  
		Last Modified: Wed, 26 Feb 2020 20:26:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491685d1af8ca17764fc8afe31ba7a2ff5e16c75290f3384d1439490c167f887`  
		Last Modified: Wed, 26 Feb 2020 20:26:42 GMT  
		Size: 196.1 MB (196068101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de47a376c9911077d087ef470748945e84c6647573288318f15af887278f0aa`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9e610cf044965dad454d528d42c1b6b2f1f8c84c34c2bfdb7d43db2118132e`  
		Last Modified: Thu, 27 Feb 2020 08:01:08 GMT  
		Size: 12.1 MB (12064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bfb13107a1423c768882ce6678fb70e0fe3e44ef0595fbacf6b548812f782d`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa76b063b521176e55f1bdf36a44cef3079df128ddeb2fb0eef33b184cc770ab`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1a970e2088fe97afeed274c6031518c9012b863564cd830deb06a4d783c99b`  
		Last Modified: Thu, 27 Feb 2020 08:18:16 GMT  
		Size: 910.1 KB (910073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8013fed710adbaba97f2b9d0892e40aace7392ec55a7c7b9db9d2ba3389240`  
		Last Modified: Thu, 27 Feb 2020 08:18:14 GMT  
		Size: 4.3 KB (4288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c990a7e40b6c86f21ea4cf7d60ca20021dce638b4684f1543beee814dea57`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 27.3 KB (27280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58b28ba1bac6cbe949dfc613ed08197985c6feaf851b1577372003d8daa151d`  
		Last Modified: Thu, 27 Feb 2020 08:18:22 GMT  
		Size: 94.7 MB (94685737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec80d9d83c2df61a029c9fca884dacae161e9a0b1feb634d1d5f522d9718cca3`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706118d77efe08fc3596458027f71b71941bb683fd58861d4796b268a0c6386`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `convertigo:latest`

```console
$ docker pull convertigo@sha256:6db1323afc63a061b5bbb0702d7c68ea525859940d535f5b51ec4dc85a295685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `convertigo:latest` - linux; amd64

```console
$ docker pull convertigo@sha256:ce4e8c24714f40393855c7cfce3c744c4b1275763aed1418dd3859c46b175a5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429028205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5076bfe973ca402023959ac79c1e25b373af1072c831e6a7ffbe9cad540d8cbf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["convertigo"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:20:00 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:01 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 26 Feb 2020 20:20:02 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:20:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:20:13 GMT
CMD ["jshell"]
# Thu, 27 Feb 2020 07:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 07:50:27 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 07:50:28 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 07:50:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Feb 2020 07:50:29 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_VERSION=9.0.31
# Thu, 27 Feb 2020 07:50:29 GMT
ENV TOMCAT_SHA512=75045ce54ad1b6ea66fd112e8b2ffa32a0740c018ab9392c7217a6dd6b829e8645b6810ab4b28dd186c12ce6045c1eb18ed19743c5d4b22c9e613e76294f22f5
# Thu, 27 Feb 2020 07:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg dirmngr 		wget ca-certificates 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'tomcat.tar.gz' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz"; 	echo "$TOMCAT_SHA512 *tomcat.tar.gz" | sha512sum --strict --check -; 	ddist 'tomcat.tar.gz.asc' "tomcat/tomcat-$TOMCAT_MAJOR/v$TOMCAT_VERSION/bin/apache-tomcat-$TOMCAT_VERSION.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME"; 		mv webapps webapps.dist; 	mkdir webapps; 		nativeBuildDir="$(mktemp -d)"; 	tar -xf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		aprConfig="$(command -v apr-1-config)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$aprConfig" 			--with-java-home="$JAVA_HOME" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find "$TOMCAT_NATIVE_LIBDIR" -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +; 		chmod -R +rX .; 	chmod 777 logs temp work
# Thu, 27 Feb 2020 07:51:03 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 27 Feb 2020 07:51:03 GMT
EXPOSE 8080
# Thu, 27 Feb 2020 07:51:04 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Feb 2020 08:17:51 GMT
MAINTAINER Nicolas Albert nicolasa@convertigo.com
# Thu, 27 Feb 2020 08:17:51 GMT
ENV SWT_GTK3=0
# Thu, 27 Feb 2020 08:17:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Feb 2020 08:17:52 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 27 Feb 2020 08:17:52 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Feb 2020 08:17:56 GMT
RUN apt-get update -y   && apt-get install -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg     unzip   && rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:17:57 GMT
ENV GOSU_GPG_KEYS=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:17:57 GMT
ENV TINI_GPG_KEYS=6380DC428747F6C393FEACA59A84159D7001A4E5
# Thu, 27 Feb 2020 08:17:59 GMT
RUN export GNUPGHOME="$(mktemp -d)"   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$GOSU_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$GOSU_GPG_KEYS" )   && curl -o /usr/local/bin/gosu -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/gosu.asc -fSL "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu   && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver pgp.mit.edu --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$TINI_GPG_KEYS"   || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$TINI_GPG_KEYS" )   && curl -o /usr/local/bin/tini -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture)"   && curl -o /usr/local/bin/tini.asc -fSL "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$(dpkg --print-architecture).asc"   && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini   && rm /usr/local/bin/tini.asc   && chmod +x /usr/local/bin/tini   && rm -rf /tmp/*
# Thu, 27 Feb 2020 08:18:00 GMT
RUN useradd -s /bin/false -m convertigo     && mkdir -p /workspace/lib /workspace/classes     && chown -R convertigo:convertigo /workspace
# Thu, 27 Feb 2020 08:18:01 GMT
RUN sed -i.bak         -e '/protocol="AJP/d'         -e '/AprLifecycleListener/d'         -e '/JasperListener/d'         -e 's/port="8080"/port="28080" maxThreads="64000" relaxedQueryChars="{}[]|"/'         -e 's,</Host>,  <Valve className="org.apache.catalina.valves.RemoteIpValve" />\n      </Host>,'         conf/server.xml     && sed -i.bak         -e 's,<Context>,<Context sessionCookiePath="/">,'         conf/context.xml     && rm -rf webapps/* bin/*.bat conf/server.xml.bak /tmp/*     && mkdir webapps/ROOT     && chown -R convertigo:convertigo conf temp work logs     && chmod -w conf/*
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_VERSION=7.7.0
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_WAR_URL=https://github.com/convertigo/convertigo/releases/download/7.7.0/convertigo-7.7.0.war
# Thu, 27 Feb 2020 08:18:01 GMT
ENV CONVERTIGO_GPG_KEYS=6A7779BB78FE368DF74B708FD4DA8FBEB64BF75F
# Thu, 27 Feb 2020 08:18:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && ( gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver pgp.mit.edu --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$CONVERTIGO_GPG_KEYS"     || gpg --batch --keyserver keyserver.pgp.com --recv-keys "$CONVERTIGO_GPG_KEYS" )     && curl -fSL -o /tmp/convertigo.war $CONVERTIGO_WAR_URL     && curl -fSL -o /tmp/convertigo.war.asc $CONVERTIGO_WAR_URL.asc     && gpg --batch --verify /tmp/convertigo.war.asc /tmp/convertigo.war     && mkdir -p webapps/ROOT webapps/convertigo     && (cd webapps/convertigo         && unzip -q /tmp/convertigo.war         && (chmod -f a+x WEB-INF/xvnc/* || true)         && (test "$(dpkg --print-architecture)" != "i386" && rm -rf WEB-INF/xulrunner WEB-INF/xvnc WEB-INF/lib/swt_* || true)         && rm -rf /tmp/*)
# Thu, 27 Feb 2020 08:18:06 GMT
COPY file:394d5b837e94d77b6fb87e0ca8bd50995186aaed1c5f3ab5bc0b482f0f769cc3 in webapps/ROOT/index.html 
# Thu, 27 Feb 2020 08:18:07 GMT
COPY file:50df0fa3f88bad82c9cf37b6054755b485e39ccdd9250b2906dc40869fcdd4e8 in / 
# Thu, 27 Feb 2020 08:18:07 GMT
WORKDIR /workspace
# Thu, 27 Feb 2020 08:18:07 GMT
VOLUME [/workspace]
# Thu, 27 Feb 2020 08:18:07 GMT
EXPOSE 28080
# Thu, 27 Feb 2020 08:18:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:18:07 GMT
CMD ["convertigo"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27ce2095ec233759347c30234b114a10cfdd9871c8338738025aba71fe11701`  
		Last Modified: Wed, 26 Feb 2020 20:26:23 GMT  
		Size: 5.3 MB (5284596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0840c2dae09d9afc27fd6c13c1851b96bd7f67831c3bcb66b28fe6eb76c15`  
		Last Modified: Wed, 26 Feb 2020 20:26:22 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491685d1af8ca17764fc8afe31ba7a2ff5e16c75290f3384d1439490c167f887`  
		Last Modified: Wed, 26 Feb 2020 20:26:42 GMT  
		Size: 196.1 MB (196068101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de47a376c9911077d087ef470748945e84c6647573288318f15af887278f0aa`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9e610cf044965dad454d528d42c1b6b2f1f8c84c34c2bfdb7d43db2118132e`  
		Last Modified: Thu, 27 Feb 2020 08:01:08 GMT  
		Size: 12.1 MB (12064653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bfb13107a1423c768882ce6678fb70e0fe3e44ef0595fbacf6b548812f782d`  
		Last Modified: Thu, 27 Feb 2020 08:01:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa76b063b521176e55f1bdf36a44cef3079df128ddeb2fb0eef33b184cc770ab`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1a970e2088fe97afeed274c6031518c9012b863564cd830deb06a4d783c99b`  
		Last Modified: Thu, 27 Feb 2020 08:18:16 GMT  
		Size: 910.1 KB (910073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8013fed710adbaba97f2b9d0892e40aace7392ec55a7c7b9db9d2ba3389240`  
		Last Modified: Thu, 27 Feb 2020 08:18:14 GMT  
		Size: 4.3 KB (4288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c990a7e40b6c86f21ea4cf7d60ca20021dce638b4684f1543beee814dea57`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 27.3 KB (27280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58b28ba1bac6cbe949dfc613ed08197985c6feaf851b1577372003d8daa151d`  
		Last Modified: Thu, 27 Feb 2020 08:18:22 GMT  
		Size: 94.7 MB (94685737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec80d9d83c2df61a029c9fca884dacae161e9a0b1feb634d1d5f522d9718cca3`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c706118d77efe08fc3596458027f71b71941bb683fd58861d4796b268a0c6386`  
		Last Modified: Thu, 27 Feb 2020 08:18:15 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
