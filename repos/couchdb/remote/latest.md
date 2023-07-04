## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ce7bf29b10de3bb90ad2c48d119ea2aaf4ca5286725c7cc4abbc6865b6c35df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:21978834fd0bf1c6087ee2b047cca56bc92b40e00020c32907bdcca59dc5d572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90239998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585ea55610d28740e25deae9f3bd53d07012da65583bfbc60300c9b5dab8cee8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:18:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 13:18:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 13:19:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:19:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 13:19:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 13:19:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:19:14 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 13:19:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 13:19:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 13:19:27 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 13:19:28 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 13:19:28 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 13:19:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 13:19:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 13:19:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 13:19:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 13:19:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b7d0341876faf741ea95c02f403b3774cce4579241a2df7a455f690241a8e`  
		Last Modified: Tue, 04 Jul 2023 13:21:11 GMT  
		Size: 3.4 KB (3407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab132f11f6f8bc2c0d7cbff53d53b006fb6682bdbbeedf4c6f735efe15f7514`  
		Last Modified: Tue, 04 Jul 2023 13:21:11 GMT  
		Size: 5.2 MB (5224499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37eb46310a60ddaf27ebe76c36edd3f279d2d931cb2c4b319f4c5437a83c6d7d`  
		Last Modified: Tue, 04 Jul 2023 13:21:10 GMT  
		Size: 610.3 KB (610261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a05974a6bb8e2d7306b8f804fd80623fe99832a49ea5834abd2065eda63bed5`  
		Last Modified: Tue, 04 Jul 2023 13:21:10 GMT  
		Size: 294.4 KB (294405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b794d535d9846a2495bb12357ce6de1908ba452964e0c198dd118f4f05fa2`  
		Last Modified: Tue, 04 Jul 2023 13:21:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8918622a4d2ab896c8f58c18f79ebe02576e86a5a7ee24b217573429a648ba`  
		Last Modified: Tue, 04 Jul 2023 13:21:13 GMT  
		Size: 52.7 MB (52686036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20b13b9d528aac3becc0a129debd625279695421feff6036cda47487240556d`  
		Last Modified: Tue, 04 Jul 2023 13:21:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c470c1fd7281ed29fe7ac5b35c1ade983d24f5134cc836c49c8ede4fd495396`  
		Last Modified: Tue, 04 Jul 2023 13:21:07 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc18f0145634642989b99be16c1d7a0eb0a2a352b6bcf643eb25b3ee57f9fec5`  
		Last Modified: Tue, 04 Jul 2023 13:21:08 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbcc505d1c4639ecda4898a3ad1687c7e849d8dbbc0eb31080ff40ac974031f`  
		Last Modified: Tue, 04 Jul 2023 13:21:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:111bef69577b043b2f8af1fdd73ffa8e23898a6bc70b3f82fd3182ff1618236a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016bedbaaaf56c355df33a499d3e134c6c17b26780b48454292818e0a91487f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:00:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 03:00:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 03:00:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 03:00:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 03:00:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:00:31 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 03:00:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 03:00:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 03:00:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 03:00:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 03:00:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:00:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 03:00:45 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 03:00:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0d271896e1f31b2370d23711036a521e9acd3228114cc23f8fac55f387dbd`  
		Last Modified: Tue, 04 Jul 2023 03:02:19 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8aac13251911c1284e2d4984341c6755bbe92e937e630352f4637e979958e68`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 5.2 MB (5209578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4219899a34e5a710d067929c59cf4cee7af11394da04941e8ec8dbdfa78c74c3`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 566.3 KB (566278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5043581719683361a4b86cda02be153567823f8d994de5929cf109fde6360729`  
		Last Modified: Tue, 04 Jul 2023 03:02:18 GMT  
		Size: 294.3 KB (294323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6faedae003b0a46ef804c85e87d669f2ac496327ecfe31589fc2ef8cb795d9`  
		Last Modified: Tue, 04 Jul 2023 03:02:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb64485bf61484d6294808283f6a71accee5b23965b220feea15e713cfe140`  
		Last Modified: Tue, 04 Jul 2023 03:02:20 GMT  
		Size: 52.5 MB (52543741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90cc018497f0216ecab317a8a855961340c9bad495e67de724c2050657df6`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3f0725b25615db7255060c7d284ae18f16ad4b6eed961e19e8b6843453968`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9180ffcb545467f2e03ea97afe6c338090bda754a8660337cb26ba571028b18d`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0e1825ffd91b4338bf24761c3146c6d0a90ea00e5d87b2b89c62e7a2489e73`  
		Last Modified: Tue, 04 Jul 2023 03:02:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:3eb5767e878cf69f2870e99b9c95b3be3dfcc0471c122389a9d0dfb659234883
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065d599166a5dc0bcef7979716402c5fca0bbc616c07314ded86709614f51e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:47:38 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 04:47:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 04:48:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 04:48:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 04:48:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:48:46 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 04:48:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 04:49:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 04:49:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 04:49:23 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 04:49:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 04:49:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 04:49:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 04:49:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 04:49:28 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 04:49:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701cbef8ba9fc49aabcd763212b84907356b9d67b68018587e12e7c54af3fee`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf807338a413416db46fc9e534bbe3265bc56baad887760486a0a54d25123b2`  
		Last Modified: Tue, 04 Jul 2023 04:50:24 GMT  
		Size: 6.0 MB (6044173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409825b5d24fb99ad06438d83de58bf0ec20c4238d23657386eb390b56cf14a`  
		Last Modified: Tue, 04 Jul 2023 04:50:22 GMT  
		Size: 662.2 KB (662178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f62ee6bf18f44a92fdcdf0283d02bd2a4f1af5b1a8bd7e85621f45a95f8a04b`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 294.4 KB (294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716fa9059088e2aa7f1ea452b78d008438054cf553aec84db5f0b1c9d45af07d`  
		Last Modified: Tue, 04 Jul 2023 04:50:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646ca9755ca8690dde79876e5cc2575157aa6676d4f208ae1df21923cccd99cd`  
		Last Modified: Tue, 04 Jul 2023 04:50:28 GMT  
		Size: 53.7 MB (53662975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f92d3e00609286c22a6359ccd30574b19d50f9d6697f0a0ea5eab26ab12bc76`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e7380fa4b617f06e977822abe3be70818da7d6d685880896b0eae0a1515be`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080782760cb6436e3664eb4f4e11c5008ca48beefe7641cd9296bcb2b0596458`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0412cece6d0a349aed06c4894e09a68bcee9300a4e7f88f629d13647544596e6`  
		Last Modified: Tue, 04 Jul 2023 04:50:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:0bcccda85f5c60188048ec57dd9459e296f769c5ad766371be2f057c1cb31202
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b56bdcd62fdc551f2173e4ad2ca3ca6490f7f1acec77826451b8fabe35fa900`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:31:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Jul 2023 02:32:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 04 Jul 2023 02:32:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 04 Jul 2023 02:32:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Jul 2023 02:32:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:32:15 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 04 Jul 2023 02:32:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 04 Jul 2023 02:32:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 04 Jul 2023 02:32:33 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 04 Jul 2023 02:32:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 02:32:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:32:34 GMT
VOLUME [/opt/couchdb/data]
# Tue, 04 Jul 2023 02:32:34 GMT
EXPOSE 4369 5984 9100
# Tue, 04 Jul 2023 02:32:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ca3d8ad5e25fe241e125f8bbbe38fc1732c37f3caa96c1ef02a7f489a5aae6`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 3.4 KB (3432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60572b3f976bbdc302097dea095b6bea87f04aaa5902a11eb46130547c2f0154`  
		Last Modified: Tue, 04 Jul 2023 02:32:52 GMT  
		Size: 5.1 MB (5110438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d956cd8463eed79cf7d437deb772330ad221345369e72ac6295e5713ca302`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd772a2ca35e7648d7321fb6b0eb780c57418a1902a7805f6217c3e30e57893`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a421ebc7a36d0af94ef7d446133f4686c9ef5a16e88004505d10bbf259c14db6`  
		Last Modified: Tue, 04 Jul 2023 02:32:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9f6c295417043fc04a54083419e1707a71800e53f2d2643c9a2085f368fb87`  
		Last Modified: Tue, 04 Jul 2023 02:32:55 GMT  
		Size: 51.4 MB (51354464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83bfa157ad1e19b57a9df85aa0579c82163bee844e2c05b20095043b063b28`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235315086a5d8e7a181854f2e016c9da2abc0c2f9a30e583979f1b0d4326ee86`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dbfd2547b3b689e42acaaa81c5eb50c74f032cf42d0e18e33a29f8253ec632`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dac4cd592579b8351c686a4fe857238634639bd8f332711ec4d2545d6a95b71`  
		Last Modified: Tue, 04 Jul 2023 02:32:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
