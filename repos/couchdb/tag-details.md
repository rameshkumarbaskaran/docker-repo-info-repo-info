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
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.0`](#couchdb330)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:2e48c0f4c5bd780169441fcdc5e0ccc545e2f5df14a0e7fdb288bde4818beed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:faa4bad03f67fe520fe6d1186416421b9b08af9e0399d3a16a42d708bd900b36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99841f3c007859c2e9cd5d253f583c3a0d0b6c338d7da7d2f397b1c1a049c7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:13:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:13:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:13:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:14:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 02:14:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:14:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 02:14:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:14:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:14:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:14:25 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:14:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599972720d277bc9a925bb59800bdd64971c76cfa26d972c7f40bdae656c68`  
		Last Modified: Wed, 21 Dec 2022 02:15:03 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f31a37f3c3e5747853e6e73bdc461cef5f603c301340e10c8fd97e24d4a06`  
		Last Modified: Wed, 21 Dec 2022 02:15:02 GMT  
		Size: 6.7 MB (6703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306ba540d4a9b1833b8ecf78343b47b37b6d63368d25bcf12f44b74791f8d91`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 1.3 MB (1259591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2648fe29e85ce421ec043671fbfff24fa8797d7d3f6c90badd7e34e8b7da2ec6`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a029c99062a4d83896a5a2f0b4f4eecb459fae065e598f5d55bdc76044aafcb4`  
		Last Modified: Wed, 21 Dec 2022 02:15:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ccf5550a2d23cc9d1897b57475a6dabf05f8895858afea80e671f390fb8f5`  
		Last Modified: Wed, 21 Dec 2022 02:15:19 GMT  
		Size: 49.1 MB (49132020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17be2e72c8ec40eb18fd7dd0d7752f47effab0b0cdeb7606364ed6e21359602`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c976932fe76368a2d801d183b2541938338bf39509a5674679b7fd818748b5d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe773d5970b7247ee6b67a5bf858bc78efcc7972a06a18c9cfcb421127646d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eb75e8148a1eee8bdb31f53c286f798ac1688f634b44ef9031a398c87169b0`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6a84c09dab4b1aa21831bf3d5a78280574d56920fd72f83b8d966c85e885525d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ac3a78172cbb2fafdf89d544ee562f4105d73d24833a2173e69d16212eeed0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:12:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:12:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:27 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 13:12:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 13:12:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 13:12:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 13:12:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 13:12:39 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 13:12:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5a5bc38e201ba09541494349d57ab285af692792c14ed4df572f9c2410a7`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668e1f80fab4a2656ef6f91303e052f69af0c0aa0a43de2bf5eb3dd2c1e5a66`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 6.6 MB (6577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8562d18e321736f052a9519034bfdcc57006ac8b2c4eb6f21a745c03b25baed`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 1.2 MB (1164524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be39e752322b09b2612e6fd2a5f42504043f78fd87e2b8a7d3afc74e63a1e3e`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 294.1 KB (294138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7d49f8d0ea47be8666ff8ba1b9a84d380904d8be474dd5746fcc9c6009519`  
		Last Modified: Wed, 21 Dec 2022 13:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ffe69eab3224742e9f7fc31423710bb9f92fcb8c3e88517c276e2285c5eb51`  
		Last Modified: Wed, 21 Dec 2022 13:13:32 GMT  
		Size: 39.0 MB (39029784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b403c23d89650fd14423e7cd9084c2ec6cbab951a2652f5d9538c5cc3ac5003`  
		Last Modified: Wed, 21 Dec 2022 13:13:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a698b6a7dc171386e23a5780ec6b1d38fa1f72b42cf278a951672e710f1b4e3`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af647178629b1f87a37de11a38ed6cdc4811173878f1e061fee26e58590ab0`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a02a4c2467a9e3dea074da20f201a159ab8ecd7af276ecbf77c36f05aea2ef`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:2e48c0f4c5bd780169441fcdc5e0ccc545e2f5df14a0e7fdb288bde4818beed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:faa4bad03f67fe520fe6d1186416421b9b08af9e0399d3a16a42d708bd900b36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99841f3c007859c2e9cd5d253f583c3a0d0b6c338d7da7d2f397b1c1a049c7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:13:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:13:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:13:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:14:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 02:14:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:14:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 02:14:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:14:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:14:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:14:25 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:14:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599972720d277bc9a925bb59800bdd64971c76cfa26d972c7f40bdae656c68`  
		Last Modified: Wed, 21 Dec 2022 02:15:03 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f31a37f3c3e5747853e6e73bdc461cef5f603c301340e10c8fd97e24d4a06`  
		Last Modified: Wed, 21 Dec 2022 02:15:02 GMT  
		Size: 6.7 MB (6703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306ba540d4a9b1833b8ecf78343b47b37b6d63368d25bcf12f44b74791f8d91`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 1.3 MB (1259591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2648fe29e85ce421ec043671fbfff24fa8797d7d3f6c90badd7e34e8b7da2ec6`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a029c99062a4d83896a5a2f0b4f4eecb459fae065e598f5d55bdc76044aafcb4`  
		Last Modified: Wed, 21 Dec 2022 02:15:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ccf5550a2d23cc9d1897b57475a6dabf05f8895858afea80e671f390fb8f5`  
		Last Modified: Wed, 21 Dec 2022 02:15:19 GMT  
		Size: 49.1 MB (49132020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17be2e72c8ec40eb18fd7dd0d7752f47effab0b0cdeb7606364ed6e21359602`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c976932fe76368a2d801d183b2541938338bf39509a5674679b7fd818748b5d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe773d5970b7247ee6b67a5bf858bc78efcc7972a06a18c9cfcb421127646d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eb75e8148a1eee8bdb31f53c286f798ac1688f634b44ef9031a398c87169b0`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6a84c09dab4b1aa21831bf3d5a78280574d56920fd72f83b8d966c85e885525d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ac3a78172cbb2fafdf89d544ee562f4105d73d24833a2173e69d16212eeed0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:12:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:12:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:27 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 13:12:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 13:12:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 13:12:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 13:12:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 13:12:39 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 13:12:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5a5bc38e201ba09541494349d57ab285af692792c14ed4df572f9c2410a7`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668e1f80fab4a2656ef6f91303e052f69af0c0aa0a43de2bf5eb3dd2c1e5a66`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 6.6 MB (6577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8562d18e321736f052a9519034bfdcc57006ac8b2c4eb6f21a745c03b25baed`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 1.2 MB (1164524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be39e752322b09b2612e6fd2a5f42504043f78fd87e2b8a7d3afc74e63a1e3e`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 294.1 KB (294138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7d49f8d0ea47be8666ff8ba1b9a84d380904d8be474dd5746fcc9c6009519`  
		Last Modified: Wed, 21 Dec 2022 13:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ffe69eab3224742e9f7fc31423710bb9f92fcb8c3e88517c276e2285c5eb51`  
		Last Modified: Wed, 21 Dec 2022 13:13:32 GMT  
		Size: 39.0 MB (39029784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b403c23d89650fd14423e7cd9084c2ec6cbab951a2652f5d9538c5cc3ac5003`  
		Last Modified: Wed, 21 Dec 2022 13:13:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a698b6a7dc171386e23a5780ec6b1d38fa1f72b42cf278a951672e710f1b4e3`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af647178629b1f87a37de11a38ed6cdc4811173878f1e061fee26e58590ab0`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a02a4c2467a9e3dea074da20f201a159ab8ecd7af276ecbf77c36f05aea2ef`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:2e48c0f4c5bd780169441fcdc5e0ccc545e2f5df14a0e7fdb288bde4818beed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:faa4bad03f67fe520fe6d1186416421b9b08af9e0399d3a16a42d708bd900b36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f99841f3c007859c2e9cd5d253f583c3a0d0b6c338d7da7d2f397b1c1a049c7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:13:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:13:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:13:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:14:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 02:14:01 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:14:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:14:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 02:14:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:14:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:14:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:14:25 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:14:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599972720d277bc9a925bb59800bdd64971c76cfa26d972c7f40bdae656c68`  
		Last Modified: Wed, 21 Dec 2022 02:15:03 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f31a37f3c3e5747853e6e73bdc461cef5f603c301340e10c8fd97e24d4a06`  
		Last Modified: Wed, 21 Dec 2022 02:15:02 GMT  
		Size: 6.7 MB (6703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306ba540d4a9b1833b8ecf78343b47b37b6d63368d25bcf12f44b74791f8d91`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 1.3 MB (1259591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2648fe29e85ce421ec043671fbfff24fa8797d7d3f6c90badd7e34e8b7da2ec6`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a029c99062a4d83896a5a2f0b4f4eecb459fae065e598f5d55bdc76044aafcb4`  
		Last Modified: Wed, 21 Dec 2022 02:15:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ccf5550a2d23cc9d1897b57475a6dabf05f8895858afea80e671f390fb8f5`  
		Last Modified: Wed, 21 Dec 2022 02:15:19 GMT  
		Size: 49.1 MB (49132020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17be2e72c8ec40eb18fd7dd0d7752f47effab0b0cdeb7606364ed6e21359602`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c976932fe76368a2d801d183b2541938338bf39509a5674679b7fd818748b5d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defe773d5970b7247ee6b67a5bf858bc78efcc7972a06a18c9cfcb421127646d`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8eb75e8148a1eee8bdb31f53c286f798ac1688f634b44ef9031a398c87169b0`  
		Last Modified: Wed, 21 Dec 2022 02:15:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6a84c09dab4b1aa21831bf3d5a78280574d56920fd72f83b8d966c85e885525d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ac3a78172cbb2fafdf89d544ee562f4105d73d24833a2173e69d16212eeed0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:12:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:12:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:27 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 21 Dec 2022 13:12:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 13:12:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 13:12:39 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 21 Dec 2022 13:12:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 13:12:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 13:12:39 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 13:12:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5a5bc38e201ba09541494349d57ab285af692792c14ed4df572f9c2410a7`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668e1f80fab4a2656ef6f91303e052f69af0c0aa0a43de2bf5eb3dd2c1e5a66`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 6.6 MB (6577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8562d18e321736f052a9519034bfdcc57006ac8b2c4eb6f21a745c03b25baed`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 1.2 MB (1164524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be39e752322b09b2612e6fd2a5f42504043f78fd87e2b8a7d3afc74e63a1e3e`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 294.1 KB (294138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa7d49f8d0ea47be8666ff8ba1b9a84d380904d8be474dd5746fcc9c6009519`  
		Last Modified: Wed, 21 Dec 2022 13:13:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ffe69eab3224742e9f7fc31423710bb9f92fcb8c3e88517c276e2285c5eb51`  
		Last Modified: Wed, 21 Dec 2022 13:13:32 GMT  
		Size: 39.0 MB (39029784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b403c23d89650fd14423e7cd9084c2ec6cbab951a2652f5d9538c5cc3ac5003`  
		Last Modified: Wed, 21 Dec 2022 13:13:29 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a698b6a7dc171386e23a5780ec6b1d38fa1f72b42cf278a951672e710f1b4e3`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af647178629b1f87a37de11a38ed6cdc4811173878f1e061fee26e58590ab0`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a02a4c2467a9e3dea074da20f201a159ab8ecd7af276ecbf77c36f05aea2ef`  
		Last Modified: Wed, 21 Dec 2022 13:13:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:09d5e033b3bc4bd43746529188747ea1f3171da37b030ed6d1870f69fcfb4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:ae80ecafc17c7ef87bfdb48d69602430d7b9385dc666c073d19817ad0c456583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e62b803500e1bbd5105b8bfe4c1c372c5c3a2fbc2dd89826bdf602c86047ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:31 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:19:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:19:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:19:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:19:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:19:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:19:48 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:19:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c62d73e217ebcfa696424d7c95f8610cc5ee5da6240e78a2e23fbea2a71761`  
		Last Modified: Tue, 03 Jan 2023 19:20:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f73fb31abf025dc7d4587f0e5d256a8559b6913815dbfcb7988b3aecc367ff`  
		Last Modified: Tue, 03 Jan 2023 19:20:33 GMT  
		Size: 52.7 MB (52693343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f4bc08af527a609227c3cc58148897c6eec4393bdc0bb263c6665af5d3ff7f`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc36a9ae0123374334b0e35f54b03c04e941986d0a68a82743982df25965498a`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce58becc6cea75ef160aeb1a391f98a5844102b03218d3d1f54338eb3ff579`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba1b55341bd92f3d1c3aba399c6f8fd91459e2bb0dcdb17800c7e94e8746000`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:49a21e5dcf9e588fc373b349539ca9e379a350eea42759624c3ad32f8c78e10b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750df03b82c0c75a7aed000f336407f5b66bbabaef8324520027019ec3924a2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:21 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:39:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:35 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:35 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc34651a5eb9515b747b593eea303ee2aefc01bc69aebf056ee34ac9b43d707`  
		Last Modified: Tue, 03 Jan 2023 19:40:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801ea55c77f52bf2940d3992c1e0a9d9483e810751da53de238b4967ebf1432`  
		Last Modified: Tue, 03 Jan 2023 19:40:15 GMT  
		Size: 52.5 MB (52549578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf19cf12b569a6f86a0e2db033a8ff1fa36e551e5d84ef62b4bfa9d56c5a171`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478b465e93eb79e7b6a55a048593b700d9eda9abcf67dda5727f459cb311035`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f826560d2f39c08cacc334458e5b6e7853c36fa0791ebec275d3838144f3d2fb`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ed4cbbdc7265029ae9819d0a957c291a9d810b1f93f8ea4c48faa474860ab`  
		Last Modified: Tue, 03 Jan 2023 19:40:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ba4c174984c3b25d98685b0b13ededd6c61a16018f36443107e7154101fd5c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96678069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7361ea93710f22f0ae06f5dc0be6774dae6c01c1e5603c373ed60bb195500`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:16:26 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:16:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:16:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:16:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:16:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:16:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:16:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:16:55 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:16:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b73dcf43d93f122dbe246f346651a1ff55410df3a658b1e3b9778268ab20170`  
		Last Modified: Tue, 03 Jan 2023 19:17:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b1d0a416e6e7b3b920881c65f33e3c2cf75a302e2aa40687f8329a6f2957e`  
		Last Modified: Tue, 03 Jan 2023 19:18:04 GMT  
		Size: 53.6 MB (53553698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabbda09d6f13fb0b720e21821ecbc30cd7af4cc89cd3af099df336d7abe9d6`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508abd8673a0eeed40af0dba638a039220a61b27fc5e3ca481936544a917a92`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0281c35302e28b1ceaa9d66e4955f2d41692ebe8d761fa94e956c2bc1a8864b`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e017aeaa6d977407bcd1c2085147004bd2e875a5b405624b5c00484d90dd9e44`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:833f239931b93786e7bd6e01811c87c825a43168181cc00746e2f34707e8915a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:7afbae8d8bfb674c9ad258dd1d39bdbee10fede3f9db3a477d344fa811f3b21e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b82c54b471632967282629a0e147cd15b6be8fd93e5eb08103a8a2bdcc5c01`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:13:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:13:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:13:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 21 Dec 2022 02:13:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:56 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:57 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:58 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599972720d277bc9a925bb59800bdd64971c76cfa26d972c7f40bdae656c68`  
		Last Modified: Wed, 21 Dec 2022 02:15:03 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f31a37f3c3e5747853e6e73bdc461cef5f603c301340e10c8fd97e24d4a06`  
		Last Modified: Wed, 21 Dec 2022 02:15:02 GMT  
		Size: 6.7 MB (6703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306ba540d4a9b1833b8ecf78343b47b37b6d63368d25bcf12f44b74791f8d91`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 1.3 MB (1259591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2648fe29e85ce421ec043671fbfff24fa8797d7d3f6c90badd7e34e8b7da2ec6`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4508cf1492bc4f9055ebcceb1ed7b37c1c2d09a85ba463e2c10eebd2cc91292`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782771013dfd945694a548b7702f9ae792a678be127f340133efd4dd33af940`  
		Last Modified: Wed, 21 Dec 2022 02:15:04 GMT  
		Size: 44.6 MB (44618646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b4945c0563369181383fffa09bc88fb54526d5401f649cdcc043f3a61adb60`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a56a5e073f87f4cff2031cae6005b1d31bd0eba0124b94e213fcc5bac223ee0`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f19358a943f3429b8b36c217882ab5e2f3e6b38aecb5ee2d11566845b64e01c`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06a2fa0d4f2de92dd11b29f2afc69997e20df51fcb2d8c34f7f039a634d8dd3`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:26cb66a19f1d71b7076f97e3bb8835a4d32b1b87f16b4ec9ff60a68f3b590826
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0dbc528f86846604435f2082aa81b70fa3d8c898333005cf7574c46f76e182`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:12:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:12:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:09 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 21 Dec 2022 13:12:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 13:12:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 13:12:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 13:12:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 13:12:22 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 21 Dec 2022 13:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 13:12:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:22 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 13:12:23 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 13:12:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5a5bc38e201ba09541494349d57ab285af692792c14ed4df572f9c2410a7`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668e1f80fab4a2656ef6f91303e052f69af0c0aa0a43de2bf5eb3dd2c1e5a66`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 6.6 MB (6577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8562d18e321736f052a9519034bfdcc57006ac8b2c4eb6f21a745c03b25baed`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 1.2 MB (1164524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be39e752322b09b2612e6fd2a5f42504043f78fd87e2b8a7d3afc74e63a1e3e`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 294.1 KB (294138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c9c9c1b5e3a9d06a2cd8d457e0dafb1de0ce235c891cf05ce0cb600e8ffe8`  
		Last Modified: Wed, 21 Dec 2022 13:13:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b0b86b7dcb320c4446aa649638d3ffb6a1a125e143f044ba14106c35a4a1f9`  
		Last Modified: Wed, 21 Dec 2022 13:13:20 GMT  
		Size: 41.1 MB (41121728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8b0ead82274fe1079fdb2f0aa9d59e1e96b7a9712620a111e6b03795b7a80`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98ec2b250cb0b94fd041bf0125183792d608d628abef004f939177ceeb8acbe`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d728da2257cff3d7553e7d2d07149b4aba6f04c009f1e58aa66a0267b15050b8`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a361928ae4c9eecc83af87882d377a8b8ceb98b3af508f241d741feaba1f5b7`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:833f239931b93786e7bd6e01811c87c825a43168181cc00746e2f34707e8915a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:7afbae8d8bfb674c9ad258dd1d39bdbee10fede3f9db3a477d344fa811f3b21e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80023623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b82c54b471632967282629a0e147cd15b6be8fd93e5eb08103a8a2bdcc5c01`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:13:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:13:35 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:13:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:13:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 21 Dec 2022 02:13:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:56 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:57 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:58 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44599972720d277bc9a925bb59800bdd64971c76cfa26d972c7f40bdae656c68`  
		Last Modified: Wed, 21 Dec 2022 02:15:03 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2f31a37f3c3e5747853e6e73bdc461cef5f603c301340e10c8fd97e24d4a06`  
		Last Modified: Wed, 21 Dec 2022 02:15:02 GMT  
		Size: 6.7 MB (6703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306ba540d4a9b1833b8ecf78343b47b37b6d63368d25bcf12f44b74791f8d91`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 1.3 MB (1259591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2648fe29e85ce421ec043671fbfff24fa8797d7d3f6c90badd7e34e8b7da2ec6`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4508cf1492bc4f9055ebcceb1ed7b37c1c2d09a85ba463e2c10eebd2cc91292`  
		Last Modified: Wed, 21 Dec 2022 02:15:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782771013dfd945694a548b7702f9ae792a678be127f340133efd4dd33af940`  
		Last Modified: Wed, 21 Dec 2022 02:15:04 GMT  
		Size: 44.6 MB (44618646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b4945c0563369181383fffa09bc88fb54526d5401f649cdcc043f3a61adb60`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a56a5e073f87f4cff2031cae6005b1d31bd0eba0124b94e213fcc5bac223ee0`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f19358a943f3429b8b36c217882ab5e2f3e6b38aecb5ee2d11566845b64e01c`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06a2fa0d4f2de92dd11b29f2afc69997e20df51fcb2d8c34f7f039a634d8dd3`  
		Last Modified: Wed, 21 Dec 2022 02:14:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:26cb66a19f1d71b7076f97e3bb8835a4d32b1b87f16b4ec9ff60a68f3b590826
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0dbc528f86846604435f2082aa81b70fa3d8c898333005cf7574c46f76e182`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:12:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:12:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:12:09 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 21 Dec 2022 13:12:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 13:12:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 13:12:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 13:12:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 13:12:22 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 21 Dec 2022 13:12:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 13:12:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:22 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 13:12:23 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 13:12:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5a5bc38e201ba09541494349d57ab285af692792c14ed4df572f9c2410a7`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668e1f80fab4a2656ef6f91303e052f69af0c0aa0a43de2bf5eb3dd2c1e5a66`  
		Last Modified: Wed, 21 Dec 2022 13:13:19 GMT  
		Size: 6.6 MB (6577037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8562d18e321736f052a9519034bfdcc57006ac8b2c4eb6f21a745c03b25baed`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 1.2 MB (1164524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be39e752322b09b2612e6fd2a5f42504043f78fd87e2b8a7d3afc74e63a1e3e`  
		Last Modified: Wed, 21 Dec 2022 13:13:18 GMT  
		Size: 294.1 KB (294138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3c9c9c1b5e3a9d06a2cd8d457e0dafb1de0ce235c891cf05ce0cb600e8ffe8`  
		Last Modified: Wed, 21 Dec 2022 13:13:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b0b86b7dcb320c4446aa649638d3ffb6a1a125e143f044ba14106c35a4a1f9`  
		Last Modified: Wed, 21 Dec 2022 13:13:20 GMT  
		Size: 41.1 MB (41121728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8b0ead82274fe1079fdb2f0aa9d59e1e96b7a9712620a111e6b03795b7a80`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98ec2b250cb0b94fd041bf0125183792d608d628abef004f939177ceeb8acbe`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d728da2257cff3d7553e7d2d07149b4aba6f04c009f1e58aa66a0267b15050b8`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a361928ae4c9eecc83af87882d377a8b8ceb98b3af508f241d741feaba1f5b7`  
		Last Modified: Wed, 21 Dec 2022 13:13:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:824bfc746f289f37129c7bdf3f463564fcae874a316d1411cebf6c75deba6151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:bfc655d4f5b6efde9f5dec2e7011bac0a0470edc1f279a2f98ddef48bbe39b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc980f785b1dba319918ab023333574d79e2c1cf70f7398afe8c72d2875cedb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:50 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:19:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:20:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:20:04 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:20:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:20:04 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:20:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:20:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:20:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:20:05 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:20:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b099813da643c7590d96161e5bb9b536684f47c8422be18adcd37aca5c4c42`  
		Last Modified: Tue, 03 Jan 2023 19:20:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26176b9dbfbcc037b38616136d9a16e5f82c769f8af4e58fd96bb3b1ead3377d`  
		Last Modified: Tue, 03 Jan 2023 19:20:54 GMT  
		Size: 49.0 MB (49047088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bae8558d4f6d235d034eb64a07a4d1a3dce2423e83b479e41a43aa312a254e`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0676edaa7a90080bff4965d3b4c75dd13fc9b2f8c53d5d1bb83b90a4d1c7cd`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e204a93c755cadc3bca382783a15ea636dae9aad6c0b8bbf7ff8b5b19e471bf5`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaa1000141a480c295f94a6ad5fc4cfe0483db9b06c462f8154f8fc7136f44b`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4792501386e780ae5c0dbba1eb7e92d0ad882c65ea0288413f69f449a3566981
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86059260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbf08d5ac42be080e1db89e57dfe31708bb5cfbd267023d00b44299e4c4ce44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:37 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:39:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:50 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:50 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac497ad0201320dc2c7bc5cf4f269c3cf9f672ed6c62c8ad11530324b4e577`  
		Last Modified: Tue, 03 Jan 2023 19:40:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e450bdd4f787dfa9a4f2865dee2014cf39ffae569707ca6928ea89df9c159`  
		Last Modified: Tue, 03 Jan 2023 19:40:34 GMT  
		Size: 49.1 MB (49066543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad809ae192f7ad7d7c9cb56111a460d8a81ff70b510963b28785e3ef68ddd9c0`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9f087c2208115735c7c52d1e06c139c06f2dd31652271005da86f0fe7bbf20`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46ae8eac5ec18a02302cab9075f5949a83a8b8516d026518024e6d3eb71290c`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a60a530f5b230c6c9d9f4825886f6efe07afd23ecf55e82420019806cf6e4`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca409ac639316a9812cddbf85b2c9cb53e3b4c9d00ee340b32d92f00918bba38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93210733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829c938f4f9a9cb4b88647e937345e05bb40effd3a48cc3f0337ce47900dea6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:17:01 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:17:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:17:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:17:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:17:27 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:17:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:17:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:17:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:17:30 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:17:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67afbca56e929e9b8626615cb2ffb7bdd626abecfc3789b80b5d128ce3c1c396`  
		Last Modified: Tue, 03 Jan 2023 19:18:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7355c658d78fcbfa3918eb2ded924d106ade9bb6c8be34af2ed7ed6784a371a`  
		Last Modified: Tue, 03 Jan 2023 19:18:34 GMT  
		Size: 50.1 MB (50086359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28901da07c2615464a67c5dc28bcf5c8a981ee4bb608daea1befd807ea362fa4`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16521ab4f1e27871302128dcbddf8b42c3a4b6f210a55299e3540900b0a4814`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb144fbb00b18371765ea3fc2d179521f7a041d9d0ae741e407f6e00af5926e`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299ad29752107c59ea3c2de2299a2dd0b6c99d0e33d0e00dcda1c484afd7f7f7`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:824bfc746f289f37129c7bdf3f463564fcae874a316d1411cebf6c75deba6151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:bfc655d4f5b6efde9f5dec2e7011bac0a0470edc1f279a2f98ddef48bbe39b76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87524312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc980f785b1dba319918ab023333574d79e2c1cf70f7398afe8c72d2875cedb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:50 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:19:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:20:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:20:04 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:20:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:20:04 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:20:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:20:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:20:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:20:05 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:20:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b099813da643c7590d96161e5bb9b536684f47c8422be18adcd37aca5c4c42`  
		Last Modified: Tue, 03 Jan 2023 19:20:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26176b9dbfbcc037b38616136d9a16e5f82c769f8af4e58fd96bb3b1ead3377d`  
		Last Modified: Tue, 03 Jan 2023 19:20:54 GMT  
		Size: 49.0 MB (49047088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bae8558d4f6d235d034eb64a07a4d1a3dce2423e83b479e41a43aa312a254e`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0676edaa7a90080bff4965d3b4c75dd13fc9b2f8c53d5d1bb83b90a4d1c7cd`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e204a93c755cadc3bca382783a15ea636dae9aad6c0b8bbf7ff8b5b19e471bf5`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaa1000141a480c295f94a6ad5fc4cfe0483db9b06c462f8154f8fc7136f44b`  
		Last Modified: Tue, 03 Jan 2023 19:20:49 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4792501386e780ae5c0dbba1eb7e92d0ad882c65ea0288413f69f449a3566981
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86059260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbf08d5ac42be080e1db89e57dfe31708bb5cfbd267023d00b44299e4c4ce44`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:37 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:39:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:50 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:50 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac497ad0201320dc2c7bc5cf4f269c3cf9f672ed6c62c8ad11530324b4e577`  
		Last Modified: Tue, 03 Jan 2023 19:40:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e450bdd4f787dfa9a4f2865dee2014cf39ffae569707ca6928ea89df9c159`  
		Last Modified: Tue, 03 Jan 2023 19:40:34 GMT  
		Size: 49.1 MB (49066543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad809ae192f7ad7d7c9cb56111a460d8a81ff70b510963b28785e3ef68ddd9c0`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9f087c2208115735c7c52d1e06c139c06f2dd31652271005da86f0fe7bbf20`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46ae8eac5ec18a02302cab9075f5949a83a8b8516d026518024e6d3eb71290c`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a60a530f5b230c6c9d9f4825886f6efe07afd23ecf55e82420019806cf6e4`  
		Last Modified: Tue, 03 Jan 2023 19:40:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca409ac639316a9812cddbf85b2c9cb53e3b4c9d00ee340b32d92f00918bba38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93210733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829c938f4f9a9cb4b88647e937345e05bb40effd3a48cc3f0337ce47900dea6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:17:01 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Tue, 03 Jan 2023 19:17:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:17:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:17:26 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:17:27 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:17:27 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:17:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:17:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:17:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:17:30 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:17:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67afbca56e929e9b8626615cb2ffb7bdd626abecfc3789b80b5d128ce3c1c396`  
		Last Modified: Tue, 03 Jan 2023 19:18:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7355c658d78fcbfa3918eb2ded924d106ade9bb6c8be34af2ed7ed6784a371a`  
		Last Modified: Tue, 03 Jan 2023 19:18:34 GMT  
		Size: 50.1 MB (50086359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28901da07c2615464a67c5dc28bcf5c8a981ee4bb608daea1befd807ea362fa4`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16521ab4f1e27871302128dcbddf8b42c3a4b6f210a55299e3540900b0a4814`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb144fbb00b18371765ea3fc2d179521f7a041d9d0ae741e407f6e00af5926e`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299ad29752107c59ea3c2de2299a2dd0b6c99d0e33d0e00dcda1c484afd7f7f7`  
		Last Modified: Tue, 03 Jan 2023 19:18:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:09d5e033b3bc4bd43746529188747ea1f3171da37b030ed6d1870f69fcfb4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:ae80ecafc17c7ef87bfdb48d69602430d7b9385dc666c073d19817ad0c456583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e62b803500e1bbd5105b8bfe4c1c372c5c3a2fbc2dd89826bdf602c86047ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:31 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:19:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:19:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:19:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:19:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:19:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:19:48 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:19:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c62d73e217ebcfa696424d7c95f8610cc5ee5da6240e78a2e23fbea2a71761`  
		Last Modified: Tue, 03 Jan 2023 19:20:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f73fb31abf025dc7d4587f0e5d256a8559b6913815dbfcb7988b3aecc367ff`  
		Last Modified: Tue, 03 Jan 2023 19:20:33 GMT  
		Size: 52.7 MB (52693343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f4bc08af527a609227c3cc58148897c6eec4393bdc0bb263c6665af5d3ff7f`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc36a9ae0123374334b0e35f54b03c04e941986d0a68a82743982df25965498a`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce58becc6cea75ef160aeb1a391f98a5844102b03218d3d1f54338eb3ff579`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba1b55341bd92f3d1c3aba399c6f8fd91459e2bb0dcdb17800c7e94e8746000`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:49a21e5dcf9e588fc373b349539ca9e379a350eea42759624c3ad32f8c78e10b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750df03b82c0c75a7aed000f336407f5b66bbabaef8324520027019ec3924a2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:21 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:39:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:35 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:35 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc34651a5eb9515b747b593eea303ee2aefc01bc69aebf056ee34ac9b43d707`  
		Last Modified: Tue, 03 Jan 2023 19:40:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801ea55c77f52bf2940d3992c1e0a9d9483e810751da53de238b4967ebf1432`  
		Last Modified: Tue, 03 Jan 2023 19:40:15 GMT  
		Size: 52.5 MB (52549578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf19cf12b569a6f86a0e2db033a8ff1fa36e551e5d84ef62b4bfa9d56c5a171`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478b465e93eb79e7b6a55a048593b700d9eda9abcf67dda5727f459cb311035`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f826560d2f39c08cacc334458e5b6e7853c36fa0791ebec275d3838144f3d2fb`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ed4cbbdc7265029ae9819d0a957c291a9d810b1f93f8ea4c48faa474860ab`  
		Last Modified: Tue, 03 Jan 2023 19:40:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ba4c174984c3b25d98685b0b13ededd6c61a16018f36443107e7154101fd5c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96678069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7361ea93710f22f0ae06f5dc0be6774dae6c01c1e5603c373ed60bb195500`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:16:26 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:16:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:16:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:16:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:16:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:16:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:16:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:16:55 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:16:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b73dcf43d93f122dbe246f346651a1ff55410df3a658b1e3b9778268ab20170`  
		Last Modified: Tue, 03 Jan 2023 19:17:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b1d0a416e6e7b3b920881c65f33e3c2cf75a302e2aa40687f8329a6f2957e`  
		Last Modified: Tue, 03 Jan 2023 19:18:04 GMT  
		Size: 53.6 MB (53553698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabbda09d6f13fb0b720e21821ecbc30cd7af4cc89cd3af099df336d7abe9d6`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508abd8673a0eeed40af0dba638a039220a61b27fc5e3ca481936544a917a92`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0281c35302e28b1ceaa9d66e4955f2d41692ebe8d761fa94e956c2bc1a8864b`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e017aeaa6d977407bcd1c2085147004bd2e875a5b405624b5c00484d90dd9e44`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.0`

```console
$ docker pull couchdb@sha256:09d5e033b3bc4bd43746529188747ea1f3171da37b030ed6d1870f69fcfb4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:ae80ecafc17c7ef87bfdb48d69602430d7b9385dc666c073d19817ad0c456583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e62b803500e1bbd5105b8bfe4c1c372c5c3a2fbc2dd89826bdf602c86047ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:31 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:19:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:19:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:19:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:19:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:19:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:19:48 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:19:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c62d73e217ebcfa696424d7c95f8610cc5ee5da6240e78a2e23fbea2a71761`  
		Last Modified: Tue, 03 Jan 2023 19:20:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f73fb31abf025dc7d4587f0e5d256a8559b6913815dbfcb7988b3aecc367ff`  
		Last Modified: Tue, 03 Jan 2023 19:20:33 GMT  
		Size: 52.7 MB (52693343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f4bc08af527a609227c3cc58148897c6eec4393bdc0bb263c6665af5d3ff7f`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc36a9ae0123374334b0e35f54b03c04e941986d0a68a82743982df25965498a`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce58becc6cea75ef160aeb1a391f98a5844102b03218d3d1f54338eb3ff579`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba1b55341bd92f3d1c3aba399c6f8fd91459e2bb0dcdb17800c7e94e8746000`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:49a21e5dcf9e588fc373b349539ca9e379a350eea42759624c3ad32f8c78e10b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750df03b82c0c75a7aed000f336407f5b66bbabaef8324520027019ec3924a2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:21 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:39:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:35 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:35 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc34651a5eb9515b747b593eea303ee2aefc01bc69aebf056ee34ac9b43d707`  
		Last Modified: Tue, 03 Jan 2023 19:40:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801ea55c77f52bf2940d3992c1e0a9d9483e810751da53de238b4967ebf1432`  
		Last Modified: Tue, 03 Jan 2023 19:40:15 GMT  
		Size: 52.5 MB (52549578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf19cf12b569a6f86a0e2db033a8ff1fa36e551e5d84ef62b4bfa9d56c5a171`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478b465e93eb79e7b6a55a048593b700d9eda9abcf67dda5727f459cb311035`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f826560d2f39c08cacc334458e5b6e7853c36fa0791ebec275d3838144f3d2fb`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ed4cbbdc7265029ae9819d0a957c291a9d810b1f93f8ea4c48faa474860ab`  
		Last Modified: Tue, 03 Jan 2023 19:40:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ba4c174984c3b25d98685b0b13ededd6c61a16018f36443107e7154101fd5c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96678069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7361ea93710f22f0ae06f5dc0be6774dae6c01c1e5603c373ed60bb195500`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:16:26 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:16:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:16:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:16:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:16:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:16:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:16:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:16:55 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:16:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b73dcf43d93f122dbe246f346651a1ff55410df3a658b1e3b9778268ab20170`  
		Last Modified: Tue, 03 Jan 2023 19:17:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b1d0a416e6e7b3b920881c65f33e3c2cf75a302e2aa40687f8329a6f2957e`  
		Last Modified: Tue, 03 Jan 2023 19:18:04 GMT  
		Size: 53.6 MB (53553698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabbda09d6f13fb0b720e21821ecbc30cd7af4cc89cd3af099df336d7abe9d6`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508abd8673a0eeed40af0dba638a039220a61b27fc5e3ca481936544a917a92`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0281c35302e28b1ceaa9d66e4955f2d41692ebe8d761fa94e956c2bc1a8864b`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e017aeaa6d977407bcd1c2085147004bd2e875a5b405624b5c00484d90dd9e44`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:09d5e033b3bc4bd43746529188747ea1f3171da37b030ed6d1870f69fcfb4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:ae80ecafc17c7ef87bfdb48d69602430d7b9385dc666c073d19817ad0c456583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e62b803500e1bbd5105b8bfe4c1c372c5c3a2fbc2dd89826bdf602c86047ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:31 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:19:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:19:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:19:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:19:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:19:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:19:48 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:19:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c62d73e217ebcfa696424d7c95f8610cc5ee5da6240e78a2e23fbea2a71761`  
		Last Modified: Tue, 03 Jan 2023 19:20:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f73fb31abf025dc7d4587f0e5d256a8559b6913815dbfcb7988b3aecc367ff`  
		Last Modified: Tue, 03 Jan 2023 19:20:33 GMT  
		Size: 52.7 MB (52693343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f4bc08af527a609227c3cc58148897c6eec4393bdc0bb263c6665af5d3ff7f`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc36a9ae0123374334b0e35f54b03c04e941986d0a68a82743982df25965498a`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce58becc6cea75ef160aeb1a391f98a5844102b03218d3d1f54338eb3ff579`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba1b55341bd92f3d1c3aba399c6f8fd91459e2bb0dcdb17800c7e94e8746000`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:49a21e5dcf9e588fc373b349539ca9e379a350eea42759624c3ad32f8c78e10b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750df03b82c0c75a7aed000f336407f5b66bbabaef8324520027019ec3924a2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:21 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:39:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:35 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:35 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc34651a5eb9515b747b593eea303ee2aefc01bc69aebf056ee34ac9b43d707`  
		Last Modified: Tue, 03 Jan 2023 19:40:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801ea55c77f52bf2940d3992c1e0a9d9483e810751da53de238b4967ebf1432`  
		Last Modified: Tue, 03 Jan 2023 19:40:15 GMT  
		Size: 52.5 MB (52549578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf19cf12b569a6f86a0e2db033a8ff1fa36e551e5d84ef62b4bfa9d56c5a171`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478b465e93eb79e7b6a55a048593b700d9eda9abcf67dda5727f459cb311035`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f826560d2f39c08cacc334458e5b6e7853c36fa0791ebec275d3838144f3d2fb`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ed4cbbdc7265029ae9819d0a957c291a9d810b1f93f8ea4c48faa474860ab`  
		Last Modified: Tue, 03 Jan 2023 19:40:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ba4c174984c3b25d98685b0b13ededd6c61a16018f36443107e7154101fd5c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96678069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7361ea93710f22f0ae06f5dc0be6774dae6c01c1e5603c373ed60bb195500`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:16:26 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:16:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:16:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:16:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:16:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:16:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:16:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:16:55 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:16:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b73dcf43d93f122dbe246f346651a1ff55410df3a658b1e3b9778268ab20170`  
		Last Modified: Tue, 03 Jan 2023 19:17:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b1d0a416e6e7b3b920881c65f33e3c2cf75a302e2aa40687f8329a6f2957e`  
		Last Modified: Tue, 03 Jan 2023 19:18:04 GMT  
		Size: 53.6 MB (53553698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabbda09d6f13fb0b720e21821ecbc30cd7af4cc89cd3af099df336d7abe9d6`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508abd8673a0eeed40af0dba638a039220a61b27fc5e3ca481936544a917a92`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0281c35302e28b1ceaa9d66e4955f2d41692ebe8d761fa94e956c2bc1a8864b`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e017aeaa6d977407bcd1c2085147004bd2e875a5b405624b5c00484d90dd9e44`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
