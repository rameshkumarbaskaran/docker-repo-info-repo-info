## `solr:6-slim`

```console
$ docker pull solr@sha256:1ae383bfa30db29652eb62da75082a9f31412915813611f218dc84fcc8a4f768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `solr:6-slim` - linux; amd64

```console
$ docker pull solr@sha256:6eed179eb42586a20492bf1e3af84b2955e8fa25cd528e56470cef97b71ae09f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225985376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ddac86dcdf4bd59166c543c62b326bafb5eb4032b2353a8176b9db110cc712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:55:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 17 Aug 2021 06:55:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 17 Aug 2021 06:55:47 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:55:47 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:55:47 GMT
ENV JAVA_VERSION=8u302
# Tue, 17 Aug 2021 06:56:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Tue, 17 Aug 2021 20:58:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 17 Aug 2021 20:58:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 17 Aug 2021 20:58:55 GMT
ARG SOLR_VERSION=6.6.6
# Tue, 17 Aug 2021 20:58:56 GMT
ARG SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c
# Tue, 17 Aug 2021 20:58:56 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Tue, 17 Aug 2021 20:58:56 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 17 Aug 2021 20:58:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 17 Aug 2021 20:59:03 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 17 Aug 2021 20:59:03 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/6.6.6/solr-6.6.6.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 20:59:04 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 17 Aug 2021 20:59:06 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 17 Aug 2021 20:59:30 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 17 Aug 2021 20:59:31 GMT
COPY --chown=solr:solrdir:24d14aedda51f56007d2c3091bd65f0167210afaf1c88aa50fac48af9e1d6037 in /opt/docker-solr/scripts 
# Tue, 17 Aug 2021 20:59:31 GMT
EXPOSE 8983
# Tue, 17 Aug 2021 20:59:31 GMT
WORKDIR /opt/solr
# Tue, 17 Aug 2021 20:59:31 GMT
USER solr
# Tue, 17 Aug 2021 20:59:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 20:59:32 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d3ca35fb9a4f8f161dc8b1007db271091ce462aa5a6c8aada7e7096f9857b5`  
		Last Modified: Tue, 17 Aug 2021 07:04:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684a63cea6ad88087bcbba64a242772c2e579702d67656a067619cf4691f0a09`  
		Last Modified: Tue, 17 Aug 2021 07:04:50 GMT  
		Size: 41.6 MB (41641133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b52cf303fdda501b4737b7ea6558b9d5c51c9f52805f48b7f267497ccefcf`  
		Last Modified: Tue, 17 Aug 2021 21:05:52 GMT  
		Size: 6.5 MB (6455314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6d417c065f1b1e52f727bb76a57d81e4ce937784d410bc0bb9f8954576d32`  
		Last Modified: Tue, 17 Aug 2021 21:05:50 GMT  
		Size: 4.3 KB (4285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a4df18213be66516e6a00c4c0b7941f7cba54b65181cb42c6a13e3ecf14617`  
		Last Modified: Tue, 17 Aug 2021 21:05:50 GMT  
		Size: 2.9 KB (2899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c92004b8be1e294f299e529290aa6151bf0b2c5e4ef00fc65c7a45e85f8e89`  
		Last Modified: Tue, 17 Aug 2021 21:06:01 GMT  
		Size: 147.5 MB (147460695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2343f25db98b48bdf84e947caddd79154842c1c7219fcf29dddad0fe43797c69`  
		Last Modified: Tue, 17 Aug 2021 21:05:50 GMT  
		Size: 6.1 KB (6086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
