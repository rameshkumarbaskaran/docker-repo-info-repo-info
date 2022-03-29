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
$ docker pull couchdb@sha256:003fdf630048eaa4593c867a167196335ffa1a2c4992a3337ce6b2889d5b72a2
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
$ docker pull couchdb@sha256:f7782f0c69bbe422003ba7c1dbc73782a2d32914999b486e2d003e45a95a1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fa683028f2fd62756b6794cd4db265f2d8a52bfb3b6ab4e3ee89eda9e9cd4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:31:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:31:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:31:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:32:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 17 Mar 2022 22:32:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:32:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:32:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:32:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:32:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 17 Mar 2022 22:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:32:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:32:31 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:32:32 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:32:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887cc6c156d9504a3fab3c1e6f6f61acedf4a74ff809ddd7f6e5e31e62ff4c6`  
		Last Modified: Thu, 17 Mar 2022 22:33:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886f3ae8cff4ce1b5e40be022905cf2809cdc74d4da4aa078c17a4872bcb68`  
		Last Modified: Thu, 17 Mar 2022 22:33:27 GMT  
		Size: 6.5 MB (6549944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42734001f002f138c343e94afbbd6b64994909feeabb109a6c739d3a95689587`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 951.2 KB (951162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2c9dade4cade80d2db50f78809407262ea3859b71ce68024bccafbaa1df2d7`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f3f8a1d6397ae2202d318ef14845173621f398e4279662f0c07d3de9708883`  
		Last Modified: Thu, 17 Mar 2022 22:33:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf455aa3931c03c25e1a8017136e8a19255e90846da1331a68fa90010d5443d3`  
		Last Modified: Thu, 17 Mar 2022 22:33:45 GMT  
		Size: 39.0 MB (39011782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7a088073517be84b563019bc533aec43e48dcfdf67882d7a40bc0e5ea7846`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d3748afd0b8f0cc317b9a92258cf6f1fddae508c1130762455ffd45ba394d`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd78fe5644364d61d11c2072ff58a37f08961b45c3cc4b979ec9dbdf9d07444`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9921aaa00af9d01f255a10f5dd74acba3715d18a69952256741337e1fd06aed4`  
		Last Modified: Thu, 17 Mar 2022 22:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:003fdf630048eaa4593c867a167196335ffa1a2c4992a3337ce6b2889d5b72a2
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
$ docker pull couchdb@sha256:f7782f0c69bbe422003ba7c1dbc73782a2d32914999b486e2d003e45a95a1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fa683028f2fd62756b6794cd4db265f2d8a52bfb3b6ab4e3ee89eda9e9cd4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:31:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:31:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:31:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:32:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 17 Mar 2022 22:32:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:32:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:32:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:32:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:32:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 17 Mar 2022 22:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:32:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:32:31 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:32:32 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:32:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887cc6c156d9504a3fab3c1e6f6f61acedf4a74ff809ddd7f6e5e31e62ff4c6`  
		Last Modified: Thu, 17 Mar 2022 22:33:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886f3ae8cff4ce1b5e40be022905cf2809cdc74d4da4aa078c17a4872bcb68`  
		Last Modified: Thu, 17 Mar 2022 22:33:27 GMT  
		Size: 6.5 MB (6549944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42734001f002f138c343e94afbbd6b64994909feeabb109a6c739d3a95689587`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 951.2 KB (951162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2c9dade4cade80d2db50f78809407262ea3859b71ce68024bccafbaa1df2d7`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f3f8a1d6397ae2202d318ef14845173621f398e4279662f0c07d3de9708883`  
		Last Modified: Thu, 17 Mar 2022 22:33:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf455aa3931c03c25e1a8017136e8a19255e90846da1331a68fa90010d5443d3`  
		Last Modified: Thu, 17 Mar 2022 22:33:45 GMT  
		Size: 39.0 MB (39011782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7a088073517be84b563019bc533aec43e48dcfdf67882d7a40bc0e5ea7846`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d3748afd0b8f0cc317b9a92258cf6f1fddae508c1130762455ffd45ba394d`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd78fe5644364d61d11c2072ff58a37f08961b45c3cc4b979ec9dbdf9d07444`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9921aaa00af9d01f255a10f5dd74acba3715d18a69952256741337e1fd06aed4`  
		Last Modified: Thu, 17 Mar 2022 22:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:003fdf630048eaa4593c867a167196335ffa1a2c4992a3337ce6b2889d5b72a2
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
$ docker pull couchdb@sha256:f7782f0c69bbe422003ba7c1dbc73782a2d32914999b486e2d003e45a95a1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fa683028f2fd62756b6794cd4db265f2d8a52bfb3b6ab4e3ee89eda9e9cd4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:31:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:31:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:31:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:32:11 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 17 Mar 2022 22:32:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:32:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:32:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:32:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:32:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 17 Mar 2022 22:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:32:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:32:31 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:32:32 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:32:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887cc6c156d9504a3fab3c1e6f6f61acedf4a74ff809ddd7f6e5e31e62ff4c6`  
		Last Modified: Thu, 17 Mar 2022 22:33:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886f3ae8cff4ce1b5e40be022905cf2809cdc74d4da4aa078c17a4872bcb68`  
		Last Modified: Thu, 17 Mar 2022 22:33:27 GMT  
		Size: 6.5 MB (6549944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42734001f002f138c343e94afbbd6b64994909feeabb109a6c739d3a95689587`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 951.2 KB (951162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2c9dade4cade80d2db50f78809407262ea3859b71ce68024bccafbaa1df2d7`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f3f8a1d6397ae2202d318ef14845173621f398e4279662f0c07d3de9708883`  
		Last Modified: Thu, 17 Mar 2022 22:33:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf455aa3931c03c25e1a8017136e8a19255e90846da1331a68fa90010d5443d3`  
		Last Modified: Thu, 17 Mar 2022 22:33:45 GMT  
		Size: 39.0 MB (39011782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7a088073517be84b563019bc533aec43e48dcfdf67882d7a40bc0e5ea7846`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d3748afd0b8f0cc317b9a92258cf6f1fddae508c1130762455ffd45ba394d`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd78fe5644364d61d11c2072ff58a37f08961b45c3cc4b979ec9dbdf9d07444`  
		Last Modified: Thu, 17 Mar 2022 22:33:40 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9921aaa00af9d01f255a10f5dd74acba3715d18a69952256741337e1fd06aed4`  
		Last Modified: Thu, 17 Mar 2022 22:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:e144f6cacb8961553c451a818f96beaeae933409aad54669ad6f00ce3324e5cf
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
$ docker pull couchdb@sha256:6e010670eae53479df647a5c7b2a01787973daa2ad17e2819f1e0360f7595d86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85380732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c9d2fa92ddd374345736ad6952edefdc4f1c4618133a0971c54c2a5810f8f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:30:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:46 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Thu, 17 Mar 2022 22:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:31:07 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:31:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:31:09 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 17 Mar 2022 22:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:31:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:31:11 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:31:12 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:31:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bdc1ef33f41e5b433a054cfeb4f58824e23daa2280fc358a3f7d37e5a4ec6b`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e73842eb2096f6a939df87f81d50ed488f6482ac93ac802a11e9f1e7fddef`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 5.0 MB (5003239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f271b4525187bb9def07fb572e35c783dd74adb1ee326f037012bffa5184f01`  
		Last Modified: Thu, 17 Mar 2022 22:33:03 GMT  
		Size: 1.2 MB (1220965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266835bf73deb3949f8112affd5434b42d3469b7f80fcab70c01e8502d1a3ed`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 79.1 KB (79120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71f197767de0c49aef4a53207c0a14587e35d1d97b3a7d9303cc5b16b61853`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d2e47e652d62fc7525bc47df98490dd98a435939dc5acab4676d98b3e800c`  
		Last Modified: Thu, 17 Mar 2022 22:33:06 GMT  
		Size: 49.0 MB (49007350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f465be74785f932a4ca40faeaa67a39e9f43971e409b9ecaf1d171c4fcead`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d65e9095a0e0dc3fa53accf60ff473a75d93788d5fb7080064993ecc6bc89`  
		Last Modified: Thu, 17 Mar 2022 22:33:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad36673b8a4026d3b7dde812d25546dc824b6d9b8d1c0eff91661092333164e`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935d288ca6a4e300d466d4b4d5f55bbe702bbd5ea7ad103eab8eab4ce700a5b`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca68de537cdbc68e18d92202e84cc547208cd8ac567616a668f2590b384f27f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93165888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472ccde809ca6b9a7f0350ad37f7a2f56483b6c2de4ceca98f8250a82c1dfd4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:59:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 19 Mar 2022 06:59:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 19 Mar 2022 07:00:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:00:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 19 Mar 2022 07:00:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 19 Mar 2022 07:01:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:01:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Sat, 19 Mar 2022 07:01:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 19 Mar 2022 07:02:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 19 Mar 2022 07:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 19 Mar 2022 07:02:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 19 Mar 2022 07:02:36 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 19 Mar 2022 07:02:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 19 Mar 2022 07:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 07:02:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 19 Mar 2022 07:02:56 GMT
EXPOSE 4369 5984 9100
# Sat, 19 Mar 2022 07:02:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd2b081b61cc8489dc9e99a0f485c440dacf9213c46c4962457fc78012d146`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e669e5a4472565c7733b7533fe008958ac628907d7d8f9284c47072cd7ac57cd`  
		Last Modified: Sat, 19 Mar 2022 07:03:27 GMT  
		Size: 6.0 MB (6043562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933408dd42d99ff8c075e020385dc263b54cec8ac89af1542ff9c814081b20e5`  
		Last Modified: Sat, 19 Mar 2022 07:03:26 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253c13d304adca68813bdc23125033baaadf4e82117653968dd309fb74cf5e0`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9cafde52d8bf05b62177527baa89b7c4b2ae1cc2763fde3bbd8d13fac2311`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b326d8353ce3da64cd9163ff80a82cabb9b3126cc938deef6f22f34f31d0a2`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 50.0 MB (50030562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77818fd3128329f534255e4130cf342d7d52e86da1f2f9927c7c056f97cf16d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006892ec108409b248607cb3ef901216879862343748396ebf3b022494a5100d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 771.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36c0ced99658412fb3b908447b64fb7d9ea394b957df185462f7dc9de1c358`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 2.2 KB (2190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b9284f0a34d1da004805e76965d24e9c6289afa861788768b9dac2519bcff`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:9d70f7b2ae39ae6f3a93af37bb95c9f4a81590253d6484370f9bfaa6585e372f
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
$ docker pull couchdb@sha256:5c094bcf7aa6c12c5f2ffd6eee06b6051ec76e2a84d3b8d636686a792a61f328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74611754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14524a3b80b14d7459d5d3592d255262b70fd34b4c192dc25d95d7968f5bd1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:31:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:31:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:31:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:40 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 17 Mar 2022 22:31:41 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:32:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:32:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:32:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 17 Mar 2022 22:32:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:32:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:32:04 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:32:05 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:32:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887cc6c156d9504a3fab3c1e6f6f61acedf4a74ff809ddd7f6e5e31e62ff4c6`  
		Last Modified: Thu, 17 Mar 2022 22:33:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886f3ae8cff4ce1b5e40be022905cf2809cdc74d4da4aa078c17a4872bcb68`  
		Last Modified: Thu, 17 Mar 2022 22:33:27 GMT  
		Size: 6.5 MB (6549944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42734001f002f138c343e94afbbd6b64994909feeabb109a6c739d3a95689587`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 951.2 KB (951162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2c9dade4cade80d2db50f78809407262ea3859b71ce68024bccafbaa1df2d7`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcd7ee79efb58e743882e96a4001e23b61d351ad860a3d7275abb40fd56af80`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dbbff3180a3b3ee2f37493ac71d6070db31ce8495be900b0ccb65952b26a25`  
		Last Modified: Thu, 17 Mar 2022 22:33:29 GMT  
		Size: 41.1 MB (41100600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4389572f277ee9a986cd1bf6fc06fbdceab76e62bb2bf4db6896fe5d4f914419`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7142434f4c4946e716530f4582cef022d409f96da9299fe339f0f4eced782cd`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e18e88a7010c7b4aa7f681913fc6a580a26fd2ecf40445273304fecef87cf45`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577df19c1b6bde5ff6dc7a6dd7e2e6f7542dd96ea6b315f0ff38688ae53dfbb3`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:9d70f7b2ae39ae6f3a93af37bb95c9f4a81590253d6484370f9bfaa6585e372f
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
$ docker pull couchdb@sha256:5c094bcf7aa6c12c5f2ffd6eee06b6051ec76e2a84d3b8d636686a792a61f328
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74611754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14524a3b80b14d7459d5d3592d255262b70fd34b4c192dc25d95d7968f5bd1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:31:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:31:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:31:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:31:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:31:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:31:40 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 17 Mar 2022 22:31:41 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:32:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:32:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:32:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 17 Mar 2022 22:32:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:32:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:32:04 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:32:05 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:32:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a887cc6c156d9504a3fab3c1e6f6f61acedf4a74ff809ddd7f6e5e31e62ff4c6`  
		Last Modified: Thu, 17 Mar 2022 22:33:28 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32886f3ae8cff4ce1b5e40be022905cf2809cdc74d4da4aa078c17a4872bcb68`  
		Last Modified: Thu, 17 Mar 2022 22:33:27 GMT  
		Size: 6.5 MB (6549944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42734001f002f138c343e94afbbd6b64994909feeabb109a6c739d3a95689587`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 951.2 KB (951162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2c9dade4cade80d2db50f78809407262ea3859b71ce68024bccafbaa1df2d7`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 79.9 KB (79896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcd7ee79efb58e743882e96a4001e23b61d351ad860a3d7275abb40fd56af80`  
		Last Modified: Thu, 17 Mar 2022 22:33:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dbbff3180a3b3ee2f37493ac71d6070db31ce8495be900b0ccb65952b26a25`  
		Last Modified: Thu, 17 Mar 2022 22:33:29 GMT  
		Size: 41.1 MB (41100600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4389572f277ee9a986cd1bf6fc06fbdceab76e62bb2bf4db6896fe5d4f914419`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7142434f4c4946e716530f4582cef022d409f96da9299fe339f0f4eced782cd`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e18e88a7010c7b4aa7f681913fc6a580a26fd2ecf40445273304fecef87cf45`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577df19c1b6bde5ff6dc7a6dd7e2e6f7542dd96ea6b315f0ff38688ae53dfbb3`  
		Last Modified: Thu, 17 Mar 2022 22:33:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:e144f6cacb8961553c451a818f96beaeae933409aad54669ad6f00ce3324e5cf
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
$ docker pull couchdb@sha256:6e010670eae53479df647a5c7b2a01787973daa2ad17e2819f1e0360f7595d86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85380732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c9d2fa92ddd374345736ad6952edefdc4f1c4618133a0971c54c2a5810f8f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:30:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:46 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Thu, 17 Mar 2022 22:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:31:07 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:31:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:31:09 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 17 Mar 2022 22:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:31:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:31:11 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:31:12 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:31:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bdc1ef33f41e5b433a054cfeb4f58824e23daa2280fc358a3f7d37e5a4ec6b`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e73842eb2096f6a939df87f81d50ed488f6482ac93ac802a11e9f1e7fddef`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 5.0 MB (5003239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f271b4525187bb9def07fb572e35c783dd74adb1ee326f037012bffa5184f01`  
		Last Modified: Thu, 17 Mar 2022 22:33:03 GMT  
		Size: 1.2 MB (1220965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266835bf73deb3949f8112affd5434b42d3469b7f80fcab70c01e8502d1a3ed`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 79.1 KB (79120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71f197767de0c49aef4a53207c0a14587e35d1d97b3a7d9303cc5b16b61853`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d2e47e652d62fc7525bc47df98490dd98a435939dc5acab4676d98b3e800c`  
		Last Modified: Thu, 17 Mar 2022 22:33:06 GMT  
		Size: 49.0 MB (49007350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f465be74785f932a4ca40faeaa67a39e9f43971e409b9ecaf1d171c4fcead`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d65e9095a0e0dc3fa53accf60ff473a75d93788d5fb7080064993ecc6bc89`  
		Last Modified: Thu, 17 Mar 2022 22:33:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad36673b8a4026d3b7dde812d25546dc824b6d9b8d1c0eff91661092333164e`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935d288ca6a4e300d466d4b4d5f55bbe702bbd5ea7ad103eab8eab4ce700a5b`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca68de537cdbc68e18d92202e84cc547208cd8ac567616a668f2590b384f27f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93165888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472ccde809ca6b9a7f0350ad37f7a2f56483b6c2de4ceca98f8250a82c1dfd4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:59:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 19 Mar 2022 06:59:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 19 Mar 2022 07:00:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:00:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 19 Mar 2022 07:00:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 19 Mar 2022 07:01:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:01:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Sat, 19 Mar 2022 07:01:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 19 Mar 2022 07:02:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 19 Mar 2022 07:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 19 Mar 2022 07:02:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 19 Mar 2022 07:02:36 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 19 Mar 2022 07:02:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 19 Mar 2022 07:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 07:02:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 19 Mar 2022 07:02:56 GMT
EXPOSE 4369 5984 9100
# Sat, 19 Mar 2022 07:02:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd2b081b61cc8489dc9e99a0f485c440dacf9213c46c4962457fc78012d146`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e669e5a4472565c7733b7533fe008958ac628907d7d8f9284c47072cd7ac57cd`  
		Last Modified: Sat, 19 Mar 2022 07:03:27 GMT  
		Size: 6.0 MB (6043562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933408dd42d99ff8c075e020385dc263b54cec8ac89af1542ff9c814081b20e5`  
		Last Modified: Sat, 19 Mar 2022 07:03:26 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253c13d304adca68813bdc23125033baaadf4e82117653968dd309fb74cf5e0`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9cafde52d8bf05b62177527baa89b7c4b2ae1cc2763fde3bbd8d13fac2311`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b326d8353ce3da64cd9163ff80a82cabb9b3126cc938deef6f22f34f31d0a2`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 50.0 MB (50030562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77818fd3128329f534255e4130cf342d7d52e86da1f2f9927c7c056f97cf16d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006892ec108409b248607cb3ef901216879862343748396ebf3b022494a5100d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 771.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36c0ced99658412fb3b908447b64fb7d9ea394b957df185462f7dc9de1c358`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 2.2 KB (2190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b9284f0a34d1da004805e76965d24e9c6289afa861788768b9dac2519bcff`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:e144f6cacb8961553c451a818f96beaeae933409aad54669ad6f00ce3324e5cf
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
$ docker pull couchdb@sha256:6e010670eae53479df647a5c7b2a01787973daa2ad17e2819f1e0360f7595d86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85380732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c9d2fa92ddd374345736ad6952edefdc4f1c4618133a0971c54c2a5810f8f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:30:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:46 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Thu, 17 Mar 2022 22:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:31:07 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:31:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:31:09 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 17 Mar 2022 22:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:31:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:31:11 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:31:12 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:31:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bdc1ef33f41e5b433a054cfeb4f58824e23daa2280fc358a3f7d37e5a4ec6b`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e73842eb2096f6a939df87f81d50ed488f6482ac93ac802a11e9f1e7fddef`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 5.0 MB (5003239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f271b4525187bb9def07fb572e35c783dd74adb1ee326f037012bffa5184f01`  
		Last Modified: Thu, 17 Mar 2022 22:33:03 GMT  
		Size: 1.2 MB (1220965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266835bf73deb3949f8112affd5434b42d3469b7f80fcab70c01e8502d1a3ed`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 79.1 KB (79120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71f197767de0c49aef4a53207c0a14587e35d1d97b3a7d9303cc5b16b61853`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d2e47e652d62fc7525bc47df98490dd98a435939dc5acab4676d98b3e800c`  
		Last Modified: Thu, 17 Mar 2022 22:33:06 GMT  
		Size: 49.0 MB (49007350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f465be74785f932a4ca40faeaa67a39e9f43971e409b9ecaf1d171c4fcead`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d65e9095a0e0dc3fa53accf60ff473a75d93788d5fb7080064993ecc6bc89`  
		Last Modified: Thu, 17 Mar 2022 22:33:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad36673b8a4026d3b7dde812d25546dc824b6d9b8d1c0eff91661092333164e`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935d288ca6a4e300d466d4b4d5f55bbe702bbd5ea7ad103eab8eab4ce700a5b`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca68de537cdbc68e18d92202e84cc547208cd8ac567616a668f2590b384f27f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93165888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472ccde809ca6b9a7f0350ad37f7a2f56483b6c2de4ceca98f8250a82c1dfd4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:59:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 19 Mar 2022 06:59:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 19 Mar 2022 07:00:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:00:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 19 Mar 2022 07:00:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 19 Mar 2022 07:01:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:01:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Sat, 19 Mar 2022 07:01:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 19 Mar 2022 07:02:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 19 Mar 2022 07:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 19 Mar 2022 07:02:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 19 Mar 2022 07:02:36 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 19 Mar 2022 07:02:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 19 Mar 2022 07:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 07:02:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 19 Mar 2022 07:02:56 GMT
EXPOSE 4369 5984 9100
# Sat, 19 Mar 2022 07:02:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd2b081b61cc8489dc9e99a0f485c440dacf9213c46c4962457fc78012d146`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e669e5a4472565c7733b7533fe008958ac628907d7d8f9284c47072cd7ac57cd`  
		Last Modified: Sat, 19 Mar 2022 07:03:27 GMT  
		Size: 6.0 MB (6043562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933408dd42d99ff8c075e020385dc263b54cec8ac89af1542ff9c814081b20e5`  
		Last Modified: Sat, 19 Mar 2022 07:03:26 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253c13d304adca68813bdc23125033baaadf4e82117653968dd309fb74cf5e0`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9cafde52d8bf05b62177527baa89b7c4b2ae1cc2763fde3bbd8d13fac2311`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b326d8353ce3da64cd9163ff80a82cabb9b3126cc938deef6f22f34f31d0a2`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 50.0 MB (50030562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77818fd3128329f534255e4130cf342d7d52e86da1f2f9927c7c056f97cf16d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006892ec108409b248607cb3ef901216879862343748396ebf3b022494a5100d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 771.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36c0ced99658412fb3b908447b64fb7d9ea394b957df185462f7dc9de1c358`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 2.2 KB (2190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b9284f0a34d1da004805e76965d24e9c6289afa861788768b9dac2519bcff`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:e144f6cacb8961553c451a818f96beaeae933409aad54669ad6f00ce3324e5cf
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
$ docker pull couchdb@sha256:6e010670eae53479df647a5c7b2a01787973daa2ad17e2819f1e0360f7595d86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85380732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c9d2fa92ddd374345736ad6952edefdc4f1c4618133a0971c54c2a5810f8f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:30:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 17 Mar 2022 22:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 17 Mar 2022 22:30:34 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 17 Mar 2022 22:30:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 17 Mar 2022 22:30:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:30:46 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Thu, 17 Mar 2022 22:30:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 17 Mar 2022 22:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 17 Mar 2022 22:31:07 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 17 Mar 2022 22:31:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 17 Mar 2022 22:31:09 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 17 Mar 2022 22:31:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 17 Mar 2022 22:31:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 22:31:11 GMT
VOLUME [/opt/couchdb/data]
# Thu, 17 Mar 2022 22:31:12 GMT
EXPOSE 4369 5984 9100
# Thu, 17 Mar 2022 22:31:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bdc1ef33f41e5b433a054cfeb4f58824e23daa2280fc358a3f7d37e5a4ec6b`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e73842eb2096f6a939df87f81d50ed488f6482ac93ac802a11e9f1e7fddef`  
		Last Modified: Thu, 17 Mar 2022 22:33:04 GMT  
		Size: 5.0 MB (5003239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f271b4525187bb9def07fb572e35c783dd74adb1ee326f037012bffa5184f01`  
		Last Modified: Thu, 17 Mar 2022 22:33:03 GMT  
		Size: 1.2 MB (1220965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266835bf73deb3949f8112affd5434b42d3469b7f80fcab70c01e8502d1a3ed`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 79.1 KB (79120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a71f197767de0c49aef4a53207c0a14587e35d1d97b3a7d9303cc5b16b61853`  
		Last Modified: Thu, 17 Mar 2022 22:33:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d2e47e652d62fc7525bc47df98490dd98a435939dc5acab4676d98b3e800c`  
		Last Modified: Thu, 17 Mar 2022 22:33:06 GMT  
		Size: 49.0 MB (49007350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f465be74785f932a4ca40faeaa67a39e9f43971e409b9ecaf1d171c4fcead`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7d65e9095a0e0dc3fa53accf60ff473a75d93788d5fb7080064993ecc6bc89`  
		Last Modified: Thu, 17 Mar 2022 22:33:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad36673b8a4026d3b7dde812d25546dc824b6d9b8d1c0eff91661092333164e`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935d288ca6a4e300d466d4b4d5f55bbe702bbd5ea7ad103eab8eab4ce700a5b`  
		Last Modified: Thu, 17 Mar 2022 22:33:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ca68de537cdbc68e18d92202e84cc547208cd8ac567616a668f2590b384f27f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93165888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472ccde809ca6b9a7f0350ad37f7a2f56483b6c2de4ceca98f8250a82c1dfd4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:59:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 19 Mar 2022 06:59:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 19 Mar 2022 07:00:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:00:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 19 Mar 2022 07:00:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 19 Mar 2022 07:01:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:01:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Sat, 19 Mar 2022 07:01:35 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 19 Mar 2022 07:02:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 19 Mar 2022 07:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 19 Mar 2022 07:02:33 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 19 Mar 2022 07:02:36 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 19 Mar 2022 07:02:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 19 Mar 2022 07:02:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 07:02:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 19 Mar 2022 07:02:56 GMT
EXPOSE 4369 5984 9100
# Sat, 19 Mar 2022 07:02:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd2b081b61cc8489dc9e99a0f485c440dacf9213c46c4962457fc78012d146`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e669e5a4472565c7733b7533fe008958ac628907d7d8f9284c47072cd7ac57cd`  
		Last Modified: Sat, 19 Mar 2022 07:03:27 GMT  
		Size: 6.0 MB (6043562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933408dd42d99ff8c075e020385dc263b54cec8ac89af1542ff9c814081b20e5`  
		Last Modified: Sat, 19 Mar 2022 07:03:26 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253c13d304adca68813bdc23125033baaadf4e82117653968dd309fb74cf5e0`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 295.6 KB (295614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9cafde52d8bf05b62177527baa89b7c4b2ae1cc2763fde3bbd8d13fac2311`  
		Last Modified: Sat, 19 Mar 2022 07:03:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b326d8353ce3da64cd9163ff80a82cabb9b3126cc938deef6f22f34f31d0a2`  
		Last Modified: Sat, 19 Mar 2022 07:03:29 GMT  
		Size: 50.0 MB (50030562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77818fd3128329f534255e4130cf342d7d52e86da1f2f9927c7c056f97cf16d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006892ec108409b248607cb3ef901216879862343748396ebf3b022494a5100d`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 771.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36c0ced99658412fb3b908447b64fb7d9ea394b957df185462f7dc9de1c358`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 2.2 KB (2190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9b9284f0a34d1da004805e76965d24e9c6289afa861788768b9dac2519bcff`  
		Last Modified: Sat, 19 Mar 2022 07:03:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
