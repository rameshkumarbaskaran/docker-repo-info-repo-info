## `tomcat:8-jre8-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:4057f71a023b0f5056ec3fe5d9c967df765c4cb8f3b0ac47dbb66ba21fa2688f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre8-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:7bf8673c994e9118cbb56ec2026fcf311fd241a58ff93cc49f273a59760b9c9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83736142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91178c624c4551d78792dd691b1251c35428a084a47ea067812910f1236b4ba`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:01:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:05 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:05 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:05 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:02:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:46:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:46:54 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:46:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:46:55 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:46:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:46:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:59:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 23 Jun 2022 22:59:21 GMT
ENV TOMCAT_MAJOR=8
# Thu, 23 Jun 2022 22:59:21 GMT
ENV TOMCAT_VERSION=8.5.81
# Thu, 23 Jun 2022 22:59:21 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Thu, 23 Jun 2022 22:59:22 GMT
COPY dir:2be3749acdb3ed4aec8b20aea036e12b5bb431176fdf010d21fc0b1f035d620d in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:59:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:59:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:59:27 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:59:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fab7e4cce528d853465a0775f91b15783a53a42b906820fb3f70f0f731667`  
		Last Modified: Thu, 23 Jun 2022 05:08:38 GMT  
		Size: 3.3 MB (3273402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cc1e3d6d3732acee702c68bf93504ebe4e5c55920790e28b99c6849e782b35`  
		Last Modified: Thu, 23 Jun 2022 05:21:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157ed8b1255f39df56128dba009619425842ec5ccbdbcc3c877a494f33a08f7b`  
		Last Modified: Thu, 23 Jun 2022 05:22:31 GMT  
		Size: 41.7 MB (41703996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf6d852829687247cbc55eb901d61eafafafa2ffb29239142c02848509f69a8`  
		Last Modified: Thu, 23 Jun 2022 23:15:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ae3347cc51f9e5d150c7004e3d704bf68946d46dbb560f9694ffac0d41523b`  
		Last Modified: Thu, 23 Jun 2022 23:26:16 GMT  
		Size: 11.2 MB (11230505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62036f4f529e2cb60224ce50734a1e887db65b7c3ddf644f2d25362a72a2778`  
		Last Modified: Thu, 23 Jun 2022 23:26:16 GMT  
		Size: 387.7 KB (387684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fee43c7a08006d50397d9ce0a08f022fd665d8d3584a7bb0b45f98b3f2faa9a`  
		Last Modified: Thu, 23 Jun 2022 23:26:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e1b9f8650165afc3b08f841c5b7eebb4f1fa00b0d858472f9f7151beafcfd9cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81191355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7726b74f27c1a553a1f82e91dd8a55efd75d22a19471b0a347804e3b5dddc54`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:15:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:25:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 15:25:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:25:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:25:38 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:25:39 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 15:27:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 24 Jun 2022 02:45:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 24 Jun 2022 02:45:26 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jun 2022 02:45:27 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 24 Jun 2022 02:45:28 GMT
WORKDIR /usr/local/tomcat
# Fri, 24 Jun 2022 02:45:29 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 02:45:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 24 Jun 2022 03:03:13 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 24 Jun 2022 03:03:14 GMT
ENV TOMCAT_MAJOR=8
# Fri, 24 Jun 2022 03:03:15 GMT
ENV TOMCAT_VERSION=8.5.81
# Fri, 24 Jun 2022 03:03:16 GMT
ENV TOMCAT_SHA512=729387275cce4a0900289722f6c70ebcf7aee924af671b110b8ea8577fd6d045d47f17d526c8db5fd41c8590102e7f5100e95e89f7fd511b941565812ecbed35
# Fri, 24 Jun 2022 03:03:18 GMT
COPY dir:a8831e21e654666536f023a92051f99102d3a2a6d3ad0f8ad107cc83a3de4934 in /usr/local/tomcat 
# Fri, 24 Jun 2022 03:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 03:03:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 24 Jun 2022 03:03:24 GMT
EXPOSE 8080
# Fri, 24 Jun 2022 03:03:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f637b7908849640db5a85b9e9242a3aae4e71783948b20c9f1e0bab2cdb5039`  
		Last Modified: Thu, 23 Jun 2022 15:38:45 GMT  
		Size: 3.1 MB (3125979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ba678a6fdebe9afb9f703af02ac98b0bb1ba64ed713c5d39205bc2d80fd49d`  
		Last Modified: Thu, 23 Jun 2022 15:54:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58eadd002186456fa7591fed8917efc4ae297f9fa2e76225ee83eb893bdfe7`  
		Last Modified: Thu, 23 Jun 2022 15:55:46 GMT  
		Size: 40.7 MB (40731103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef783b7db8600bd8a0839e8bf10416af46d07b01faabae51c2b54a74e19aa6`  
		Last Modified: Fri, 24 Jun 2022 03:30:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53e810ee0e24e9d360e92fe3505f2f5e6fe47e717ea2104507cd4257ad819f4`  
		Last Modified: Fri, 24 Jun 2022 03:42:41 GMT  
		Size: 11.2 MB (11246245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eedf3a00d729aa6ddc1dd7e85febcbfb3ed918b4fbd8a993b951ec4ca170d9`  
		Last Modified: Fri, 24 Jun 2022 03:42:39 GMT  
		Size: 173.7 KB (173650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
