## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1efb5e9441743c2484354b3f669a00ad5c20680ea1a06e57de8f2f597a2151b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:22e9280b268b8caa2f2021625d5010e74073750461e4caeca905647437d6ae6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d192dbd829de795da87d8dc6dece3903a5cade43a89b9fb683cd55ae52454e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:56:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:56:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:56:49 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:56:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:56:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:56:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:56:58 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:56:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:57:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:57:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:57:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:57:12 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:57:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:57:13 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:57:13 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:57:13 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:57:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c029352d6e0f41e74d653fdc71dbc69bda9009f57e85465147674484e06b79`  
		Last Modified: Sat, 28 May 2022 02:58:36 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265551ca8b9ff654a991ba9e5f4911773e11086c4203dd4b64f9a3aeb45fb9c3`  
		Last Modified: Sat, 28 May 2022 02:58:35 GMT  
		Size: 5.2 MB (5224009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbbd597550b26d2892aa168f8fae48a1cf62051742155d314dc37ac84afb82f`  
		Last Modified: Sat, 28 May 2022 02:58:34 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5f425c3db6175ac30bc52edbffcfcfced94c952a75314ef107f0ddcb2ec33`  
		Last Modified: Sat, 28 May 2022 02:58:34 GMT  
		Size: 295.6 KB (295556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2054cad465f7bbb739898605777b27b62cf86ba69ef82ad7093de39eb689819`  
		Last Modified: Sat, 28 May 2022 02:58:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751dacd84d2a058c37c15ff2c2b0988cf53f1ab8eca6df89f8580f4041cbe3fa`  
		Last Modified: Sat, 28 May 2022 02:58:37 GMT  
		Size: 49.0 MB (49039357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45208ba64941d9171ab808f553514f510b77b9d22cd04a73fec3f9cc0ab28ab1`  
		Last Modified: Sat, 28 May 2022 02:58:32 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5035976403e31c0fcbda2b93c61ac1e6fbf3c5cc5f73b235f7b0ac7279aa5f0f`  
		Last Modified: Sat, 28 May 2022 02:58:32 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aa492f461185af266cc4dbb2eac84a6b891594290e4b46608ebe01e5b75a09`  
		Last Modified: Sat, 28 May 2022 02:58:31 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10156bba14d9e1bc41e496ba7a5931e78589b33ab9f1c80b477e9a6cfa254e7a`  
		Last Modified: Sat, 28 May 2022 02:58:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2ae0ffc4c377ee938da9a432c88899028b8daaded48a9b8709aabfbe549c6806
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137eb0cb0d3d6b84966c58c7b4f1e89b60281aac5617846a7f304eec5c713117`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:09:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:09:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:09:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:09:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:09:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:09:59 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 02:10:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:10:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:10:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:10:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:10:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 02:10:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:10:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:10:25 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:10:26 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:10:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019212e3841694cf915d2b4e3a102c24a48dc2d9b1209f9dfa7fa5543a16a11`  
		Last Modified: Sat, 28 May 2022 02:12:30 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521f7861665e16dfd49c07f787e547874576d4059000fc11030b17e0764f34b`  
		Last Modified: Sat, 28 May 2022 02:12:29 GMT  
		Size: 5.0 MB (5003022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff02a9a55d396ff6ab401ff8ac0cb819932c2978d35472b245bb1ec9478c76b`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3658fbe5e3be4dbdd901239e554c80fae1f781fa21942f3b60aa3fe97713d6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 79.2 KB (79191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9437832abdd28bcf179cd3b59f44729f00647bebcbd751d4de97c5c672416b6`  
		Last Modified: Sat, 28 May 2022 02:12:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc4682e178e1470eed9a7df80cf8bc0351edcdd374e553a1a6af823f80919d7`  
		Last Modified: Sat, 28 May 2022 02:12:31 GMT  
		Size: 49.1 MB (49051159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6a360daac77bf8e38418a4c0736676d5261a47c342f274fe3f3a4bb60afef1`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da968eb8433ffe2a36ef9c4d86873b79f94e7f0a1969101ed4fff7b3cbad84b5`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0dedcc40dd9866f51ac6d9620fe64dd7e2e13c25da0403571fd6ba8c4776f8`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098da8954095caac906291f3740c25905e4b6634cfc8ce2f576ee0dd2a36c655`  
		Last Modified: Sat, 28 May 2022 02:12:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:2774d021f2ec7122da9a2d24c153e70c92bbff47c8608c8c99f681447ec30dd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93223893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd6b0d3fe9a02e0fa3d5ef15549a3ec8c4f6909334bfe85b6737c3421c53899`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 May 2022 01:32:29 GMT
ADD file:1e94716789ec21981460f74be38a668bc212bd804c1d41cecf90036a5bccac5a in / 
# Wed, 11 May 2022 01:32:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:53:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 May 2022 03:53:23 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 May 2022 03:54:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:55:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 May 2022 03:55:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 May 2022 03:56:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:56:40 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 11 May 2022 03:56:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 May 2022 03:58:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 May 2022 03:58:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 May 2022 03:58:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 May 2022 03:58:40 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 11 May 2022 03:58:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 May 2022 03:58:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 May 2022 03:58:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 May 2022 03:59:03 GMT
EXPOSE 4369 5984 9100
# Wed, 11 May 2022 03:59:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2533109ed11eefd6415e0370d6d7a3ea879b582b1887c98b819a598ad18fca24`  
		Last Modified: Wed, 11 May 2022 01:43:03 GMT  
		Size: 35.3 MB (35286467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62610198665bf7ba0256e568d5b533eb4e86ea7f0d929be775a0edf50ebe6dc1`  
		Last Modified: Wed, 11 May 2022 03:59:43 GMT  
		Size: 3.4 KB (3420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924366ccb76483e136508811146cb69efe23b89757b2bd2275986b5774755ad0`  
		Last Modified: Wed, 11 May 2022 03:59:42 GMT  
		Size: 6.0 MB (6043834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66a4e119d34d65b8c9643522e2c01733a94e0e8597177f4147500a9378efcd9`  
		Last Modified: Wed, 11 May 2022 03:59:41 GMT  
		Size: 1.5 MB (1509406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dbb3458296e8bed85cdb20ce2cdf724d7d32d1cad906bbfab48f30a0e33c3d`  
		Last Modified: Wed, 11 May 2022 03:59:40 GMT  
		Size: 295.8 KB (295806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c39bf83571d20caef422c066a90fe7046ae845342df092c85e52e4a41b551f`  
		Last Modified: Wed, 11 May 2022 03:59:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f869c09e50b754b4b85542688e149abd8b44f5fd83675ef3302efc7d19841fa`  
		Last Modified: Wed, 11 May 2022 03:59:44 GMT  
		Size: 50.1 MB (50081223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d9045ae6ae651b94c46fbd30c331cbc0ed8744fb4f74457e84bca35db4f535`  
		Last Modified: Wed, 11 May 2022 03:59:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86d7cc3cfc58048e044f5d8a637fceda45c5512800db339db878ee4985d2f43`  
		Last Modified: Wed, 11 May 2022 03:59:36 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181a6fd70115927a806d685a3235d0e0e80b50449a8ee03840b960bf5924173`  
		Last Modified: Wed, 11 May 2022 03:59:36 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6343a3495bb02e302378fb4d0983462a14d9398bdac27e9d30d3f18e4ebe59bc`  
		Last Modified: Wed, 11 May 2022 03:59:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
