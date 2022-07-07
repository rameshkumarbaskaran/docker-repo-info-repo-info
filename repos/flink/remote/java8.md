## `flink:java8`

```console
$ docker pull flink@sha256:2e5d8a8dc50450d5f0fce569eb79a7b35824d41df425478eebf1c47edd45d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `flink:java8` - linux; amd64

```console
$ docker pull flink@sha256:e70b66d9666515590176ca7e14d75305a19048aab5059ebd490a8a9ffcb0982f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556889009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f60b5a49e6a98cc3463beac8baaaee5845801c3415ca72a0bff8a23668e3777`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:50:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:01:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:22 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:22 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 19:57:53 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 19:57:54 GMT
ENV GOSU_VERSION=1.11
# Thu, 23 Jun 2022 19:58:27 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 07 Jul 2022 20:19:49 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.1/flink-1.15.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.1/flink-1.15.1-bin-scala_2.12.tgz.asc GPG_KEY=7D660377995CA7A5AFEBA79A3EE012FEE982F098 CHECK_GPG=true
# Thu, 07 Jul 2022 20:19:50 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 07 Jul 2022 20:19:50 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Jul 2022 20:19:50 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 07 Jul 2022 20:19:50 GMT
WORKDIR /opt/flink
# Thu, 07 Jul 2022 20:20:58 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;   sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Thu, 07 Jul 2022 20:20:59 GMT
COPY file:e308297ef6ffd9c3cff00834ffd8c0f8baacafe7ea8ed0b19a897eb03baceb28 in / 
# Thu, 07 Jul 2022 20:20:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Jul 2022 20:20:59 GMT
EXPOSE 6123 8081
# Thu, 07 Jul 2022 20:20:59 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c78fa1b97999d08408734a61040475ade5bd7e33e91c0d5170dba2c7c7a92fd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 5.2 MB (5155961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0d2bd524377dc42d072443c0e5e7cafa14f5df609d39bb1f717f43817a2cd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 10.9 MB (10875087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023992b49610b0f24fd4b80779987a1e9ed4a039f7a93c612a259c40f26d75f3`  
		Last Modified: Thu, 23 Jun 2022 05:18:22 GMT  
		Size: 5.7 MB (5657511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c157ac5e2cd4a56f16e8f79611a67fcda7bebc6cf1dd87de30cb8fcdecd5e4`  
		Last Modified: Thu, 23 Jun 2022 05:21:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6fa2323bbb580f1865fca355dc5c76eb695d48205552c09a066b4be10ebe3`  
		Last Modified: Thu, 23 Jun 2022 05:21:37 GMT  
		Size: 41.4 MB (41424478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db50bf8c383e353ffb6117639ce314679af126469764c6573386939b1cc4368c`  
		Last Modified: Thu, 23 Jun 2022 20:20:37 GMT  
		Size: 1.7 MB (1689749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301a8f543e04dfd7e1e92797dd88e94fa0de436581ea6b5e5868ef16ef46de4e`  
		Last Modified: Thu, 23 Jun 2022 20:20:34 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b91d02c14502a963e2b84e4e9133c23f80b3a70d73a024891b902bf282244e1`  
		Last Modified: Thu, 07 Jul 2022 20:24:07 GMT  
		Size: 4.6 KB (4606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e49e563bf990c59eedc04c3073fa0529d264cd07d1d2a51381822c629d3809`  
		Last Modified: Thu, 07 Jul 2022 20:24:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a2da0b4d86e67ea07400cccbbf1fe4fbe0b238710e44b73ea7b0c9c58e090f`  
		Last Modified: Thu, 07 Jul 2022 20:24:27 GMT  
		Size: 436.2 MB (436168916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656008f25693df0b24be1952153ef28181e7f38703ede3ea82277cf8404465b5`  
		Last Modified: Thu, 07 Jul 2022 20:24:08 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `flink:java8` - linux; arm64 variant v8

```console
$ docker pull flink@sha256:2b29a4ff0cda3a37b8324e1d35af321c9e7cbc60b83bb6b4d6cad0ce7d6cf2ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.9 MB (553927602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8862be7594e0b44cebb48b9e22fb5a18a104588bd2bac1040779ea067f94a136`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:28 GMT
ADD file:64c455af1bb18ff2c202a244e058b6e5ac147b89410ed36edc5e29f4b6f02c5d in / 
# Thu, 23 Jun 2022 00:40:29 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:26:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 15:26:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 15:26:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:26:05 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 15:26:06 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 15:26:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 24 Jun 2022 00:40:19 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base libjemalloc-dev;   rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 00:40:20 GMT
ENV GOSU_VERSION=1.11
# Fri, 24 Jun 2022 00:41:07 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 07 Jul 2022 20:39:44 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.15.1/flink-1.15.1-bin-scala_2.12.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.15.1/flink-1.15.1-bin-scala_2.12.tgz.asc GPG_KEY=7D660377995CA7A5AFEBA79A3EE012FEE982F098 CHECK_GPG=true
# Thu, 07 Jul 2022 20:39:44 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 07 Jul 2022 20:39:45 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Jul 2022 20:39:46 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 07 Jul 2022 20:39:47 GMT
WORKDIR /opt/flink
# Thu, 07 Jul 2022 20:41:07 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;   sed -i 's/rest.address: localhost/rest.address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/rest.bind-address: localhost/rest.bind-address: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/jobmanager.bind-host: localhost/jobmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i 's/taskmanager.bind-host: localhost/taskmanager.bind-host: 0.0.0.0/g' $FLINK_HOME/conf/flink-conf.yaml;   sed -i '/taskmanager.host: localhost/d' $FLINK_HOME/conf/flink-conf.yaml;
# Thu, 07 Jul 2022 20:41:09 GMT
COPY file:e308297ef6ffd9c3cff00834ffd8c0f8baacafe7ea8ed0b19a897eb03baceb28 in / 
# Thu, 07 Jul 2022 20:41:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 07 Jul 2022 20:41:10 GMT
EXPOSE 6123 8081
# Thu, 07 Jul 2022 20:41:11 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:f873dfbc59b181817d5bc2b9fc31d90d8f9139c8cabb2fa7264f9bd7b418b8d2`  
		Last Modified: Thu, 23 Jun 2022 00:46:51 GMT  
		Size: 53.7 MB (53696815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b65e0e9cdc28c8cedaabbc5cbae4652c9b107c47684de49f01a77741a5ded`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 4.9 MB (4938760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43836e7983cba8b758620a218a0ee622daf5513308b6a9e8316f94c271ecafd`  
		Last Modified: Thu, 23 Jun 2022 01:21:51 GMT  
		Size: 10.7 MB (10656970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1d06b8e25e46c71e32c7364495bbd08b14643238b8910969df33b87769e5db`  
		Last Modified: Thu, 23 Jun 2022 15:50:44 GMT  
		Size: 5.6 MB (5649772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318d900ff62efcbf8fd6b8be1865c5c016cc04aacd4e52f40632c1d1facc3c5e`  
		Last Modified: Thu, 23 Jun 2022 15:54:39 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735b99b666a03d0e044db6be8593002c8d7b5e7358256dc39c740c7f4bd06cf`  
		Last Modified: Thu, 23 Jun 2022 15:54:44 GMT  
		Size: 40.7 MB (40664994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edac4ea463eab11fd8dfe3c14338b9dc8dda033f3823fbf759bcd4281925d691`  
		Last Modified: Fri, 24 Jun 2022 00:50:16 GMT  
		Size: 1.3 MB (1309391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad6d3cda66d5685fa8784ee27f16254bc7c2d85a68ac1896560a8df8133737`  
		Last Modified: Fri, 24 Jun 2022 00:50:13 GMT  
		Size: 835.4 KB (835388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da334286700250ff9c172f7d3593ebcfd920f7feae026cffcc4baa5ca10db4d0`  
		Last Modified: Thu, 07 Jul 2022 20:44:01 GMT  
		Size: 4.5 KB (4525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8ce8d916ac8446bb5c2bd86a7507661fdbdc09320152af0cf00a2831595742`  
		Last Modified: Thu, 07 Jul 2022 20:44:01 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f149cd5e57ed137391851f0984f02addbf23e62face7e00835e5b8ce7e527`  
		Last Modified: Thu, 07 Jul 2022 20:44:34 GMT  
		Size: 436.2 MB (436168719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c63dd9912e0369d1678da764afd577f9140ed5c906f9a32f6fd2d52e2afdfdc`  
		Last Modified: Thu, 07 Jul 2022 20:44:01 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
