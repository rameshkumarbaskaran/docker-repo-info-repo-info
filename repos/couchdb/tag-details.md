<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.0`](#couchdb30)
-	[`couchdb:3.0.0`](#couchdb300)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:72df800f97113bfce2516f9f05ea6c7d8241e2a4198b06ab0619e347becf2f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:b877af600e293895f04c59e49e685dee7fa7aaf4bcfafb516491ebd1d9152543
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82429326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350347cb484e1547188c36bbe2dd1b3ee7c081ac1f05a85c92e9562bb25637`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:12:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Feb 2020 02:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:08:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:08:32 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:08:33 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:08:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:08:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:08:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:08:45 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 27 Feb 2020 08:08:46 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:09:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:09:06 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 27 Feb 2020 08:09:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:09:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:09:08 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:09:08 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:09:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6e27e7e388472b48cf83765a4f27fa4615fd380f386d82a7eeee2fba34070`  
		Last Modified: Wed, 26 Feb 2020 02:14:37 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5abda8b4a3e62a2faddff8d21372fd32b94a032ded88f27d3010e505e1b9e`  
		Last Modified: Thu, 27 Feb 2020 08:09:34 GMT  
		Size: 8.5 MB (8515111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bebdbf0d037d803d51fae63b193e7e2b4458370919ebab58ed24fbf3a1615ce`  
		Last Modified: Thu, 27 Feb 2020 08:09:33 GMT  
		Size: 1.2 MB (1190689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe5c72aa46503572e798c8500c0de0e0c7f999865ad8798405b7b1b076e666`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826e8450a2f98b70aa71cd68585774411c45f3ed5b91bfaec1263028df3918b7`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b532c77aaab49f250eb837693e426a98cb275fa3259bceb41e1385d6e2b0b003`  
		Last Modified: Thu, 27 Feb 2020 08:09:39 GMT  
		Size: 50.2 MB (50200707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082543d2064fca725b468e48a674bace29f627213e0307d75d00ac5899f6b055`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ef01c661ae73c09a102d8dc655a487197bb3ed38e5a1acefc7481d6d660890`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc430133d600fe359c6ddff8ab2bf5ce8db9731797e36aa557dc528a24ca390e`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97babb4122712dd6b11da70f42fc6ca414813f0d426f8eaaac4ccbf4677324`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:72df800f97113bfce2516f9f05ea6c7d8241e2a4198b06ab0619e347becf2f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:b877af600e293895f04c59e49e685dee7fa7aaf4bcfafb516491ebd1d9152543
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82429326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350347cb484e1547188c36bbe2dd1b3ee7c081ac1f05a85c92e9562bb25637`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:12:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Feb 2020 02:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:08:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:08:32 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:08:33 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:08:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:08:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:08:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:08:45 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 27 Feb 2020 08:08:46 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:09:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:09:06 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 27 Feb 2020 08:09:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:09:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:09:08 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:09:08 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:09:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6e27e7e388472b48cf83765a4f27fa4615fd380f386d82a7eeee2fba34070`  
		Last Modified: Wed, 26 Feb 2020 02:14:37 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5abda8b4a3e62a2faddff8d21372fd32b94a032ded88f27d3010e505e1b9e`  
		Last Modified: Thu, 27 Feb 2020 08:09:34 GMT  
		Size: 8.5 MB (8515111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bebdbf0d037d803d51fae63b193e7e2b4458370919ebab58ed24fbf3a1615ce`  
		Last Modified: Thu, 27 Feb 2020 08:09:33 GMT  
		Size: 1.2 MB (1190689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe5c72aa46503572e798c8500c0de0e0c7f999865ad8798405b7b1b076e666`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826e8450a2f98b70aa71cd68585774411c45f3ed5b91bfaec1263028df3918b7`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b532c77aaab49f250eb837693e426a98cb275fa3259bceb41e1385d6e2b0b003`  
		Last Modified: Thu, 27 Feb 2020 08:09:39 GMT  
		Size: 50.2 MB (50200707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082543d2064fca725b468e48a674bace29f627213e0307d75d00ac5899f6b055`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ef01c661ae73c09a102d8dc655a487197bb3ed38e5a1acefc7481d6d660890`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc430133d600fe359c6ddff8ab2bf5ce8db9731797e36aa557dc528a24ca390e`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97babb4122712dd6b11da70f42fc6ca414813f0d426f8eaaac4ccbf4677324`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:72df800f97113bfce2516f9f05ea6c7d8241e2a4198b06ab0619e347becf2f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:b877af600e293895f04c59e49e685dee7fa7aaf4bcfafb516491ebd1d9152543
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82429326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23350347cb484e1547188c36bbe2dd1b3ee7c081ac1f05a85c92e9562bb25637`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:12:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Feb 2020 02:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:08:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:08:32 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:08:33 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:08:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:08:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:08:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:08:45 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 27 Feb 2020 08:08:46 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:09:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:09:06 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:09:07 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 27 Feb 2020 08:09:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:09:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:09:08 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:09:08 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:09:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6e27e7e388472b48cf83765a4f27fa4615fd380f386d82a7eeee2fba34070`  
		Last Modified: Wed, 26 Feb 2020 02:14:37 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b5abda8b4a3e62a2faddff8d21372fd32b94a032ded88f27d3010e505e1b9e`  
		Last Modified: Thu, 27 Feb 2020 08:09:34 GMT  
		Size: 8.5 MB (8515111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bebdbf0d037d803d51fae63b193e7e2b4458370919ebab58ed24fbf3a1615ce`  
		Last Modified: Thu, 27 Feb 2020 08:09:33 GMT  
		Size: 1.2 MB (1190689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe5c72aa46503572e798c8500c0de0e0c7f999865ad8798405b7b1b076e666`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826e8450a2f98b70aa71cd68585774411c45f3ed5b91bfaec1263028df3918b7`  
		Last Modified: Thu, 27 Feb 2020 08:09:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b532c77aaab49f250eb837693e426a98cb275fa3259bceb41e1385d6e2b0b003`  
		Last Modified: Thu, 27 Feb 2020 08:09:39 GMT  
		Size: 50.2 MB (50200707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082543d2064fca725b468e48a674bace29f627213e0307d75d00ac5899f6b055`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ef01c661ae73c09a102d8dc655a487197bb3ed38e5a1acefc7481d6d660890`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc430133d600fe359c6ddff8ab2bf5ce8db9731797e36aa557dc528a24ca390e`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97babb4122712dd6b11da70f42fc6ca414813f0d426f8eaaac4ccbf4677324`  
		Last Modified: Thu, 27 Feb 2020 08:09:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9a04017623a7ac09f355f523522f51c617558a0ca642f71dff4c96cd4b7bfb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:be21b69c55178641d3a4349f1e913115b863fc50f1a048962d0b1fd04f395c38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82329758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b547df9dfc1448448c80a57f3c7ed76dc366b06430507960cbb0424ca4a36c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Thu, 27 Feb 2020 08:07:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 27 Feb 2020 08:07:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:07:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:07:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:07:50 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:07:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:07:56 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:07:57 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:07:57 GMT
ENV COUCHDB_VERSION=3.0.0
# Thu, 27 Feb 2020 08:07:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:08:13 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 27 Feb 2020 08:08:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:08:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:08:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:08:15 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:08:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b53e02635d8416b196c9fe115804b4dc8943eabcc4804e516cf617f73eab91`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b2c6707d6f654831a47885d7285814124b3918f32df47209a41e22658f999`  
		Last Modified: Thu, 27 Feb 2020 08:09:22 GMT  
		Size: 6.7 MB (6669970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476af73bc07748b5d44dca190a7aebe3b3f1c4df87d94b31348544e03a105c97`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 1.2 MB (1192657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9097bacd3cb959d27a1255b8ce0c153da110462b820aee8eb4a8fd54f90c1d`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1735d1e02fcb398d6befed3863406252ebc094b9b1d4f56b5e1ccf73975f97`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d290ca762469cd7dc8fade671d4565d0ffa7846499ce0896163d0031aba9c5e`  
		Last Modified: Thu, 27 Feb 2020 08:09:25 GMT  
		Size: 47.4 MB (47365869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61019970e8209e99565e63aec224cfb0f1c0ec124497b05a9dbe6225e797727b`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efd4f928fc2eb12d8fe8e0fe88585d2fc7dbceedd3622e75979c957ee517061`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2de1ec2ac9a6ca190a9b1c101726e25cc0bcbbdf51d44f8f11e15f1f3ab5341`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b2b47b6f3dec92716a21ebee72dec0c67d3ced282154d71575615dfaa7575e`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:9a04017623a7ac09f355f523522f51c617558a0ca642f71dff4c96cd4b7bfb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:be21b69c55178641d3a4349f1e913115b863fc50f1a048962d0b1fd04f395c38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82329758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b547df9dfc1448448c80a57f3c7ed76dc366b06430507960cbb0424ca4a36c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Thu, 27 Feb 2020 08:07:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 27 Feb 2020 08:07:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:07:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:07:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:07:50 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:07:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:07:56 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:07:57 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:07:57 GMT
ENV COUCHDB_VERSION=3.0.0
# Thu, 27 Feb 2020 08:07:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:08:13 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 27 Feb 2020 08:08:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:08:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:08:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:08:15 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:08:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b53e02635d8416b196c9fe115804b4dc8943eabcc4804e516cf617f73eab91`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b2c6707d6f654831a47885d7285814124b3918f32df47209a41e22658f999`  
		Last Modified: Thu, 27 Feb 2020 08:09:22 GMT  
		Size: 6.7 MB (6669970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476af73bc07748b5d44dca190a7aebe3b3f1c4df87d94b31348544e03a105c97`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 1.2 MB (1192657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9097bacd3cb959d27a1255b8ce0c153da110462b820aee8eb4a8fd54f90c1d`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1735d1e02fcb398d6befed3863406252ebc094b9b1d4f56b5e1ccf73975f97`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d290ca762469cd7dc8fade671d4565d0ffa7846499ce0896163d0031aba9c5e`  
		Last Modified: Thu, 27 Feb 2020 08:09:25 GMT  
		Size: 47.4 MB (47365869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61019970e8209e99565e63aec224cfb0f1c0ec124497b05a9dbe6225e797727b`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efd4f928fc2eb12d8fe8e0fe88585d2fc7dbceedd3622e75979c957ee517061`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2de1ec2ac9a6ca190a9b1c101726e25cc0bcbbdf51d44f8f11e15f1f3ab5341`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b2b47b6f3dec92716a21ebee72dec0c67d3ced282154d71575615dfaa7575e`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.0`

```console
$ docker pull couchdb@sha256:9a04017623a7ac09f355f523522f51c617558a0ca642f71dff4c96cd4b7bfb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:3.0.0` - linux; amd64

```console
$ docker pull couchdb@sha256:be21b69c55178641d3a4349f1e913115b863fc50f1a048962d0b1fd04f395c38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82329758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b547df9dfc1448448c80a57f3c7ed76dc366b06430507960cbb0424ca4a36c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Thu, 27 Feb 2020 08:07:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 27 Feb 2020 08:07:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:07:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:07:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:07:50 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:07:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:07:56 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:07:57 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:07:57 GMT
ENV COUCHDB_VERSION=3.0.0
# Thu, 27 Feb 2020 08:07:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:08:13 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 27 Feb 2020 08:08:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:08:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:08:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:08:15 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:08:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b53e02635d8416b196c9fe115804b4dc8943eabcc4804e516cf617f73eab91`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b2c6707d6f654831a47885d7285814124b3918f32df47209a41e22658f999`  
		Last Modified: Thu, 27 Feb 2020 08:09:22 GMT  
		Size: 6.7 MB (6669970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476af73bc07748b5d44dca190a7aebe3b3f1c4df87d94b31348544e03a105c97`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 1.2 MB (1192657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9097bacd3cb959d27a1255b8ce0c153da110462b820aee8eb4a8fd54f90c1d`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1735d1e02fcb398d6befed3863406252ebc094b9b1d4f56b5e1ccf73975f97`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d290ca762469cd7dc8fade671d4565d0ffa7846499ce0896163d0031aba9c5e`  
		Last Modified: Thu, 27 Feb 2020 08:09:25 GMT  
		Size: 47.4 MB (47365869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61019970e8209e99565e63aec224cfb0f1c0ec124497b05a9dbe6225e797727b`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efd4f928fc2eb12d8fe8e0fe88585d2fc7dbceedd3622e75979c957ee517061`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2de1ec2ac9a6ca190a9b1c101726e25cc0bcbbdf51d44f8f11e15f1f3ab5341`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b2b47b6f3dec92716a21ebee72dec0c67d3ced282154d71575615dfaa7575e`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9a04017623a7ac09f355f523522f51c617558a0ca642f71dff4c96cd4b7bfb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:be21b69c55178641d3a4349f1e913115b863fc50f1a048962d0b1fd04f395c38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82329758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b547df9dfc1448448c80a57f3c7ed76dc366b06430507960cbb0424ca4a36c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Thu, 27 Feb 2020 08:07:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 27 Feb 2020 08:07:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 27 Feb 2020 08:07:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 08:07:50 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Feb 2020 08:07:50 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 08:07:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 27 Feb 2020 08:07:56 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 27 Feb 2020 08:07:57 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 27 Feb 2020 08:07:57 GMT
ENV COUCHDB_VERSION=3.0.0
# Thu, 27 Feb 2020 08:07:58 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 27 Feb 2020 08:08:13 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 27 Feb 2020 08:08:14 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 27 Feb 2020 08:08:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 27 Feb 2020 08:08:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 27 Feb 2020 08:08:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 27 Feb 2020 08:08:15 GMT
EXPOSE 4369 5984 9100
# Thu, 27 Feb 2020 08:08:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b53e02635d8416b196c9fe115804b4dc8943eabcc4804e516cf617f73eab91`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3b2c6707d6f654831a47885d7285814124b3918f32df47209a41e22658f999`  
		Last Modified: Thu, 27 Feb 2020 08:09:22 GMT  
		Size: 6.7 MB (6669970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476af73bc07748b5d44dca190a7aebe3b3f1c4df87d94b31348544e03a105c97`  
		Last Modified: Thu, 27 Feb 2020 08:09:20 GMT  
		Size: 1.2 MB (1192657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9097bacd3cb959d27a1255b8ce0c153da110462b820aee8eb4a8fd54f90c1d`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1735d1e02fcb398d6befed3863406252ebc094b9b1d4f56b5e1ccf73975f97`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d290ca762469cd7dc8fade671d4565d0ffa7846499ce0896163d0031aba9c5e`  
		Last Modified: Thu, 27 Feb 2020 08:09:25 GMT  
		Size: 47.4 MB (47365869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61019970e8209e99565e63aec224cfb0f1c0ec124497b05a9dbe6225e797727b`  
		Last Modified: Thu, 27 Feb 2020 08:09:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efd4f928fc2eb12d8fe8e0fe88585d2fc7dbceedd3622e75979c957ee517061`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2de1ec2ac9a6ca190a9b1c101726e25cc0bcbbdf51d44f8f11e15f1f3ab5341`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b2b47b6f3dec92716a21ebee72dec0c67d3ced282154d71575615dfaa7575e`  
		Last Modified: Thu, 27 Feb 2020 08:09:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
