## `tomcat:8-jre11-openjdk-slim`

```console
$ docker pull tomcat@sha256:9c5bdf6ea2608aba6410c1c788a4bbe76a6eae00eaafa9ed4931c7b8c7cda114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre11-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:7dc782d8d4fb72fa101b731cb1c587a7d09874b62ac65e2224e481f5fe82b696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90560897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e4ab22f2cdf1088093944f572ed21e75d28c0c7717b7a8f475310925385f93`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:59:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Jul 2022 01:59:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Jul 2022 01:59:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 01:59:32 GMT
ENV LANG=C.UTF-8
# Mon, 25 Jul 2022 20:26:59 GMT
ENV JAVA_VERSION=11.0.16
# Mon, 25 Jul 2022 20:28:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Jul 2022 23:11:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Jul 2022 23:11:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Jul 2022 23:11:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Jul 2022 23:11:13 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Jul 2022 23:11:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:11:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Jul 2022 23:24:24 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 25 Jul 2022 23:24:24 GMT
ENV TOMCAT_MAJOR=8
# Mon, 25 Jul 2022 23:24:24 GMT
ENV TOMCAT_VERSION=8.5.81
# Mon, 25 Jul 2022 23:24:24 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Mon, 25 Jul 2022 23:24:25 GMT
COPY dir:cd74e43d7bbbb1fb77393e5ec39447f7e5637e4e4dc6218c2bec460d388930a2 in /usr/local/tomcat 
# Mon, 25 Jul 2022 23:24:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Jul 2022 23:24:30 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Jul 2022 23:24:30 GMT
EXPOSE 8080
# Mon, 25 Jul 2022 23:24:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693ef00b582081dff0c396dca2fc62b2050dc4220400c6964508f017e45f0d1`  
		Last Modified: Tue, 12 Jul 2022 02:09:05 GMT  
		Size: 1.6 MB (1582273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f2c7b97846c27df3b102c39306d65db4d55e68ea17b9a33ba5b0c329704354`  
		Last Modified: Tue, 12 Jul 2022 02:17:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b95d8dbc64495a77dab8fac9679d708357700cc4afadebf932683d3611e016a`  
		Last Modified: Mon, 25 Jul 2022 20:41:11 GMT  
		Size: 46.0 MB (46042395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457727f4faccfa910b528b5751af3324b789f584942e93dddd1ba2480ca51403`  
		Last Modified: Mon, 25 Jul 2022 23:39:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a37ee75556087924c543bf1076780e984cc41ed187c34f009df329e6c4eaf6d`  
		Last Modified: Mon, 25 Jul 2022 23:50:53 GMT  
		Size: 11.2 MB (11172807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5da48f696e9b989765b08ff5dc5580d524b470e07ca1a6f5aa13f1470f06f1`  
		Last Modified: Mon, 25 Jul 2022 23:50:52 GMT  
		Size: 396.3 KB (396300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ac30f52e544f642b7e8a6cb8af09336e914d5b2d4a596c0446f0acd8540a18`  
		Last Modified: Mon, 25 Jul 2022 23:50:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:98a3010e1b6ba5113025df1d0fbe8b38f1f021822ac1327b4ae799fc9ecb2b67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88111507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84989c8911887011335c157bc2b6a8977c965b3478d4d3cf353b41e9c1224a8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 02 Aug 2022 04:48:18 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 02 Aug 2022 04:48:19 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:48:20 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 04:48:21 GMT
ENV JAVA_VERSION=11.0.16
# Tue, 02 Aug 2022 04:50:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_linux_11.0.16_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_aarch64_linux_11.0.16_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 03 Aug 2022 01:55:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:55:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:55:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:55:11 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:55:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:55:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 02:29:51 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 03 Aug 2022 02:29:52 GMT
ENV TOMCAT_MAJOR=8
# Wed, 03 Aug 2022 02:29:53 GMT
ENV TOMCAT_VERSION=8.5.81
# Wed, 03 Aug 2022 02:29:54 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Wed, 03 Aug 2022 02:29:56 GMT
COPY dir:d114209858f7b06162abf118766351c5b0cfee361fe43a191439dfde92324529 in /usr/local/tomcat 
# Wed, 03 Aug 2022 02:29:59 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 02:30:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 02:30:02 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 02:30:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4015b6e8cc8db11af172df5c0369552bc2a74cd69094b0756d21fc6b0b2a5393`  
		Last Modified: Tue, 02 Aug 2022 05:03:25 GMT  
		Size: 1.6 MB (1565954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd343789f78f94e3d0fa4df3267fdadbc18138ad5785aa9a8afec60ec0407136`  
		Last Modified: Tue, 02 Aug 2022 05:14:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8df94248cfc56b40d896855ef271976224c34fbfbe8a456006be727a3635c0`  
		Last Modified: Tue, 02 Aug 2022 05:16:53 GMT  
		Size: 45.1 MB (45126519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f5e0da9b3de3c71aac0a5e8758b7a6fee85d1c14dee1637d3bc6949997acc`  
		Last Modified: Wed, 03 Aug 2022 03:04:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b774610064f7c4abc5fad41d368dd7385a89f2016b4d43d86d6ba670ade18172`  
		Last Modified: Wed, 03 Aug 2022 03:27:33 GMT  
		Size: 11.2 MB (11184471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5d3631e354799beba5ce090b5c479b3daed97690fc995239203b78d26944f`  
		Last Modified: Wed, 03 Aug 2022 03:27:31 GMT  
		Size: 179.9 KB (179908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
