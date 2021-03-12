<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `storm`

-	[`storm:1.1`](#storm11)
-	[`storm:1.1.3`](#storm113)
-	[`storm:1.2`](#storm12)
-	[`storm:1.2.3`](#storm123)
-	[`storm:2.2`](#storm22)
-	[`storm:2.2.0`](#storm220)
-	[`storm:latest`](#stormlatest)

## `storm:1.1`

```console
$ docker pull storm@sha256:0daca0a500f94cc30a070856b0b9dc1ebac2f762b3b5d8daddc7a7ef95b505f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:1.1` - linux; amd64

```console
$ docker pull storm@sha256:da0f75915351f8ad7d2a42569cae937da079939abf8161376200a1d906ce56c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168454464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a4cda9f02baf036377d322bd217a33170cbfec52d4120c0d9ec74dd62b967`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:04:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Mar 2021 21:04:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:04:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:04:37 GMT
ENV JAVA_VERSION=8u282
# Tue, 09 Mar 2021 21:05:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jre_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 10 Mar 2021 01:57:28 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:57:29 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:57:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:57:38 GMT
ARG GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
# Wed, 10 Mar 2021 01:57:39 GMT
ARG DISTRO_NAME=apache-storm-1.1.3
# Wed, 10 Mar 2021 01:58:04 GMT
# ARGS: DISTRO_NAME=apache-storm-1.1.3 GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 01:58:04 GMT
WORKDIR /apache-storm-1.1.3
# Wed, 10 Mar 2021 01:58:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-1.1.3/bin
# Wed, 10 Mar 2021 01:58:04 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 01:58:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262868e4544c2f89b0140c83d6d6b61447eb8d28d91d63b0cc5d54315f83a45b`  
		Last Modified: Tue, 09 Mar 2021 21:24:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0fec43ba3fb9ef8fefcc0ebb46605f4104ec57bf6538e3c4392db1848e8be4`  
		Last Modified: Tue, 09 Mar 2021 21:25:26 GMT  
		Size: 41.6 MB (41596010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9afd3621fb3d6e7535e1ad327f174886da2db9ff5f0b51812ec5146473d56`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62992ae4518d2a4bd3ff70c36da0d156bfd16a2f73767f620f12b8ea1c6a2b76`  
		Last Modified: Wed, 10 Mar 2021 02:02:25 GMT  
		Size: 13.1 MB (13127010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067093fb7235ab6d85a5114086c4be80231c797de69d0f064fd029b3481dcf1`  
		Last Modified: Wed, 10 Mar 2021 02:02:28 GMT  
		Size: 83.4 MB (83365285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeca558c24831095074d9c4592471adf8c3b232f3364abe27460042367861542`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:1.1.3`

```console
$ docker pull storm@sha256:0daca0a500f94cc30a070856b0b9dc1ebac2f762b3b5d8daddc7a7ef95b505f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:1.1.3` - linux; amd64

```console
$ docker pull storm@sha256:da0f75915351f8ad7d2a42569cae937da079939abf8161376200a1d906ce56c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168454464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a4cda9f02baf036377d322bd217a33170cbfec52d4120c0d9ec74dd62b967`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:04:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Mar 2021 21:04:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:04:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:04:37 GMT
ENV JAVA_VERSION=8u282
# Tue, 09 Mar 2021 21:05:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jre_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 10 Mar 2021 01:57:28 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:57:29 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:57:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:57:38 GMT
ARG GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
# Wed, 10 Mar 2021 01:57:39 GMT
ARG DISTRO_NAME=apache-storm-1.1.3
# Wed, 10 Mar 2021 01:58:04 GMT
# ARGS: DISTRO_NAME=apache-storm-1.1.3 GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 01:58:04 GMT
WORKDIR /apache-storm-1.1.3
# Wed, 10 Mar 2021 01:58:04 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-1.1.3/bin
# Wed, 10 Mar 2021 01:58:04 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 01:58:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262868e4544c2f89b0140c83d6d6b61447eb8d28d91d63b0cc5d54315f83a45b`  
		Last Modified: Tue, 09 Mar 2021 21:24:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0fec43ba3fb9ef8fefcc0ebb46605f4104ec57bf6538e3c4392db1848e8be4`  
		Last Modified: Tue, 09 Mar 2021 21:25:26 GMT  
		Size: 41.6 MB (41596010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9afd3621fb3d6e7535e1ad327f174886da2db9ff5f0b51812ec5146473d56`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62992ae4518d2a4bd3ff70c36da0d156bfd16a2f73767f620f12b8ea1c6a2b76`  
		Last Modified: Wed, 10 Mar 2021 02:02:25 GMT  
		Size: 13.1 MB (13127010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067093fb7235ab6d85a5114086c4be80231c797de69d0f064fd029b3481dcf1`  
		Last Modified: Wed, 10 Mar 2021 02:02:28 GMT  
		Size: 83.4 MB (83365285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeca558c24831095074d9c4592471adf8c3b232f3364abe27460042367861542`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:1.2`

```console
$ docker pull storm@sha256:70f698d44de4c7451004c81553c21810fea9bed00316e61c9e1e32c9ca963858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:1.2` - linux; amd64

```console
$ docker pull storm@sha256:f0923f5a537d3986422b3a0918efa33822e4f17c3a9f354dc47bf5955af0f534
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254226231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302d358e2354b11f991840790b973034dc35855e1b7b93e08e94c458367224a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:04:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Mar 2021 21:04:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:04:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:04:37 GMT
ENV JAVA_VERSION=8u282
# Tue, 09 Mar 2021 21:05:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jre_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 10 Mar 2021 01:57:28 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:57:29 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:57:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:57:38 GMT
ARG GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
# Wed, 10 Mar 2021 01:58:10 GMT
ARG DISTRO_NAME=apache-storm-1.2.3
# Wed, 10 Mar 2021 01:58:25 GMT
# ARGS: DISTRO_NAME=apache-storm-1.2.3 GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 01:58:25 GMT
WORKDIR /apache-storm-1.2.3
# Wed, 10 Mar 2021 01:58:25 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-1.2.3/bin
# Wed, 10 Mar 2021 01:58:26 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 01:58:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262868e4544c2f89b0140c83d6d6b61447eb8d28d91d63b0cc5d54315f83a45b`  
		Last Modified: Tue, 09 Mar 2021 21:24:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0fec43ba3fb9ef8fefcc0ebb46605f4104ec57bf6538e3c4392db1848e8be4`  
		Last Modified: Tue, 09 Mar 2021 21:25:26 GMT  
		Size: 41.6 MB (41596010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9afd3621fb3d6e7535e1ad327f174886da2db9ff5f0b51812ec5146473d56`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62992ae4518d2a4bd3ff70c36da0d156bfd16a2f73767f620f12b8ea1c6a2b76`  
		Last Modified: Wed, 10 Mar 2021 02:02:25 GMT  
		Size: 13.1 MB (13127010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfe9a48c8cfbc91b71b8b4be52ecbb9621a42abe79042bbe8cb70581b090b38`  
		Last Modified: Wed, 10 Mar 2021 02:02:56 GMT  
		Size: 169.1 MB (169137052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122373e5371da0f7204dd3bf28837109d4cc1d267525c08fdcc197c29f2797f0`  
		Last Modified: Wed, 10 Mar 2021 02:02:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:1.2.3`

```console
$ docker pull storm@sha256:70f698d44de4c7451004c81553c21810fea9bed00316e61c9e1e32c9ca963858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:1.2.3` - linux; amd64

```console
$ docker pull storm@sha256:f0923f5a537d3986422b3a0918efa33822e4f17c3a9f354dc47bf5955af0f534
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254226231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302d358e2354b11f991840790b973034dc35855e1b7b93e08e94c458367224a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:04:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 09 Mar 2021 21:04:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:04:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:04:37 GMT
ENV JAVA_VERSION=8u282
# Tue, 09 Mar 2021 21:05:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jre_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 10 Mar 2021 01:57:28 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:57:29 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:57:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:57:38 GMT
ARG GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
# Wed, 10 Mar 2021 01:58:10 GMT
ARG DISTRO_NAME=apache-storm-1.2.3
# Wed, 10 Mar 2021 01:58:25 GMT
# ARGS: DISTRO_NAME=apache-storm-1.2.3 GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 01:58:25 GMT
WORKDIR /apache-storm-1.2.3
# Wed, 10 Mar 2021 01:58:25 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-1.2.3/bin
# Wed, 10 Mar 2021 01:58:26 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 01:58:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262868e4544c2f89b0140c83d6d6b61447eb8d28d91d63b0cc5d54315f83a45b`  
		Last Modified: Tue, 09 Mar 2021 21:24:21 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0fec43ba3fb9ef8fefcc0ebb46605f4104ec57bf6538e3c4392db1848e8be4`  
		Last Modified: Tue, 09 Mar 2021 21:25:26 GMT  
		Size: 41.6 MB (41596010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9afd3621fb3d6e7535e1ad327f174886da2db9ff5f0b51812ec5146473d56`  
		Last Modified: Wed, 10 Mar 2021 02:02:22 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62992ae4518d2a4bd3ff70c36da0d156bfd16a2f73767f620f12b8ea1c6a2b76`  
		Last Modified: Wed, 10 Mar 2021 02:02:25 GMT  
		Size: 13.1 MB (13127010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfe9a48c8cfbc91b71b8b4be52ecbb9621a42abe79042bbe8cb70581b090b38`  
		Last Modified: Wed, 10 Mar 2021 02:02:56 GMT  
		Size: 169.1 MB (169137052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122373e5371da0f7204dd3bf28837109d4cc1d267525c08fdcc197c29f2797f0`  
		Last Modified: Wed, 10 Mar 2021 02:02:45 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:2.2`

```console
$ docker pull storm@sha256:8f633d6c2c688069c84fc97761d64af5e526d42bcf86b4e27aae399b5216d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:2.2` - linux; amd64

```console
$ docker pull storm@sha256:5483a2a7532aaaed89ec6b78c55951dcf95569e045910028438dff7868381b6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407808002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50072b5447bcdd94dedbee7fa50bbcd236ee1cc368de3cb584eb8c3ab90ad773`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:02:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 09 Mar 2021 21:03:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:03:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:03:01 GMT
ENV JAVA_VERSION=11.0.10
# Tue, 09 Mar 2021 21:03:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 10 Mar 2021 01:58:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:58:30 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:58:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:58:39 GMT
ARG GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
# Wed, 10 Mar 2021 01:58:40 GMT
ARG DISTRO_NAME=apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:56 GMT
# ARGS: DISTRO_NAME=apache-storm-2.2.0 GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 02:01:57 GMT
WORKDIR /apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:57 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.2.0/bin
# Wed, 10 Mar 2021 02:01:57 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 02:01:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067f9902c49d08116077b996d56b7e092a3b61d723bb08811abb7752bbb438b`  
		Last Modified: Tue, 09 Mar 2021 21:21:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4050aab9e2efebf0acd7f0be22bd4fcc1db040313aae07deb0570fedd3f61`  
		Last Modified: Tue, 09 Mar 2021 21:22:28 GMT  
		Size: 47.0 MB (47045736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c9a96e621de5131c2e199ec29a7cef73114b11ed612ba57300f791932125b9`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4786327372006320197593962a9797950e188d4e1860ceee7b99e8d8a7115606`  
		Last Modified: Wed, 10 Mar 2021 02:03:15 GMT  
		Size: 13.1 MB (13127132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c15cea81cc621ac31cdfff4d44627f76336804a25842a7283b5fe8b143a9cf`  
		Last Modified: Wed, 10 Mar 2021 02:03:33 GMT  
		Size: 317.3 MB (317268979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8769eb7923a60d7a26bac14f54c0af71087a257175f33d4abbf6bdd73d9963`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:2.2.0`

```console
$ docker pull storm@sha256:8f633d6c2c688069c84fc97761d64af5e526d42bcf86b4e27aae399b5216d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:2.2.0` - linux; amd64

```console
$ docker pull storm@sha256:5483a2a7532aaaed89ec6b78c55951dcf95569e045910028438dff7868381b6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407808002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50072b5447bcdd94dedbee7fa50bbcd236ee1cc368de3cb584eb8c3ab90ad773`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:02:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 09 Mar 2021 21:03:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:03:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:03:01 GMT
ENV JAVA_VERSION=11.0.10
# Tue, 09 Mar 2021 21:03:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 10 Mar 2021 01:58:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:58:30 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:58:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:58:39 GMT
ARG GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
# Wed, 10 Mar 2021 01:58:40 GMT
ARG DISTRO_NAME=apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:56 GMT
# ARGS: DISTRO_NAME=apache-storm-2.2.0 GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 02:01:57 GMT
WORKDIR /apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:57 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.2.0/bin
# Wed, 10 Mar 2021 02:01:57 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 02:01:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067f9902c49d08116077b996d56b7e092a3b61d723bb08811abb7752bbb438b`  
		Last Modified: Tue, 09 Mar 2021 21:21:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4050aab9e2efebf0acd7f0be22bd4fcc1db040313aae07deb0570fedd3f61`  
		Last Modified: Tue, 09 Mar 2021 21:22:28 GMT  
		Size: 47.0 MB (47045736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c9a96e621de5131c2e199ec29a7cef73114b11ed612ba57300f791932125b9`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4786327372006320197593962a9797950e188d4e1860ceee7b99e8d8a7115606`  
		Last Modified: Wed, 10 Mar 2021 02:03:15 GMT  
		Size: 13.1 MB (13127132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c15cea81cc621ac31cdfff4d44627f76336804a25842a7283b5fe8b143a9cf`  
		Last Modified: Wed, 10 Mar 2021 02:03:33 GMT  
		Size: 317.3 MB (317268979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8769eb7923a60d7a26bac14f54c0af71087a257175f33d4abbf6bdd73d9963`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `storm:latest`

```console
$ docker pull storm@sha256:8f633d6c2c688069c84fc97761d64af5e526d42bcf86b4e27aae399b5216d8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:5483a2a7532aaaed89ec6b78c55951dcf95569e045910028438dff7868381b6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407808002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50072b5447bcdd94dedbee7fa50bbcd236ee1cc368de3cb584eb8c3ab90ad773`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Mar 2021 20:57:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Mar 2021 21:02:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 09 Mar 2021 21:03:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 09 Mar 2021 21:03:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 21:03:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Mar 2021 21:03:01 GMT
ENV JAVA_VERSION=11.0.10
# Tue, 09 Mar 2021 21:03:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 10 Mar 2021 01:58:29 GMT
ENV STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Wed, 10 Mar 2021 01:58:30 GMT
RUN set -eux;     groupadd -r storm --gid=1000;     useradd -r -g storm --uid=1000 storm;     mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR";     chown -R storm:storm "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"``
# Wed, 10 Mar 2021 01:58:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         bash         ca-certificates         dirmngr         gosu         gnupg         python         procps         wget;     rm -rf /var/lib/apt/lists/*;     gosu nobody true
# Wed, 10 Mar 2021 01:58:39 GMT
ARG GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
# Wed, 10 Mar 2021 01:58:40 GMT
ARG DISTRO_NAME=apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:56 GMT
# ARGS: DISTRO_NAME=apache-storm-2.2.0 GPG_KEY=79B03D059E628478FC9F1D8B152CAD0C46E87B61
RUN set -eux;     ddist() {         local f="$1"; shift;         local distFile="$1"; shift;         local success=;         local distUrl=;         for distUrl in             'https://www.apache.org/dyn/closer.cgi?action=download&filename='             https://www-us.apache.org/dist/             https://www.apache.org/dist/             https://archive.apache.org/dist/         ; do             if wget -q -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then                 success=1;                 break;             fi;         done;         [ -n "$success" ];     };     ddist "$DISTRO_NAME.tar.gz" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz";     ddist "$DISTRO_NAME.tar.gz.asc" "storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY" ||     gpg --keyserver pgp.mit.edu --recv-keys "$GPG_KEY" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$GPG_KEY";     gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz";     tar -xzf "$DISTRO_NAME.tar.gz";     rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc";     chown -R storm:storm "$DISTRO_NAME"
# Wed, 10 Mar 2021 02:01:57 GMT
WORKDIR /apache-storm-2.2.0
# Wed, 10 Mar 2021 02:01:57 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/apache-storm-2.2.0/bin
# Wed, 10 Mar 2021 02:01:57 GMT
COPY file:c74c732450146abc9cc672380c7829a8d892099ec5aa1f81e3fe02c4e8f97f32 in / 
# Wed, 10 Mar 2021 02:01:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f1fbf102b7eaa0998133d35bbcc37641d4d23626a4a2673cb9a2393cb7c34c`  
		Last Modified: Tue, 09 Mar 2021 21:10:48 GMT  
		Size: 3.3 MB (3268548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067f9902c49d08116077b996d56b7e092a3b61d723bb08811abb7752bbb438b`  
		Last Modified: Tue, 09 Mar 2021 21:21:09 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4050aab9e2efebf0acd7f0be22bd4fcc1db040313aae07deb0570fedd3f61`  
		Last Modified: Tue, 09 Mar 2021 21:22:28 GMT  
		Size: 47.0 MB (47045736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c9a96e621de5131c2e199ec29a7cef73114b11ed612ba57300f791932125b9`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4786327372006320197593962a9797950e188d4e1860ceee7b99e8d8a7115606`  
		Last Modified: Wed, 10 Mar 2021 02:03:15 GMT  
		Size: 13.1 MB (13127132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c15cea81cc621ac31cdfff4d44627f76336804a25842a7283b5fe8b143a9cf`  
		Last Modified: Wed, 10 Mar 2021 02:03:33 GMT  
		Size: 317.3 MB (317268979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8769eb7923a60d7a26bac14f54c0af71087a257175f33d4abbf6bdd73d9963`  
		Last Modified: Wed, 10 Mar 2021 02:03:12 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
