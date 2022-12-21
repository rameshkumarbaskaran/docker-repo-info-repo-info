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
$ docker pull couchdb@sha256:7b916bded37c5f0ab055a33b4351ba7dc19cc1360ef9950383db45f65cbe972b
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
$ docker pull couchdb@sha256:21054e97140089d142e745baf6c98e7e2c97c4d4f6f0299565fbd8a56ff9a2e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002af8d850591fbca889f6047a4a4bc29941b54819e0928f66cf32733826ace`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:37:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:37:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:37:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:37:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:41 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 06 Dec 2022 02:37:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:54 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4cd43a0448eef68b0cb6dec18ea5533732271e60ca08d219e19646bce854b`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4122820f112f3d7a65eb655a09df0186564b7c5697d14e007c3090b2b97395`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 6.6 MB (6577031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97185d0a17fb0863c9a24d3fa01871e9302d438e6b693ebbfe27573e4da289eb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da625903a8b5a1b460de4bff4479f9ed3c01c00aa481fc777c3ce0d2615b65cd`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 294.1 KB (294124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042831a023d1382c8e69c939943de0550b36233f2bf7ac90ca1615a932a24c7f`  
		Last Modified: Tue, 06 Dec 2022 02:38:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04475a79e193ed810245962b2685b3a9c0523dd7557711bc40aced83fbf383`  
		Last Modified: Tue, 06 Dec 2022 02:38:44 GMT  
		Size: 39.0 MB (39029837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde3cb9155fe10594f524cef76dc63066528c91555f791e5a2e465d1dbcc2ef`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d0881508f210055e66499a1a8f8f16f5b39403b29f3eead48caac02f53b91`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831fea526803bb427d0f5c8b80a1343318e83c110faee8e84fcfb3cc93874e21`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed8756cb78c425652d5d8e6d6e3873a5149c19d7973d9285d234e2be88a3c7c`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:7b916bded37c5f0ab055a33b4351ba7dc19cc1360ef9950383db45f65cbe972b
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
$ docker pull couchdb@sha256:21054e97140089d142e745baf6c98e7e2c97c4d4f6f0299565fbd8a56ff9a2e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002af8d850591fbca889f6047a4a4bc29941b54819e0928f66cf32733826ace`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:37:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:37:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:37:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:37:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:41 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 06 Dec 2022 02:37:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:54 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4cd43a0448eef68b0cb6dec18ea5533732271e60ca08d219e19646bce854b`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4122820f112f3d7a65eb655a09df0186564b7c5697d14e007c3090b2b97395`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 6.6 MB (6577031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97185d0a17fb0863c9a24d3fa01871e9302d438e6b693ebbfe27573e4da289eb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da625903a8b5a1b460de4bff4479f9ed3c01c00aa481fc777c3ce0d2615b65cd`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 294.1 KB (294124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042831a023d1382c8e69c939943de0550b36233f2bf7ac90ca1615a932a24c7f`  
		Last Modified: Tue, 06 Dec 2022 02:38:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04475a79e193ed810245962b2685b3a9c0523dd7557711bc40aced83fbf383`  
		Last Modified: Tue, 06 Dec 2022 02:38:44 GMT  
		Size: 39.0 MB (39029837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde3cb9155fe10594f524cef76dc63066528c91555f791e5a2e465d1dbcc2ef`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d0881508f210055e66499a1a8f8f16f5b39403b29f3eead48caac02f53b91`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831fea526803bb427d0f5c8b80a1343318e83c110faee8e84fcfb3cc93874e21`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed8756cb78c425652d5d8e6d6e3873a5149c19d7973d9285d234e2be88a3c7c`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:7b916bded37c5f0ab055a33b4351ba7dc19cc1360ef9950383db45f65cbe972b
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
$ docker pull couchdb@sha256:21054e97140089d142e745baf6c98e7e2c97c4d4f6f0299565fbd8a56ff9a2e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72987485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002af8d850591fbca889f6047a4a4bc29941b54819e0928f66cf32733826ace`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:37:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:37:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:37:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:37:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:41 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 06 Dec 2022 02:37:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:54 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:54 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:54 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4cd43a0448eef68b0cb6dec18ea5533732271e60ca08d219e19646bce854b`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4122820f112f3d7a65eb655a09df0186564b7c5697d14e007c3090b2b97395`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 6.6 MB (6577031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97185d0a17fb0863c9a24d3fa01871e9302d438e6b693ebbfe27573e4da289eb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da625903a8b5a1b460de4bff4479f9ed3c01c00aa481fc777c3ce0d2615b65cd`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 294.1 KB (294124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042831a023d1382c8e69c939943de0550b36233f2bf7ac90ca1615a932a24c7f`  
		Last Modified: Tue, 06 Dec 2022 02:38:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd04475a79e193ed810245962b2685b3a9c0523dd7557711bc40aced83fbf383`  
		Last Modified: Tue, 06 Dec 2022 02:38:44 GMT  
		Size: 39.0 MB (39029837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde3cb9155fe10594f524cef76dc63066528c91555f791e5a2e465d1dbcc2ef`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d0881508f210055e66499a1a8f8f16f5b39403b29f3eead48caac02f53b91`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831fea526803bb427d0f5c8b80a1343318e83c110faee8e84fcfb3cc93874e21`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed8756cb78c425652d5d8e6d6e3873a5149c19d7973d9285d234e2be88a3c7c`  
		Last Modified: Tue, 06 Dec 2022 02:38:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:a6cf82556e9c7f773c4af3882dada0fea00d96bf74fad2af574084d727b4bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:69e3140fc00d9c0f885ff03055012fdab90db4cc736f6eb18f65022e77165c22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87523053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114c92a39fea1fd696db0900df018a9dadc256175716aa59f0b3132911152e1a`
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
# Wed, 21 Dec 2022 02:12:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:12:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:13 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:13 GMT
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
	-	`sha256:8e80c43e2d7f82631a66dedad7964af36d287b9557f7099e8fb604aa60c672cf`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace6350a50d54a1dffa1f7d11719feb538c3187d27ca67a653473e8669a39ff8`  
		Last Modified: Wed, 21 Dec 2022 02:14:46 GMT  
		Size: 49.0 MB (49045836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6134064240e9f33fdf7715463f34130b4a3584ea1693020ed2490c430a08bc`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9dc9868d1534b2fd0801484d6ee3137b551d9fb4ab743b92d4cb7f47c8512b`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0039b74aa2aba73e0aee4fb54b111610e37c116aba1cd23efec3684b7a46a1f`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955a82800ff24edd9c8213ff3b2961f5195bbebd8401bdff686085e43506fd32`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01018d93a18c79773dd7bbe769325e38d19ba48c318ccfc2ef441d8ad7b61d5e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86075918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead15cfe5d467c356162256c209623d5d5982246c130d1147be026e05ef98c0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:36:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:36:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:36:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:36:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:48 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 06 Dec 2022 02:36:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:01 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52978b09e2554ffbd028007d31a4a2833c7a8cfe23376f79ad433f0a0f467b04`  
		Last Modified: Tue, 06 Dec 2022 02:38:13 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7363660f0290f9bf69f9ab50f5cffc179c5adc83a5540cf98b171237f816cf9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 5.2 MB (5210587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d423be69a434de8ce0a40b5c1a09c920f45dff093382eb6ee57ee2f000feb3`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 1.4 MB (1436872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968973ab936bac3d8a1a603cd5e2610eab8338066238a66c2fb8bf561a783d0`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 296.2 KB (296157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cb0772563c207436f69961c46ff4164931f8597263861f5552b1ee6d03679a`  
		Last Modified: Tue, 06 Dec 2022 02:38:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e348c01e0f44562a3e0f4ee7ce7ca54478f014bfb250b87048be67cc6d560`  
		Last Modified: Tue, 06 Dec 2022 02:38:14 GMT  
		Size: 49.1 MB (49064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2e45be5bc4db8b1d6450de17e8f4f516dc7495720184856472fd43e9539f7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9796347789b28192a0f4425fc6bda42d858708e7628262250c191e5709a4fd9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13768b759ebbcb8fba738a44e9895e1fa9a72f899587e0c60d8273b6ea59bc7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526c3a368d90235506e6ccd9932bf1345ba9b39fe0e0c12eff0ca7d813c1560`  
		Last Modified: Tue, 06 Dec 2022 02:38:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:7e985503909dfa7d52758f7e2104bfd945efe255ead669cdb50c749019bd1130
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d9a6f3db4265fd81ecabeaaac94814ab2e88bd8f32fd73833186287bbf1a96`
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
# Wed, 21 Dec 2022 02:29:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:29:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:30:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:30:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:30:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:30:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:30:38 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:30:38 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:30:39 GMT
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
	-	`sha256:3ce38e1da98514a16da26df9dff65377c08ef67841cd5df29a45789547baccca`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dc61bc0cabffa78c54e8d8a3236954380cd293e3029c0dde6a2e62524d702`  
		Last Modified: Wed, 21 Dec 2022 02:31:05 GMT  
		Size: 50.1 MB (50085383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d521e7c3fdef6b5e26081973960a4a2df93634f814d41f109cede323030ce0`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77630b86e19275000f30678170ed9652da70b9cbdf86da1fe63076e44f3268d3`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb358847e818687c9e3116214e08ca12ecd7fcb754b38d43889ee89e9e2eab`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c698775e4990fc4be7e8060c25335e8101ae60e8555c08f58c89a999b299ec7`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:0a3016bd124ea9214e518530944284fe32f1c4c7957532970b8a7e92cb1994e2
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
$ docker pull couchdb@sha256:fb48a2f011367f82db30c64f2967697cb2123170ffe5ecdfc6e3a581f6639bc1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fcea3fe9997872b17a80bed0364aace4f94466d245e215f177d59d9195c67a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:37:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:37:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:37:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:37:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 06 Dec 2022 02:37:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:36 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:37 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:37 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4cd43a0448eef68b0cb6dec18ea5533732271e60ca08d219e19646bce854b`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4122820f112f3d7a65eb655a09df0186564b7c5697d14e007c3090b2b97395`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 6.6 MB (6577031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97185d0a17fb0863c9a24d3fa01871e9302d438e6b693ebbfe27573e4da289eb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da625903a8b5a1b460de4bff4479f9ed3c01c00aa481fc777c3ce0d2615b65cd`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 294.1 KB (294124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f14b8a596acc8afa56faf1c000b1b69f96dc7b581dcbc6945ec5271099075bb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ac85bb15c25ca628b6cbd4ae5cdd71328bb8830f8baacee9b4307aa89c94aa`  
		Last Modified: Tue, 06 Dec 2022 02:38:32 GMT  
		Size: 41.1 MB (41121905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11b1eabd26ea65c93d245682f9cab7fad33165dd8dd33ffa8a0f3c5c28791c`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88ca8539aeb997b6b9fecee4bc2656004e5d50d9d39c33797af30887f5246d1`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2e34cb08123dc03eda52bac747d2ffbc7d5c483cf93573611a7e8098695735`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15d51e3805166230beaecf447465f391a4bf66940b8f4bb46cda6ee7e3c217f`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:0a3016bd124ea9214e518530944284fe32f1c4c7957532970b8a7e92cb1994e2
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
$ docker pull couchdb@sha256:fb48a2f011367f82db30c64f2967697cb2123170ffe5ecdfc6e3a581f6639bc1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fcea3fe9997872b17a80bed0364aace4f94466d245e215f177d59d9195c67a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:37:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:37:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:37:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:37:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:37:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:37:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 06 Dec 2022 02:37:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:36 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:37 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:37 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa4cd43a0448eef68b0cb6dec18ea5533732271e60ca08d219e19646bce854b`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4122820f112f3d7a65eb655a09df0186564b7c5697d14e007c3090b2b97395`  
		Last Modified: Tue, 06 Dec 2022 02:38:31 GMT  
		Size: 6.6 MB (6577031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97185d0a17fb0863c9a24d3fa01871e9302d438e6b693ebbfe27573e4da289eb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 1.2 MB (1164503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da625903a8b5a1b460de4bff4479f9ed3c01c00aa481fc777c3ce0d2615b65cd`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 294.1 KB (294124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f14b8a596acc8afa56faf1c000b1b69f96dc7b581dcbc6945ec5271099075bb`  
		Last Modified: Tue, 06 Dec 2022 02:38:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ac85bb15c25ca628b6cbd4ae5cdd71328bb8830f8baacee9b4307aa89c94aa`  
		Last Modified: Tue, 06 Dec 2022 02:38:32 GMT  
		Size: 41.1 MB (41121905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11b1eabd26ea65c93d245682f9cab7fad33165dd8dd33ffa8a0f3c5c28791c`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88ca8539aeb997b6b9fecee4bc2656004e5d50d9d39c33797af30887f5246d1`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2e34cb08123dc03eda52bac747d2ffbc7d5c483cf93573611a7e8098695735`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15d51e3805166230beaecf447465f391a4bf66940b8f4bb46cda6ee7e3c217f`  
		Last Modified: Tue, 06 Dec 2022 02:38:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:a6cf82556e9c7f773c4af3882dada0fea00d96bf74fad2af574084d727b4bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:69e3140fc00d9c0f885ff03055012fdab90db4cc736f6eb18f65022e77165c22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87523053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114c92a39fea1fd696db0900df018a9dadc256175716aa59f0b3132911152e1a`
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
# Wed, 21 Dec 2022 02:12:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:12:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:13 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:13 GMT
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
	-	`sha256:8e80c43e2d7f82631a66dedad7964af36d287b9557f7099e8fb604aa60c672cf`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace6350a50d54a1dffa1f7d11719feb538c3187d27ca67a653473e8669a39ff8`  
		Last Modified: Wed, 21 Dec 2022 02:14:46 GMT  
		Size: 49.0 MB (49045836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6134064240e9f33fdf7715463f34130b4a3584ea1693020ed2490c430a08bc`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9dc9868d1534b2fd0801484d6ee3137b551d9fb4ab743b92d4cb7f47c8512b`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0039b74aa2aba73e0aee4fb54b111610e37c116aba1cd23efec3684b7a46a1f`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955a82800ff24edd9c8213ff3b2961f5195bbebd8401bdff686085e43506fd32`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01018d93a18c79773dd7bbe769325e38d19ba48c318ccfc2ef441d8ad7b61d5e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86075918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead15cfe5d467c356162256c209623d5d5982246c130d1147be026e05ef98c0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:36:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:36:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:36:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:36:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:48 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 06 Dec 2022 02:36:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:01 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52978b09e2554ffbd028007d31a4a2833c7a8cfe23376f79ad433f0a0f467b04`  
		Last Modified: Tue, 06 Dec 2022 02:38:13 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7363660f0290f9bf69f9ab50f5cffc179c5adc83a5540cf98b171237f816cf9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 5.2 MB (5210587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d423be69a434de8ce0a40b5c1a09c920f45dff093382eb6ee57ee2f000feb3`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 1.4 MB (1436872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968973ab936bac3d8a1a603cd5e2610eab8338066238a66c2fb8bf561a783d0`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 296.2 KB (296157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cb0772563c207436f69961c46ff4164931f8597263861f5552b1ee6d03679a`  
		Last Modified: Tue, 06 Dec 2022 02:38:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e348c01e0f44562a3e0f4ee7ce7ca54478f014bfb250b87048be67cc6d560`  
		Last Modified: Tue, 06 Dec 2022 02:38:14 GMT  
		Size: 49.1 MB (49064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2e45be5bc4db8b1d6450de17e8f4f516dc7495720184856472fd43e9539f7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9796347789b28192a0f4425fc6bda42d858708e7628262250c191e5709a4fd9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13768b759ebbcb8fba738a44e9895e1fa9a72f899587e0c60d8273b6ea59bc7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526c3a368d90235506e6ccd9932bf1345ba9b39fe0e0c12eff0ca7d813c1560`  
		Last Modified: Tue, 06 Dec 2022 02:38:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:7e985503909dfa7d52758f7e2104bfd945efe255ead669cdb50c749019bd1130
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d9a6f3db4265fd81ecabeaaac94814ab2e88bd8f32fd73833186287bbf1a96`
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
# Wed, 21 Dec 2022 02:29:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:29:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:30:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:30:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:30:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:30:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:30:38 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:30:38 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:30:39 GMT
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
	-	`sha256:3ce38e1da98514a16da26df9dff65377c08ef67841cd5df29a45789547baccca`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dc61bc0cabffa78c54e8d8a3236954380cd293e3029c0dde6a2e62524d702`  
		Last Modified: Wed, 21 Dec 2022 02:31:05 GMT  
		Size: 50.1 MB (50085383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d521e7c3fdef6b5e26081973960a4a2df93634f814d41f109cede323030ce0`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77630b86e19275000f30678170ed9652da70b9cbdf86da1fe63076e44f3268d3`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb358847e818687c9e3116214e08ca12ecd7fcb754b38d43889ee89e9e2eab`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c698775e4990fc4be7e8060c25335e8101ae60e8555c08f58c89a999b299ec7`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:a6cf82556e9c7f773c4af3882dada0fea00d96bf74fad2af574084d727b4bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:69e3140fc00d9c0f885ff03055012fdab90db4cc736f6eb18f65022e77165c22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87523053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114c92a39fea1fd696db0900df018a9dadc256175716aa59f0b3132911152e1a`
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
# Wed, 21 Dec 2022 02:12:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:12:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:13 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:13 GMT
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
	-	`sha256:8e80c43e2d7f82631a66dedad7964af36d287b9557f7099e8fb604aa60c672cf`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace6350a50d54a1dffa1f7d11719feb538c3187d27ca67a653473e8669a39ff8`  
		Last Modified: Wed, 21 Dec 2022 02:14:46 GMT  
		Size: 49.0 MB (49045836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6134064240e9f33fdf7715463f34130b4a3584ea1693020ed2490c430a08bc`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9dc9868d1534b2fd0801484d6ee3137b551d9fb4ab743b92d4cb7f47c8512b`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0039b74aa2aba73e0aee4fb54b111610e37c116aba1cd23efec3684b7a46a1f`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955a82800ff24edd9c8213ff3b2961f5195bbebd8401bdff686085e43506fd32`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01018d93a18c79773dd7bbe769325e38d19ba48c318ccfc2ef441d8ad7b61d5e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86075918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead15cfe5d467c356162256c209623d5d5982246c130d1147be026e05ef98c0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:36:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:36:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:36:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:36:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:48 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 06 Dec 2022 02:36:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:01 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52978b09e2554ffbd028007d31a4a2833c7a8cfe23376f79ad433f0a0f467b04`  
		Last Modified: Tue, 06 Dec 2022 02:38:13 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7363660f0290f9bf69f9ab50f5cffc179c5adc83a5540cf98b171237f816cf9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 5.2 MB (5210587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d423be69a434de8ce0a40b5c1a09c920f45dff093382eb6ee57ee2f000feb3`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 1.4 MB (1436872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968973ab936bac3d8a1a603cd5e2610eab8338066238a66c2fb8bf561a783d0`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 296.2 KB (296157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cb0772563c207436f69961c46ff4164931f8597263861f5552b1ee6d03679a`  
		Last Modified: Tue, 06 Dec 2022 02:38:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e348c01e0f44562a3e0f4ee7ce7ca54478f014bfb250b87048be67cc6d560`  
		Last Modified: Tue, 06 Dec 2022 02:38:14 GMT  
		Size: 49.1 MB (49064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2e45be5bc4db8b1d6450de17e8f4f516dc7495720184856472fd43e9539f7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9796347789b28192a0f4425fc6bda42d858708e7628262250c191e5709a4fd9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13768b759ebbcb8fba738a44e9895e1fa9a72f899587e0c60d8273b6ea59bc7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526c3a368d90235506e6ccd9932bf1345ba9b39fe0e0c12eff0ca7d813c1560`  
		Last Modified: Tue, 06 Dec 2022 02:38:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:7e985503909dfa7d52758f7e2104bfd945efe255ead669cdb50c749019bd1130
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d9a6f3db4265fd81ecabeaaac94814ab2e88bd8f32fd73833186287bbf1a96`
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
# Wed, 21 Dec 2022 02:29:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:29:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:30:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:30:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:30:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:30:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:30:38 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:30:38 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:30:39 GMT
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
	-	`sha256:3ce38e1da98514a16da26df9dff65377c08ef67841cd5df29a45789547baccca`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dc61bc0cabffa78c54e8d8a3236954380cd293e3029c0dde6a2e62524d702`  
		Last Modified: Wed, 21 Dec 2022 02:31:05 GMT  
		Size: 50.1 MB (50085383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d521e7c3fdef6b5e26081973960a4a2df93634f814d41f109cede323030ce0`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77630b86e19275000f30678170ed9652da70b9cbdf86da1fe63076e44f3268d3`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb358847e818687c9e3116214e08ca12ecd7fcb754b38d43889ee89e9e2eab`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c698775e4990fc4be7e8060c25335e8101ae60e8555c08f58c89a999b299ec7`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:a6cf82556e9c7f773c4af3882dada0fea00d96bf74fad2af574084d727b4bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:69e3140fc00d9c0f885ff03055012fdab90db4cc736f6eb18f65022e77165c22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87523053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114c92a39fea1fd696db0900df018a9dadc256175716aa59f0b3132911152e1a`
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
# Wed, 21 Dec 2022 02:12:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:12:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:13:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:13:12 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:13:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:13:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:13:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:13:13 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:13:13 GMT
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
	-	`sha256:8e80c43e2d7f82631a66dedad7964af36d287b9557f7099e8fb604aa60c672cf`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace6350a50d54a1dffa1f7d11719feb538c3187d27ca67a653473e8669a39ff8`  
		Last Modified: Wed, 21 Dec 2022 02:14:46 GMT  
		Size: 49.0 MB (49045836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6134064240e9f33fdf7715463f34130b4a3584ea1693020ed2490c430a08bc`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9dc9868d1534b2fd0801484d6ee3137b551d9fb4ab743b92d4cb7f47c8512b`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0039b74aa2aba73e0aee4fb54b111610e37c116aba1cd23efec3684b7a46a1f`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955a82800ff24edd9c8213ff3b2961f5195bbebd8401bdff686085e43506fd32`  
		Last Modified: Wed, 21 Dec 2022 02:14:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:01018d93a18c79773dd7bbe769325e38d19ba48c318ccfc2ef441d8ad7b61d5e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86075918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead15cfe5d467c356162256c209623d5d5982246c130d1147be026e05ef98c0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:36:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 Dec 2022 02:36:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 06 Dec 2022 02:36:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 06 Dec 2022 02:36:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 Dec 2022 02:36:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:36:48 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 06 Dec 2022 02:36:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 06 Dec 2022 02:37:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 06 Dec 2022 02:37:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 06 Dec 2022 02:37:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 06 Dec 2022 02:37:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 02:37:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 Dec 2022 02:37:01 GMT
EXPOSE 4369 5984 9100
# Tue, 06 Dec 2022 02:37:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52978b09e2554ffbd028007d31a4a2833c7a8cfe23376f79ad433f0a0f467b04`  
		Last Modified: Tue, 06 Dec 2022 02:38:13 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7363660f0290f9bf69f9ab50f5cffc179c5adc83a5540cf98b171237f816cf9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 5.2 MB (5210587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d423be69a434de8ce0a40b5c1a09c920f45dff093382eb6ee57ee2f000feb3`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 1.4 MB (1436872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968973ab936bac3d8a1a603cd5e2610eab8338066238a66c2fb8bf561a783d0`  
		Last Modified: Tue, 06 Dec 2022 02:38:12 GMT  
		Size: 296.2 KB (296157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cb0772563c207436f69961c46ff4164931f8597263861f5552b1ee6d03679a`  
		Last Modified: Tue, 06 Dec 2022 02:38:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e348c01e0f44562a3e0f4ee7ce7ca54478f014bfb250b87048be67cc6d560`  
		Last Modified: Tue, 06 Dec 2022 02:38:14 GMT  
		Size: 49.1 MB (49064819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2e45be5bc4db8b1d6450de17e8f4f516dc7495720184856472fd43e9539f7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9796347789b28192a0f4425fc6bda42d858708e7628262250c191e5709a4fd9c`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13768b759ebbcb8fba738a44e9895e1fa9a72f899587e0c60d8273b6ea59bc7`  
		Last Modified: Tue, 06 Dec 2022 02:38:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526c3a368d90235506e6ccd9932bf1345ba9b39fe0e0c12eff0ca7d813c1560`  
		Last Modified: Tue, 06 Dec 2022 02:38:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:7e985503909dfa7d52758f7e2104bfd945efe255ead669cdb50c749019bd1130
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d9a6f3db4265fd81ecabeaaac94814ab2e88bd8f32fd73833186287bbf1a96`
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
# Wed, 21 Dec 2022 02:29:57 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 21 Dec 2022 02:29:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 21 Dec 2022 02:30:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 21 Dec 2022 02:30:36 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 21 Dec 2022 02:30:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 21 Dec 2022 02:30:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 21 Dec 2022 02:30:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:30:38 GMT
VOLUME [/opt/couchdb/data]
# Wed, 21 Dec 2022 02:30:38 GMT
EXPOSE 4369 5984 9100
# Wed, 21 Dec 2022 02:30:39 GMT
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
	-	`sha256:3ce38e1da98514a16da26df9dff65377c08ef67841cd5df29a45789547baccca`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dc61bc0cabffa78c54e8d8a3236954380cd293e3029c0dde6a2e62524d702`  
		Last Modified: Wed, 21 Dec 2022 02:31:05 GMT  
		Size: 50.1 MB (50085383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d521e7c3fdef6b5e26081973960a4a2df93634f814d41f109cede323030ce0`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77630b86e19275000f30678170ed9652da70b9cbdf86da1fe63076e44f3268d3`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb358847e818687c9e3116214e08ca12ecd7fcb754b38d43889ee89e9e2eab`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c698775e4990fc4be7e8060c25335e8101ae60e8555c08f58c89a999b299ec7`  
		Last Modified: Wed, 21 Dec 2022 02:30:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
