## `flink:scala_2.11`

```console
$ docker pull flink@sha256:2c1f2877b19a4311b0911256fff187029a83330b47c2cff5a4201b5f3078d76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:scala_2.11` - linux; amd64

```console
$ docker pull flink@sha256:b7a46e6eeee948aa46d3a856b66ad8bdb5fb7f409901fb8d95c16952e7762724
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437702014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736b8ce8aa26b80be1f642ef5f7231bbbac9dea3de871bf0b02e8193083b0b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 17 Nov 2020 20:20:58 GMT
ADD file:9a4fd72d749f4a791e75e0f6fc6028d0771e3381b6d84a8d0b07a4887bc7c641 in / 
# Tue, 17 Nov 2020 20:20:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:30:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:30:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 19 Nov 2020 03:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Nov 2020 03:06:45 GMT
ENV LANG=C.UTF-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 19 Nov 2020 03:07:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Nov 2020 03:07:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Nov 2020 03:07:32 GMT
ENV JAVA_VERSION=8u275
# Thu, 19 Nov 2020 03:07:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jre_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz.asc "$downloadUrl.sign"; 	wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 10 Dec 2020 14:20:30 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5 gettext-base;   rm -rf /var/lib/apt/lists/*
# Thu, 10 Dec 2020 14:20:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Dec 2020 14:20:32 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   for server in ha.pool.sks-keyservers.net $(shuf -e                           hkp://p80.pool.sks-keyservers.net:80                           keyserver.ubuntu.com                           hkp://keyserver.ubuntu.com:80                           pgp.mit.edu) ; do       gpg --batch --keyserver "$server" --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;   done &&   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   gpgconf --kill all;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz.asc GPG_KEY=C63E230EFFF519A5BBF2C9AE6767487CD505859C CHECK_GPG=true
# Thu, 10 Dec 2020 14:21:05 GMT
ENV FLINK_HOME=/opt/flink
# Thu, 10 Dec 2020 14:21:06 GMT
ENV PATH=/opt/flink/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Dec 2020 14:21:07 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Thu, 10 Dec 2020 14:21:07 GMT
WORKDIR /opt/flink
# Thu, 10 Dec 2020 14:21:24 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";     if [ "$CHECK_GPG" = "true" ]; then     wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";     for server in ha.pool.sks-keyservers.net $(shuf -e                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys "$GPG_KEY" && break || : ;     done &&     gpg --batch --verify flink.tgz.asc flink.tgz;     gpgconf --kill all;     rm -rf "$GNUPGHOME" flink.tgz.asc;   fi;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Thu, 10 Dec 2020 14:21:24 GMT
COPY file:5118b9265b7774ef32131b2cbf42fd9bf26c640be3ebb42b4972a3ae8ed5125e in / 
# Thu, 10 Dec 2020 14:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Dec 2020 14:21:24 GMT
EXPOSE 6123 8081
# Thu, 10 Dec 2020 14:21:24 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:756975cb9c7e7933d824af9319b512dd72a50894232761d06ef3be59981df838`  
		Last Modified: Tue, 17 Nov 2020 20:27:06 GMT  
		Size: 50.4 MB (50397725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77915b4e630d47296770ce4cf481894885978072432456615172af463433cc5`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 7.8 MB (7811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37a0a41b6b03489dd7de0aa2a79e369fd8b219bbc36b52f3f9790dc128e74b`  
		Last Modified: Wed, 18 Nov 2020 00:49:42 GMT  
		Size: 10.0 MB (9996233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713f7746108e0e07f616eec5ac22de7d9981c7e5087a3d63d92193b71d3e98e3`  
		Last Modified: Thu, 19 Nov 2020 03:12:18 GMT  
		Size: 5.5 MB (5529433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba38f0ad15ed007b8974fb97b174e2f3e0418a49a03c215e237812c058006714`  
		Last Modified: Thu, 19 Nov 2020 03:12:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef0ecdbb4512b269e1df4a3a65f0ff50bbfbdbfe16779256f3f3954f36eb61b`  
		Last Modified: Thu, 19 Nov 2020 03:12:58 GMT  
		Size: 41.3 MB (41301352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745520d3d21cb70ca09af29670ced791449e9f1c925f19d7a1fa775482344a8d`  
		Last Modified: Thu, 10 Dec 2020 14:33:12 GMT  
		Size: 531.0 KB (531047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce52e15aefc2da2b033c790a29c6c4b10df43c8b41ed3f271ad85a32e92f1c`  
		Last Modified: Thu, 10 Dec 2020 14:33:10 GMT  
		Size: 900.5 KB (900512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e4284ec8cf96c80fc42d6b17e6fc63747d638671fd975abc9c70bde02cbf00`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 4.6 KB (4607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ffa647a49f95c2f65c3b454cc69f9152f9ed7450b60233f0004d0bbe52548a`  
		Last Modified: Thu, 10 Dec 2020 14:33:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc52dab532693bf96bffb3b8b6adcbc546c9990bc921234d6e314d570fc94226`  
		Last Modified: Thu, 10 Dec 2020 14:34:03 GMT  
		Size: 321.2 MB (321227373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0536c0e6f1e36d72325ee0f945ba473de994711714dd4b15b099315b7ad3888`  
		Last Modified: Thu, 10 Dec 2020 14:33:44 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
