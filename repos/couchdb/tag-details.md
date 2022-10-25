<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.2`](#couchdb322)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:bb44133c719a2f72b23a2983449a70b1a0b528de7b14c1a6667667f2a15a7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:6bfa0c63118cc551231a6c9f66888efe9994eff949c5cdf93c09a0140be77fc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84529402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2695394336cc3c0b33abf96483195d65b99ce6f3297899655bd2ecf038fc13`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:54:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:54:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:54:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:55:02 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 05 Oct 2022 01:55:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:55:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 05 Oct 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:55:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:55:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:55:25 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:55:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec87ba537290953e899b660193e5bb7f3878854413a2dfb4845bae815f2dbf7`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53637f2aa395282433b4bec0cb705eb8ff5b56f564c6ca9c6325ab47bc0874`  
		Last Modified: Wed, 05 Oct 2022 01:56:09 GMT  
		Size: 6.7 MB (6698608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe7771eede499889c711fe9577563e4fc035d8be22a96485abec7736baa8c8`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 1.3 MB (1258320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd61eff79af60ac4fdd43efe778148bc679cab9c6451d8da10055cb64646d25`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 293.1 KB (293055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f76fc240cdc66635f05cff5f3c124051443a27af50078e5bd496a0ae7ba73`  
		Last Modified: Wed, 05 Oct 2022 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189b747aebaca39179cbabc925e8ba8dd71ec37d4fd79f642d5f29a9ecbc4a2b`  
		Last Modified: Wed, 05 Oct 2022 01:56:27 GMT  
		Size: 49.1 MB (49134356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f404d48d2eb6da68bf8943dc98d738e84f5552bcae60de6dc77205b5607a54`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a812e3f5839156fd725135efbe606c5842f10069e24b33b17652b81dde8c243`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f99aea20b6247cd46ffaca4ecd3dc88abfeb920c4a6b9f3f3f7e43f945857`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d8746d2a396b502f7556c7272d84b2290857618924b2262e71d4dc128bea2`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9ea30e3d50b924a34e818d2831d8d5423b5d53ced52dc6dfdf9480f4ab0fa2b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ca5345ba308f5847527eb1f42a77ff4a2288caa8d67b3ee3037dbec81ac31`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:40:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:40:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:41:08 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 25 Oct 2022 08:41:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:41:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 25 Oct 2022 08:41:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:41:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:41:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:41:21 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:41:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63baddf4b4aada2e9cd0c13e4b0d54569f09066247805a3b044bc4345131c55`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befab36040f5596e6ba4aee532c1ca587e42f039f9c4f63d49f1d85cabfeca3f`  
		Last Modified: Tue, 25 Oct 2022 08:42:00 GMT  
		Size: 6.6 MB (6577008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875bb9efee93c19298ff30f16e44441c60694a5040ffb63f61af3672f2ee57d4`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 1.2 MB (1164499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c29a709f5f5425020e908c0d1b7c58e3d103dae6623855e8daaf7334bb4e0d`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a07b23847be1b061840e59e6e9124a2fbaee94fad57001b176ddf94d0865969`  
		Last Modified: Tue, 25 Oct 2022 08:42:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38afaa696e9e897a5c335473e50f0269259f2faa9f08cc74426bdb71a1f2a69b`  
		Last Modified: Tue, 25 Oct 2022 08:42:14 GMT  
		Size: 39.0 MB (39029631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f7b976d5f00f48b76f2fc5fcd3be6a5a00a2ccaa4ccf8f4fd7ad6a2a4d8c06`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999191422a2aa02e396d320c25bca44554ab97be5b822acc3f1ebbcbd0d7e078`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c865d00b66d280ebf1e15a4793e4ee56667b9dd8ee7c7c5679c8e8854c9ec12`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb94b462ccf70cac032dcd335be4b15c9865cd73adb7dbd9af10c1473ebb95`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:bb44133c719a2f72b23a2983449a70b1a0b528de7b14c1a6667667f2a15a7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6bfa0c63118cc551231a6c9f66888efe9994eff949c5cdf93c09a0140be77fc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84529402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2695394336cc3c0b33abf96483195d65b99ce6f3297899655bd2ecf038fc13`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:54:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:54:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:54:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:55:02 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 05 Oct 2022 01:55:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:55:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 05 Oct 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:55:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:55:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:55:25 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:55:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec87ba537290953e899b660193e5bb7f3878854413a2dfb4845bae815f2dbf7`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53637f2aa395282433b4bec0cb705eb8ff5b56f564c6ca9c6325ab47bc0874`  
		Last Modified: Wed, 05 Oct 2022 01:56:09 GMT  
		Size: 6.7 MB (6698608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe7771eede499889c711fe9577563e4fc035d8be22a96485abec7736baa8c8`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 1.3 MB (1258320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd61eff79af60ac4fdd43efe778148bc679cab9c6451d8da10055cb64646d25`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 293.1 KB (293055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f76fc240cdc66635f05cff5f3c124051443a27af50078e5bd496a0ae7ba73`  
		Last Modified: Wed, 05 Oct 2022 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189b747aebaca39179cbabc925e8ba8dd71ec37d4fd79f642d5f29a9ecbc4a2b`  
		Last Modified: Wed, 05 Oct 2022 01:56:27 GMT  
		Size: 49.1 MB (49134356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f404d48d2eb6da68bf8943dc98d738e84f5552bcae60de6dc77205b5607a54`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a812e3f5839156fd725135efbe606c5842f10069e24b33b17652b81dde8c243`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f99aea20b6247cd46ffaca4ecd3dc88abfeb920c4a6b9f3f3f7e43f945857`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d8746d2a396b502f7556c7272d84b2290857618924b2262e71d4dc128bea2`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9ea30e3d50b924a34e818d2831d8d5423b5d53ced52dc6dfdf9480f4ab0fa2b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ca5345ba308f5847527eb1f42a77ff4a2288caa8d67b3ee3037dbec81ac31`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:40:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:40:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:41:08 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 25 Oct 2022 08:41:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:41:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 25 Oct 2022 08:41:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:41:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:41:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:41:21 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:41:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63baddf4b4aada2e9cd0c13e4b0d54569f09066247805a3b044bc4345131c55`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befab36040f5596e6ba4aee532c1ca587e42f039f9c4f63d49f1d85cabfeca3f`  
		Last Modified: Tue, 25 Oct 2022 08:42:00 GMT  
		Size: 6.6 MB (6577008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875bb9efee93c19298ff30f16e44441c60694a5040ffb63f61af3672f2ee57d4`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 1.2 MB (1164499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c29a709f5f5425020e908c0d1b7c58e3d103dae6623855e8daaf7334bb4e0d`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a07b23847be1b061840e59e6e9124a2fbaee94fad57001b176ddf94d0865969`  
		Last Modified: Tue, 25 Oct 2022 08:42:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38afaa696e9e897a5c335473e50f0269259f2faa9f08cc74426bdb71a1f2a69b`  
		Last Modified: Tue, 25 Oct 2022 08:42:14 GMT  
		Size: 39.0 MB (39029631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f7b976d5f00f48b76f2fc5fcd3be6a5a00a2ccaa4ccf8f4fd7ad6a2a4d8c06`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999191422a2aa02e396d320c25bca44554ab97be5b822acc3f1ebbcbd0d7e078`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c865d00b66d280ebf1e15a4793e4ee56667b9dd8ee7c7c5679c8e8854c9ec12`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb94b462ccf70cac032dcd335be4b15c9865cd73adb7dbd9af10c1473ebb95`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:bb44133c719a2f72b23a2983449a70b1a0b528de7b14c1a6667667f2a15a7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:6bfa0c63118cc551231a6c9f66888efe9994eff949c5cdf93c09a0140be77fc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84529402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2695394336cc3c0b33abf96483195d65b99ce6f3297899655bd2ecf038fc13`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:54:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:54:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:54:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:55:02 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 05 Oct 2022 01:55:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:55:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:55:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 05 Oct 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:55:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:55:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:55:25 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:55:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec87ba537290953e899b660193e5bb7f3878854413a2dfb4845bae815f2dbf7`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53637f2aa395282433b4bec0cb705eb8ff5b56f564c6ca9c6325ab47bc0874`  
		Last Modified: Wed, 05 Oct 2022 01:56:09 GMT  
		Size: 6.7 MB (6698608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe7771eede499889c711fe9577563e4fc035d8be22a96485abec7736baa8c8`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 1.3 MB (1258320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd61eff79af60ac4fdd43efe778148bc679cab9c6451d8da10055cb64646d25`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 293.1 KB (293055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5f76fc240cdc66635f05cff5f3c124051443a27af50078e5bd496a0ae7ba73`  
		Last Modified: Wed, 05 Oct 2022 01:56:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189b747aebaca39179cbabc925e8ba8dd71ec37d4fd79f642d5f29a9ecbc4a2b`  
		Last Modified: Wed, 05 Oct 2022 01:56:27 GMT  
		Size: 49.1 MB (49134356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f404d48d2eb6da68bf8943dc98d738e84f5552bcae60de6dc77205b5607a54`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a812e3f5839156fd725135efbe606c5842f10069e24b33b17652b81dde8c243`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f99aea20b6247cd46ffaca4ecd3dc88abfeb920c4a6b9f3f3f7e43f945857`  
		Last Modified: Wed, 05 Oct 2022 01:56:20 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d8746d2a396b502f7556c7272d84b2290857618924b2262e71d4dc128bea2`  
		Last Modified: Wed, 05 Oct 2022 01:56:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9ea30e3d50b924a34e818d2831d8d5423b5d53ced52dc6dfdf9480f4ab0fa2b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ca5345ba308f5847527eb1f42a77ff4a2288caa8d67b3ee3037dbec81ac31`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:40:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:40:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:41:08 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 25 Oct 2022 08:41:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:41:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:41:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 25 Oct 2022 08:41:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:41:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:41:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:41:21 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:41:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63baddf4b4aada2e9cd0c13e4b0d54569f09066247805a3b044bc4345131c55`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befab36040f5596e6ba4aee532c1ca587e42f039f9c4f63d49f1d85cabfeca3f`  
		Last Modified: Tue, 25 Oct 2022 08:42:00 GMT  
		Size: 6.6 MB (6577008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875bb9efee93c19298ff30f16e44441c60694a5040ffb63f61af3672f2ee57d4`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 1.2 MB (1164499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c29a709f5f5425020e908c0d1b7c58e3d103dae6623855e8daaf7334bb4e0d`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a07b23847be1b061840e59e6e9124a2fbaee94fad57001b176ddf94d0865969`  
		Last Modified: Tue, 25 Oct 2022 08:42:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38afaa696e9e897a5c335473e50f0269259f2faa9f08cc74426bdb71a1f2a69b`  
		Last Modified: Tue, 25 Oct 2022 08:42:14 GMT  
		Size: 39.0 MB (39029631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f7b976d5f00f48b76f2fc5fcd3be6a5a00a2ccaa4ccf8f4fd7ad6a2a4d8c06`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999191422a2aa02e396d320c25bca44554ab97be5b822acc3f1ebbcbd0d7e078`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c865d00b66d280ebf1e15a4793e4ee56667b9dd8ee7c7c5679c8e8854c9ec12`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfb94b462ccf70cac032dcd335be4b15c9865cd73adb7dbd9af10c1473ebb95`  
		Last Modified: Tue, 25 Oct 2022 08:42:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:ef21112377bd5df6dacafc462d02123bb108814064cd81218f0d08972d76240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:c976642fe0bfed70d8481293702fb32f3fcfdac0950f239f069c45daf356be80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994fdcd357aad6beca4304e782ea3a7229ecba3e960b971af51f441d5239efa6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:53:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:53:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:53:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:53:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:52 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 05 Oct 2022 01:53:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:07 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:07 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:07 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50830c09adfb39841093b2852fab7bea49db61e68b181aa91f648c74e4fc3e0b`  
		Last Modified: Wed, 05 Oct 2022 01:55:48 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d0a873bcb23ad01abb767d707f3b6f081cb277e8c122922cf47a303ff355`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 5.2 MB (5224222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133338a2a25751a2cd2f69feab9b8f6df2ba1b6de10397de86f03bc729671988`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 1.6 MB (1553266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161d047ac6b618b63098da64cfe365c125d4f1c4fc18d6d0b37766316b72fa5a`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b72fa5f875f42c5673b59fc12f6c245e49d4f7bd00feb59be64338f8f1c1dde`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091ee36bd0f70205d0e31b10bbc8e7b208bc234f6cc6f3cc3f0783949ac4b2a`  
		Last Modified: Wed, 05 Oct 2022 01:55:49 GMT  
		Size: 49.0 MB (49045858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122333888771cf497009bb9f5b7ea36ab9f42124c802dd3cf7a288063965b0d1`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4e15d74c555d6cda273d6a13afd6916c978a8e719f392f84b1db3428b35f0`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295483f6e8ed514ad1436fee874f7dc7bc996719cab0933ba483af2464386e`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57950f766fe983d4ac0415aa1846954b52f66e8fd0abf3db9a77c7b829f523c2`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c6321e09db67f1dc549f0b88f47eecc661909a13df3091aa1c15dc5d612f4517
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86079388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e938314e7b989894f554622a99e2f8542531fc53907665142c0c627e40c9b19e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:39:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:39:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:08 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 08:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:40:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 08:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:40:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:40:22 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:40:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d23f6b06399e9bd464a459acdc4c5c668a317ab7231cffc5f27eac8199f72d`  
		Last Modified: Tue, 25 Oct 2022 08:41:41 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41831134def03097216279113f63f0641dd6a106c6dacab0e44d5bcdc04a1119`  
		Last Modified: Tue, 25 Oct 2022 08:41:40 GMT  
		Size: 5.2 MB (5210639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee1e386badd8830f59d5c191976d414ec54a54f881c953cfca494ecda5c7865`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 1.4 MB (1436840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaddafba9ea8080d1b03937df4a483be6b90049f69d6461597f6075f9fada1b`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7f6063276c306b3277136f1c37858808bb1b8026c5c7a1e497e58f6dd92c4`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b19d7b61b708513238e91d0d40922a634436964b676dcf00d19e2272ad729`  
		Last Modified: Tue, 25 Oct 2022 08:41:42 GMT  
		Size: 49.1 MB (49064645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fd5becf524c2c60380cbf6dc372680e6a8dee96da0ce01757ab6364c8b48`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72aeecb31de29af7924212303cfa1abac0569b9ff4d929e23086918d4da3ea0`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd8deb1668c6e9c4ba1901de4d52f1c741db7ccb81d3d6c0e6ce2f3586770`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395df954ad376ace92f48219e833cb04343fb6c72c1fd8379844422774bc0031`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:573d9f033093c79429f5843b2a1845aa5b5c8701a3d8cefa3bf152f2f1bce088
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a5850a83bb2bf101cfa7b9bb0103dcd391c3ab793dfc9e5f8b95a52a137e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:06:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 06:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 06:07:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 06:07:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 06:07:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:25 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 06:07:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 06:07:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 06:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 06:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 06:07:51 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 06:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff951905b209915c9a1df313fb16760244fac7d51fb589c9f6916ce989182da9`  
		Last Modified: Tue, 25 Oct 2022 06:08:19 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712443240476010b6c006ffa2d932751e6a255ccf2bd596dd1cbcc186e0fb5e`  
		Last Modified: Tue, 25 Oct 2022 06:08:18 GMT  
		Size: 6.0 MB (6045421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f46f597f71b51e9ffcdfe3f8cf65b3491a0ebfa511eb59f6e3ff451da97250`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 1.5 MB (1509798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bfa28563276da0d4ed400b10397b96bda9f17d00515d9d055228fbfe9fbd4`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 296.1 KB (296141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf29c43588bb1a85d84ad57b455a4deabff4dd3e3f08943c1856fbb833c10`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60206143ed7547d03f4b565c8a75579fee7d7f413101d112a407be39258a70b1`  
		Last Modified: Tue, 25 Oct 2022 06:08:24 GMT  
		Size: 50.1 MB (50086243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbc205c67ebc790386455cf628f98ef1efd3d8e904116ebcb13960e8f60824`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef686fe48f6ff7d5d868d3cd987b968a42d57e6aa75fe77fee0e915ebcffa789`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62513520123c4ad12dd19aa946930c527f1ed47cf745829a9e3edcc51f36cbe`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1f67b4e79b0ebb1f15b26357f97af2973fc445cb7a1f41c9460ce5821d26`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:b9443bc99665a97a9b7a2f1510d4909dee9f20423d95329de46cffc071d10b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:15609f891bb0ed4f6de7d11c1a98c79f2853f6de9c19d4f7e06d42d5a17d5176
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80012333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888ba1d853302d491c8a60072926ec8247c1b7862d03ac25f6b22b1223a1798`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:54:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:54:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:54:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:37 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 05 Oct 2022 01:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:54 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:54 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec87ba537290953e899b660193e5bb7f3878854413a2dfb4845bae815f2dbf7`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53637f2aa395282433b4bec0cb705eb8ff5b56f564c6ca9c6325ab47bc0874`  
		Last Modified: Wed, 05 Oct 2022 01:56:09 GMT  
		Size: 6.7 MB (6698608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe7771eede499889c711fe9577563e4fc035d8be22a96485abec7736baa8c8`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 1.3 MB (1258320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd61eff79af60ac4fdd43efe778148bc679cab9c6451d8da10055cb64646d25`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 293.1 KB (293055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf2434bf12d16c23376086e5d672fef9fbf805c698ce76799acdd548609c4a0`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649966bbf588d3d9b99a775bdb8852a4788fab5d5992dd08c50afd31ac8ea152`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 44.6 MB (44617299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da212b8578d97d290894dd4ebdf54f781a4796f7904ce4abcbdc42f192acd621`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e9c1267dd05667e858fd996aa85bb035fdc47f222d8a54c9b1d0c9837c9c1a`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423db0aa4e277f15b985f531a7ae8b4874ba8e223aa4d17029d6ee9620d23cf1`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5b95744f6902108ecec623a6f2cbfab6eb669799ee90d4a6a8d37d7daa8734`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9c8a6574b7ecc838c0755376f987b634eaab3f364c3498d0f64f7f4ba5d730bb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d6e2b4976f2576274b4f14c29442d5de7c5ac779ad2996b1be990602177f68`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:40:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:40:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 25 Oct 2022 08:40:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:41:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:41:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:41:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:41:01 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 25 Oct 2022 08:41:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:41:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:41:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:41:01 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:41:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63baddf4b4aada2e9cd0c13e4b0d54569f09066247805a3b044bc4345131c55`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befab36040f5596e6ba4aee532c1ca587e42f039f9c4f63d49f1d85cabfeca3f`  
		Last Modified: Tue, 25 Oct 2022 08:42:00 GMT  
		Size: 6.6 MB (6577008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875bb9efee93c19298ff30f16e44441c60694a5040ffb63f61af3672f2ee57d4`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 1.2 MB (1164499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c29a709f5f5425020e908c0d1b7c58e3d103dae6623855e8daaf7334bb4e0d`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca68eda53bd05ec736fc92cb9b7ef51afbf57496e8baff68dbf0bd943b44bdd`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042e6cdb78ced50a44ab23ba2f14ef695b8ae0818eb4cebcba0027d7ec13ab35`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 41.1 MB (41121741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2edd080cb80d60aa1d3160f6ccdf2c9383ed999e3d6a82946bd822b751320`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6811d7c4ccbe13e726975e1d4eccdb8234d76532a9c895259e68f8e5b7a45d1`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e20853ca11ddf8f1cf5dcbdd2da41fd0803010abddaa5fadbf8f007acf6e20d`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e611ec39ee8dc9d8190d19bb7204dc5e417382d3cf7a9fdcea29819d49487a65`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:b9443bc99665a97a9b7a2f1510d4909dee9f20423d95329de46cffc071d10b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:15609f891bb0ed4f6de7d11c1a98c79f2853f6de9c19d4f7e06d42d5a17d5176
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80012333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8888ba1d853302d491c8a60072926ec8247c1b7862d03ac25f6b22b1223a1798`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:54:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:54:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:54:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:54:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:54:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:54:37 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 05 Oct 2022 01:54:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:53 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:54 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:54 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec87ba537290953e899b660193e5bb7f3878854413a2dfb4845bae815f2dbf7`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53637f2aa395282433b4bec0cb705eb8ff5b56f564c6ca9c6325ab47bc0874`  
		Last Modified: Wed, 05 Oct 2022 01:56:09 GMT  
		Size: 6.7 MB (6698608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe7771eede499889c711fe9577563e4fc035d8be22a96485abec7736baa8c8`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 1.3 MB (1258320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd61eff79af60ac4fdd43efe778148bc679cab9c6451d8da10055cb64646d25`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 293.1 KB (293055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf2434bf12d16c23376086e5d672fef9fbf805c698ce76799acdd548609c4a0`  
		Last Modified: Wed, 05 Oct 2022 01:56:08 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649966bbf588d3d9b99a775bdb8852a4788fab5d5992dd08c50afd31ac8ea152`  
		Last Modified: Wed, 05 Oct 2022 01:56:10 GMT  
		Size: 44.6 MB (44617299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da212b8578d97d290894dd4ebdf54f781a4796f7904ce4abcbdc42f192acd621`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e9c1267dd05667e858fd996aa85bb035fdc47f222d8a54c9b1d0c9837c9c1a`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423db0aa4e277f15b985f531a7ae8b4874ba8e223aa4d17029d6ee9620d23cf1`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5b95744f6902108ecec623a6f2cbfab6eb669799ee90d4a6a8d37d7daa8734`  
		Last Modified: Wed, 05 Oct 2022 01:56:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9c8a6574b7ecc838c0755376f987b634eaab3f364c3498d0f64f7f4ba5d730bb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d6e2b4976f2576274b4f14c29442d5de7c5ac779ad2996b1be990602177f68`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:40:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:40:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 25 Oct 2022 08:40:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:41:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:41:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:41:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:41:01 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 25 Oct 2022 08:41:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:41:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:41:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:41:01 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:41:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63baddf4b4aada2e9cd0c13e4b0d54569f09066247805a3b044bc4345131c55`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befab36040f5596e6ba4aee532c1ca587e42f039f9c4f63d49f1d85cabfeca3f`  
		Last Modified: Tue, 25 Oct 2022 08:42:00 GMT  
		Size: 6.6 MB (6577008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875bb9efee93c19298ff30f16e44441c60694a5040ffb63f61af3672f2ee57d4`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 1.2 MB (1164499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c29a709f5f5425020e908c0d1b7c58e3d103dae6623855e8daaf7334bb4e0d`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca68eda53bd05ec736fc92cb9b7ef51afbf57496e8baff68dbf0bd943b44bdd`  
		Last Modified: Tue, 25 Oct 2022 08:41:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042e6cdb78ced50a44ab23ba2f14ef695b8ae0818eb4cebcba0027d7ec13ab35`  
		Last Modified: Tue, 25 Oct 2022 08:42:01 GMT  
		Size: 41.1 MB (41121741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2edd080cb80d60aa1d3160f6ccdf2c9383ed999e3d6a82946bd822b751320`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6811d7c4ccbe13e726975e1d4eccdb8234d76532a9c895259e68f8e5b7a45d1`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e20853ca11ddf8f1cf5dcbdd2da41fd0803010abddaa5fadbf8f007acf6e20d`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e611ec39ee8dc9d8190d19bb7204dc5e417382d3cf7a9fdcea29819d49487a65`  
		Last Modified: Tue, 25 Oct 2022 08:41:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:ef21112377bd5df6dacafc462d02123bb108814064cd81218f0d08972d76240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:c976642fe0bfed70d8481293702fb32f3fcfdac0950f239f069c45daf356be80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994fdcd357aad6beca4304e782ea3a7229ecba3e960b971af51f441d5239efa6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:53:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:53:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:53:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:53:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:52 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 05 Oct 2022 01:53:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:07 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:07 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:07 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50830c09adfb39841093b2852fab7bea49db61e68b181aa91f648c74e4fc3e0b`  
		Last Modified: Wed, 05 Oct 2022 01:55:48 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d0a873bcb23ad01abb767d707f3b6f081cb277e8c122922cf47a303ff355`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 5.2 MB (5224222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133338a2a25751a2cd2f69feab9b8f6df2ba1b6de10397de86f03bc729671988`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 1.6 MB (1553266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161d047ac6b618b63098da64cfe365c125d4f1c4fc18d6d0b37766316b72fa5a`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b72fa5f875f42c5673b59fc12f6c245e49d4f7bd00feb59be64338f8f1c1dde`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091ee36bd0f70205d0e31b10bbc8e7b208bc234f6cc6f3cc3f0783949ac4b2a`  
		Last Modified: Wed, 05 Oct 2022 01:55:49 GMT  
		Size: 49.0 MB (49045858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122333888771cf497009bb9f5b7ea36ab9f42124c802dd3cf7a288063965b0d1`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4e15d74c555d6cda273d6a13afd6916c978a8e719f392f84b1db3428b35f0`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295483f6e8ed514ad1436fee874f7dc7bc996719cab0933ba483af2464386e`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57950f766fe983d4ac0415aa1846954b52f66e8fd0abf3db9a77c7b829f523c2`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c6321e09db67f1dc549f0b88f47eecc661909a13df3091aa1c15dc5d612f4517
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86079388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e938314e7b989894f554622a99e2f8542531fc53907665142c0c627e40c9b19e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:39:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:39:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:08 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 08:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:40:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 08:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:40:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:40:22 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:40:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d23f6b06399e9bd464a459acdc4c5c668a317ab7231cffc5f27eac8199f72d`  
		Last Modified: Tue, 25 Oct 2022 08:41:41 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41831134def03097216279113f63f0641dd6a106c6dacab0e44d5bcdc04a1119`  
		Last Modified: Tue, 25 Oct 2022 08:41:40 GMT  
		Size: 5.2 MB (5210639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee1e386badd8830f59d5c191976d414ec54a54f881c953cfca494ecda5c7865`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 1.4 MB (1436840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaddafba9ea8080d1b03937df4a483be6b90049f69d6461597f6075f9fada1b`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7f6063276c306b3277136f1c37858808bb1b8026c5c7a1e497e58f6dd92c4`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b19d7b61b708513238e91d0d40922a634436964b676dcf00d19e2272ad729`  
		Last Modified: Tue, 25 Oct 2022 08:41:42 GMT  
		Size: 49.1 MB (49064645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fd5becf524c2c60380cbf6dc372680e6a8dee96da0ce01757ab6364c8b48`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72aeecb31de29af7924212303cfa1abac0569b9ff4d929e23086918d4da3ea0`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd8deb1668c6e9c4ba1901de4d52f1c741db7ccb81d3d6c0e6ce2f3586770`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395df954ad376ace92f48219e833cb04343fb6c72c1fd8379844422774bc0031`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:573d9f033093c79429f5843b2a1845aa5b5c8701a3d8cefa3bf152f2f1bce088
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a5850a83bb2bf101cfa7b9bb0103dcd391c3ab793dfc9e5f8b95a52a137e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:06:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 06:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 06:07:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 06:07:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 06:07:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:25 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 06:07:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 06:07:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 06:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 06:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 06:07:51 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 06:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff951905b209915c9a1df313fb16760244fac7d51fb589c9f6916ce989182da9`  
		Last Modified: Tue, 25 Oct 2022 06:08:19 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712443240476010b6c006ffa2d932751e6a255ccf2bd596dd1cbcc186e0fb5e`  
		Last Modified: Tue, 25 Oct 2022 06:08:18 GMT  
		Size: 6.0 MB (6045421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f46f597f71b51e9ffcdfe3f8cf65b3491a0ebfa511eb59f6e3ff451da97250`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 1.5 MB (1509798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bfa28563276da0d4ed400b10397b96bda9f17d00515d9d055228fbfe9fbd4`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 296.1 KB (296141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf29c43588bb1a85d84ad57b455a4deabff4dd3e3f08943c1856fbb833c10`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60206143ed7547d03f4b565c8a75579fee7d7f413101d112a407be39258a70b1`  
		Last Modified: Tue, 25 Oct 2022 06:08:24 GMT  
		Size: 50.1 MB (50086243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbc205c67ebc790386455cf628f98ef1efd3d8e904116ebcb13960e8f60824`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef686fe48f6ff7d5d868d3cd987b968a42d57e6aa75fe77fee0e915ebcffa789`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62513520123c4ad12dd19aa946930c527f1ed47cf745829a9e3edcc51f36cbe`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1f67b4e79b0ebb1f15b26357f97af2973fc445cb7a1f41c9460ce5821d26`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:ef21112377bd5df6dacafc462d02123bb108814064cd81218f0d08972d76240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:c976642fe0bfed70d8481293702fb32f3fcfdac0950f239f069c45daf356be80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994fdcd357aad6beca4304e782ea3a7229ecba3e960b971af51f441d5239efa6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:53:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:53:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:53:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:53:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:52 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 05 Oct 2022 01:53:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:07 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:07 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:07 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50830c09adfb39841093b2852fab7bea49db61e68b181aa91f648c74e4fc3e0b`  
		Last Modified: Wed, 05 Oct 2022 01:55:48 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d0a873bcb23ad01abb767d707f3b6f081cb277e8c122922cf47a303ff355`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 5.2 MB (5224222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133338a2a25751a2cd2f69feab9b8f6df2ba1b6de10397de86f03bc729671988`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 1.6 MB (1553266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161d047ac6b618b63098da64cfe365c125d4f1c4fc18d6d0b37766316b72fa5a`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b72fa5f875f42c5673b59fc12f6c245e49d4f7bd00feb59be64338f8f1c1dde`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091ee36bd0f70205d0e31b10bbc8e7b208bc234f6cc6f3cc3f0783949ac4b2a`  
		Last Modified: Wed, 05 Oct 2022 01:55:49 GMT  
		Size: 49.0 MB (49045858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122333888771cf497009bb9f5b7ea36ab9f42124c802dd3cf7a288063965b0d1`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4e15d74c555d6cda273d6a13afd6916c978a8e719f392f84b1db3428b35f0`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295483f6e8ed514ad1436fee874f7dc7bc996719cab0933ba483af2464386e`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57950f766fe983d4ac0415aa1846954b52f66e8fd0abf3db9a77c7b829f523c2`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c6321e09db67f1dc549f0b88f47eecc661909a13df3091aa1c15dc5d612f4517
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86079388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e938314e7b989894f554622a99e2f8542531fc53907665142c0c627e40c9b19e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:39:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:39:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:08 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 08:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:40:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 08:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:40:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:40:22 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:40:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d23f6b06399e9bd464a459acdc4c5c668a317ab7231cffc5f27eac8199f72d`  
		Last Modified: Tue, 25 Oct 2022 08:41:41 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41831134def03097216279113f63f0641dd6a106c6dacab0e44d5bcdc04a1119`  
		Last Modified: Tue, 25 Oct 2022 08:41:40 GMT  
		Size: 5.2 MB (5210639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee1e386badd8830f59d5c191976d414ec54a54f881c953cfca494ecda5c7865`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 1.4 MB (1436840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaddafba9ea8080d1b03937df4a483be6b90049f69d6461597f6075f9fada1b`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7f6063276c306b3277136f1c37858808bb1b8026c5c7a1e497e58f6dd92c4`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b19d7b61b708513238e91d0d40922a634436964b676dcf00d19e2272ad729`  
		Last Modified: Tue, 25 Oct 2022 08:41:42 GMT  
		Size: 49.1 MB (49064645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fd5becf524c2c60380cbf6dc372680e6a8dee96da0ce01757ab6364c8b48`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72aeecb31de29af7924212303cfa1abac0569b9ff4d929e23086918d4da3ea0`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd8deb1668c6e9c4ba1901de4d52f1c741db7ccb81d3d6c0e6ce2f3586770`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395df954ad376ace92f48219e833cb04343fb6c72c1fd8379844422774bc0031`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:573d9f033093c79429f5843b2a1845aa5b5c8701a3d8cefa3bf152f2f1bce088
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a5850a83bb2bf101cfa7b9bb0103dcd391c3ab793dfc9e5f8b95a52a137e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:06:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 06:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 06:07:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 06:07:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 06:07:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:25 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 06:07:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 06:07:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 06:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 06:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 06:07:51 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 06:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff951905b209915c9a1df313fb16760244fac7d51fb589c9f6916ce989182da9`  
		Last Modified: Tue, 25 Oct 2022 06:08:19 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712443240476010b6c006ffa2d932751e6a255ccf2bd596dd1cbcc186e0fb5e`  
		Last Modified: Tue, 25 Oct 2022 06:08:18 GMT  
		Size: 6.0 MB (6045421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f46f597f71b51e9ffcdfe3f8cf65b3491a0ebfa511eb59f6e3ff451da97250`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 1.5 MB (1509798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bfa28563276da0d4ed400b10397b96bda9f17d00515d9d055228fbfe9fbd4`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 296.1 KB (296141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf29c43588bb1a85d84ad57b455a4deabff4dd3e3f08943c1856fbb833c10`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60206143ed7547d03f4b565c8a75579fee7d7f413101d112a407be39258a70b1`  
		Last Modified: Tue, 25 Oct 2022 06:08:24 GMT  
		Size: 50.1 MB (50086243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbc205c67ebc790386455cf628f98ef1efd3d8e904116ebcb13960e8f60824`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef686fe48f6ff7d5d868d3cd987b968a42d57e6aa75fe77fee0e915ebcffa789`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62513520123c4ad12dd19aa946930c527f1ed47cf745829a9e3edcc51f36cbe`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1f67b4e79b0ebb1f15b26357f97af2973fc445cb7a1f41c9460ce5821d26`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ef21112377bd5df6dacafc462d02123bb108814064cd81218f0d08972d76240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:c976642fe0bfed70d8481293702fb32f3fcfdac0950f239f069c45daf356be80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994fdcd357aad6beca4304e782ea3a7229ecba3e960b971af51f441d5239efa6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:53:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:53:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:53:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:53:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:52 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 05 Oct 2022 01:53:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:07 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:07 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:07 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50830c09adfb39841093b2852fab7bea49db61e68b181aa91f648c74e4fc3e0b`  
		Last Modified: Wed, 05 Oct 2022 01:55:48 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d0a873bcb23ad01abb767d707f3b6f081cb277e8c122922cf47a303ff355`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 5.2 MB (5224222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133338a2a25751a2cd2f69feab9b8f6df2ba1b6de10397de86f03bc729671988`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 1.6 MB (1553266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161d047ac6b618b63098da64cfe365c125d4f1c4fc18d6d0b37766316b72fa5a`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b72fa5f875f42c5673b59fc12f6c245e49d4f7bd00feb59be64338f8f1c1dde`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091ee36bd0f70205d0e31b10bbc8e7b208bc234f6cc6f3cc3f0783949ac4b2a`  
		Last Modified: Wed, 05 Oct 2022 01:55:49 GMT  
		Size: 49.0 MB (49045858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122333888771cf497009bb9f5b7ea36ab9f42124c802dd3cf7a288063965b0d1`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4e15d74c555d6cda273d6a13afd6916c978a8e719f392f84b1db3428b35f0`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295483f6e8ed514ad1436fee874f7dc7bc996719cab0933ba483af2464386e`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57950f766fe983d4ac0415aa1846954b52f66e8fd0abf3db9a77c7b829f523c2`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c6321e09db67f1dc549f0b88f47eecc661909a13df3091aa1c15dc5d612f4517
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86079388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e938314e7b989894f554622a99e2f8542531fc53907665142c0c627e40c9b19e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:39:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:39:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:08 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 08:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:40:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 08:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:40:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:40:22 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:40:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d23f6b06399e9bd464a459acdc4c5c668a317ab7231cffc5f27eac8199f72d`  
		Last Modified: Tue, 25 Oct 2022 08:41:41 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41831134def03097216279113f63f0641dd6a106c6dacab0e44d5bcdc04a1119`  
		Last Modified: Tue, 25 Oct 2022 08:41:40 GMT  
		Size: 5.2 MB (5210639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee1e386badd8830f59d5c191976d414ec54a54f881c953cfca494ecda5c7865`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 1.4 MB (1436840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaddafba9ea8080d1b03937df4a483be6b90049f69d6461597f6075f9fada1b`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7f6063276c306b3277136f1c37858808bb1b8026c5c7a1e497e58f6dd92c4`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b19d7b61b708513238e91d0d40922a634436964b676dcf00d19e2272ad729`  
		Last Modified: Tue, 25 Oct 2022 08:41:42 GMT  
		Size: 49.1 MB (49064645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fd5becf524c2c60380cbf6dc372680e6a8dee96da0ce01757ab6364c8b48`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72aeecb31de29af7924212303cfa1abac0569b9ff4d929e23086918d4da3ea0`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd8deb1668c6e9c4ba1901de4d52f1c741db7ccb81d3d6c0e6ce2f3586770`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395df954ad376ace92f48219e833cb04343fb6c72c1fd8379844422774bc0031`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:573d9f033093c79429f5843b2a1845aa5b5c8701a3d8cefa3bf152f2f1bce088
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a5850a83bb2bf101cfa7b9bb0103dcd391c3ab793dfc9e5f8b95a52a137e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:06:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 06:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 06:07:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 06:07:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 06:07:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:25 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 06:07:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 06:07:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 06:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 06:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 06:07:51 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 06:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff951905b209915c9a1df313fb16760244fac7d51fb589c9f6916ce989182da9`  
		Last Modified: Tue, 25 Oct 2022 06:08:19 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712443240476010b6c006ffa2d932751e6a255ccf2bd596dd1cbcc186e0fb5e`  
		Last Modified: Tue, 25 Oct 2022 06:08:18 GMT  
		Size: 6.0 MB (6045421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f46f597f71b51e9ffcdfe3f8cf65b3491a0ebfa511eb59f6e3ff451da97250`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 1.5 MB (1509798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bfa28563276da0d4ed400b10397b96bda9f17d00515d9d055228fbfe9fbd4`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 296.1 KB (296141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf29c43588bb1a85d84ad57b455a4deabff4dd3e3f08943c1856fbb833c10`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60206143ed7547d03f4b565c8a75579fee7d7f413101d112a407be39258a70b1`  
		Last Modified: Tue, 25 Oct 2022 06:08:24 GMT  
		Size: 50.1 MB (50086243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbc205c67ebc790386455cf628f98ef1efd3d8e904116ebcb13960e8f60824`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef686fe48f6ff7d5d868d3cd987b968a42d57e6aa75fe77fee0e915ebcffa789`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62513520123c4ad12dd19aa946930c527f1ed47cf745829a9e3edcc51f36cbe`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1f67b4e79b0ebb1f15b26357f97af2973fc445cb7a1f41c9460ce5821d26`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
