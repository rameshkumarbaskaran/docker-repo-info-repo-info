<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.0`](#couchdb30)
-	[`couchdb:3.0.1`](#couchdb301)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.0`](#couchdb310)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:cfd17fd500f50c0ab15ef92f07e243daeb95dd7246d9768fd6d375f06f2c1da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:360f9a9d01ee87e56e68c4d179c2b1bd04379f0fcfeb64bc6e63a076cdfe18e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82411034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3096f7517c03a5abcb25ed932c97ec69691a9b94386aa87d4639666850c11401`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:04:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:04:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:04:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:04:30 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:04:30 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:04:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:04:40 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:06:01 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:06:01 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 04 Aug 2020 21:06:02 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:06:24 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:06:25 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 04 Aug 2020 21:06:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:06:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:06:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:06:26 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:06:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1848fbf067c9d41ee5aa7fe77a9eb08708ce30b8b385660636722dcb28f873e3`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a034c19637c52005b5c1cbaa7e99f05ab866e09a6018416111ae96830d8817`  
		Last Modified: Tue, 04 Aug 2020 21:07:07 GMT  
		Size: 8.5 MB (8471846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e97721123d10ee0bb42f8a48a85e1704564cd8a83bd0719c9cd21392d829603`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 1.2 MB (1190354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a63953f9f69683b01effe1cb3c726174d73774128b1d543247783c021d860`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1246c96ca18a792930ad63a5c81512b0d335002e5ca0cb9c011a4dbd1368b2`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9772e1ea477ce63d161a3451e9ec4516cb17ad575f5aedf83691561db2994`  
		Last Modified: Tue, 04 Aug 2020 21:07:14 GMT  
		Size: 50.2 MB (50217089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa997e7fa84c89a95e82ddcd99b0e47406cce55e695c6739c8f01cb1f243b46`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89ce0ebe93a8c35a0ef456ee2f0d3cb5799bc6eb88bac82be3a3014908905`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77926159a4ca9e284de9cca57258c2413e33c9935f74e2a85895b9d2ddfe8e9`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b7ffd753664e561fb45396cee057d0bf81b72ee89d8843fb81987ac2fd02b`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2094cb25ca62d1c91ddfdbe0e082a4e3707a9f0452b8de0bcac5ad42d26cc38f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76926974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e33da7e2e1ac5778efd976c2890c9309dcfc55d1b4cf5fd98766109ca1fdd08`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:57 GMT
ADD file:fe3fc1ceb78e0b280e8429ba94710b765701de58e9958d27e9bcb8af97084f1b in / 
# Wed, 09 Sep 2020 23:55:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:21:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:21:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:21:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:21:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:21:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:21:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:21:51 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:21:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:21:56 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 10 Sep 2020 00:21:57 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:22:31 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:22:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:22:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:22:35 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 10 Sep 2020 00:22:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:22:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:22:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:22:38 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:22:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:852f38eca5e441cf6f4d6130ee167637bc8117d57f8f0156f5e489e8c3dd8f17`  
		Last Modified: Thu, 10 Sep 2020 00:01:56 GMT  
		Size: 20.4 MB (20377071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308fc08e8aa0a74a63a5cdf460de80bddfb598f10c8c906fee62c7d7ac72733`  
		Last Modified: Thu, 10 Sep 2020 00:23:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1672b403525190244a10e5ba5d05120cb5ee037b2faa32a16785e954aa2f7906`  
		Last Modified: Thu, 10 Sep 2020 00:23:34 GMT  
		Size: 7.6 MB (7610318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd36439b676c57f644b402cf783bbebfb7d9d4010acd789f1b45563d297818bd`  
		Last Modified: Thu, 10 Sep 2020 00:23:32 GMT  
		Size: 1.1 MB (1124946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c94a073c1d42e3f0f5f22886f6e7e1109ff5a5c91a0f3a3fa600e22d1eb1c`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f3a82559678a1cb7c3edd1775d84d9d31b1e3b034c905d554a1e25044f9406`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cbe2dd87152f574abc4901d6ef8d30504c32bd5f4ba0df67a1028a2798ded`  
		Last Modified: Thu, 10 Sep 2020 00:23:43 GMT  
		Size: 47.8 MB (47805143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d7fd2241fd355b180c17bf8ff3722066e3d542797cde7bdeef8575145d5c`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b1eea60a06f4a39ac21c490fdb7ce65c79c6e0e1494c6514f5403d035ce55`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a42df5ad45f011ca96704ad9292de95a205ef38ccbffd110dece2af80ea70`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122c378fe0f524831a1079cc87e54b985fac3dca56ed618677dff1397e970e23`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:cfd17fd500f50c0ab15ef92f07e243daeb95dd7246d9768fd6d375f06f2c1da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:360f9a9d01ee87e56e68c4d179c2b1bd04379f0fcfeb64bc6e63a076cdfe18e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82411034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3096f7517c03a5abcb25ed932c97ec69691a9b94386aa87d4639666850c11401`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:04:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:04:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:04:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:04:30 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:04:30 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:04:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:04:40 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:06:01 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:06:01 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 04 Aug 2020 21:06:02 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:06:24 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:06:25 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 04 Aug 2020 21:06:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:06:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:06:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:06:26 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:06:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1848fbf067c9d41ee5aa7fe77a9eb08708ce30b8b385660636722dcb28f873e3`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a034c19637c52005b5c1cbaa7e99f05ab866e09a6018416111ae96830d8817`  
		Last Modified: Tue, 04 Aug 2020 21:07:07 GMT  
		Size: 8.5 MB (8471846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e97721123d10ee0bb42f8a48a85e1704564cd8a83bd0719c9cd21392d829603`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 1.2 MB (1190354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a63953f9f69683b01effe1cb3c726174d73774128b1d543247783c021d860`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1246c96ca18a792930ad63a5c81512b0d335002e5ca0cb9c011a4dbd1368b2`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9772e1ea477ce63d161a3451e9ec4516cb17ad575f5aedf83691561db2994`  
		Last Modified: Tue, 04 Aug 2020 21:07:14 GMT  
		Size: 50.2 MB (50217089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa997e7fa84c89a95e82ddcd99b0e47406cce55e695c6739c8f01cb1f243b46`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89ce0ebe93a8c35a0ef456ee2f0d3cb5799bc6eb88bac82be3a3014908905`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77926159a4ca9e284de9cca57258c2413e33c9935f74e2a85895b9d2ddfe8e9`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b7ffd753664e561fb45396cee057d0bf81b72ee89d8843fb81987ac2fd02b`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2094cb25ca62d1c91ddfdbe0e082a4e3707a9f0452b8de0bcac5ad42d26cc38f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76926974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e33da7e2e1ac5778efd976c2890c9309dcfc55d1b4cf5fd98766109ca1fdd08`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:57 GMT
ADD file:fe3fc1ceb78e0b280e8429ba94710b765701de58e9958d27e9bcb8af97084f1b in / 
# Wed, 09 Sep 2020 23:55:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:21:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:21:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:21:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:21:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:21:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:21:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:21:51 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:21:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:21:56 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 10 Sep 2020 00:21:57 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:22:31 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:22:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:22:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:22:35 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 10 Sep 2020 00:22:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:22:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:22:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:22:38 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:22:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:852f38eca5e441cf6f4d6130ee167637bc8117d57f8f0156f5e489e8c3dd8f17`  
		Last Modified: Thu, 10 Sep 2020 00:01:56 GMT  
		Size: 20.4 MB (20377071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308fc08e8aa0a74a63a5cdf460de80bddfb598f10c8c906fee62c7d7ac72733`  
		Last Modified: Thu, 10 Sep 2020 00:23:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1672b403525190244a10e5ba5d05120cb5ee037b2faa32a16785e954aa2f7906`  
		Last Modified: Thu, 10 Sep 2020 00:23:34 GMT  
		Size: 7.6 MB (7610318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd36439b676c57f644b402cf783bbebfb7d9d4010acd789f1b45563d297818bd`  
		Last Modified: Thu, 10 Sep 2020 00:23:32 GMT  
		Size: 1.1 MB (1124946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c94a073c1d42e3f0f5f22886f6e7e1109ff5a5c91a0f3a3fa600e22d1eb1c`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f3a82559678a1cb7c3edd1775d84d9d31b1e3b034c905d554a1e25044f9406`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cbe2dd87152f574abc4901d6ef8d30504c32bd5f4ba0df67a1028a2798ded`  
		Last Modified: Thu, 10 Sep 2020 00:23:43 GMT  
		Size: 47.8 MB (47805143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d7fd2241fd355b180c17bf8ff3722066e3d542797cde7bdeef8575145d5c`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b1eea60a06f4a39ac21c490fdb7ce65c79c6e0e1494c6514f5403d035ce55`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a42df5ad45f011ca96704ad9292de95a205ef38ccbffd110dece2af80ea70`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122c378fe0f524831a1079cc87e54b985fac3dca56ed618677dff1397e970e23`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:cfd17fd500f50c0ab15ef92f07e243daeb95dd7246d9768fd6d375f06f2c1da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:360f9a9d01ee87e56e68c4d179c2b1bd04379f0fcfeb64bc6e63a076cdfe18e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82411034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3096f7517c03a5abcb25ed932c97ec69691a9b94386aa87d4639666850c11401`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:04:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:04:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:04:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:04:30 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:04:30 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:04:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:04:40 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:06:01 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:06:01 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 04 Aug 2020 21:06:02 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:06:24 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:06:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:06:25 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 04 Aug 2020 21:06:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:06:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:06:26 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:06:26 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:06:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1848fbf067c9d41ee5aa7fe77a9eb08708ce30b8b385660636722dcb28f873e3`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a034c19637c52005b5c1cbaa7e99f05ab866e09a6018416111ae96830d8817`  
		Last Modified: Tue, 04 Aug 2020 21:07:07 GMT  
		Size: 8.5 MB (8471846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e97721123d10ee0bb42f8a48a85e1704564cd8a83bd0719c9cd21392d829603`  
		Last Modified: Tue, 04 Aug 2020 21:07:06 GMT  
		Size: 1.2 MB (1190354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716a63953f9f69683b01effe1cb3c726174d73774128b1d543247783c021d860`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1246c96ca18a792930ad63a5c81512b0d335002e5ca0cb9c011a4dbd1368b2`  
		Last Modified: Tue, 04 Aug 2020 21:07:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df9772e1ea477ce63d161a3451e9ec4516cb17ad575f5aedf83691561db2994`  
		Last Modified: Tue, 04 Aug 2020 21:07:14 GMT  
		Size: 50.2 MB (50217089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa997e7fa84c89a95e82ddcd99b0e47406cce55e695c6739c8f01cb1f243b46`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89ce0ebe93a8c35a0ef456ee2f0d3cb5799bc6eb88bac82be3a3014908905`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77926159a4ca9e284de9cca57258c2413e33c9935f74e2a85895b9d2ddfe8e9`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b7ffd753664e561fb45396cee057d0bf81b72ee89d8843fb81987ac2fd02b`  
		Last Modified: Tue, 04 Aug 2020 21:07:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2094cb25ca62d1c91ddfdbe0e082a4e3707a9f0452b8de0bcac5ad42d26cc38f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76926974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e33da7e2e1ac5778efd976c2890c9309dcfc55d1b4cf5fd98766109ca1fdd08`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:54:57 GMT
ADD file:fe3fc1ceb78e0b280e8429ba94710b765701de58e9958d27e9bcb8af97084f1b in / 
# Wed, 09 Sep 2020 23:55:02 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:21:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:21:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:21:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:21:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:21:37 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:21:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:21:51 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:21:55 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:21:56 GMT
ENV COUCHDB_VERSION=2.3.1
# Thu, 10 Sep 2020 00:21:57 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:22:31 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:22:33 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:22:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:22:35 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Thu, 10 Sep 2020 00:22:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:22:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:22:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:22:38 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:22:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:852f38eca5e441cf6f4d6130ee167637bc8117d57f8f0156f5e489e8c3dd8f17`  
		Last Modified: Thu, 10 Sep 2020 00:01:56 GMT  
		Size: 20.4 MB (20377071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308fc08e8aa0a74a63a5cdf460de80bddfb598f10c8c906fee62c7d7ac72733`  
		Last Modified: Thu, 10 Sep 2020 00:23:33 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1672b403525190244a10e5ba5d05120cb5ee037b2faa32a16785e954aa2f7906`  
		Last Modified: Thu, 10 Sep 2020 00:23:34 GMT  
		Size: 7.6 MB (7610318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd36439b676c57f644b402cf783bbebfb7d9d4010acd789f1b45563d297818bd`  
		Last Modified: Thu, 10 Sep 2020 00:23:32 GMT  
		Size: 1.1 MB (1124946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6c94a073c1d42e3f0f5f22886f6e7e1109ff5a5c91a0f3a3fa600e22d1eb1c`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f3a82559678a1cb7c3edd1775d84d9d31b1e3b034c905d554a1e25044f9406`  
		Last Modified: Thu, 10 Sep 2020 00:23:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cbe2dd87152f574abc4901d6ef8d30504c32bd5f4ba0df67a1028a2798ded`  
		Last Modified: Thu, 10 Sep 2020 00:23:43 GMT  
		Size: 47.8 MB (47805143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7731d7fd2241fd355b180c17bf8ff3722066e3d542797cde7bdeef8575145d5c`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b1eea60a06f4a39ac21c490fdb7ce65c79c6e0e1494c6514f5403d035ce55`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a42df5ad45f011ca96704ad9292de95a205ef38ccbffd110dece2af80ea70`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122c378fe0f524831a1079cc87e54b985fac3dca56ed618677dff1397e970e23`  
		Last Modified: Thu, 10 Sep 2020 00:23:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:b7dff7b8dcea706002cc608e411a87f0dafe2d60a05a36a11ca622e2c6a60a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:d3565459075e662e724e940dbd8db70aa0e53f5ed0c65fa2b0ec748eddfa4bd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83237578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e26f92ae7277ceea6a328f890cc67542de722f69fc9db262b8605308ce85984`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:25 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 21:03:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:03:42 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:03:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:03:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:03:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:03:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:03:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2831b8f2c39ca084bd9a3db8cbc7c26ecf6843178486100f334b8309db2a038`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bcd658e2c9bc4e6fbe69acc54da03ae9b632af67c485b0d653861373936dc`  
		Last Modified: Tue, 04 Aug 2020 21:06:47 GMT  
		Size: 48.3 MB (48274001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4bfa72be706aa7191b0a69177163d4ec0ee83df8853a1c41a1ea15602fcdb2`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0ad5d1ade1b2822a59f7e139ffc5097849a574fd1c733d21a96018851dc5a0`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf89cee2ad7afece717eb9e1337699305e44a1d75df1d33c0b8a803115a936c`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8f755ddaabea33c99d856747cbbcb229c776f5d261bf814cba0b9614ca9fd`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4069af54b87095c432037ff292fdf5c076e3c24eb7decd56112e122daac2a894
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78293970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f29c1d1ebc4aa0eab96e672a067afdba584a96d68e625af7c187b97aeac56`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:19:46 GMT
ENV COUCHDB_VERSION=3.1.0
# Thu, 10 Sep 2020 00:19:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:20:14 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:20:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:20:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:20:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:20:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:20:21 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:20:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e0d5f29cbe810e318f6820b03a0c40f00cca5f4e4ee6bc39bd226da1f4bb99`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d471e067af4f1ba37fa3d8271dfd68a10eedc4f4e2ae5f5de5062f80d6872a8`  
		Last Modified: Thu, 10 Sep 2020 00:23:03 GMT  
		Size: 44.8 MB (44774645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193ae714b7e42000afd56d463ea0797e6ae3ad2a95f274dea7d03e1544adb94`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3792a63cca28963fed03b3fae5de1bbc02e12a1354d53d5b36ca96d20e39ed25`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d316c01fabebba9e6b75f27af7a670ec0d08cc92b6c3c63488d9be82f0d91e`  
		Last Modified: Thu, 10 Sep 2020 00:22:52 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce073933c79b64094b52fd7dc8c2e5dab9754bf21d3c82ba051d26eeb70a41`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4e4efe2d1a9a90b66b661625f3333dc20df81a757e6748f831de604650b540b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88391919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087d15c167696d2d8f1093fc0f0fc07263b2f3061c58e50fab775732757eded5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:52:10 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 07:52:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:53:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:53:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:53:28 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:53:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:53:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:53:54 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:53:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af12a6a18a59ed1aef906f51546b85c1b02236d728f0ce416ad136dc3d73cd6`  
		Last Modified: Tue, 04 Aug 2020 07:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639d58161af2c93cd580784899573f0fa02ccd7c20aff6e8e9a554cf97a78bc6`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 49.2 MB (49168292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca599954990f82d57ffcf138335c3cb179c3db86ffaefde9ddfadb9011b8d07`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30403a70c5583db97f3868c966bf7f30bda01e62207a9f075ebfd54bee1d3c87`  
		Last Modified: Tue, 04 Aug 2020 07:56:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197f041e43cf54d96cbbbdccb4a72dac5d1fa203e5af92d33387521f2370964d`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8868aaf24510aa277829771b1fa3869d77c6c3cf4bec891a6415e91d9a100673`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:96c40132934f30714ace41a637e8149620b8043d74e43b0c4e8a255052c342a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:06995f756449628660f6d9cab500bd023e1a709550db28788ecc26741bd7ff8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83193358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bb5b4b4a74d372d1a6177903c19143e2afa6e3bc2eb31e1618f8a3c29a759c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:54 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 04 Aug 2020 21:03:55 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:04:12 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:04:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:04:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:04:12 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:04:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:04:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:04:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:04:14 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:04:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109439ba5e17eeb2189e6e9752d7dd9dbd5ef1fff8714372622272b019b8f81`  
		Last Modified: Tue, 04 Aug 2020 21:06:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a130ca86145c9f3f44985619a1ef0734b970240cbeeb5f0d9205c289558e79`  
		Last Modified: Tue, 04 Aug 2020 21:07:00 GMT  
		Size: 48.2 MB (48229773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad912b8330c6b38ea219a456bc213a66fb5077dd329345407ac03c3ea764c5d4`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22df149c9c883787f85fcaa2ffe8526204bc2de9ae2297bf56f3bbacb2935646`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940038c9d1548e2f31b367bbc926f32715f08c56e4e53fc268ccadb9b5f2b67f`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab38787e5e2f03bceabc64581e0b2ffa92df8ba2e97fc0088f87817e3e9f30b7`  
		Last Modified: Tue, 04 Aug 2020 21:06:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bc6fbe10cc9817ec4039aec7e22adf6292c1c2424ec51240bf915b36c27fa3d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78227669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8126b6b618ff8a2ef56fbaaaf661ec5d95545011b24dbdd6ced380299605c39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:20:32 GMT
ENV COUCHDB_VERSION=3.0.1
# Thu, 10 Sep 2020 00:20:33 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:21:00 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:21:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:21:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:21:03 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:21:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:21:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:21:06 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:21:06 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:21:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d61a49e154394829949248416406e087c0ec93490c6d371a3736b9c29f5f1d2`  
		Last Modified: Thu, 10 Sep 2020 00:23:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e065870c1b3f781c941005c5c172bb69c060a48445679f01bda503f572604`  
		Last Modified: Thu, 10 Sep 2020 00:23:23 GMT  
		Size: 44.7 MB (44708354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65720afa2f7df2e4918e587cf91c59bf06062bc2f68416e7c6b4924760dbb8ca`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887d132089601a5d543491bb0c81ef85042a9a1bf47aff95b81d1aeabcffecdd`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af8c6ff180b2954ff2fe054cad870eb034c3f09cefb2f3660ac0fcb588c9d2a`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c12e0bd5e621324ce58943dc9a2683144902dbf1a8adb699f741359d4f22db`  
		Last Modified: Thu, 10 Sep 2020 00:23:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ee811c5efee82562026dcfdeb8b09314ecb20998f4e65ca976427927d0c2b4b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88348046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca18e95ee995ef760533f338e22e5a3ab8cbbc8c3bb319c7e6b0c33be346addf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:54:09 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 04 Aug 2020 07:54:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:55:16 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:55:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:55:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:55:23 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:55:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:55:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:55:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:55:43 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:55:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47ad8fb6eda0a07f357c50e7d0037a193fb0b8da4fd7c7dd5cf7b4b47b0752`  
		Last Modified: Tue, 04 Aug 2020 07:56:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e001842a0bbd8bbe950173d35b2f0c6ebcba8fc9afd521cc3e8309af9f95f5`  
		Last Modified: Tue, 04 Aug 2020 07:56:58 GMT  
		Size: 49.1 MB (49124422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecd170312e8af8d90f51b49c642061439624a1b412852fccb13b56004a2d4a2`  
		Last Modified: Tue, 04 Aug 2020 07:56:49 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5358403c082ef3344dc2fb421586a0126ef55eca74540461bb598b22a15843b8`  
		Last Modified: Tue, 04 Aug 2020 07:56:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ff665acad7c328292d34fe7efb59d81add34e300138987a939f51df70e11f`  
		Last Modified: Tue, 04 Aug 2020 07:56:49 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02e7a5b97dd3ee2b131d04ccc9ed3259a9c5b91496b9ee5920aa64fdf79b2da`  
		Last Modified: Tue, 04 Aug 2020 07:56:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.1`

```console
$ docker pull couchdb@sha256:96c40132934f30714ace41a637e8149620b8043d74e43b0c4e8a255052c342a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0.1` - linux; amd64

```console
$ docker pull couchdb@sha256:06995f756449628660f6d9cab500bd023e1a709550db28788ecc26741bd7ff8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83193358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bb5b4b4a74d372d1a6177903c19143e2afa6e3bc2eb31e1618f8a3c29a759c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:54 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 04 Aug 2020 21:03:55 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:04:12 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:04:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:04:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:04:12 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:04:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:04:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:04:13 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:04:14 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:04:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7109439ba5e17eeb2189e6e9752d7dd9dbd5ef1fff8714372622272b019b8f81`  
		Last Modified: Tue, 04 Aug 2020 21:06:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a130ca86145c9f3f44985619a1ef0734b970240cbeeb5f0d9205c289558e79`  
		Last Modified: Tue, 04 Aug 2020 21:07:00 GMT  
		Size: 48.2 MB (48229773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad912b8330c6b38ea219a456bc213a66fb5077dd329345407ac03c3ea764c5d4`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22df149c9c883787f85fcaa2ffe8526204bc2de9ae2297bf56f3bbacb2935646`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940038c9d1548e2f31b367bbc926f32715f08c56e4e53fc268ccadb9b5f2b67f`  
		Last Modified: Tue, 04 Aug 2020 21:06:52 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab38787e5e2f03bceabc64581e0b2ffa92df8ba2e97fc0088f87817e3e9f30b7`  
		Last Modified: Tue, 04 Aug 2020 21:06:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bc6fbe10cc9817ec4039aec7e22adf6292c1c2424ec51240bf915b36c27fa3d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78227669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8126b6b618ff8a2ef56fbaaaf661ec5d95545011b24dbdd6ced380299605c39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:20:32 GMT
ENV COUCHDB_VERSION=3.0.1
# Thu, 10 Sep 2020 00:20:33 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:21:00 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:21:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:21:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:21:03 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:21:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:21:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:21:06 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:21:06 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:21:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d61a49e154394829949248416406e087c0ec93490c6d371a3736b9c29f5f1d2`  
		Last Modified: Thu, 10 Sep 2020 00:23:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200e065870c1b3f781c941005c5c172bb69c060a48445679f01bda503f572604`  
		Last Modified: Thu, 10 Sep 2020 00:23:23 GMT  
		Size: 44.7 MB (44708354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65720afa2f7df2e4918e587cf91c59bf06062bc2f68416e7c6b4924760dbb8ca`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887d132089601a5d543491bb0c81ef85042a9a1bf47aff95b81d1aeabcffecdd`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af8c6ff180b2954ff2fe054cad870eb034c3f09cefb2f3660ac0fcb588c9d2a`  
		Last Modified: Thu, 10 Sep 2020 00:23:13 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c12e0bd5e621324ce58943dc9a2683144902dbf1a8adb699f741359d4f22db`  
		Last Modified: Thu, 10 Sep 2020 00:23:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ee811c5efee82562026dcfdeb8b09314ecb20998f4e65ca976427927d0c2b4b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88348046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca18e95ee995ef760533f338e22e5a3ab8cbbc8c3bb319c7e6b0c33be346addf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:54:09 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 04 Aug 2020 07:54:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:55:16 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:55:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:55:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:55:23 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:55:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:55:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:55:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:55:43 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:55:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce47ad8fb6eda0a07f357c50e7d0037a193fb0b8da4fd7c7dd5cf7b4b47b0752`  
		Last Modified: Tue, 04 Aug 2020 07:56:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e001842a0bbd8bbe950173d35b2f0c6ebcba8fc9afd521cc3e8309af9f95f5`  
		Last Modified: Tue, 04 Aug 2020 07:56:58 GMT  
		Size: 49.1 MB (49124422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecd170312e8af8d90f51b49c642061439624a1b412852fccb13b56004a2d4a2`  
		Last Modified: Tue, 04 Aug 2020 07:56:49 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5358403c082ef3344dc2fb421586a0126ef55eca74540461bb598b22a15843b8`  
		Last Modified: Tue, 04 Aug 2020 07:56:50 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ff665acad7c328292d34fe7efb59d81add34e300138987a939f51df70e11f`  
		Last Modified: Tue, 04 Aug 2020 07:56:49 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02e7a5b97dd3ee2b131d04ccc9ed3259a9c5b91496b9ee5920aa64fdf79b2da`  
		Last Modified: Tue, 04 Aug 2020 07:56:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:b7dff7b8dcea706002cc608e411a87f0dafe2d60a05a36a11ca622e2c6a60a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:d3565459075e662e724e940dbd8db70aa0e53f5ed0c65fa2b0ec748eddfa4bd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83237578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e26f92ae7277ceea6a328f890cc67542de722f69fc9db262b8605308ce85984`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:25 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 21:03:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:03:42 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:03:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:03:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:03:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:03:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:03:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2831b8f2c39ca084bd9a3db8cbc7c26ecf6843178486100f334b8309db2a038`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bcd658e2c9bc4e6fbe69acc54da03ae9b632af67c485b0d653861373936dc`  
		Last Modified: Tue, 04 Aug 2020 21:06:47 GMT  
		Size: 48.3 MB (48274001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4bfa72be706aa7191b0a69177163d4ec0ee83df8853a1c41a1ea15602fcdb2`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0ad5d1ade1b2822a59f7e139ffc5097849a574fd1c733d21a96018851dc5a0`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf89cee2ad7afece717eb9e1337699305e44a1d75df1d33c0b8a803115a936c`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8f755ddaabea33c99d856747cbbcb229c776f5d261bf814cba0b9614ca9fd`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4069af54b87095c432037ff292fdf5c076e3c24eb7decd56112e122daac2a894
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78293970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f29c1d1ebc4aa0eab96e672a067afdba584a96d68e625af7c187b97aeac56`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:19:46 GMT
ENV COUCHDB_VERSION=3.1.0
# Thu, 10 Sep 2020 00:19:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:20:14 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:20:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:20:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:20:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:20:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:20:21 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:20:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e0d5f29cbe810e318f6820b03a0c40f00cca5f4e4ee6bc39bd226da1f4bb99`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d471e067af4f1ba37fa3d8271dfd68a10eedc4f4e2ae5f5de5062f80d6872a8`  
		Last Modified: Thu, 10 Sep 2020 00:23:03 GMT  
		Size: 44.8 MB (44774645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193ae714b7e42000afd56d463ea0797e6ae3ad2a95f274dea7d03e1544adb94`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3792a63cca28963fed03b3fae5de1bbc02e12a1354d53d5b36ca96d20e39ed25`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d316c01fabebba9e6b75f27af7a670ec0d08cc92b6c3c63488d9be82f0d91e`  
		Last Modified: Thu, 10 Sep 2020 00:22:52 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce073933c79b64094b52fd7dc8c2e5dab9754bf21d3c82ba051d26eeb70a41`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4e4efe2d1a9a90b66b661625f3333dc20df81a757e6748f831de604650b540b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88391919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087d15c167696d2d8f1093fc0f0fc07263b2f3061c58e50fab775732757eded5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:52:10 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 07:52:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:53:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:53:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:53:28 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:53:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:53:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:53:54 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:53:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af12a6a18a59ed1aef906f51546b85c1b02236d728f0ce416ad136dc3d73cd6`  
		Last Modified: Tue, 04 Aug 2020 07:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639d58161af2c93cd580784899573f0fa02ccd7c20aff6e8e9a554cf97a78bc6`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 49.2 MB (49168292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca599954990f82d57ffcf138335c3cb179c3db86ffaefde9ddfadb9011b8d07`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30403a70c5583db97f3868c966bf7f30bda01e62207a9f075ebfd54bee1d3c87`  
		Last Modified: Tue, 04 Aug 2020 07:56:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197f041e43cf54d96cbbbdccb4a72dac5d1fa203e5af92d33387521f2370964d`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8868aaf24510aa277829771b1fa3869d77c6c3cf4bec891a6415e91d9a100673`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.0`

```console
$ docker pull couchdb@sha256:b7dff7b8dcea706002cc608e411a87f0dafe2d60a05a36a11ca622e2c6a60a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1.0` - linux; amd64

```console
$ docker pull couchdb@sha256:d3565459075e662e724e940dbd8db70aa0e53f5ed0c65fa2b0ec748eddfa4bd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83237578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e26f92ae7277ceea6a328f890cc67542de722f69fc9db262b8605308ce85984`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:25 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 21:03:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:03:42 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:03:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:03:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:03:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:03:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:03:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2831b8f2c39ca084bd9a3db8cbc7c26ecf6843178486100f334b8309db2a038`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bcd658e2c9bc4e6fbe69acc54da03ae9b632af67c485b0d653861373936dc`  
		Last Modified: Tue, 04 Aug 2020 21:06:47 GMT  
		Size: 48.3 MB (48274001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4bfa72be706aa7191b0a69177163d4ec0ee83df8853a1c41a1ea15602fcdb2`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0ad5d1ade1b2822a59f7e139ffc5097849a574fd1c733d21a96018851dc5a0`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf89cee2ad7afece717eb9e1337699305e44a1d75df1d33c0b8a803115a936c`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8f755ddaabea33c99d856747cbbcb229c776f5d261bf814cba0b9614ca9fd`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4069af54b87095c432037ff292fdf5c076e3c24eb7decd56112e122daac2a894
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78293970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f29c1d1ebc4aa0eab96e672a067afdba584a96d68e625af7c187b97aeac56`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:19:46 GMT
ENV COUCHDB_VERSION=3.1.0
# Thu, 10 Sep 2020 00:19:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:20:14 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:20:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:20:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:20:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:20:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:20:21 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:20:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e0d5f29cbe810e318f6820b03a0c40f00cca5f4e4ee6bc39bd226da1f4bb99`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d471e067af4f1ba37fa3d8271dfd68a10eedc4f4e2ae5f5de5062f80d6872a8`  
		Last Modified: Thu, 10 Sep 2020 00:23:03 GMT  
		Size: 44.8 MB (44774645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193ae714b7e42000afd56d463ea0797e6ae3ad2a95f274dea7d03e1544adb94`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3792a63cca28963fed03b3fae5de1bbc02e12a1354d53d5b36ca96d20e39ed25`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d316c01fabebba9e6b75f27af7a670ec0d08cc92b6c3c63488d9be82f0d91e`  
		Last Modified: Thu, 10 Sep 2020 00:22:52 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce073933c79b64094b52fd7dc8c2e5dab9754bf21d3c82ba051d26eeb70a41`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4e4efe2d1a9a90b66b661625f3333dc20df81a757e6748f831de604650b540b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88391919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087d15c167696d2d8f1093fc0f0fc07263b2f3061c58e50fab775732757eded5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:52:10 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 07:52:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:53:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:53:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:53:28 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:53:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:53:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:53:54 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:53:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af12a6a18a59ed1aef906f51546b85c1b02236d728f0ce416ad136dc3d73cd6`  
		Last Modified: Tue, 04 Aug 2020 07:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639d58161af2c93cd580784899573f0fa02ccd7c20aff6e8e9a554cf97a78bc6`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 49.2 MB (49168292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca599954990f82d57ffcf138335c3cb179c3db86ffaefde9ddfadb9011b8d07`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30403a70c5583db97f3868c966bf7f30bda01e62207a9f075ebfd54bee1d3c87`  
		Last Modified: Tue, 04 Aug 2020 07:56:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197f041e43cf54d96cbbbdccb4a72dac5d1fa203e5af92d33387521f2370964d`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8868aaf24510aa277829771b1fa3869d77c6c3cf4bec891a6415e91d9a100673`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b7dff7b8dcea706002cc608e411a87f0dafe2d60a05a36a11ca622e2c6a60a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:d3565459075e662e724e940dbd8db70aa0e53f5ed0c65fa2b0ec748eddfa4bd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83237578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e26f92ae7277ceea6a328f890cc67542de722f69fc9db262b8605308ce85984`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 21:03:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 21:03:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 21:03:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 21:03:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 21:03:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 21:03:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 21:03:24 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 21:03:25 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 21:03:25 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 21:03:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 21:03:42 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 21:03:43 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 21:03:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 21:03:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 21:03:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 21:03:44 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 21:03:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0133380524efee52a03c0ed79096be517fe448baba94af415edef43f42b36fd5`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1461e31bfd234018071517b2deada8261904979b54c5e005d4553ab7f1ecc1`  
		Last Modified: Tue, 04 Aug 2020 21:06:43 GMT  
		Size: 6.7 MB (6669349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4318fadf222c24da8e03343347c7909d18954266c0c9dc771c5aeceb0bc967`  
		Last Modified: Tue, 04 Aug 2020 21:06:42 GMT  
		Size: 1.2 MB (1192669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59ba1e6f8e28f84f6eed2802de18caf7192548a4676acfb3850e98a00897c30`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2831b8f2c39ca084bd9a3db8cbc7c26ecf6843178486100f334b8309db2a038`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bcd658e2c9bc4e6fbe69acc54da03ae9b632af67c485b0d653861373936dc`  
		Last Modified: Tue, 04 Aug 2020 21:06:47 GMT  
		Size: 48.3 MB (48274001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4bfa72be706aa7191b0a69177163d4ec0ee83df8853a1c41a1ea15602fcdb2`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0ad5d1ade1b2822a59f7e139ffc5097849a574fd1c733d21a96018851dc5a0`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf89cee2ad7afece717eb9e1337699305e44a1d75df1d33c0b8a803115a936c`  
		Last Modified: Tue, 04 Aug 2020 21:06:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8f755ddaabea33c99d856747cbbcb229c776f5d261bf814cba0b9614ca9fd`  
		Last Modified: Tue, 04 Aug 2020 21:06:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4069af54b87095c432037ff292fdf5c076e3c24eb7decd56112e122daac2a894
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78293970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f29c1d1ebc4aa0eab96e672a067afdba584a96d68e625af7c187b97aeac56`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:54 GMT
ADD file:d870fb0484ea283840d9cc923c9c3fe36d1bb6b3b5ecfefcce06aa26a22c9414 in / 
# Wed, 09 Sep 2020 23:50:57 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:19:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 10 Sep 2020 00:19:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 10 Sep 2020 00:19:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 00:19:30 GMT
ENV GOSU_VERSION=1.11
# Thu, 10 Sep 2020 00:19:31 GMT
ENV TINI_VERSION=0.18.0
# Thu, 10 Sep 2020 00:19:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Thu, 10 Sep 2020 00:19:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Thu, 10 Sep 2020 00:19:45 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Thu, 10 Sep 2020 00:19:46 GMT
ENV COUCHDB_VERSION=3.1.0
# Thu, 10 Sep 2020 00:19:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Thu, 10 Sep 2020 00:20:14 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 10 Sep 2020 00:20:16 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 10 Sep 2020 00:20:17 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Thu, 10 Sep 2020 00:20:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 10 Sep 2020 00:20:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 10 Sep 2020 00:20:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 10 Sep 2020 00:20:21 GMT
EXPOSE 4369 5984 9100
# Thu, 10 Sep 2020 00:20:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a6d76de28f58f3470aff71c934c0fec4e5d0fad788f8b8bcc50601266fc1b34d`  
		Last Modified: Wed, 09 Sep 2020 23:59:09 GMT  
		Size: 25.8 MB (25849325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa1d5e2236c2701e7e74ca08be2a89142dfadcc2bd7dce3db06a3e06ecb755`  
		Last Modified: Thu, 10 Sep 2020 00:22:57 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc743dcbcb4bc16d167ec8425c0b676156c29ecb0dd2eff52c7b0daafee6835f`  
		Last Modified: Thu, 10 Sep 2020 00:22:56 GMT  
		Size: 6.5 MB (6533419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22487211af47d0de4662cca16ee71ba85979669412a917c34a2b00971412cfd3`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 1.1 MB (1127103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67227b6c479212c785ced10baaacb8e41022ef47208627773f4627b7e4f66a72`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e0d5f29cbe810e318f6820b03a0c40f00cca5f4e4ee6bc39bd226da1f4bb99`  
		Last Modified: Thu, 10 Sep 2020 00:22:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d471e067af4f1ba37fa3d8271dfd68a10eedc4f4e2ae5f5de5062f80d6872a8`  
		Last Modified: Thu, 10 Sep 2020 00:23:03 GMT  
		Size: 44.8 MB (44774645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a193ae714b7e42000afd56d463ea0797e6ae3ad2a95f274dea7d03e1544adb94`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3792a63cca28963fed03b3fae5de1bbc02e12a1354d53d5b36ca96d20e39ed25`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d316c01fabebba9e6b75f27af7a670ec0d08cc92b6c3c63488d9be82f0d91e`  
		Last Modified: Thu, 10 Sep 2020 00:22:52 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce073933c79b64094b52fd7dc8c2e5dab9754bf21d3c82ba051d26eeb70a41`  
		Last Modified: Thu, 10 Sep 2020 00:22:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4e4efe2d1a9a90b66b661625f3333dc20df81a757e6748f831de604650b540b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88391919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087d15c167696d2d8f1093fc0f0fc07263b2f3061c58e50fab775732757eded5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:48:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Aug 2020 07:48:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Aug 2020 07:50:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:50:23 GMT
ENV GOSU_VERSION=1.11
# Tue, 04 Aug 2020 07:50:26 GMT
ENV TINI_VERSION=0.18.0
# Tue, 04 Aug 2020 07:51:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 04 Aug 2020 07:51:55 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 04 Aug 2020 07:52:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 04 Aug 2020 07:52:10 GMT
ENV COUCHDB_VERSION=3.1.0
# Tue, 04 Aug 2020 07:52:18 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 04 Aug 2020 07:53:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Aug 2020 07:53:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Aug 2020 07:53:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 04 Aug 2020 07:53:28 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Tue, 04 Aug 2020 07:53:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Aug 2020 07:53:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 07:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Aug 2020 07:53:54 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Aug 2020 07:53:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dffc17a2b5ed9e5a97b43eca8060ba62931c0f020ecf499e7c20a2683c1b7e`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 3.4 KB (3422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2978e7e2195b235a826971311755980b291954b3a622d04282918003dcbf1c9`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 7.6 MB (7580171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd013112e0f4d3589c61213b7547b903f0b3ede758d2846b630d125fb2d7394`  
		Last Modified: Tue, 04 Aug 2020 07:56:30 GMT  
		Size: 1.1 MB (1116147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36c54517f4124fe4b67a3bd13f47f4e420c776113638e3478d0e176264c30f3`  
		Last Modified: Tue, 04 Aug 2020 07:56:28 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af12a6a18a59ed1aef906f51546b85c1b02236d728f0ce416ad136dc3d73cd6`  
		Last Modified: Tue, 04 Aug 2020 07:56:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639d58161af2c93cd580784899573f0fa02ccd7c20aff6e8e9a554cf97a78bc6`  
		Last Modified: Tue, 04 Aug 2020 07:56:33 GMT  
		Size: 49.2 MB (49168292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca599954990f82d57ffcf138335c3cb179c3db86ffaefde9ddfadb9011b8d07`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30403a70c5583db97f3868c966bf7f30bda01e62207a9f075ebfd54bee1d3c87`  
		Last Modified: Tue, 04 Aug 2020 07:56:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197f041e43cf54d96cbbbdccb4a72dac5d1fa203e5af92d33387521f2370964d`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8868aaf24510aa277829771b1fa3869d77c6c3cf4bec891a6415e91d9a100673`  
		Last Modified: Tue, 04 Aug 2020 07:56:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
