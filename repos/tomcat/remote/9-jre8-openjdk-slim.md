## `tomcat:9-jre8-openjdk-slim`

```console
$ docker pull tomcat@sha256:a9a834ca998ff7cbab122c0cecc2122eeaa2378b9c75e929b6623479cc2ef8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:3b06aa8dcc825c96d2fb2891546e25694cc7034112fbd3c13b4d0b8a4b95281c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87212038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543cbededa92c7b17c8f604d6b293d16b6452cf1cf4a4682cf077d096428168`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:00:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:00:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:00:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:00:37 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:00:37 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:46:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:46:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:46:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:46:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:46:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:46:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:52:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_MAJOR=9
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_VERSION=9.0.64
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Thu, 23 Jun 2022 22:52:06 GMT
COPY dir:da6e561ebf837f306d29c5e0c12324d6f84a1f9c9329a24c4faf24655d59fe2f in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:52:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:52:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:52:11 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:52:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4dc029a36926590a5070a9a58443942497e3b2d48cff116b8b15004d386a40`  
		Last Modified: Thu, 23 Jun 2022 05:07:14 GMT  
		Size: 1.6 MB (1582249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e04eeb91a4371c25329796317d1b09a60bacf789ea0952f690c5680fc3cf4`  
		Last Modified: Thu, 23 Jun 2022 05:20:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba945e1408ccd99f81b8a3b5741ad91ef403ac4b97efc3a34175dc79d1dc3eae`  
		Last Modified: Thu, 23 Jun 2022 05:21:52 GMT  
		Size: 41.7 MB (41697352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22878f33e97a17ad713697f81fceb0da94ab4829be3b309e5e61167f31da4124`  
		Last Modified: Thu, 23 Jun 2022 23:14:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c82b953679ce2d79349c2051f5f63771eb1ecac6be23388f11c0e13dbf67ff`  
		Last Modified: Thu, 23 Jun 2022 23:20:27 GMT  
		Size: 12.2 MB (12156254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334f2cb0fff020b1b263d92b4d90bf7464e255ad6e4804845c1c4f0162e74ec`  
		Last Modified: Thu, 23 Jun 2022 23:20:26 GMT  
		Size: 396.3 KB (396266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e29c34ad5071e4e7196b7608e5cd5f66be49c106ee8ff2938a0a13af2028c4`  
		Last Modified: Thu, 23 Jun 2022 23:20:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7978e8df1c5e1914aabaa8a740f23ebabe02a855857713d04b9be2d8cb8179f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84494853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1785310e8d913c2297811d2f42a09ea888b6d6bc3e10f4492ced3d9a3939738`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:14:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:24:54 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 15:24:54 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:24:55 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:24:56 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:24:57 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 15:26:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 24 Jun 2022 02:44:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 24 Jun 2022 02:44:07 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 02:44:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 24 Jun 2022 02:44:09 GMT
WORKDIR /usr/local/tomcat
# Fri, 24 Jun 2022 02:44:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:44:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:53:08 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 24 Jun 2022 02:53:09 GMT
ENV TOMCAT_MAJOR=9
# Fri, 24 Jun 2022 02:53:10 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 24 Jun 2022 02:53:11 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 24 Jun 2022 02:53:13 GMT
COPY dir:30bab2b19c483c782492b44f1fe005d3110c0233475c2e3be641199ed7f1a7f6 in /usr/local/tomcat 
# Fri, 24 Jun 2022 02:53:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 02:53:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 24 Jun 2022 02:53:19 GMT
EXPOSE 8080
# Fri, 24 Jun 2022 02:53:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b1362d29199a34271f94fac2115a6940998ae50f16fd5de481ae77825beed`  
		Last Modified: Thu, 23 Jun 2022 15:36:55 GMT  
		Size: 1.4 MB (1361261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80e4628674709d62b54ef05d6c8a54e664ef194a8491937afe4a7d5b0b3a14b`  
		Last Modified: Thu, 23 Jun 2022 15:53:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfb3c848237ab39b9a8ea4ff3313d2566747248c9345f9a3bc53b57c86975a0`  
		Last Modified: Thu, 23 Jun 2022 15:55:03 GMT  
		Size: 40.7 MB (40720858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4487e4982608c06cbb2fc5f6d5605c939c873d5b9977c13eff8b325389ca2f9f`  
		Last Modified: Fri, 24 Jun 2022 03:28:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6284f44d09a0702df56f84701adcae33c3fe514d922f04642d73bb242e826e`  
		Last Modified: Fri, 24 Jun 2022 03:35:49 GMT  
		Size: 12.2 MB (12166725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a2c07c2637a97d0c811fe97793162ff0816bbfe905785d48201058e780fb56`  
		Last Modified: Fri, 24 Jun 2022 03:35:48 GMT  
		Size: 179.9 KB (179938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
