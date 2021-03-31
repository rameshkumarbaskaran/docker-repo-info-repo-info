<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.0`](#couchdb30)
-	[`couchdb:3.0.1`](#couchdb301)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.1`](#couchdb311)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:45a38a46e6e8728605bf4466f2aa292e6730905d98f8f9372336dfd2f1891987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:5b1ad84fee0c4c546cff98a8cb6a3e49382796127da8b67a2bf24105c41acadb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82423394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056ed9e8977a262594f4a12dcdc08fb06a13c6883e15a30f03e9440a404f7f11`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:21:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:21:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:21:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:21:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:21:32 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:21:45 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:21:46 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:22:59 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:22:59 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 23:23:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:23:18 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 23:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:23:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:23:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:23:21 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:23:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d98cadce3a8cf7cacf4d205d1296258f3f689d2d538a182756632c48c5b2ed3`  
		Last Modified: Tue, 30 Mar 2021 23:24:41 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dac62c01d5943a9a1c355517c9fbe20d6d57c447a5c62d075958e01adb39577`  
		Last Modified: Tue, 30 Mar 2021 23:24:43 GMT  
		Size: 8.5 MB (8490021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05b50eec7dc206f06d7ae11c97548e557f1b21256d3155f0afe8e703888308`  
		Last Modified: Tue, 30 Mar 2021 23:24:39 GMT  
		Size: 1.2 MB (1190546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1a00a97f4592f061de96cd04d03f83daaffdcd59b8de2095775360cf456247`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29437eee87ca4211defcd93a2b9081855ac2366fef53928f7febeea8935a808c`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe06f407c40ad08a7685054f672157692d47056b7cae9c19b4930e3aff2b24`  
		Last Modified: Tue, 30 Mar 2021 23:24:47 GMT  
		Size: 50.2 MB (50205097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a75c57724e74ca51e590b6b3f6d767871a4ed76d11d5d2419cdb6d434419b2e`  
		Last Modified: Tue, 30 Mar 2021 23:24:35 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41643bd93e19d1186ae08dbd8b17bda9129dc55e3a38fc28d8222fc65c41933`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452cf68d1be8b8b9c429d3686fa27c4a6fc7029059dab14e2ec1be126788d49`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfbc354d5a37a27ba9fc03fd243632ab18865cc806c6de6546c3094de9073ad`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:279949032079eff4f5389a944140b648fcbe3c1726420df03258a2a5f0a100c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2270bf0fe0baae7dafe8d60452ab815c1e3cff871370a6196d855a82de442cb3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:33:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:33:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:34:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:34:06 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:34:07 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:34:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:34:22 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:34:28 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:34:29 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 22:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:35:05 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:35:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:35:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 22:35:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:35:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:35:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:35:15 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:35:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c8e23905e8c23eabe90895fb77df5b94ce3c5e700b523af5fe7b902ce4d2be`  
		Last Modified: Tue, 30 Mar 2021 22:36:29 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567e392dd97f0063b5cc10c70e8a09d895daae0ec2c22da6b102db37fdaddcf3`  
		Last Modified: Tue, 30 Mar 2021 22:36:30 GMT  
		Size: 7.6 MB (7628949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0ccd49662e651467c8cbfa1d55226d2345992622f15f66d8d845e5e60f9d5`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 1.1 MB (1125051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de031b2ec9b23c62b6fe66e90e177b478e36ffdb776e6177fa57dd3c5e0d7f`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03223e39c8a64b623cf3d221b04b0407fcf7b1e90e148a29a337016b257fe7`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd1f931313353a2da7d5851b9cffbcf5904a0b3c5824dad48e044980076234`  
		Last Modified: Tue, 30 Mar 2021 22:36:37 GMT  
		Size: 47.8 MB (47805336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505838b117e7ce8c8cee6ac19c66490812e2e35961fdb3ae66a22382bb9508df`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4796e29c46272504c9b8fddae3105f7e1a9cb35adfac759d9c4d723377f8b5`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a8722d9914190a6380e80df28b780af85cf9e7055ab45cbe7ee013e3ff24b7`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390199b6dd0ff74ea6fb1657da91899f14b0841c298d35c5ca61b126528ebf1`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:45a38a46e6e8728605bf4466f2aa292e6730905d98f8f9372336dfd2f1891987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:5b1ad84fee0c4c546cff98a8cb6a3e49382796127da8b67a2bf24105c41acadb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82423394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056ed9e8977a262594f4a12dcdc08fb06a13c6883e15a30f03e9440a404f7f11`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:21:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:21:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:21:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:21:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:21:32 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:21:45 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:21:46 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:22:59 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:22:59 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 23:23:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:23:18 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 23:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:23:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:23:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:23:21 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:23:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d98cadce3a8cf7cacf4d205d1296258f3f689d2d538a182756632c48c5b2ed3`  
		Last Modified: Tue, 30 Mar 2021 23:24:41 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dac62c01d5943a9a1c355517c9fbe20d6d57c447a5c62d075958e01adb39577`  
		Last Modified: Tue, 30 Mar 2021 23:24:43 GMT  
		Size: 8.5 MB (8490021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05b50eec7dc206f06d7ae11c97548e557f1b21256d3155f0afe8e703888308`  
		Last Modified: Tue, 30 Mar 2021 23:24:39 GMT  
		Size: 1.2 MB (1190546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1a00a97f4592f061de96cd04d03f83daaffdcd59b8de2095775360cf456247`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29437eee87ca4211defcd93a2b9081855ac2366fef53928f7febeea8935a808c`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe06f407c40ad08a7685054f672157692d47056b7cae9c19b4930e3aff2b24`  
		Last Modified: Tue, 30 Mar 2021 23:24:47 GMT  
		Size: 50.2 MB (50205097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a75c57724e74ca51e590b6b3f6d767871a4ed76d11d5d2419cdb6d434419b2e`  
		Last Modified: Tue, 30 Mar 2021 23:24:35 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41643bd93e19d1186ae08dbd8b17bda9129dc55e3a38fc28d8222fc65c41933`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452cf68d1be8b8b9c429d3686fa27c4a6fc7029059dab14e2ec1be126788d49`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfbc354d5a37a27ba9fc03fd243632ab18865cc806c6de6546c3094de9073ad`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:279949032079eff4f5389a944140b648fcbe3c1726420df03258a2a5f0a100c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2270bf0fe0baae7dafe8d60452ab815c1e3cff871370a6196d855a82de442cb3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:33:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:33:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:34:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:34:06 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:34:07 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:34:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:34:22 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:34:28 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:34:29 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 22:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:35:05 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:35:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:35:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 22:35:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:35:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:35:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:35:15 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:35:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c8e23905e8c23eabe90895fb77df5b94ce3c5e700b523af5fe7b902ce4d2be`  
		Last Modified: Tue, 30 Mar 2021 22:36:29 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567e392dd97f0063b5cc10c70e8a09d895daae0ec2c22da6b102db37fdaddcf3`  
		Last Modified: Tue, 30 Mar 2021 22:36:30 GMT  
		Size: 7.6 MB (7628949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0ccd49662e651467c8cbfa1d55226d2345992622f15f66d8d845e5e60f9d5`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 1.1 MB (1125051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de031b2ec9b23c62b6fe66e90e177b478e36ffdb776e6177fa57dd3c5e0d7f`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03223e39c8a64b623cf3d221b04b0407fcf7b1e90e148a29a337016b257fe7`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd1f931313353a2da7d5851b9cffbcf5904a0b3c5824dad48e044980076234`  
		Last Modified: Tue, 30 Mar 2021 22:36:37 GMT  
		Size: 47.8 MB (47805336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505838b117e7ce8c8cee6ac19c66490812e2e35961fdb3ae66a22382bb9508df`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4796e29c46272504c9b8fddae3105f7e1a9cb35adfac759d9c4d723377f8b5`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a8722d9914190a6380e80df28b780af85cf9e7055ab45cbe7ee013e3ff24b7`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390199b6dd0ff74ea6fb1657da91899f14b0841c298d35c5ca61b126528ebf1`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:45a38a46e6e8728605bf4466f2aa292e6730905d98f8f9372336dfd2f1891987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:5b1ad84fee0c4c546cff98a8cb6a3e49382796127da8b67a2bf24105c41acadb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82423394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056ed9e8977a262594f4a12dcdc08fb06a13c6883e15a30f03e9440a404f7f11`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:21:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:21:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:21:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:21:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:21:32 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:21:45 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:21:46 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:22:59 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:22:59 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 23:23:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:23:18 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:23:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 23:23:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:23:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:23:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:23:21 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:23:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d98cadce3a8cf7cacf4d205d1296258f3f689d2d538a182756632c48c5b2ed3`  
		Last Modified: Tue, 30 Mar 2021 23:24:41 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dac62c01d5943a9a1c355517c9fbe20d6d57c447a5c62d075958e01adb39577`  
		Last Modified: Tue, 30 Mar 2021 23:24:43 GMT  
		Size: 8.5 MB (8490021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05b50eec7dc206f06d7ae11c97548e557f1b21256d3155f0afe8e703888308`  
		Last Modified: Tue, 30 Mar 2021 23:24:39 GMT  
		Size: 1.2 MB (1190546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1a00a97f4592f061de96cd04d03f83daaffdcd59b8de2095775360cf456247`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29437eee87ca4211defcd93a2b9081855ac2366fef53928f7febeea8935a808c`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe06f407c40ad08a7685054f672157692d47056b7cae9c19b4930e3aff2b24`  
		Last Modified: Tue, 30 Mar 2021 23:24:47 GMT  
		Size: 50.2 MB (50205097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a75c57724e74ca51e590b6b3f6d767871a4ed76d11d5d2419cdb6d434419b2e`  
		Last Modified: Tue, 30 Mar 2021 23:24:35 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41643bd93e19d1186ae08dbd8b17bda9129dc55e3a38fc28d8222fc65c41933`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452cf68d1be8b8b9c429d3686fa27c4a6fc7029059dab14e2ec1be126788d49`  
		Last Modified: Tue, 30 Mar 2021 23:24:38 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfbc354d5a37a27ba9fc03fd243632ab18865cc806c6de6546c3094de9073ad`  
		Last Modified: Tue, 30 Mar 2021 23:24:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:279949032079eff4f5389a944140b648fcbe3c1726420df03258a2a5f0a100c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2270bf0fe0baae7dafe8d60452ab815c1e3cff871370a6196d855a82de442cb3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:13 GMT
ADD file:6c50a12d856589b3002e4262ecb952f6fe3fd89eddc1f9c23391aa0f6228f6ac in / 
# Tue, 30 Mar 2021 21:50:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:33:42 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:33:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:34:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:34:06 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:34:07 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:34:21 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:34:22 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:34:28 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:34:29 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 30 Mar 2021 22:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:35:05 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:35:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:35:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 30 Mar 2021 22:35:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:35:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:35:14 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:35:15 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:35:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:723b7d0e9b209513e3eedf36e7b5f2cab85bc1bb7d8fbee1286ee2a0e982ddda`  
		Last Modified: Tue, 30 Mar 2021 21:57:06 GMT  
		Size: 20.4 MB (20389310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c8e23905e8c23eabe90895fb77df5b94ce3c5e700b523af5fe7b902ce4d2be`  
		Last Modified: Tue, 30 Mar 2021 22:36:29 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567e392dd97f0063b5cc10c70e8a09d895daae0ec2c22da6b102db37fdaddcf3`  
		Last Modified: Tue, 30 Mar 2021 22:36:30 GMT  
		Size: 7.6 MB (7628949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0ccd49662e651467c8cbfa1d55226d2345992622f15f66d8d845e5e60f9d5`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 1.1 MB (1125051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de031b2ec9b23c62b6fe66e90e177b478e36ffdb776e6177fa57dd3c5e0d7f`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03223e39c8a64b623cf3d221b04b0407fcf7b1e90e148a29a337016b257fe7`  
		Last Modified: Tue, 30 Mar 2021 22:36:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd1f931313353a2da7d5851b9cffbcf5904a0b3c5824dad48e044980076234`  
		Last Modified: Tue, 30 Mar 2021 22:36:37 GMT  
		Size: 47.8 MB (47805336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505838b117e7ce8c8cee6ac19c66490812e2e35961fdb3ae66a22382bb9508df`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4796e29c46272504c9b8fddae3105f7e1a9cb35adfac759d9c4d723377f8b5`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a8722d9914190a6380e80df28b780af85cf9e7055ab45cbe7ee013e3ff24b7`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e390199b6dd0ff74ea6fb1657da91899f14b0841c298d35c5ca61b126528ebf1`  
		Last Modified: Tue, 30 Mar 2021 22:36:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9fa42057a18c07ba752cb729c7ecd748e223b21fa2a3fafac66db80acc87ac19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:109605e6cc9ed28c0fb7e7ff140a2803f84d19b3cee0e5617761c3b45b1672b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83405507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6763bc849b3616fc568c8ba36a94ee3d774acfdf642db2dc831783a75950f9f2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:03 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 23:20:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:20:26 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:20:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:20:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:20:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:20:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:20:30 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:20:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b711f28e3802cafa75ec03e72df83d1a09437b9c47b76c8d36b33c592c70d6`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e95ac563f98d2cedd7bb6735e3132e1d8743fd823a8f7649e04b61980938c`  
		Last Modified: Tue, 30 Mar 2021 23:23:56 GMT  
		Size: 48.4 MB (48373188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb98448f1f51129e6125e41f2f572cf1caf7feeaf040ea62fafbe9f0b7bcd7d`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750636c2569f383d2117128b05859f4b68fef9f2c5c83c6e25db61cfc93e343e`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e302f906e55f5ffe05ed7ecc1e04c7c4a40f9bf4e3dfb21d92fbf34bfa1ad9f1`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e10ff52f24fe0401b55359e81ab3c0ad9e0553131b0b876c3182d9802876fa`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a1b8626d92b5896a5862bf75f24a3cc96e3e3e8d92992f2c0dacc52477d78ea6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78447250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d358ae3ee30dc9cdcd168d84b74fb7cd1f6dc198a862fe2854aec95b8550d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:31:56 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 22:31:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:32:20 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:32:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:32:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:32:24 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:32:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:32:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:32:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:32:31 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:32:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8812431571d7831e615ee3ddc48eeeed6d46370149d4706b5481fe803bfea46a`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b792a6db484672b083412b36c49b049246739079c9e2d374681a8032efa40`  
		Last Modified: Tue, 30 Mar 2021 22:35:53 GMT  
		Size: 44.9 MB (44855799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ff67237eddd174e97acf6f02ad56f0e38d094240cdd9311815ea7364e9c4c1`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0a92e480e31d7eacf9dc3b8372716a4525467a6ad0b865aff0beaa1cec522`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e774112921aeb3a6fc19fbd212be2fb485966f4e6d9e287f86a4cdad9a26bf`  
		Last Modified: Tue, 30 Mar 2021 22:35:44 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b2498856cfba64ffc8a87a061aa0affa53df2f40b8bf38f468ce5cf08d4983`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:e359609265745bed67e2ba6d225e7c84c1b545865c0c18525ef1f436b81155a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:320d00d2af1d57c18345de56639759e070c183ad8a0af0315ee04f0119ef0442
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83263284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dd072676e28e4132679a14ebdd0911f0c44ef10a1dcc6ca7404ebdd8187b4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:40 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 30 Mar 2021 23:20:42 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:21:02 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:21:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:21:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:21:04 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:21:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:21:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:21:07 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:21:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc493669419c8b170039da15f8bf009eb64509e633d8b1d329a6ff6e504d7e4`  
		Last Modified: Tue, 30 Mar 2021 23:24:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50830ba35b442eb6efbb8fb75192317025b37da24098012a829ea0a6067f0d`  
		Last Modified: Tue, 30 Mar 2021 23:24:23 GMT  
		Size: 48.2 MB (48230972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0f8c8b4c0bf339114cdfd18b91d0fa900d3078380586fd95e5519319c3593`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b9eeb95e5266beb8a3065ea2a442333ebefcbba619eee889a7e38e89b8572c`  
		Last Modified: Tue, 30 Mar 2021 23:24:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66e4e279519bfee40ad4f5b46532c292aca54238fa33a5d904ac94ed2b5c5bf`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6cf2c9b5ec46e7e595d37c1ca3f6405bdcec76fd873a0bf361fa27d9a88787`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0c0dc8167a975d29e45826f2335f2ed6b691a62fc09ab99416f3f1924151addf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78299913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456671f3880740b73b65f4dd904da57609ed685f407254eb1e5d3e619191289`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:32:53 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 30 Mar 2021 22:32:56 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:33:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:33:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:33:23 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:33:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:33:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:33:28 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:33:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68332489640b80e2dace2aceeed4cfaef58f98655836dc393f69c9595e0b30bb`  
		Last Modified: Tue, 30 Mar 2021 22:36:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e32aa990b281cac3253978dbaa41e197f190f212eedec69b61d17891e3213a`  
		Last Modified: Tue, 30 Mar 2021 22:36:18 GMT  
		Size: 44.7 MB (44708458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a63bb689b9426cbbf0d89d0733931da0a4606cf84bb80d888524c5dbc8259c3`  
		Last Modified: Tue, 30 Mar 2021 22:36:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4c069e02e1a61116d1127e03767aa2b432ebe7d003c0c4eae0ce0a5a146345`  
		Last Modified: Tue, 30 Mar 2021 22:36:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8525b8050db2f5c6c8c778373473d340750c290c58e06ce00ad62e10fffd45`  
		Last Modified: Tue, 30 Mar 2021 22:36:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce08cde74d128d1cf8ec3f2de803f31ec545312e49179dea564a77e802ec133b`  
		Last Modified: Tue, 30 Mar 2021 22:36:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.1`

```console
$ docker pull couchdb@sha256:e359609265745bed67e2ba6d225e7c84c1b545865c0c18525ef1f436b81155a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.0.1` - linux; amd64

```console
$ docker pull couchdb@sha256:320d00d2af1d57c18345de56639759e070c183ad8a0af0315ee04f0119ef0442
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83263284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dd072676e28e4132679a14ebdd0911f0c44ef10a1dcc6ca7404ebdd8187b4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:40 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 30 Mar 2021 23:20:42 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:21:02 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:21:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:21:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:21:04 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:21:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:21:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:21:07 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:21:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc493669419c8b170039da15f8bf009eb64509e633d8b1d329a6ff6e504d7e4`  
		Last Modified: Tue, 30 Mar 2021 23:24:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50830ba35b442eb6efbb8fb75192317025b37da24098012a829ea0a6067f0d`  
		Last Modified: Tue, 30 Mar 2021 23:24:23 GMT  
		Size: 48.2 MB (48230972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d0f8c8b4c0bf339114cdfd18b91d0fa900d3078380586fd95e5519319c3593`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b9eeb95e5266beb8a3065ea2a442333ebefcbba619eee889a7e38e89b8572c`  
		Last Modified: Tue, 30 Mar 2021 23:24:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66e4e279519bfee40ad4f5b46532c292aca54238fa33a5d904ac94ed2b5c5bf`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6cf2c9b5ec46e7e595d37c1ca3f6405bdcec76fd873a0bf361fa27d9a88787`  
		Last Modified: Tue, 30 Mar 2021 23:24:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0c0dc8167a975d29e45826f2335f2ed6b691a62fc09ab99416f3f1924151addf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78299913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8456671f3880740b73b65f4dd904da57609ed685f407254eb1e5d3e619191289`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:32:53 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 30 Mar 2021 22:32:56 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:33:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:33:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:33:23 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:33:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:33:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:33:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:33:28 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:33:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68332489640b80e2dace2aceeed4cfaef58f98655836dc393f69c9595e0b30bb`  
		Last Modified: Tue, 30 Mar 2021 22:36:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e32aa990b281cac3253978dbaa41e197f190f212eedec69b61d17891e3213a`  
		Last Modified: Tue, 30 Mar 2021 22:36:18 GMT  
		Size: 44.7 MB (44708458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a63bb689b9426cbbf0d89d0733931da0a4606cf84bb80d888524c5dbc8259c3`  
		Last Modified: Tue, 30 Mar 2021 22:36:12 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4c069e02e1a61116d1127e03767aa2b432ebe7d003c0c4eae0ce0a5a146345`  
		Last Modified: Tue, 30 Mar 2021 22:36:10 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8525b8050db2f5c6c8c778373473d340750c290c58e06ce00ad62e10fffd45`  
		Last Modified: Tue, 30 Mar 2021 22:36:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce08cde74d128d1cf8ec3f2de803f31ec545312e49179dea564a77e802ec133b`  
		Last Modified: Tue, 30 Mar 2021 22:36:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:9fa42057a18c07ba752cb729c7ecd748e223b21fa2a3fafac66db80acc87ac19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:109605e6cc9ed28c0fb7e7ff140a2803f84d19b3cee0e5617761c3b45b1672b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83405507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6763bc849b3616fc568c8ba36a94ee3d774acfdf642db2dc831783a75950f9f2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:03 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 23:20:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:20:26 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:20:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:20:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:20:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:20:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:20:30 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:20:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b711f28e3802cafa75ec03e72df83d1a09437b9c47b76c8d36b33c592c70d6`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e95ac563f98d2cedd7bb6735e3132e1d8743fd823a8f7649e04b61980938c`  
		Last Modified: Tue, 30 Mar 2021 23:23:56 GMT  
		Size: 48.4 MB (48373188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb98448f1f51129e6125e41f2f572cf1caf7feeaf040ea62fafbe9f0b7bcd7d`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750636c2569f383d2117128b05859f4b68fef9f2c5c83c6e25db61cfc93e343e`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e302f906e55f5ffe05ed7ecc1e04c7c4a40f9bf4e3dfb21d92fbf34bfa1ad9f1`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e10ff52f24fe0401b55359e81ab3c0ad9e0553131b0b876c3182d9802876fa`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a1b8626d92b5896a5862bf75f24a3cc96e3e3e8d92992f2c0dacc52477d78ea6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78447250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d358ae3ee30dc9cdcd168d84b74fb7cd1f6dc198a862fe2854aec95b8550d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:31:56 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 22:31:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:32:20 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:32:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:32:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:32:24 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:32:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:32:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:32:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:32:31 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:32:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8812431571d7831e615ee3ddc48eeeed6d46370149d4706b5481fe803bfea46a`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b792a6db484672b083412b36c49b049246739079c9e2d374681a8032efa40`  
		Last Modified: Tue, 30 Mar 2021 22:35:53 GMT  
		Size: 44.9 MB (44855799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ff67237eddd174e97acf6f02ad56f0e38d094240cdd9311815ea7364e9c4c1`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0a92e480e31d7eacf9dc3b8372716a4525467a6ad0b865aff0beaa1cec522`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e774112921aeb3a6fc19fbd212be2fb485966f4e6d9e287f86a4cdad9a26bf`  
		Last Modified: Tue, 30 Mar 2021 22:35:44 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b2498856cfba64ffc8a87a061aa0affa53df2f40b8bf38f468ce5cf08d4983`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.1`

```console
$ docker pull couchdb@sha256:9fa42057a18c07ba752cb729c7ecd748e223b21fa2a3fafac66db80acc87ac19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.1` - linux; amd64

```console
$ docker pull couchdb@sha256:109605e6cc9ed28c0fb7e7ff140a2803f84d19b3cee0e5617761c3b45b1672b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83405507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6763bc849b3616fc568c8ba36a94ee3d774acfdf642db2dc831783a75950f9f2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:03 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 23:20:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:20:26 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:20:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:20:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:20:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:20:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:20:30 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:20:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b711f28e3802cafa75ec03e72df83d1a09437b9c47b76c8d36b33c592c70d6`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e95ac563f98d2cedd7bb6735e3132e1d8743fd823a8f7649e04b61980938c`  
		Last Modified: Tue, 30 Mar 2021 23:23:56 GMT  
		Size: 48.4 MB (48373188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb98448f1f51129e6125e41f2f572cf1caf7feeaf040ea62fafbe9f0b7bcd7d`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750636c2569f383d2117128b05859f4b68fef9f2c5c83c6e25db61cfc93e343e`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e302f906e55f5ffe05ed7ecc1e04c7c4a40f9bf4e3dfb21d92fbf34bfa1ad9f1`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e10ff52f24fe0401b55359e81ab3c0ad9e0553131b0b876c3182d9802876fa`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a1b8626d92b5896a5862bf75f24a3cc96e3e3e8d92992f2c0dacc52477d78ea6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78447250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d358ae3ee30dc9cdcd168d84b74fb7cd1f6dc198a862fe2854aec95b8550d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:31:56 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 22:31:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:32:20 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:32:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:32:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:32:24 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:32:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:32:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:32:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:32:31 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:32:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8812431571d7831e615ee3ddc48eeeed6d46370149d4706b5481fe803bfea46a`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b792a6db484672b083412b36c49b049246739079c9e2d374681a8032efa40`  
		Last Modified: Tue, 30 Mar 2021 22:35:53 GMT  
		Size: 44.9 MB (44855799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ff67237eddd174e97acf6f02ad56f0e38d094240cdd9311815ea7364e9c4c1`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0a92e480e31d7eacf9dc3b8372716a4525467a6ad0b865aff0beaa1cec522`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e774112921aeb3a6fc19fbd212be2fb485966f4e6d9e287f86a4cdad9a26bf`  
		Last Modified: Tue, 30 Mar 2021 22:35:44 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b2498856cfba64ffc8a87a061aa0affa53df2f40b8bf38f468ce5cf08d4983`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9fa42057a18c07ba752cb729c7ecd748e223b21fa2a3fafac66db80acc87ac19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:109605e6cc9ed28c0fb7e7ff140a2803f84d19b3cee0e5617761c3b45b1672b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83405507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6763bc849b3616fc568c8ba36a94ee3d774acfdf642db2dc831783a75950f9f2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:19:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 23:19:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 23:19:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:19:49 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 23:19:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 23:20:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 23:20:00 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 23:20:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 23:20:03 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 23:20:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 23:20:26 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 23:20:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 23:20:27 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 23:20:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 23:20:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 23:20:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 23:20:30 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 23:20:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a43bed8daf3f1411d84dfee77cd96971ded64e167627fb6f96e3d317f91e82`  
		Last Modified: Tue, 30 Mar 2021 23:23:55 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226feb4f47e0808452e1bf69f56c5f01350896a6bc369e1ebde3f91df57d8ba6`  
		Last Modified: Tue, 30 Mar 2021 23:23:54 GMT  
		Size: 6.7 MB (6690684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede2b415de4315c555ee81767597beea652504ddacaa4a185968392e88d7d190`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 1.2 MB (1192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8f93aac6aa8272708935f621ac7e138518557d2852018eb582cc740fa79ead`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b711f28e3802cafa75ec03e72df83d1a09437b9c47b76c8d36b33c592c70d6`  
		Last Modified: Tue, 30 Mar 2021 23:23:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e95ac563f98d2cedd7bb6735e3132e1d8743fd823a8f7649e04b61980938c`  
		Last Modified: Tue, 30 Mar 2021 23:23:56 GMT  
		Size: 48.4 MB (48373188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb98448f1f51129e6125e41f2f572cf1caf7feeaf040ea62fafbe9f0b7bcd7d`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750636c2569f383d2117128b05859f4b68fef9f2c5c83c6e25db61cfc93e343e`  
		Last Modified: Tue, 30 Mar 2021 23:23:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e302f906e55f5ffe05ed7ecc1e04c7c4a40f9bf4e3dfb21d92fbf34bfa1ad9f1`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e10ff52f24fe0401b55359e81ab3c0ad9e0553131b0b876c3182d9802876fa`  
		Last Modified: Tue, 30 Mar 2021 23:23:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a1b8626d92b5896a5862bf75f24a3cc96e3e3e8d92992f2c0dacc52477d78ea6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78447250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d358ae3ee30dc9cdcd168d84b74fb7cd1f6dc198a862fe2854aec95b8550d0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 30 Mar 2021 21:47:15 GMT
ADD file:a9b57ded2400fc7f60ea40e5ccdd3e9bf0f72acfcc47223ceb66b4fa16955059 in / 
# Tue, 30 Mar 2021 21:47:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 30 Mar 2021 22:31:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 30 Mar 2021 22:31:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:31:39 GMT
ENV GOSU_VERSION=1.11
# Tue, 30 Mar 2021 22:31:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Mar 2021 22:31:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 30 Mar 2021 22:31:53 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 30 Mar 2021 22:31:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 30 Mar 2021 22:31:56 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 30 Mar 2021 22:31:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 30 Mar 2021 22:32:20 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 30 Mar 2021 22:32:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 30 Mar 2021 22:32:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 30 Mar 2021 22:32:24 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 30 Mar 2021 22:32:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 30 Mar 2021 22:32:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 30 Mar 2021 22:32:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 30 Mar 2021 22:32:31 GMT
EXPOSE 4369 5984 9100
# Tue, 30 Mar 2021 22:32:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6fcf2156bc23db75595b822b865fbc962ed6f4521dec8cae509e66742a6a5ad3`  
		Last Modified: Tue, 30 Mar 2021 21:54:27 GMT  
		Size: 25.9 MB (25904513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cd979a49aa447de970c8cf22111075b145f3d7097be5c374828b879c4b7ef4`  
		Last Modified: Tue, 30 Mar 2021 22:35:50 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ace878928f7573e0acee7ddb3d011bd3c7fa8dbd948c62da3f0474a552b896a`  
		Last Modified: Tue, 30 Mar 2021 22:35:49 GMT  
		Size: 6.6 MB (6550259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3b5d74649db1f3e4b98f407c232293e2332f06b6ef6f1240dce7c6f56c3217`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 1.1 MB (1127209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ec2f69f75fc2660271a70899d73a83ab88fb86109843389913522232dbe8e`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8812431571d7831e615ee3ddc48eeeed6d46370149d4706b5481fe803bfea46a`  
		Last Modified: Tue, 30 Mar 2021 22:35:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b792a6db484672b083412b36c49b049246739079c9e2d374681a8032efa40`  
		Last Modified: Tue, 30 Mar 2021 22:35:53 GMT  
		Size: 44.9 MB (44855799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ff67237eddd174e97acf6f02ad56f0e38d094240cdd9311815ea7364e9c4c1`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a0a92e480e31d7eacf9dc3b8372716a4525467a6ad0b865aff0beaa1cec522`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e774112921aeb3a6fc19fbd212be2fb485966f4e6d9e287f86a4cdad9a26bf`  
		Last Modified: Tue, 30 Mar 2021 22:35:44 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b2498856cfba64ffc8a87a061aa0affa53df2f40b8bf38f468ce5cf08d4983`  
		Last Modified: Tue, 30 Mar 2021 22:35:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
