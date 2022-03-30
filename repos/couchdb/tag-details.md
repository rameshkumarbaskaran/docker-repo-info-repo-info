<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.1`](#couchdb321)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:ab25340682a4ac3307e903b728be507b00ba3aae77a01150da4b402bae997261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:ad36fd6dfe7cd7f781972ba406d34a51016ebf906a8e28f9aff54d8343f5bf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423c97c0064f6fe6f057adfe1b52f79090d1edef4aef30d4d6122840d489972`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:43:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:43:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:43:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:59 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 29 Mar 2022 17:44:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:44:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 29 Mar 2022 17:44:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:44:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:44:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:44:19 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:44:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80c2ec71c18a546328f27f525729f0c3e18f4fb7dc284b71c87cd40c658816`  
		Last Modified: Tue, 29 Mar 2022 17:45:07 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d76737fe782adae7752b9647c8648f0053f8922839426e07c0a0baf9cc5e15`  
		Last Modified: Tue, 29 Mar 2022 17:45:06 GMT  
		Size: 6.7 MB (6698553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e96feda56228c6ba8df27fdf66d3f1012c101798991db8e46d3a671e4300da`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 1.3 MB (1258347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cc3267bf58605d4e4c2790d9699e6ed942f5aca374fe06f9a7dd40d6868168`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 293.0 KB (293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b8a8a4eb7c2784f0a5547114b61d49419286c64e4d4b847de40c64b3229a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fe6235da47e775247c6b70aca81d534d5abe742a2cdf75a3db52624ce65060`  
		Last Modified: Tue, 29 Mar 2022 17:45:24 GMT  
		Size: 49.1 MB (49127187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f388ebe7a8ffb5d8461c70bcea44ed910d76509629985c5fa5fe0b8fec9251f7`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cacb782e6b36cda2946b4ed6600aed5f25288f2e767e2cc62621071e1675ef2`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e230c34932cefb3ed9b0fddc3cbde48793eb60c90fb314ddd5f6da3952584`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b573aa46dd288da4293255de0626c59bce7c983735240e3a27c6abe4fe8a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f11020437515dc145d99c6fcc981ac1d17a4aec58280c8ffb826ccac85aa1c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551b1606ec1e72d98fb4b67539e905f4378e41f848e149173c11e4634d9d352a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:27:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:27:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:27:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:27:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:28:30 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 30 Mar 2022 08:28:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:28:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:28:51 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:28:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 30 Mar 2022 08:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:28:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:28:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:28:56 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:28:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd2c778e6c3051b4b30d4eb5d5f245d9b40e9de2d14ceebdd59b28d1b1b388`  
		Last Modified: Wed, 30 Mar 2022 08:29:53 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c38ec0537937bfb3f0322239b514e7bb076e412f499bb91a8765a9e36ce4a43`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 6.6 MB (6556421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862e45303a7d460f09d3f9404c5d27cf52442f6408aa02cab784e4b921f52dd`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 951.2 KB (951176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fdd2c33338555a9c5b5656b51150443bc138c332535e3d4459de8e2bf98256`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 80.0 KB (79973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e947b153b5e6adc3464fc9dddbeae87cb1c5e928e7390145d405c9c6a8de8435`  
		Last Modified: Wed, 30 Mar 2022 08:30:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5f88e2f0e33e2f3e6f54203d56e7805e5b77d17f2a66655f06b528eecea5f`  
		Last Modified: Wed, 30 Mar 2022 08:30:09 GMT  
		Size: 39.0 MB (39023508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f294d42c17da31c8b6d162362b8bb2218ffcdaca354a0c0a424c3ad84b8ac6a0`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e492ba698a6596e07aabc7fde207012518a598dfc607be49d2b7bcf48eb8a21c`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456f48430b2a71e906a870518dbbb5b9406ba768489a57c55e14909585aac914`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a1eeee9e8b930375ffce110ab770f3caba8627780a86d2470591908e1cba93`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ab25340682a4ac3307e903b728be507b00ba3aae77a01150da4b402bae997261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:ad36fd6dfe7cd7f781972ba406d34a51016ebf906a8e28f9aff54d8343f5bf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423c97c0064f6fe6f057adfe1b52f79090d1edef4aef30d4d6122840d489972`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:43:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:43:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:43:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:59 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 29 Mar 2022 17:44:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:44:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 29 Mar 2022 17:44:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:44:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:44:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:44:19 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:44:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80c2ec71c18a546328f27f525729f0c3e18f4fb7dc284b71c87cd40c658816`  
		Last Modified: Tue, 29 Mar 2022 17:45:07 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d76737fe782adae7752b9647c8648f0053f8922839426e07c0a0baf9cc5e15`  
		Last Modified: Tue, 29 Mar 2022 17:45:06 GMT  
		Size: 6.7 MB (6698553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e96feda56228c6ba8df27fdf66d3f1012c101798991db8e46d3a671e4300da`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 1.3 MB (1258347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cc3267bf58605d4e4c2790d9699e6ed942f5aca374fe06f9a7dd40d6868168`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 293.0 KB (293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b8a8a4eb7c2784f0a5547114b61d49419286c64e4d4b847de40c64b3229a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fe6235da47e775247c6b70aca81d534d5abe742a2cdf75a3db52624ce65060`  
		Last Modified: Tue, 29 Mar 2022 17:45:24 GMT  
		Size: 49.1 MB (49127187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f388ebe7a8ffb5d8461c70bcea44ed910d76509629985c5fa5fe0b8fec9251f7`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cacb782e6b36cda2946b4ed6600aed5f25288f2e767e2cc62621071e1675ef2`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e230c34932cefb3ed9b0fddc3cbde48793eb60c90fb314ddd5f6da3952584`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b573aa46dd288da4293255de0626c59bce7c983735240e3a27c6abe4fe8a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f11020437515dc145d99c6fcc981ac1d17a4aec58280c8ffb826ccac85aa1c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551b1606ec1e72d98fb4b67539e905f4378e41f848e149173c11e4634d9d352a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:27:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:27:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:27:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:27:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:28:30 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 30 Mar 2022 08:28:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:28:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:28:51 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:28:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 30 Mar 2022 08:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:28:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:28:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:28:56 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:28:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd2c778e6c3051b4b30d4eb5d5f245d9b40e9de2d14ceebdd59b28d1b1b388`  
		Last Modified: Wed, 30 Mar 2022 08:29:53 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c38ec0537937bfb3f0322239b514e7bb076e412f499bb91a8765a9e36ce4a43`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 6.6 MB (6556421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862e45303a7d460f09d3f9404c5d27cf52442f6408aa02cab784e4b921f52dd`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 951.2 KB (951176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fdd2c33338555a9c5b5656b51150443bc138c332535e3d4459de8e2bf98256`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 80.0 KB (79973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e947b153b5e6adc3464fc9dddbeae87cb1c5e928e7390145d405c9c6a8de8435`  
		Last Modified: Wed, 30 Mar 2022 08:30:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5f88e2f0e33e2f3e6f54203d56e7805e5b77d17f2a66655f06b528eecea5f`  
		Last Modified: Wed, 30 Mar 2022 08:30:09 GMT  
		Size: 39.0 MB (39023508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f294d42c17da31c8b6d162362b8bb2218ffcdaca354a0c0a424c3ad84b8ac6a0`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e492ba698a6596e07aabc7fde207012518a598dfc607be49d2b7bcf48eb8a21c`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456f48430b2a71e906a870518dbbb5b9406ba768489a57c55e14909585aac914`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a1eeee9e8b930375ffce110ab770f3caba8627780a86d2470591908e1cba93`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ab25340682a4ac3307e903b728be507b00ba3aae77a01150da4b402bae997261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:ad36fd6dfe7cd7f781972ba406d34a51016ebf906a8e28f9aff54d8343f5bf4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84536076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423c97c0064f6fe6f057adfe1b52f79090d1edef4aef30d4d6122840d489972`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:43:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:43:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:43:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:59 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 29 Mar 2022 17:44:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:44:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:44:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 29 Mar 2022 17:44:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:44:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:44:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:44:19 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:44:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80c2ec71c18a546328f27f525729f0c3e18f4fb7dc284b71c87cd40c658816`  
		Last Modified: Tue, 29 Mar 2022 17:45:07 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d76737fe782adae7752b9647c8648f0053f8922839426e07c0a0baf9cc5e15`  
		Last Modified: Tue, 29 Mar 2022 17:45:06 GMT  
		Size: 6.7 MB (6698553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e96feda56228c6ba8df27fdf66d3f1012c101798991db8e46d3a671e4300da`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 1.3 MB (1258347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cc3267bf58605d4e4c2790d9699e6ed942f5aca374fe06f9a7dd40d6868168`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 293.0 KB (293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b8a8a4eb7c2784f0a5547114b61d49419286c64e4d4b847de40c64b3229a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fe6235da47e775247c6b70aca81d534d5abe742a2cdf75a3db52624ce65060`  
		Last Modified: Tue, 29 Mar 2022 17:45:24 GMT  
		Size: 49.1 MB (49127187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f388ebe7a8ffb5d8461c70bcea44ed910d76509629985c5fa5fe0b8fec9251f7`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cacb782e6b36cda2946b4ed6600aed5f25288f2e767e2cc62621071e1675ef2`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e230c34932cefb3ed9b0fddc3cbde48793eb60c90fb314ddd5f6da3952584`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3b573aa46dd288da4293255de0626c59bce7c983735240e3a27c6abe4fe8a3`  
		Last Modified: Tue, 29 Mar 2022 17:45:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f11020437515dc145d99c6fcc981ac1d17a4aec58280c8ffb826ccac85aa1c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551b1606ec1e72d98fb4b67539e905f4378e41f848e149173c11e4634d9d352a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:27:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:27:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:27:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:27:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:28:30 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 30 Mar 2022 08:28:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:28:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:28:51 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:28:53 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 30 Mar 2022 08:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:28:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:28:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:28:56 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:28:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd2c778e6c3051b4b30d4eb5d5f245d9b40e9de2d14ceebdd59b28d1b1b388`  
		Last Modified: Wed, 30 Mar 2022 08:29:53 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c38ec0537937bfb3f0322239b514e7bb076e412f499bb91a8765a9e36ce4a43`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 6.6 MB (6556421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862e45303a7d460f09d3f9404c5d27cf52442f6408aa02cab784e4b921f52dd`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 951.2 KB (951176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fdd2c33338555a9c5b5656b51150443bc138c332535e3d4459de8e2bf98256`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 80.0 KB (79973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e947b153b5e6adc3464fc9dddbeae87cb1c5e928e7390145d405c9c6a8de8435`  
		Last Modified: Wed, 30 Mar 2022 08:30:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5f88e2f0e33e2f3e6f54203d56e7805e5b77d17f2a66655f06b528eecea5f`  
		Last Modified: Wed, 30 Mar 2022 08:30:09 GMT  
		Size: 39.0 MB (39023508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f294d42c17da31c8b6d162362b8bb2218ffcdaca354a0c0a424c3ad84b8ac6a0`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e492ba698a6596e07aabc7fde207012518a598dfc607be49d2b7bcf48eb8a21c`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456f48430b2a71e906a870518dbbb5b9406ba768489a57c55e14909585aac914`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a1eeee9e8b930375ffce110ab770f3caba8627780a86d2470591908e1cba93`  
		Last Modified: Wed, 30 Mar 2022 08:30:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:df9862fdb9057e6fe1efbba3c1035524de717ae0e40860096b76ad804788ae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:8ee4e9e4ca3cfbaf5daaa04a4a16afe5fdb11f09aa41dc608e9bd0e05714a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7114097399f946884e7241747ddae4059f78348becca61923ea391269f5ed0c6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:42:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:42:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:42:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:06 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 29 Mar 2022 17:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:20 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:20 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696c3a7bd6345ad3dec2ca659258cc837ee8571eccb157d64903e720345f01f`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985564977890f4d120ec2e33e06bde120102045d55b49561f7bf84a56d7754e`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 5.2 MB (5223719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af07aee7e25c153d2ef231f90acc4dfa3a720f79bde9ccfe2cfb99d9584ab14c`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 1.6 MB (1553279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f92deea0074a11b57afd14540d1b94e65fefc1b3062c355cea2027bcd3f56`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 295.6 KB (295557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e864d22b442a1e3bd13c38e716e30fd74dd0174ee568cea450b2f327620aa8`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8770a376654cc5b074075f3966059d8d345cec01e26e3e2d01168b30c4dc7b`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 49.0 MB (48992758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e89ca780ed0008db1f4194631474ea761c40582871f70e83a4ceefedc60d10`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3787af7df9836507827f5d3c0898ed7b3634c14d618b1ef33661101e3c2f651a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63db53b08f10548afad6f3264cd087f3cf504ffb8c5b9c815093abdef55a227a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3858cce7020b361c512d44b74800e576f4165209a6119c81d47e7371187cbc6`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:246537cdbbaac98b9afbc9367c7ce8b8d1491ef96ea0f07c03852443dd11c3e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85382083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc83543249a5d2861765bd92cafa0b84e9a0f40fa1e86bbaafa4359181495b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:26:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:26:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:26:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:26:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:26:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:54 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 08:26:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:27:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:27:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:27:13 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:27:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 08:27:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:27:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:27:16 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:27:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:27:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8c8acb0d3f459f4a82531d2da282c651c8205dd7b6bd0617e5e9004a41bebc`  
		Last Modified: Wed, 30 Mar 2022 08:29:27 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be11bd6efb04bece693da92602fbe034b7d40555a74f8d1edae0f37c7cdb4a`  
		Last Modified: Wed, 30 Mar 2022 08:29:26 GMT  
		Size: 5.0 MB (5003011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cf8ef1765d69e3490c938cb65494fd1af30b179862575d93bae50194a7ca9`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 1.2 MB (1221079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1645640211e15f616708007ae13071ca927c0640e44703d85f71be0f349c61`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 79.2 KB (79207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ad0867dd44f11c972190d269051120e31e7589afa36984831c1432ed063e7`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d963f005819a7af1244e8553dbbae5d9f1a0215d9cf654bd50ea71d1596e43`  
		Last Modified: Wed, 30 Mar 2022 08:29:28 GMT  
		Size: 49.0 MB (49007420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c23ac21cb8331594e767265c53dec6017caf5611b24e31aae2aea5b241e3546`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd8e51c736ae943f5c95f37ba1c31036b72af83b64b01f91b286f6020be10b`  
		Last Modified: Wed, 30 Mar 2022 08:29:22 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804d96f21b6f0b22381d16648e7af1978742821728e1943c0e2c8951a0ccd8fe`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a6f3d37897cfaa7e241172d0b6971beeae609d47d9eaf7725ed1d5334b047`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a0ec772898e7b98ab726da9bbf9e2a8067686b33407d545eb345b3cce3afc553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93167466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958978428a8edc826010f4eb4f833438a7e7c7417d4228fa95f577ed5102c636`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 10:49:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 10:49:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 10:50:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:50:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 10:50:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 10:51:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:51:11 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 10:51:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 10:51:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 10:51:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 10:51:58 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 10:52:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 10:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 10:52:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:52:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 10:52:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 10:52:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e95f94117dc731d116e8d312bc23f0c7c790e38bd6ab7f727ec457b553c993`  
		Last Modified: Wed, 30 Mar 2022 10:52:49 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f5e8f5cbad19275da76f517a0a7ef0ec7f0e54ad76035a18c00fd4a37134c`  
		Last Modified: Wed, 30 Mar 2022 10:52:47 GMT  
		Size: 6.0 MB (6043641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0779c52e66bf4a49e1fe70a0882b6f3d14d1416145a03b89332f18baabc8e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 1.5 MB (1509286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bee7e95e7677193b00f56a750d6362cc0f2076daac532b0f932b19bf1518e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 295.6 KB (295648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54285c6aef4afa86d38a12cd2da3259c66f04a426ce7565f44407391e624a12a`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57879a9c4ffc05dabe1871b51ede9836db31b04ede125d89443e49e5cda0c9`  
		Last Modified: Wed, 30 Mar 2022 10:52:48 GMT  
		Size: 50.0 MB (50029239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6cd7b2f21c43f6964cca89efbc25e47a664495439380cfa6893fa22f55de93`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d472bb6e5961d60b48ba0d00a55475445b0ac511e884daa55db57a536e99a`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a27af1791dc6b357b1d5c107f38d595649b0820b031f8771c16e48d54382a3`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2c1d4e6f6c55894d6e3ce5ff51e6555cd0b856ade14a766c4b7bb7e4f8277`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:e74aefb21b621d474f8c5deb473805efd8fd528dd9b8c43e4117eab38ee571d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:368d61037a216fe4345da19069181ac6659abb7eceed8db7096510bdb7c87dcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80021196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618fbd3b3ba7efd2a9429d4ea1913c6918450398752b889ab399e11377ef1bb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:43:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:43:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:43:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 29 Mar 2022 17:43:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:56 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:57 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80c2ec71c18a546328f27f525729f0c3e18f4fb7dc284b71c87cd40c658816`  
		Last Modified: Tue, 29 Mar 2022 17:45:07 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d76737fe782adae7752b9647c8648f0053f8922839426e07c0a0baf9cc5e15`  
		Last Modified: Tue, 29 Mar 2022 17:45:06 GMT  
		Size: 6.7 MB (6698553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e96feda56228c6ba8df27fdf66d3f1012c101798991db8e46d3a671e4300da`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 1.3 MB (1258347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cc3267bf58605d4e4c2790d9699e6ed942f5aca374fe06f9a7dd40d6868168`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 293.0 KB (293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4646cb3889b90d6bebb4e47d5c9cb300948f168523d048eabca56e13010f4d5`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1fe60861ad58b82efc89822a721d8548eaf433212fccd62cbe094b8393cbc5`  
		Last Modified: Tue, 29 Mar 2022 17:45:08 GMT  
		Size: 44.6 MB (44612312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cacbc393ee9546ceed54cb65dcf0353670fcddfa682946d194a36525f6ec2b9`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5d2b9521c0543062d38279d493831ae5d26a9364967e905cbae693ac7c84f0`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3722bacfe8101f6e6238165e5ebc20116421df13b398ceaefc8a1c5b217f01`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4340be74f99c82e73e4f16fee415fa55b16c8b87e4ef816981470139e8dd82a`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:af2f845e462ecd308679189c77e9b265107398f7caf396bcf90bce56cbe7b7f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74626904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13acc33ef373e04b3729ffeb706b2a6356e40e710eceecaa77ce8909e4b3c1d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:27:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:27:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:27:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:27:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:57 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 30 Mar 2022 08:27:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:28:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:28:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:28:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:28:17 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 30 Mar 2022 08:28:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:28:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:28:19 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:28:20 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:28:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd2c778e6c3051b4b30d4eb5d5f245d9b40e9de2d14ceebdd59b28d1b1b388`  
		Last Modified: Wed, 30 Mar 2022 08:29:53 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c38ec0537937bfb3f0322239b514e7bb076e412f499bb91a8765a9e36ce4a43`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 6.6 MB (6556421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862e45303a7d460f09d3f9404c5d27cf52442f6408aa02cab784e4b921f52dd`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 951.2 KB (951176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fdd2c33338555a9c5b5656b51150443bc138c332535e3d4459de8e2bf98256`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 80.0 KB (79973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10684516734122d64b1319e992f1691b2cb1cd33719a04dfb7b0003345acc7c`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d014d72b94b4b0702ea15516528b8d2ff03ff8eacb4fe81ce38dfb273d47d6`  
		Last Modified: Wed, 30 Mar 2022 08:29:52 GMT  
		Size: 41.1 MB (41112641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7692b1518e2b03369982567eb8e74627c5f7721ee9954230741c4ca5843e57b7`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5816217966c485cdb83bff05b6d32be87b9a5ce18f2b8d513b771a8c2255ea0`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3176123b7b828a4ef814ac554046a3eae4136a88cc8c2d7dfff66bf319edaaed`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5d7737bd8ff65c17d510f315cc4a97fa10cc77945215c0ad38332b21bbde07`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:e74aefb21b621d474f8c5deb473805efd8fd528dd9b8c43e4117eab38ee571d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:368d61037a216fe4345da19069181ac6659abb7eceed8db7096510bdb7c87dcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80021196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618fbd3b3ba7efd2a9429d4ea1913c6918450398752b889ab399e11377ef1bb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:43:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:43:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:43:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:36 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:42 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 29 Mar 2022 17:43:42 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:56 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:57 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd80c2ec71c18a546328f27f525729f0c3e18f4fb7dc284b71c87cd40c658816`  
		Last Modified: Tue, 29 Mar 2022 17:45:07 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d76737fe782adae7752b9647c8648f0053f8922839426e07c0a0baf9cc5e15`  
		Last Modified: Tue, 29 Mar 2022 17:45:06 GMT  
		Size: 6.7 MB (6698553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e96feda56228c6ba8df27fdf66d3f1012c101798991db8e46d3a671e4300da`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 1.3 MB (1258347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cc3267bf58605d4e4c2790d9699e6ed942f5aca374fe06f9a7dd40d6868168`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 293.0 KB (293001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4646cb3889b90d6bebb4e47d5c9cb300948f168523d048eabca56e13010f4d5`  
		Last Modified: Tue, 29 Mar 2022 17:45:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1fe60861ad58b82efc89822a721d8548eaf433212fccd62cbe094b8393cbc5`  
		Last Modified: Tue, 29 Mar 2022 17:45:08 GMT  
		Size: 44.6 MB (44612312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cacbc393ee9546ceed54cb65dcf0353670fcddfa682946d194a36525f6ec2b9`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5d2b9521c0543062d38279d493831ae5d26a9364967e905cbae693ac7c84f0`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3722bacfe8101f6e6238165e5ebc20116421df13b398ceaefc8a1c5b217f01`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4340be74f99c82e73e4f16fee415fa55b16c8b87e4ef816981470139e8dd82a`  
		Last Modified: Tue, 29 Mar 2022 17:45:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:af2f845e462ecd308679189c77e9b265107398f7caf396bcf90bce56cbe7b7f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74626904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13acc33ef373e04b3729ffeb706b2a6356e40e710eceecaa77ce8909e4b3c1d2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:27:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:27:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:27:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:27:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:27:57 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 30 Mar 2022 08:27:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:28:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:28:15 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:28:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:28:17 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 30 Mar 2022 08:28:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:28:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:28:19 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:28:20 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:28:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd2c778e6c3051b4b30d4eb5d5f245d9b40e9de2d14ceebdd59b28d1b1b388`  
		Last Modified: Wed, 30 Mar 2022 08:29:53 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c38ec0537937bfb3f0322239b514e7bb076e412f499bb91a8765a9e36ce4a43`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 6.6 MB (6556421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862e45303a7d460f09d3f9404c5d27cf52442f6408aa02cab784e4b921f52dd`  
		Last Modified: Wed, 30 Mar 2022 08:29:50 GMT  
		Size: 951.2 KB (951176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fdd2c33338555a9c5b5656b51150443bc138c332535e3d4459de8e2bf98256`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 80.0 KB (79973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10684516734122d64b1319e992f1691b2cb1cd33719a04dfb7b0003345acc7c`  
		Last Modified: Wed, 30 Mar 2022 08:29:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d014d72b94b4b0702ea15516528b8d2ff03ff8eacb4fe81ce38dfb273d47d6`  
		Last Modified: Wed, 30 Mar 2022 08:29:52 GMT  
		Size: 41.1 MB (41112641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7692b1518e2b03369982567eb8e74627c5f7721ee9954230741c4ca5843e57b7`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5816217966c485cdb83bff05b6d32be87b9a5ce18f2b8d513b771a8c2255ea0`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3176123b7b828a4ef814ac554046a3eae4136a88cc8c2d7dfff66bf319edaaed`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5d7737bd8ff65c17d510f315cc4a97fa10cc77945215c0ad38332b21bbde07`  
		Last Modified: Wed, 30 Mar 2022 08:29:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:df9862fdb9057e6fe1efbba3c1035524de717ae0e40860096b76ad804788ae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:8ee4e9e4ca3cfbaf5daaa04a4a16afe5fdb11f09aa41dc608e9bd0e05714a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7114097399f946884e7241747ddae4059f78348becca61923ea391269f5ed0c6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:42:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:42:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:42:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:06 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 29 Mar 2022 17:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:20 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:20 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696c3a7bd6345ad3dec2ca659258cc837ee8571eccb157d64903e720345f01f`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985564977890f4d120ec2e33e06bde120102045d55b49561f7bf84a56d7754e`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 5.2 MB (5223719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af07aee7e25c153d2ef231f90acc4dfa3a720f79bde9ccfe2cfb99d9584ab14c`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 1.6 MB (1553279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f92deea0074a11b57afd14540d1b94e65fefc1b3062c355cea2027bcd3f56`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 295.6 KB (295557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e864d22b442a1e3bd13c38e716e30fd74dd0174ee568cea450b2f327620aa8`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8770a376654cc5b074075f3966059d8d345cec01e26e3e2d01168b30c4dc7b`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 49.0 MB (48992758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e89ca780ed0008db1f4194631474ea761c40582871f70e83a4ceefedc60d10`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3787af7df9836507827f5d3c0898ed7b3634c14d618b1ef33661101e3c2f651a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63db53b08f10548afad6f3264cd087f3cf504ffb8c5b9c815093abdef55a227a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3858cce7020b361c512d44b74800e576f4165209a6119c81d47e7371187cbc6`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:246537cdbbaac98b9afbc9367c7ce8b8d1491ef96ea0f07c03852443dd11c3e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85382083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc83543249a5d2861765bd92cafa0b84e9a0f40fa1e86bbaafa4359181495b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:26:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:26:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:26:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:26:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:26:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:54 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 08:26:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:27:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:27:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:27:13 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:27:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 08:27:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:27:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:27:16 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:27:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:27:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8c8acb0d3f459f4a82531d2da282c651c8205dd7b6bd0617e5e9004a41bebc`  
		Last Modified: Wed, 30 Mar 2022 08:29:27 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be11bd6efb04bece693da92602fbe034b7d40555a74f8d1edae0f37c7cdb4a`  
		Last Modified: Wed, 30 Mar 2022 08:29:26 GMT  
		Size: 5.0 MB (5003011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cf8ef1765d69e3490c938cb65494fd1af30b179862575d93bae50194a7ca9`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 1.2 MB (1221079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1645640211e15f616708007ae13071ca927c0640e44703d85f71be0f349c61`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 79.2 KB (79207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ad0867dd44f11c972190d269051120e31e7589afa36984831c1432ed063e7`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d963f005819a7af1244e8553dbbae5d9f1a0215d9cf654bd50ea71d1596e43`  
		Last Modified: Wed, 30 Mar 2022 08:29:28 GMT  
		Size: 49.0 MB (49007420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c23ac21cb8331594e767265c53dec6017caf5611b24e31aae2aea5b241e3546`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd8e51c736ae943f5c95f37ba1c31036b72af83b64b01f91b286f6020be10b`  
		Last Modified: Wed, 30 Mar 2022 08:29:22 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804d96f21b6f0b22381d16648e7af1978742821728e1943c0e2c8951a0ccd8fe`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a6f3d37897cfaa7e241172d0b6971beeae609d47d9eaf7725ed1d5334b047`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a0ec772898e7b98ab726da9bbf9e2a8067686b33407d545eb345b3cce3afc553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93167466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958978428a8edc826010f4eb4f833438a7e7c7417d4228fa95f577ed5102c636`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 10:49:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 10:49:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 10:50:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:50:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 10:50:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 10:51:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:51:11 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 10:51:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 10:51:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 10:51:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 10:51:58 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 10:52:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 10:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 10:52:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:52:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 10:52:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 10:52:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e95f94117dc731d116e8d312bc23f0c7c790e38bd6ab7f727ec457b553c993`  
		Last Modified: Wed, 30 Mar 2022 10:52:49 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f5e8f5cbad19275da76f517a0a7ef0ec7f0e54ad76035a18c00fd4a37134c`  
		Last Modified: Wed, 30 Mar 2022 10:52:47 GMT  
		Size: 6.0 MB (6043641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0779c52e66bf4a49e1fe70a0882b6f3d14d1416145a03b89332f18baabc8e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 1.5 MB (1509286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bee7e95e7677193b00f56a750d6362cc0f2076daac532b0f932b19bf1518e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 295.6 KB (295648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54285c6aef4afa86d38a12cd2da3259c66f04a426ce7565f44407391e624a12a`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57879a9c4ffc05dabe1871b51ede9836db31b04ede125d89443e49e5cda0c9`  
		Last Modified: Wed, 30 Mar 2022 10:52:48 GMT  
		Size: 50.0 MB (50029239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6cd7b2f21c43f6964cca89efbc25e47a664495439380cfa6893fa22f55de93`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d472bb6e5961d60b48ba0d00a55475445b0ac511e884daa55db57a536e99a`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a27af1791dc6b357b1d5c107f38d595649b0820b031f8771c16e48d54382a3`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2c1d4e6f6c55894d6e3ce5ff51e6555cd0b856ade14a766c4b7bb7e4f8277`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:df9862fdb9057e6fe1efbba3c1035524de717ae0e40860096b76ad804788ae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:8ee4e9e4ca3cfbaf5daaa04a4a16afe5fdb11f09aa41dc608e9bd0e05714a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7114097399f946884e7241747ddae4059f78348becca61923ea391269f5ed0c6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:42:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:42:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:42:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:06 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 29 Mar 2022 17:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:20 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:20 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696c3a7bd6345ad3dec2ca659258cc837ee8571eccb157d64903e720345f01f`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985564977890f4d120ec2e33e06bde120102045d55b49561f7bf84a56d7754e`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 5.2 MB (5223719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af07aee7e25c153d2ef231f90acc4dfa3a720f79bde9ccfe2cfb99d9584ab14c`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 1.6 MB (1553279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f92deea0074a11b57afd14540d1b94e65fefc1b3062c355cea2027bcd3f56`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 295.6 KB (295557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e864d22b442a1e3bd13c38e716e30fd74dd0174ee568cea450b2f327620aa8`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8770a376654cc5b074075f3966059d8d345cec01e26e3e2d01168b30c4dc7b`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 49.0 MB (48992758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e89ca780ed0008db1f4194631474ea761c40582871f70e83a4ceefedc60d10`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3787af7df9836507827f5d3c0898ed7b3634c14d618b1ef33661101e3c2f651a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63db53b08f10548afad6f3264cd087f3cf504ffb8c5b9c815093abdef55a227a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3858cce7020b361c512d44b74800e576f4165209a6119c81d47e7371187cbc6`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:246537cdbbaac98b9afbc9367c7ce8b8d1491ef96ea0f07c03852443dd11c3e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85382083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc83543249a5d2861765bd92cafa0b84e9a0f40fa1e86bbaafa4359181495b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:26:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:26:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:26:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:26:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:26:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:54 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 08:26:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:27:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:27:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:27:13 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:27:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 08:27:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:27:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:27:16 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:27:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:27:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8c8acb0d3f459f4a82531d2da282c651c8205dd7b6bd0617e5e9004a41bebc`  
		Last Modified: Wed, 30 Mar 2022 08:29:27 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be11bd6efb04bece693da92602fbe034b7d40555a74f8d1edae0f37c7cdb4a`  
		Last Modified: Wed, 30 Mar 2022 08:29:26 GMT  
		Size: 5.0 MB (5003011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cf8ef1765d69e3490c938cb65494fd1af30b179862575d93bae50194a7ca9`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 1.2 MB (1221079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1645640211e15f616708007ae13071ca927c0640e44703d85f71be0f349c61`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 79.2 KB (79207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ad0867dd44f11c972190d269051120e31e7589afa36984831c1432ed063e7`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d963f005819a7af1244e8553dbbae5d9f1a0215d9cf654bd50ea71d1596e43`  
		Last Modified: Wed, 30 Mar 2022 08:29:28 GMT  
		Size: 49.0 MB (49007420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c23ac21cb8331594e767265c53dec6017caf5611b24e31aae2aea5b241e3546`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd8e51c736ae943f5c95f37ba1c31036b72af83b64b01f91b286f6020be10b`  
		Last Modified: Wed, 30 Mar 2022 08:29:22 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804d96f21b6f0b22381d16648e7af1978742821728e1943c0e2c8951a0ccd8fe`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a6f3d37897cfaa7e241172d0b6971beeae609d47d9eaf7725ed1d5334b047`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a0ec772898e7b98ab726da9bbf9e2a8067686b33407d545eb345b3cce3afc553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93167466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958978428a8edc826010f4eb4f833438a7e7c7417d4228fa95f577ed5102c636`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 10:49:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 10:49:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 10:50:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:50:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 10:50:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 10:51:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:51:11 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 10:51:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 10:51:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 10:51:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 10:51:58 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 10:52:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 10:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 10:52:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:52:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 10:52:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 10:52:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e95f94117dc731d116e8d312bc23f0c7c790e38bd6ab7f727ec457b553c993`  
		Last Modified: Wed, 30 Mar 2022 10:52:49 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f5e8f5cbad19275da76f517a0a7ef0ec7f0e54ad76035a18c00fd4a37134c`  
		Last Modified: Wed, 30 Mar 2022 10:52:47 GMT  
		Size: 6.0 MB (6043641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0779c52e66bf4a49e1fe70a0882b6f3d14d1416145a03b89332f18baabc8e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 1.5 MB (1509286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bee7e95e7677193b00f56a750d6362cc0f2076daac532b0f932b19bf1518e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 295.6 KB (295648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54285c6aef4afa86d38a12cd2da3259c66f04a426ce7565f44407391e624a12a`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57879a9c4ffc05dabe1871b51ede9836db31b04ede125d89443e49e5cda0c9`  
		Last Modified: Wed, 30 Mar 2022 10:52:48 GMT  
		Size: 50.0 MB (50029239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6cd7b2f21c43f6964cca89efbc25e47a664495439380cfa6893fa22f55de93`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d472bb6e5961d60b48ba0d00a55475445b0ac511e884daa55db57a536e99a`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a27af1791dc6b357b1d5c107f38d595649b0820b031f8771c16e48d54382a3`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2c1d4e6f6c55894d6e3ce5ff51e6555cd0b856ade14a766c4b7bb7e4f8277`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:df9862fdb9057e6fe1efbba3c1035524de717ae0e40860096b76ad804788ae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:8ee4e9e4ca3cfbaf5daaa04a4a16afe5fdb11f09aa41dc608e9bd0e05714a13e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7114097399f946884e7241747ddae4059f78348becca61923ea391269f5ed0c6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:42:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 29 Mar 2022 17:42:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 29 Mar 2022 17:42:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 29 Mar 2022 17:43:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 29 Mar 2022 17:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:43:06 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 29 Mar 2022 17:43:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 29 Mar 2022 17:43:19 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 29 Mar 2022 17:43:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 29 Mar 2022 17:43:20 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 29 Mar 2022 17:43:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 29 Mar 2022 17:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 29 Mar 2022 17:43:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 29 Mar 2022 17:43:20 GMT
EXPOSE 4369 5984 9100
# Tue, 29 Mar 2022 17:43:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c696c3a7bd6345ad3dec2ca659258cc837ee8571eccb157d64903e720345f01f`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985564977890f4d120ec2e33e06bde120102045d55b49561f7bf84a56d7754e`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 5.2 MB (5223719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af07aee7e25c153d2ef231f90acc4dfa3a720f79bde9ccfe2cfb99d9584ab14c`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 1.6 MB (1553279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2f92deea0074a11b57afd14540d1b94e65fefc1b3062c355cea2027bcd3f56`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 295.6 KB (295557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e864d22b442a1e3bd13c38e716e30fd74dd0174ee568cea450b2f327620aa8`  
		Last Modified: Tue, 29 Mar 2022 17:44:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8770a376654cc5b074075f3966059d8d345cec01e26e3e2d01168b30c4dc7b`  
		Last Modified: Tue, 29 Mar 2022 17:44:45 GMT  
		Size: 49.0 MB (48992758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e89ca780ed0008db1f4194631474ea761c40582871f70e83a4ceefedc60d10`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3787af7df9836507827f5d3c0898ed7b3634c14d618b1ef33661101e3c2f651a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63db53b08f10548afad6f3264cd087f3cf504ffb8c5b9c815093abdef55a227a`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3858cce7020b361c512d44b74800e576f4165209a6119c81d47e7371187cbc6`  
		Last Modified: Tue, 29 Mar 2022 17:44:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:246537cdbbaac98b9afbc9367c7ce8b8d1491ef96ea0f07c03852443dd11c3e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85382083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc83543249a5d2861765bd92cafa0b84e9a0f40fa1e86bbaafa4359181495b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:26:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 08:26:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 08:26:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 08:26:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 08:26:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:26:54 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 08:26:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 08:27:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 08:27:12 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 08:27:13 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 08:27:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 08:27:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 08:27:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 08:27:16 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 08:27:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 08:27:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8c8acb0d3f459f4a82531d2da282c651c8205dd7b6bd0617e5e9004a41bebc`  
		Last Modified: Wed, 30 Mar 2022 08:29:27 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be11bd6efb04bece693da92602fbe034b7d40555a74f8d1edae0f37c7cdb4a`  
		Last Modified: Wed, 30 Mar 2022 08:29:26 GMT  
		Size: 5.0 MB (5003011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cf8ef1765d69e3490c938cb65494fd1af30b179862575d93bae50194a7ca9`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 1.2 MB (1221079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1645640211e15f616708007ae13071ca927c0640e44703d85f71be0f349c61`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 79.2 KB (79207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ad0867dd44f11c972190d269051120e31e7589afa36984831c1432ed063e7`  
		Last Modified: Wed, 30 Mar 2022 08:29:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d963f005819a7af1244e8553dbbae5d9f1a0215d9cf654bd50ea71d1596e43`  
		Last Modified: Wed, 30 Mar 2022 08:29:28 GMT  
		Size: 49.0 MB (49007420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c23ac21cb8331594e767265c53dec6017caf5611b24e31aae2aea5b241e3546`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befd8e51c736ae943f5c95f37ba1c31036b72af83b64b01f91b286f6020be10b`  
		Last Modified: Wed, 30 Mar 2022 08:29:22 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804d96f21b6f0b22381d16648e7af1978742821728e1943c0e2c8951a0ccd8fe`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a6f3d37897cfaa7e241172d0b6971beeae609d47d9eaf7725ed1d5334b047`  
		Last Modified: Wed, 30 Mar 2022 08:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a0ec772898e7b98ab726da9bbf9e2a8067686b33407d545eb345b3cce3afc553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93167466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958978428a8edc826010f4eb4f833438a7e7c7417d4228fa95f577ed5102c636`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 10:49:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 30 Mar 2022 10:49:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 30 Mar 2022 10:50:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:50:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 30 Mar 2022 10:50:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 30 Mar 2022 10:51:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 10:51:11 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 30 Mar 2022 10:51:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 30 Mar 2022 10:51:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 30 Mar 2022 10:51:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 30 Mar 2022 10:51:58 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 30 Mar 2022 10:52:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 30 Mar 2022 10:52:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 30 Mar 2022 10:52:08 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 30 Mar 2022 10:52:13 GMT
VOLUME [/opt/couchdb/data]
# Wed, 30 Mar 2022 10:52:17 GMT
EXPOSE 4369 5984 9100
# Wed, 30 Mar 2022 10:52:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e95f94117dc731d116e8d312bc23f0c7c790e38bd6ab7f727ec457b553c993`  
		Last Modified: Wed, 30 Mar 2022 10:52:49 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02f5e8f5cbad19275da76f517a0a7ef0ec7f0e54ad76035a18c00fd4a37134c`  
		Last Modified: Wed, 30 Mar 2022 10:52:47 GMT  
		Size: 6.0 MB (6043641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0779c52e66bf4a49e1fe70a0882b6f3d14d1416145a03b89332f18baabc8e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 1.5 MB (1509286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bee7e95e7677193b00f56a750d6362cc0f2076daac532b0f932b19bf1518e`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 295.6 KB (295648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54285c6aef4afa86d38a12cd2da3259c66f04a426ce7565f44407391e624a12a`  
		Last Modified: Wed, 30 Mar 2022 10:52:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb57879a9c4ffc05dabe1871b51ede9836db31b04ede125d89443e49e5cda0c9`  
		Last Modified: Wed, 30 Mar 2022 10:52:48 GMT  
		Size: 50.0 MB (50029239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6cd7b2f21c43f6964cca89efbc25e47a664495439380cfa6893fa22f55de93`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5d472bb6e5961d60b48ba0d00a55475445b0ac511e884daa55db57a536e99a`  
		Last Modified: Wed, 30 Mar 2022 10:52:40 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a27af1791dc6b357b1d5c107f38d595649b0820b031f8771c16e48d54382a3`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2c1d4e6f6c55894d6e3ce5ff51e6555cd0b856ade14a766c4b7bb7e4f8277`  
		Last Modified: Wed, 30 Mar 2022 10:52:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
