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
$ docker pull couchdb@sha256:ef018cbf1e098b129ae3a90c915539150d530ed747da7d7a202830b3d9a31217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34a4bf495b56c46b4210c78eb838887fd7d20f3a7f115cf81698088c8d6d653f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77c6f7853bb1988f5fe9c2f6343bcd05e35338b549b8b25fccd414c9909bca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:31:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:31:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:31:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:31:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:32:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:32:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:32:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:32:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:32:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:32:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:32:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:32:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:32:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:32:43 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:32:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e0a57c46a5315cb1d11c57ac722817413fe3cadbacf223f1aa8ce114406ec`  
		Last Modified: Thu, 23 Jun 2022 01:33:38 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e8d5de3561578c1db47d789836c0e3ba5786c95deeb25ec39e329b47ac2b0`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 6.6 MB (6556727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594af3cc54a385abcc779ac03c1aab7baca2eeea5a8769d851d3e2362a0d642`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 951.2 KB (951172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a83b57a833b432d62052af739a8cc3190501e66da89c3886d09a3c012961c`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 79.9 KB (79930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460230e538a7d8339ed697166f4b15e3fd69efd51a52d10b83485d17494afcaf`  
		Last Modified: Thu, 23 Jun 2022 01:33:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09def0d121fd830c245719503b3410ca43b84dff377bf4f3ece13c3547d9510`  
		Last Modified: Thu, 23 Jun 2022 01:33:56 GMT  
		Size: 39.0 MB (39023599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7fbf6ab60f242f0c3cc014063e99ec91bdebaa3b461239bfb63f22bf929975`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7b968ece16b34738fb93380b0775be8bf4ed18be1742bb26e7ef67165127b`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dea4f7b426409fb86041d3a451cddac4fb5beb7a069c088d50838b0a2f5e8dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e4c629ec59732ddcc5ef2e818fa59525fc9671a90c2c39c9d1389f3f0d9d6`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ef018cbf1e098b129ae3a90c915539150d530ed747da7d7a202830b3d9a31217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34a4bf495b56c46b4210c78eb838887fd7d20f3a7f115cf81698088c8d6d653f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77c6f7853bb1988f5fe9c2f6343bcd05e35338b549b8b25fccd414c9909bca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:31:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:31:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:31:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:31:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:32:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:32:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:32:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:32:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:32:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:32:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:32:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:32:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:32:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:32:43 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:32:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e0a57c46a5315cb1d11c57ac722817413fe3cadbacf223f1aa8ce114406ec`  
		Last Modified: Thu, 23 Jun 2022 01:33:38 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e8d5de3561578c1db47d789836c0e3ba5786c95deeb25ec39e329b47ac2b0`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 6.6 MB (6556727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594af3cc54a385abcc779ac03c1aab7baca2eeea5a8769d851d3e2362a0d642`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 951.2 KB (951172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a83b57a833b432d62052af739a8cc3190501e66da89c3886d09a3c012961c`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 79.9 KB (79930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460230e538a7d8339ed697166f4b15e3fd69efd51a52d10b83485d17494afcaf`  
		Last Modified: Thu, 23 Jun 2022 01:33:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09def0d121fd830c245719503b3410ca43b84dff377bf4f3ece13c3547d9510`  
		Last Modified: Thu, 23 Jun 2022 01:33:56 GMT  
		Size: 39.0 MB (39023599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7fbf6ab60f242f0c3cc014063e99ec91bdebaa3b461239bfb63f22bf929975`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7b968ece16b34738fb93380b0775be8bf4ed18be1742bb26e7ef67165127b`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dea4f7b426409fb86041d3a451cddac4fb5beb7a069c088d50838b0a2f5e8dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e4c629ec59732ddcc5ef2e818fa59525fc9671a90c2c39c9d1389f3f0d9d6`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ef018cbf1e098b129ae3a90c915539150d530ed747da7d7a202830b3d9a31217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:89ec990c38a98c072461b37efc3fdd3e6af059d26bab0bc14ca0c03a75eb9a29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7730f520a9e0d91cc76a3b1213178dc8c039c5f847aba061618f531f13e9b598`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:07:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:53 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:53 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f02b79ba8f20a74d6043fa2f3eceab9cb4311187e228e822cedc254f3c158b7`  
		Last Modified: Thu, 23 Jun 2022 01:08:50 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44dcfa4a8386763976c2fa29204037a9051563713501777f0b060e85e38bb1`  
		Last Modified: Thu, 23 Jun 2022 01:08:53 GMT  
		Size: 49.1 MB (49127735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb73a35366ebb8c0aa3c79869555b534dabcb30bc834f9457de16c3681034e4f`  
		Last Modified: Thu, 23 Jun 2022 01:08:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c0c6f989ed30ae055bd89195fdc6a7330b0ec131d12fd1b3b277e8319d4f10`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f7fc0dd5f8432ce4345dadaeb1a417adf17681a5d1c27cbd407149d546d862`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ac49a371125c8caea5047c3e01280a947350ace78997afcd09bf91c05ab518`  
		Last Modified: Thu, 23 Jun 2022 01:08:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:34a4bf495b56c46b4210c78eb838887fd7d20f3a7f115cf81698088c8d6d653f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77c6f7853bb1988f5fe9c2f6343bcd05e35338b549b8b25fccd414c9909bca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:31:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:31:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:31:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:31:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:32:19 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 23 Jun 2022 01:32:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:32:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:32:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:32:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:32:40 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 23 Jun 2022 01:32:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:32:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:32:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:32:43 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:32:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e0a57c46a5315cb1d11c57ac722817413fe3cadbacf223f1aa8ce114406ec`  
		Last Modified: Thu, 23 Jun 2022 01:33:38 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e8d5de3561578c1db47d789836c0e3ba5786c95deeb25ec39e329b47ac2b0`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 6.6 MB (6556727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594af3cc54a385abcc779ac03c1aab7baca2eeea5a8769d851d3e2362a0d642`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 951.2 KB (951172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a83b57a833b432d62052af739a8cc3190501e66da89c3886d09a3c012961c`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 79.9 KB (79930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460230e538a7d8339ed697166f4b15e3fd69efd51a52d10b83485d17494afcaf`  
		Last Modified: Thu, 23 Jun 2022 01:33:54 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09def0d121fd830c245719503b3410ca43b84dff377bf4f3ece13c3547d9510`  
		Last Modified: Thu, 23 Jun 2022 01:33:56 GMT  
		Size: 39.0 MB (39023599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7fbf6ab60f242f0c3cc014063e99ec91bdebaa3b461239bfb63f22bf929975`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d7b968ece16b34738fb93380b0775be8bf4ed18be1742bb26e7ef67165127b`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dea4f7b426409fb86041d3a451cddac4fb5beb7a069c088d50838b0a2f5e8dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e4c629ec59732ddcc5ef2e818fa59525fc9671a90c2c39c9d1389f3f0d9d6`  
		Last Modified: Thu, 23 Jun 2022 01:33:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:e240d825d255af751f5f55af8d9671beabdf2236c0a3b4e2639b3e182d994c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:963c6bdce2865332088af6db49b38fa74bf976524a961428a7f9722bc9eef2d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a3f9bc4086335eba387e8861b885c1c1dc01693341c683f8bd6a301930b7c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:30:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:46 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:31:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:31:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:31:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:31:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:31:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:31:10 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:31:11 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:31:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e4beb83730624f8bcf51b1774b4100e1e412f82bf7581c2102c32d21babc2`  
		Last Modified: Thu, 23 Jun 2022 01:33:14 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e72f96be5467954693838bc974a9b240de99dc781c890b8854a9b72ffe7810`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 5.0 MB (5003043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fe9d6128b137e4021863af326262d53382dc923b8253440d8c35dca9346dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8033bc1cbfbb70b4bd70c8b6b05f4b51d787550ec906faaf7058fc28d2e0d541`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 79.2 KB (79250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a155e5dda342d8db092d0838f17a385cac7c9e6b675c52aa622eab8691e9d436`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f539b2f3aceca17ca461e400c845f07355901db19b62abd957e9f73637648`  
		Last Modified: Thu, 23 Jun 2022 01:33:15 GMT  
		Size: 49.1 MB (49051089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8329e9015b73d2e5486a08a39b87b23aed1ec9c1ab1e696789f89e27827f751`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30a74bb6d8fc4574cf72fe64367d6ad19cd0054333a0910265d35011060b0c1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e3d24862203426b8ad799b0ccf323a227be762d42c8592d9de3cf67c47377`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b8990f4d7ba62fff96860921dae1c48d5826104ead7d5d1d6574470b914a1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fe710ef109d9aab74fc18e8b33b7d0a5b48142ab2faa245f21bac4176ba86580
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93224180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61ad9d7a30afc783707e6c406a035e3db84a4606f0dc12ff2843c46620213fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:32 GMT
ADD file:e18c13649ea1f145047652c8e171c4824f9b6b0dbc92127a914c7fca910acf96 in / 
# Thu, 23 Jun 2022 02:02:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 05:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 05:01:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 05:02:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:02:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 05:02:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 05:03:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:03:36 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 05:03:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 05:04:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 05:04:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 05:04:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 05:04:26 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 05:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 05:04:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 05:04:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 05:04:42 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 05:04:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7716f0df7ba06b6f1937cd664805984e25e386a4165f2c6acc65356686e35221`  
		Last Modified: Thu, 23 Jun 2022 02:15:20 GMT  
		Size: 35.3 MB (35286823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a41d0487993148ae74198a437440d8cc8cafc08287418a6708059b83ef16ac9`  
		Last Modified: Thu, 23 Jun 2022 05:05:14 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36306692d69624a869e064a49d97a053aef815d059a8f200a8a234d328a6ab43`  
		Last Modified: Thu, 23 Jun 2022 05:05:13 GMT  
		Size: 6.0 MB (6044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0185210640fad2504565eec769730020fd99045c6c25bb372f53801287c3cf`  
		Last Modified: Thu, 23 Jun 2022 05:05:12 GMT  
		Size: 1.5 MB (1509406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604024ac9e627dac3af9aad8ebc6109c296f48a3301f0bf2c8aa7585226a42eb`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 295.8 KB (295782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d6b476ceb2d52c21a4f992dbf5cb865f96e83e014f0e61a21052bdbe9ea60c`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a1150e7fced5bca6693e712841c25bdc1142c1180f82ea19648a46d3661d1`  
		Last Modified: Thu, 23 Jun 2022 05:05:16 GMT  
		Size: 50.1 MB (50081001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462a4447c4a9d01b8dbf6b0c4a5ad3d6d3f6aab08dde611b9ad151b4a6cefa7`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a08687fa852c5f675f0637135f7bc517159c8169bf70f35f9873c164e2fbb1`  
		Last Modified: Thu, 23 Jun 2022 05:05:09 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b31d9afdc3af6402209eb89a5bc5ff9c6504ba61ac250738c776934816bdf`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d60da9bd78a2c81dea2d9fb14963cf46a9efd95218c42861a21f2e2050b16`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:c6d02de5c8bb76c07e0bb731aa0aaa13f0f0ab59256efa7fea24117b48053c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:413d8286b4c41b50d81c70155616baca746bf61966818efc4d57b08ad6309a77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da75b5fe58ef3791d83c5a02f6ac1d085c7a6abf21b91b86e331fcbd3119f76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:31:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:31:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:31:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:31:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:39 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:31:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:32:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:32:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:32:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:32:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:32:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:32:04 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:32:05 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:32:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e0a57c46a5315cb1d11c57ac722817413fe3cadbacf223f1aa8ce114406ec`  
		Last Modified: Thu, 23 Jun 2022 01:33:38 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e8d5de3561578c1db47d789836c0e3ba5786c95deeb25ec39e329b47ac2b0`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 6.6 MB (6556727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594af3cc54a385abcc779ac03c1aab7baca2eeea5a8769d851d3e2362a0d642`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 951.2 KB (951172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a83b57a833b432d62052af739a8cc3190501e66da89c3886d09a3c012961c`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 79.9 KB (79930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7966fecbe0ebd11b89d5cea9b4f7f1d394a2dcaa07a6363f22bc7ebec468281`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b995c19d5653ff40f1fe9cc6462cae0bd6df29ce7ad43a7a33e46d1f88c89a`  
		Last Modified: Thu, 23 Jun 2022 01:33:39 GMT  
		Size: 41.1 MB (41112223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980dfe7cf66786f56b8a563b0d4a1fca33eee307a876469dccae41c1f91ae110`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa38928f6353d902381e2469961069e70fd17b955b772beda964ed1a0b693095`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a454064a1a2609f1b69dacab13edde797609e268dfcc91a6f622272057a151`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd69eb321493607da9d6a794192024da185cbdb52184011788e49ee1675b006`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:c6d02de5c8bb76c07e0bb731aa0aaa13f0f0ab59256efa7fea24117b48053c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:f5e1d26a55dca17d784c1f2b9f669b81abac7ef6338e7eea1521a44df2fa2f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833bfc7acc1bf6fb4701f88ab1edd3d6175e9fae0d5e5c87a0f63be9ea39785`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:07:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:07:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:07:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:07:10 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:07:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:07:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:07:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:07:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:07:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:07:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:07:25 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:07:26 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:07:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69caca0907d0d3335526c4d01aa9f4018f6eae9e239fdb1afcfdc62ed9e5daad`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c152806aa1f11ef047a8e625f1ac3b14e27b6910e7c53d9b251e354dd5f1f4`  
		Last Modified: Thu, 23 Jun 2022 01:08:36 GMT  
		Size: 6.7 MB (6698639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097208c33cdf0f816d46acc41fd59d699629045ca85f0320512c41edcc1233e5`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 1.3 MB (1258355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72a65c6c95aed0b420a0e8b5633733436228ebdb423b9cb5ca98829aba0d1da`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 293.1 KB (293057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab9ba22220b6188d53d6fc816b63e62996f696e875a21ba2861e839ec5a6861`  
		Last Modified: Thu, 23 Jun 2022 01:08:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdda34c0972965fdcda16044c6018c724818515b86c4c58acf9c1b051b20858`  
		Last Modified: Thu, 23 Jun 2022 01:08:37 GMT  
		Size: 44.6 MB (44612451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a85c10523399f67c5c6eefeda3cdd2db8d6ba9dae6f6ef9733ed4d1754e9553`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea223f715c88770fbcef6e32b8cb5f10171bdbe81362aec840af62e8fe3b03d`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35c25494b5c7fa8293dd4ada6b829e1802920894aaad64c7feb17e29b0057e0`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9f94e6c2271887064031d91d640c36b409089a60fa5db5f7ef0734c643e48`  
		Last Modified: Thu, 23 Jun 2022 01:08:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:413d8286b4c41b50d81c70155616baca746bf61966818efc4d57b08ad6309a77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da75b5fe58ef3791d83c5a02f6ac1d085c7a6abf21b91b86e331fcbd3119f76`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:08 GMT
ADD file:e491c8ce913289e0c673bd14014c5506cca7b78575aa5c8303ec856525209505 in / 
# Thu, 23 Jun 2022 00:41:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:31:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:31:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:31:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:31:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:31:39 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 23 Jun 2022 01:31:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:32:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:32:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:32:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 23 Jun 2022 01:32:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:32:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:32:04 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:32:05 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:32:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d8b55b2b6839f70c2ed0662b18f4d9724108500136dfd03e999a5f91c815984b`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 25.9 MB (25914029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9e0a57c46a5315cb1d11c57ac722817413fe3cadbacf223f1aa8ce114406ec`  
		Last Modified: Thu, 23 Jun 2022 01:33:38 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50e8d5de3561578c1db47d789836c0e3ba5786c95deeb25ec39e329b47ac2b0`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 6.6 MB (6556727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594af3cc54a385abcc779ac03c1aab7baca2eeea5a8769d851d3e2362a0d642`  
		Last Modified: Thu, 23 Jun 2022 01:33:37 GMT  
		Size: 951.2 KB (951172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a83b57a833b432d62052af739a8cc3190501e66da89c3886d09a3c012961c`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 79.9 KB (79930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7966fecbe0ebd11b89d5cea9b4f7f1d394a2dcaa07a6363f22bc7ebec468281`  
		Last Modified: Thu, 23 Jun 2022 01:33:36 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b995c19d5653ff40f1fe9cc6462cae0bd6df29ce7ad43a7a33e46d1f88c89a`  
		Last Modified: Thu, 23 Jun 2022 01:33:39 GMT  
		Size: 41.1 MB (41112223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980dfe7cf66786f56b8a563b0d4a1fca33eee307a876469dccae41c1f91ae110`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa38928f6353d902381e2469961069e70fd17b955b772beda964ed1a0b693095`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a454064a1a2609f1b69dacab13edde797609e268dfcc91a6f622272057a151`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd69eb321493607da9d6a794192024da185cbdb52184011788e49ee1675b006`  
		Last Modified: Thu, 23 Jun 2022 01:33:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:e240d825d255af751f5f55af8d9671beabdf2236c0a3b4e2639b3e182d994c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:963c6bdce2865332088af6db49b38fa74bf976524a961428a7f9722bc9eef2d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a3f9bc4086335eba387e8861b885c1c1dc01693341c683f8bd6a301930b7c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:30:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:46 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:31:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:31:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:31:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:31:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:31:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:31:10 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:31:11 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:31:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e4beb83730624f8bcf51b1774b4100e1e412f82bf7581c2102c32d21babc2`  
		Last Modified: Thu, 23 Jun 2022 01:33:14 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e72f96be5467954693838bc974a9b240de99dc781c890b8854a9b72ffe7810`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 5.0 MB (5003043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fe9d6128b137e4021863af326262d53382dc923b8253440d8c35dca9346dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8033bc1cbfbb70b4bd70c8b6b05f4b51d787550ec906faaf7058fc28d2e0d541`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 79.2 KB (79250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a155e5dda342d8db092d0838f17a385cac7c9e6b675c52aa622eab8691e9d436`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f539b2f3aceca17ca461e400c845f07355901db19b62abd957e9f73637648`  
		Last Modified: Thu, 23 Jun 2022 01:33:15 GMT  
		Size: 49.1 MB (49051089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8329e9015b73d2e5486a08a39b87b23aed1ec9c1ab1e696789f89e27827f751`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30a74bb6d8fc4574cf72fe64367d6ad19cd0054333a0910265d35011060b0c1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e3d24862203426b8ad799b0ccf323a227be762d42c8592d9de3cf67c47377`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b8990f4d7ba62fff96860921dae1c48d5826104ead7d5d1d6574470b914a1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fe710ef109d9aab74fc18e8b33b7d0a5b48142ab2faa245f21bac4176ba86580
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93224180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61ad9d7a30afc783707e6c406a035e3db84a4606f0dc12ff2843c46620213fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:32 GMT
ADD file:e18c13649ea1f145047652c8e171c4824f9b6b0dbc92127a914c7fca910acf96 in / 
# Thu, 23 Jun 2022 02:02:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 05:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 05:01:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 05:02:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:02:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 05:02:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 05:03:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:03:36 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 05:03:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 05:04:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 05:04:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 05:04:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 05:04:26 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 05:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 05:04:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 05:04:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 05:04:42 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 05:04:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7716f0df7ba06b6f1937cd664805984e25e386a4165f2c6acc65356686e35221`  
		Last Modified: Thu, 23 Jun 2022 02:15:20 GMT  
		Size: 35.3 MB (35286823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a41d0487993148ae74198a437440d8cc8cafc08287418a6708059b83ef16ac9`  
		Last Modified: Thu, 23 Jun 2022 05:05:14 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36306692d69624a869e064a49d97a053aef815d059a8f200a8a234d328a6ab43`  
		Last Modified: Thu, 23 Jun 2022 05:05:13 GMT  
		Size: 6.0 MB (6044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0185210640fad2504565eec769730020fd99045c6c25bb372f53801287c3cf`  
		Last Modified: Thu, 23 Jun 2022 05:05:12 GMT  
		Size: 1.5 MB (1509406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604024ac9e627dac3af9aad8ebc6109c296f48a3301f0bf2c8aa7585226a42eb`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 295.8 KB (295782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d6b476ceb2d52c21a4f992dbf5cb865f96e83e014f0e61a21052bdbe9ea60c`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a1150e7fced5bca6693e712841c25bdc1142c1180f82ea19648a46d3661d1`  
		Last Modified: Thu, 23 Jun 2022 05:05:16 GMT  
		Size: 50.1 MB (50081001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462a4447c4a9d01b8dbf6b0c4a5ad3d6d3f6aab08dde611b9ad151b4a6cefa7`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a08687fa852c5f675f0637135f7bc517159c8169bf70f35f9873c164e2fbb1`  
		Last Modified: Thu, 23 Jun 2022 05:05:09 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b31d9afdc3af6402209eb89a5bc5ff9c6504ba61ac250738c776934816bdf`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d60da9bd78a2c81dea2d9fb14963cf46a9efd95218c42861a21f2e2050b16`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:e240d825d255af751f5f55af8d9671beabdf2236c0a3b4e2639b3e182d994c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:963c6bdce2865332088af6db49b38fa74bf976524a961428a7f9722bc9eef2d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a3f9bc4086335eba387e8861b885c1c1dc01693341c683f8bd6a301930b7c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:30:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:46 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:31:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:31:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:31:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:31:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:31:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:31:10 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:31:11 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:31:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e4beb83730624f8bcf51b1774b4100e1e412f82bf7581c2102c32d21babc2`  
		Last Modified: Thu, 23 Jun 2022 01:33:14 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e72f96be5467954693838bc974a9b240de99dc781c890b8854a9b72ffe7810`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 5.0 MB (5003043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fe9d6128b137e4021863af326262d53382dc923b8253440d8c35dca9346dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8033bc1cbfbb70b4bd70c8b6b05f4b51d787550ec906faaf7058fc28d2e0d541`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 79.2 KB (79250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a155e5dda342d8db092d0838f17a385cac7c9e6b675c52aa622eab8691e9d436`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f539b2f3aceca17ca461e400c845f07355901db19b62abd957e9f73637648`  
		Last Modified: Thu, 23 Jun 2022 01:33:15 GMT  
		Size: 49.1 MB (49051089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8329e9015b73d2e5486a08a39b87b23aed1ec9c1ab1e696789f89e27827f751`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30a74bb6d8fc4574cf72fe64367d6ad19cd0054333a0910265d35011060b0c1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e3d24862203426b8ad799b0ccf323a227be762d42c8592d9de3cf67c47377`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b8990f4d7ba62fff96860921dae1c48d5826104ead7d5d1d6574470b914a1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fe710ef109d9aab74fc18e8b33b7d0a5b48142ab2faa245f21bac4176ba86580
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93224180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61ad9d7a30afc783707e6c406a035e3db84a4606f0dc12ff2843c46620213fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:32 GMT
ADD file:e18c13649ea1f145047652c8e171c4824f9b6b0dbc92127a914c7fca910acf96 in / 
# Thu, 23 Jun 2022 02:02:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 05:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 05:01:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 05:02:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:02:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 05:02:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 05:03:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:03:36 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 05:03:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 05:04:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 05:04:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 05:04:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 05:04:26 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 05:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 05:04:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 05:04:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 05:04:42 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 05:04:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7716f0df7ba06b6f1937cd664805984e25e386a4165f2c6acc65356686e35221`  
		Last Modified: Thu, 23 Jun 2022 02:15:20 GMT  
		Size: 35.3 MB (35286823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a41d0487993148ae74198a437440d8cc8cafc08287418a6708059b83ef16ac9`  
		Last Modified: Thu, 23 Jun 2022 05:05:14 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36306692d69624a869e064a49d97a053aef815d059a8f200a8a234d328a6ab43`  
		Last Modified: Thu, 23 Jun 2022 05:05:13 GMT  
		Size: 6.0 MB (6044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0185210640fad2504565eec769730020fd99045c6c25bb372f53801287c3cf`  
		Last Modified: Thu, 23 Jun 2022 05:05:12 GMT  
		Size: 1.5 MB (1509406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604024ac9e627dac3af9aad8ebc6109c296f48a3301f0bf2c8aa7585226a42eb`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 295.8 KB (295782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d6b476ceb2d52c21a4f992dbf5cb865f96e83e014f0e61a21052bdbe9ea60c`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a1150e7fced5bca6693e712841c25bdc1142c1180f82ea19648a46d3661d1`  
		Last Modified: Thu, 23 Jun 2022 05:05:16 GMT  
		Size: 50.1 MB (50081001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462a4447c4a9d01b8dbf6b0c4a5ad3d6d3f6aab08dde611b9ad151b4a6cefa7`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a08687fa852c5f675f0637135f7bc517159c8169bf70f35f9873c164e2fbb1`  
		Last Modified: Thu, 23 Jun 2022 05:05:09 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b31d9afdc3af6402209eb89a5bc5ff9c6504ba61ac250738c776934816bdf`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d60da9bd78a2c81dea2d9fb14963cf46a9efd95218c42861a21f2e2050b16`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:e240d825d255af751f5f55af8d9671beabdf2236c0a3b4e2639b3e182d994c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:3ea7f178b119a1bbd2adbec78486241a087ba35d1d3ec9128a3ada704d55ec97
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87498751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee9d2dcf03aa6b53788baca7b138c9069926ce70119f77c999d0e2d0858e21d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:06:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:06:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:06:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:06:30 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:06:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:06:35 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:06:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:06:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:06:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:06:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:06:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:06:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:06:50 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:06:50 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b67ef10ab3031244bf995ed483d30c4423feb9f42f12d55c8511d7497c931`  
		Last Modified: Thu, 23 Jun 2022 01:08:14 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd945ed68b3fecb83857780d70642d81019952136407b87a9f4b6b94711e7dda`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 5.2 MB (5224047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d67ad9668554764252390c4e5b06fb0f33517e33a831601a00c10a05cfbe7`  
		Last Modified: Thu, 23 Jun 2022 01:08:13 GMT  
		Size: 1.6 MB (1553288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b56aaaffae17f3010ab5ba52d88e22126a8b18f5f8fd49ea4a01655c55e20b`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 295.6 KB (295555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e601de752a6ea7ddb9a0b7201437219d647dd0a6555b1d9f48ae8d94004f40`  
		Last Modified: Thu, 23 Jun 2022 01:08:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd769730295be73a2aae5a0882ad80bb9284ad34c68bff96c93ccd15f3cc73`  
		Last Modified: Thu, 23 Jun 2022 01:08:15 GMT  
		Size: 49.0 MB (49039317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0fe21a89a509108c6d599b399458e374353649854cc07814e901deb7030198`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9700366d2b2b831d620b0ee23a1b1ed39c86a91aa69aaad560465e5dd33889`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd356f58092365eb5086db70cc449f1fce114ea73ac0ee9bc18298ac6c579120`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f797d1e3134f5eda53222acba18a0644f920f20c2431b5b3604ab90b7d882c09`  
		Last Modified: Thu, 23 Jun 2022 01:08:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:963c6bdce2865332088af6db49b38fa74bf976524a961428a7f9722bc9eef2d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a3f9bc4086335eba387e8861b885c1c1dc01693341c683f8bd6a301930b7c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 01:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 01:30:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 01:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 01:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:30:46 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 01:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 01:31:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 01:31:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 01:31:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 01:31:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 01:31:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 01:31:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 01:31:10 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 01:31:11 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 01:31:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e4beb83730624f8bcf51b1774b4100e1e412f82bf7581c2102c32d21babc2`  
		Last Modified: Thu, 23 Jun 2022 01:33:14 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e72f96be5467954693838bc974a9b240de99dc781c890b8854a9b72ffe7810`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 5.0 MB (5003043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fe9d6128b137e4021863af326262d53382dc923b8253440d8c35dca9346dc`  
		Last Modified: Thu, 23 Jun 2022 01:33:12 GMT  
		Size: 1.2 MB (1221097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8033bc1cbfbb70b4bd70c8b6b05f4b51d787550ec906faaf7058fc28d2e0d541`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 79.2 KB (79250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a155e5dda342d8db092d0838f17a385cac7c9e6b675c52aa622eab8691e9d436`  
		Last Modified: Thu, 23 Jun 2022 01:33:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f539b2f3aceca17ca461e400c845f07355901db19b62abd957e9f73637648`  
		Last Modified: Thu, 23 Jun 2022 01:33:15 GMT  
		Size: 49.1 MB (49051089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8329e9015b73d2e5486a08a39b87b23aed1ec9c1ab1e696789f89e27827f751`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30a74bb6d8fc4574cf72fe64367d6ad19cd0054333a0910265d35011060b0c1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e3d24862203426b8ad799b0ccf323a227be762d42c8592d9de3cf67c47377`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66b8990f4d7ba62fff96860921dae1c48d5826104ead7d5d1d6574470b914a1`  
		Last Modified: Thu, 23 Jun 2022 01:33:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fe710ef109d9aab74fc18e8b33b7d0a5b48142ab2faa245f21bac4176ba86580
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93224180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61ad9d7a30afc783707e6c406a035e3db84a4606f0dc12ff2843c46620213fc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:32 GMT
ADD file:e18c13649ea1f145047652c8e171c4824f9b6b0dbc92127a914c7fca910acf96 in / 
# Thu, 23 Jun 2022 02:02:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 05:01:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 23 Jun 2022 05:01:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 23 Jun 2022 05:02:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:02:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 23 Jun 2022 05:02:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 23 Jun 2022 05:03:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:03:36 GMT
ENV COUCHDB_VERSION=3.2.2
# Thu, 23 Jun 2022 05:03:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 23 Jun 2022 05:04:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 23 Jun 2022 05:04:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 23 Jun 2022 05:04:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 23 Jun 2022 05:04:26 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 23 Jun 2022 05:04:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 05:04:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 23 Jun 2022 05:04:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 23 Jun 2022 05:04:42 GMT
EXPOSE 4369 5984 9100
# Thu, 23 Jun 2022 05:04:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7716f0df7ba06b6f1937cd664805984e25e386a4165f2c6acc65356686e35221`  
		Last Modified: Thu, 23 Jun 2022 02:15:20 GMT  
		Size: 35.3 MB (35286823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a41d0487993148ae74198a437440d8cc8cafc08287418a6708059b83ef16ac9`  
		Last Modified: Thu, 23 Jun 2022 05:05:14 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36306692d69624a869e064a49d97a053aef815d059a8f200a8a234d328a6ab43`  
		Last Modified: Thu, 23 Jun 2022 05:05:13 GMT  
		Size: 6.0 MB (6044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0185210640fad2504565eec769730020fd99045c6c25bb372f53801287c3cf`  
		Last Modified: Thu, 23 Jun 2022 05:05:12 GMT  
		Size: 1.5 MB (1509406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604024ac9e627dac3af9aad8ebc6109c296f48a3301f0bf2c8aa7585226a42eb`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 295.8 KB (295782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d6b476ceb2d52c21a4f992dbf5cb865f96e83e014f0e61a21052bdbe9ea60c`  
		Last Modified: Thu, 23 Jun 2022 05:05:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5a1150e7fced5bca6693e712841c25bdc1142c1180f82ea19648a46d3661d1`  
		Last Modified: Thu, 23 Jun 2022 05:05:16 GMT  
		Size: 50.1 MB (50081001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462a4447c4a9d01b8dbf6b0c4a5ad3d6d3f6aab08dde611b9ad151b4a6cefa7`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a08687fa852c5f675f0637135f7bc517159c8169bf70f35f9873c164e2fbb1`  
		Last Modified: Thu, 23 Jun 2022 05:05:09 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196b31d9afdc3af6402209eb89a5bc5ff9c6504ba61ac250738c776934816bdf`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d60da9bd78a2c81dea2d9fb14963cf46a9efd95218c42861a21f2e2050b16`  
		Last Modified: Thu, 23 Jun 2022 05:05:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
