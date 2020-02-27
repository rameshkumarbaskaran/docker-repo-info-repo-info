## `solr:7-slim`

```console
$ docker pull solr@sha256:b5c8eb037a08ca84d9c674af3118f23e37726c40c0d0f48420b280ab5c4ec4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:7-slim` - linux; amd64

```console
$ docker pull solr@sha256:630df9b02f97e5a32e7662701d1c0f88264848012180a6cb684ecd2e923a1951
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404609368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d303c9882ce21c7c430476a7af15157cca595fbe996185103c97f5fd5127ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 20:15:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:20:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 20:20:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:20:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:20:24 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 20:20:24 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 26 Feb 2020 20:20:24 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 20:20:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:20:43 GMT
CMD ["jshell"]
# Thu, 27 Feb 2020 07:36:10 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Thu, 27 Feb 2020 07:36:10 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 27 Feb 2020 07:39:22 GMT
ARG SOLR_VERSION=7.7.2
# Thu, 27 Feb 2020 07:39:22 GMT
ARG SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85
# Thu, 27 Feb 2020 07:39:22 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Thu, 27 Feb 2020 07:39:22 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 27 Feb 2020 07:39:22 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 27 Feb 2020 07:39:29 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 07:39:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.2/solr-7.7.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 07:39:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 07:39:30 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 27 Feb 2020 07:39:30 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 27 Feb 2020 07:39:30 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Thu, 27 Feb 2020 07:39:31 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 27 Feb 2020 07:39:32 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 27 Feb 2020 07:40:03 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 27 Feb 2020 07:40:04 GMT
COPY --chown=solr:solrdir:ad5f25b55b5e1dd053c2ddf3b986d9715d168efb9fedcd5c63ece6818a1f856a in /opt/docker-solr/scripts 
# Thu, 27 Feb 2020 07:40:04 GMT
EXPOSE 8983
# Thu, 27 Feb 2020 07:40:04 GMT
WORKDIR /opt/solr
# Thu, 27 Feb 2020 07:40:04 GMT
USER solr
# Thu, 27 Feb 2020 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2020 07:40:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4874c5772968dcab87c114bee2baf2c7e9a06dda36e63bdfeab71bd4d6f02890`  
		Last Modified: Wed, 26 Feb 2020 20:23:57 GMT  
		Size: 3.2 MB (3249096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa8e973e226cdc57cde0ef199d85ee1aa93b5f6a04abf68dc4952cdab931d5`  
		Last Modified: Wed, 26 Feb 2020 20:26:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c2579437efd953b28ecb17b4af8bcdb145093663f6935c35a5e2d9344986c6`  
		Last Modified: Wed, 26 Feb 2020 20:27:10 GMT  
		Size: 196.3 MB (196343109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286c03fd4edd0b3a504b8bf6183a679dfbf244f58d093f5cedafbf3d443d731b`  
		Last Modified: Thu, 27 Feb 2020 07:46:24 GMT  
		Size: 5.5 MB (5465770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55d88826d14090e302f9e91135d6c5bcd05dc9df6ad2f01dd54fdd663894b33`  
		Last Modified: Thu, 27 Feb 2020 07:46:23 GMT  
		Size: 4.3 KB (4282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296a10e28a1b654e3c45d73bed1242107cc7d8ddcbe922c6d2d862fc31b21beb`  
		Last Modified: Thu, 27 Feb 2020 07:46:23 GMT  
		Size: 26.6 KB (26564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da72a03cbe5382a5b0b8ae4121582caf4078c1764e8f812540a6c38ff7c2670f`  
		Last Modified: Thu, 27 Feb 2020 07:46:34 GMT  
		Size: 172.4 MB (172422468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027208553faec1e02c98b2730b0a488d31be64ea8598541a094aed2406cd12c1`  
		Last Modified: Thu, 27 Feb 2020 07:46:23 GMT  
		Size: 6.0 KB (6048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:7-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9a4da2ceebb9f54a331200e7d7c0544d9979ace15602a7063ebc8d51493596cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.8 MB (400819979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c056434735f9a6d6be97c46f7b105ac8b9384b4d9e72bd05690193445074d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:51 GMT
ADD file:a93818b0ffcb2823807811dffd78092a3e3f4981aabf48c3cb75f2fa319ac055 in / 
# Wed, 26 Feb 2020 00:46:55 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:56:44 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 14:56:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Feb 2020 14:56:45 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 14:56:47 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 14:56:48 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 26 Feb 2020 14:56:49 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.6%2B10/OpenJDK11U-jdk_
# Wed, 26 Feb 2020 14:56:50 GMT
ENV JAVA_URL_VERSION=11.0.6_10
# Wed, 26 Feb 2020 14:57:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac --version; 	java --version
# Wed, 26 Feb 2020 14:57:29 GMT
CMD ["jshell"]
# Thu, 27 Feb 2020 03:39:11 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Thu, 27 Feb 2020 03:39:11 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 27 Feb 2020 03:50:47 GMT
ARG SOLR_VERSION=7.7.2
# Thu, 27 Feb 2020 03:50:48 GMT
ARG SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85
# Thu, 27 Feb 2020 03:50:51 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Thu, 27 Feb 2020 03:50:52 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 27 Feb 2020 03:50:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 27 Feb 2020 03:51:13 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:51:14 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.2/solr-7.7.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2020 03:51:14 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 03:51:15 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 27 Feb 2020 03:51:16 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 27 Feb 2020 03:51:17 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Thu, 27 Feb 2020 03:51:18 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 27 Feb 2020 03:51:21 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 27 Feb 2020 03:52:12 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 27 Feb 2020 03:52:15 GMT
COPY --chown=solr:solrdir:ad5f25b55b5e1dd053c2ddf3b986d9715d168efb9fedcd5c63ece6818a1f856a in /opt/docker-solr/scripts 
# Thu, 27 Feb 2020 03:52:17 GMT
EXPOSE 8983
# Thu, 27 Feb 2020 03:52:18 GMT
WORKDIR /opt/solr
# Thu, 27 Feb 2020 03:52:19 GMT
USER solr
# Thu, 27 Feb 2020 03:52:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2020 03:52:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f338bc35613f66cfaad272234de7b77a91d6c5422855bf6239f2b0ff9d73f0a4`  
		Last Modified: Wed, 26 Feb 2020 00:56:15 GMT  
		Size: 25.9 MB (25851563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa702e5900f7e9b9cc9f5827bff3c63c77b495471757e961459c43e338147a`  
		Last Modified: Wed, 26 Feb 2020 15:00:01 GMT  
		Size: 3.1 MB (3101218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b200df05fed1b744d2e15b2ec347e0774604f6b6f8073c708edf529bba593b`  
		Last Modified: Wed, 26 Feb 2020 15:00:00 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17eb2a0dd6cb81a29e570c7a7d4474b04214a928ba40e73a4f5c8a76c9433fc`  
		Last Modified: Wed, 26 Feb 2020 15:00:32 GMT  
		Size: 194.0 MB (194015131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab14fb115228d4a29955f3b1450491a88c224933ddf69f1a374de3ab3910341`  
		Last Modified: Thu, 27 Feb 2020 03:57:59 GMT  
		Size: 5.5 MB (5458199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad01c6dd1ac70e324729825d644ada40369cdd1b1fc2fb77c3d4ee9130c5653a`  
		Last Modified: Thu, 27 Feb 2020 03:57:58 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7381391ee849bb665ee0e16c9833ac306d7af74204dba72cdb8ddf8faf390b`  
		Last Modified: Thu, 27 Feb 2020 03:57:58 GMT  
		Size: 26.6 KB (26609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ebbd4c2eb82c80e37342598adae6a2a2ba5e2148e61b07bbd44c21e99c158`  
		Last Modified: Thu, 27 Feb 2020 03:58:17 GMT  
		Size: 172.4 MB (172356652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8c800ba5ab175b65bbe66f688b04ac69a7b308dbe6379e20e0a400ec0e88db`  
		Last Modified: Thu, 27 Feb 2020 03:57:57 GMT  
		Size: 6.1 KB (6074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
