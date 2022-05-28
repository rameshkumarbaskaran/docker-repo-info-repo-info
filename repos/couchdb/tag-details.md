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
$ docker pull couchdb@sha256:021ac2bcbae22ff592edf98cb312df8ed73d5798b2468d13feb397f64716ea38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:0c99347ca1ba7255eaec69094a628c730b5cfad026d30db8badc491919866e9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f27ef0f67785c407d16791d641a832a1c6e4009c26844aec01de8ec6eb7397`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:57:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:57:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:57:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:57:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:57:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:57:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:58:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:58:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:58:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:58:15 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:58:15 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:58:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f99a339ac8aac6cb6417cd305c3676a442ab53f101ae8641436d886dd7c13`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9aa96f4bf4c28d4a7e8c3c18ab5e6fcce5d286935c1f1721e167ea62b9320f`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2aaefc047070930f04669cb4781cfa65a7ec4cfd3614c89c9f4472612d52c8`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 1.3 MB (1258365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4421e37c5db830dfb2c82272133505440a32ccb74ee0da6b8d86972ac8b7a`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 293.0 KB (293021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9f8ae9f14dffdf4dd64a4af8a11373c9eb83e9f532f60676ab7ffed0485f31`  
		Last Modified: Sat, 28 May 2022 02:59:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fe968a9e396daa666b25f10a022a4a39485c6dd58dfff8de75566036c9c9f7`  
		Last Modified: Sat, 28 May 2022 02:59:14 GMT  
		Size: 49.1 MB (49127742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ca210449591c75f4a75473eb909c2919be3399f288ef3ff9cc5aa4ebcdf10`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca0ea754b916151707858ac4a8e2c3bae394670c8e76e6ae60a624b1e8da83`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09916d486f044b65a746ce7e0a377a0e3c9f424c71cc7ca7e64ebd821bcf1710`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bd915effe1aa6274a27fb5fdfff8517fdeabd79edbee1778c2f8d1f7e62c53`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:021ac2bcbae22ff592edf98cb312df8ed73d5798b2468d13feb397f64716ea38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:0c99347ca1ba7255eaec69094a628c730b5cfad026d30db8badc491919866e9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f27ef0f67785c407d16791d641a832a1c6e4009c26844aec01de8ec6eb7397`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:57:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:57:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:57:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:57:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:57:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:57:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:58:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:58:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:58:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:58:15 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:58:15 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:58:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f99a339ac8aac6cb6417cd305c3676a442ab53f101ae8641436d886dd7c13`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9aa96f4bf4c28d4a7e8c3c18ab5e6fcce5d286935c1f1721e167ea62b9320f`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2aaefc047070930f04669cb4781cfa65a7ec4cfd3614c89c9f4472612d52c8`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 1.3 MB (1258365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4421e37c5db830dfb2c82272133505440a32ccb74ee0da6b8d86972ac8b7a`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 293.0 KB (293021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9f8ae9f14dffdf4dd64a4af8a11373c9eb83e9f532f60676ab7ffed0485f31`  
		Last Modified: Sat, 28 May 2022 02:59:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fe968a9e396daa666b25f10a022a4a39485c6dd58dfff8de75566036c9c9f7`  
		Last Modified: Sat, 28 May 2022 02:59:14 GMT  
		Size: 49.1 MB (49127742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ca210449591c75f4a75473eb909c2919be3399f288ef3ff9cc5aa4ebcdf10`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca0ea754b916151707858ac4a8e2c3bae394670c8e76e6ae60a624b1e8da83`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09916d486f044b65a746ce7e0a377a0e3c9f424c71cc7ca7e64ebd821bcf1710`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bd915effe1aa6274a27fb5fdfff8517fdeabd79edbee1778c2f8d1f7e62c53`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:021ac2bcbae22ff592edf98cb312df8ed73d5798b2468d13feb397f64716ea38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:0c99347ca1ba7255eaec69094a628c730b5cfad026d30db8badc491919866e9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f27ef0f67785c407d16791d641a832a1c6e4009c26844aec01de8ec6eb7397`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:57:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:57:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:57:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:57:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:57:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:55 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:57:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:58:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:58:14 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:58:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:58:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:58:15 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:58:15 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:58:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f99a339ac8aac6cb6417cd305c3676a442ab53f101ae8641436d886dd7c13`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9aa96f4bf4c28d4a7e8c3c18ab5e6fcce5d286935c1f1721e167ea62b9320f`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2aaefc047070930f04669cb4781cfa65a7ec4cfd3614c89c9f4472612d52c8`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 1.3 MB (1258365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4421e37c5db830dfb2c82272133505440a32ccb74ee0da6b8d86972ac8b7a`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 293.0 KB (293021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9f8ae9f14dffdf4dd64a4af8a11373c9eb83e9f532f60676ab7ffed0485f31`  
		Last Modified: Sat, 28 May 2022 02:59:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fe968a9e396daa666b25f10a022a4a39485c6dd58dfff8de75566036c9c9f7`  
		Last Modified: Sat, 28 May 2022 02:59:14 GMT  
		Size: 49.1 MB (49127742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ca210449591c75f4a75473eb909c2919be3399f288ef3ff9cc5aa4ebcdf10`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca0ea754b916151707858ac4a8e2c3bae394670c8e76e6ae60a624b1e8da83`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09916d486f044b65a746ce7e0a377a0e3c9f424c71cc7ca7e64ebd821bcf1710`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bd915effe1aa6274a27fb5fdfff8517fdeabd79edbee1778c2f8d1f7e62c53`  
		Last Modified: Sat, 28 May 2022 02:59:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:04da7034c2d938d1359d1d119fecd0585094fe541c830db2f981b68e760f50d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72532212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beabb9121b8b32406b286c1228b74aeb48a9e5d1c8977f3497fdb3c106890c8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:38 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Sat, 28 May 2022 02:11:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:54 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:56 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Sat, 28 May 2022 02:11:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:58 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:59 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:12:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c92a64d57c7ff3c2606f7b9944afa6a20f3075589a35b5b3abfa2a192c70e`  
		Last Modified: Sat, 28 May 2022 02:13:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87df0f0db5e9ffaf7f8c019cce783c94ab9e64dcd32eda09be56e7698b68e055`  
		Last Modified: Sat, 28 May 2022 02:13:12 GMT  
		Size: 39.0 MB (39023420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d0578cd28a91cb154e00cd03fd7217372e288d9cc0f86e8180f1b16a6980a`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1ec7cc039a84d291862bfa8bc4adb2debfbb048e828e73e5f441466ce3dd5d`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e1b514fa109f16f2af17c44ce0b0d0a08b60e4434789b992e857c21458a40`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a2a0b44558153945d91cd4dcefc8cac563fd23e45a0ae4dbd9de8edc47de6`  
		Last Modified: Sat, 28 May 2022 02:13:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:2559521ee6212bf582315ee829cefd5ea618dc0e7c01adb5d928a3f61f5ddde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:827e134ca8e56281f2a37786c609d828231fba860dbc1ed2b01a12010ff7d785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:fe94297a30a48b6488c51e5bbfc92b7a31291a6159ecf5eb04ce369a3379025e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80008811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd18b7d81e078b147e51545b93e09639c0caaf95d76d6e9a8eec801b77c84ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:57:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:57:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:57:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:57:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:57:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:34 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:57:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:57:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:57:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:57:48 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:57:48 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:57:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:57:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:57:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:57:49 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:57:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f99a339ac8aac6cb6417cd305c3676a442ab53f101ae8641436d886dd7c13`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9aa96f4bf4c28d4a7e8c3c18ab5e6fcce5d286935c1f1721e167ea62b9320f`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2aaefc047070930f04669cb4781cfa65a7ec4cfd3614c89c9f4472612d52c8`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 1.3 MB (1258365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4421e37c5db830dfb2c82272133505440a32ccb74ee0da6b8d86972ac8b7a`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 293.0 KB (293021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5017314c79e922fcbdec562e0abcb1cd051afa07031a5ef8a578eda82a928fc2`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a6ab0d9ad7e19c4207485529c39d63a838a7e1daf16af1ee57ef76643d9f6`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 44.6 MB (44611628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eeee3e9f5d758ff8ec7528d8b56d1593d837112538b93b6ebf580edeffc30d7`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1476cb88988f62fe840c0675b1e35915ebd4d1074c9d871499533e0823d2c232`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30e442424da2cfa40c288b6f249e96983fbca8c0e716b4a7a788ede64fd2b0`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de78e5175b7672bae6f05f2204495067b0ecfa0a8739ec254de677c5cda3f525`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:847e2c962236313df65996d351b8e3931b4ae8719bcb96398079f15e3765e6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc584cf6b2bf00f347d30a3ffec6b181f9a5faba80b39eb639df5eb1da2136`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:03 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:11:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:26 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:11:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:29 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:11:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539d7e341cbcd00982b2f11dc0397ecd3486187357afe47e566e43399a1673d`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2524916e993a60f307cc1b61f1da428e13143afdd839e96665727d8ace3d44`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 41.1 MB (41112565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee69a3a77f17bda355f100fa3c2133c87760f680ae0b228cfbd6d0d2b50f3e5`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2cd60ccdcd13ab0550a20f9d1271e32a1f7a012ec851ae3efe7113693a8c73`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfea82c5bcc6c9add963ff1fef209ce5628576752fe80f9eacd7319ee56a140`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a37410d58b1e6329af6294978dd6d13f946f8950e6cfcaee1127826a8b462`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:827e134ca8e56281f2a37786c609d828231fba860dbc1ed2b01a12010ff7d785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:fe94297a30a48b6488c51e5bbfc92b7a31291a6159ecf5eb04ce369a3379025e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80008811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd18b7d81e078b147e51545b93e09639c0caaf95d76d6e9a8eec801b77c84ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:57:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:57:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:57:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:57:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:57:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:57:34 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:57:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:57:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:57:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:57:48 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:57:48 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:57:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:57:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:57:49 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:57:49 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:57:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f99a339ac8aac6cb6417cd305c3676a442ab53f101ae8641436d886dd7c13`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9aa96f4bf4c28d4a7e8c3c18ab5e6fcce5d286935c1f1721e167ea62b9320f`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2aaefc047070930f04669cb4781cfa65a7ec4cfd3614c89c9f4472612d52c8`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 1.3 MB (1258365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d4421e37c5db830dfb2c82272133505440a32ccb74ee0da6b8d86972ac8b7a`  
		Last Modified: Sat, 28 May 2022 02:58:55 GMT  
		Size: 293.0 KB (293021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5017314c79e922fcbdec562e0abcb1cd051afa07031a5ef8a578eda82a928fc2`  
		Last Modified: Sat, 28 May 2022 02:58:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a6ab0d9ad7e19c4207485529c39d63a838a7e1daf16af1ee57ef76643d9f6`  
		Last Modified: Sat, 28 May 2022 02:58:58 GMT  
		Size: 44.6 MB (44611628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eeee3e9f5d758ff8ec7528d8b56d1593d837112538b93b6ebf580edeffc30d7`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1476cb88988f62fe840c0675b1e35915ebd4d1074c9d871499533e0823d2c232`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30e442424da2cfa40c288b6f249e96983fbca8c0e716b4a7a788ede64fd2b0`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de78e5175b7672bae6f05f2204495067b0ecfa0a8739ec254de677c5cda3f525`  
		Last Modified: Sat, 28 May 2022 02:58:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:847e2c962236313df65996d351b8e3931b4ae8719bcb96398079f15e3765e6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc584cf6b2bf00f347d30a3ffec6b181f9a5faba80b39eb639df5eb1da2136`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:10:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 02:10:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 02:10:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:10:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 02:10:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 02:11:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:11:03 GMT
ENV COUCHDB_VERSION=3.1.2
# Sat, 28 May 2022 02:11:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 02:11:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 02:11:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 02:11:25 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 02:11:26 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Sat, 28 May 2022 02:11:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 02:11:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 02:11:28 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 02:11:29 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 02:11:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df87715dbbc0f7e9fa4464ebf57262fda4e050c820a30b343e73a1f4b5ddd809`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5910279a024018bff17c24cc89641da2954a3729de66031786a65c1c6f3e48`  
		Last Modified: Sat, 28 May 2022 02:12:54 GMT  
		Size: 6.6 MB (6556694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f084ee6afeab9340278b262b3fa9696bc76445c96dd5894e9084040bdfda17`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 951.2 KB (951185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43024313a99504411fbb816f5b182c78bfc4ddefe215ead2b9e70dde7f212db1`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6539d7e341cbcd00982b2f11dc0397ecd3486187357afe47e566e43399a1673d`  
		Last Modified: Sat, 28 May 2022 02:12:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2524916e993a60f307cc1b61f1da428e13143afdd839e96665727d8ace3d44`  
		Last Modified: Sat, 28 May 2022 02:12:55 GMT  
		Size: 41.1 MB (41112565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee69a3a77f17bda355f100fa3c2133c87760f680ae0b228cfbd6d0d2b50f3e5`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2cd60ccdcd13ab0550a20f9d1271e32a1f7a012ec851ae3efe7113693a8c73`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfea82c5bcc6c9add963ff1fef209ce5628576752fe80f9eacd7319ee56a140`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a37410d58b1e6329af6294978dd6d13f946f8950e6cfcaee1127826a8b462`  
		Last Modified: Sat, 28 May 2022 02:12:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:2559521ee6212bf582315ee829cefd5ea618dc0e7c01adb5d928a3f61f5ddde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

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

### `couchdb:3.2` - linux; arm64 variant v8

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

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:2559521ee6212bf582315ee829cefd5ea618dc0e7c01adb5d928a3f61f5ddde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

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

### `couchdb:3.2.2` - linux; arm64 variant v8

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

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2559521ee6212bf582315ee829cefd5ea618dc0e7c01adb5d928a3f61f5ddde2
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
$ docker pull couchdb@sha256:f95e2cea87b96ad9d1f58b2f7a1cc297fafa4a0ba2ac8264ac49d1638308fc9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93222784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b27bcbda415fb7a19f938be7247b5b8374059229cdc9cd529fb5307a210896`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:40:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sat, 28 May 2022 03:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sat, 28 May 2022 03:41:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:41:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Sat, 28 May 2022 03:41:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Sat, 28 May 2022 03:42:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:42:07 GMT
ENV COUCHDB_VERSION=3.2.2
# Sat, 28 May 2022 03:42:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Sat, 28 May 2022 03:42:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Sat, 28 May 2022 03:42:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Sat, 28 May 2022 03:42:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sat, 28 May 2022 03:43:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Sat, 28 May 2022 03:43:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sat, 28 May 2022 03:43:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sat, 28 May 2022 03:43:12 GMT
VOLUME [/opt/couchdb/data]
# Sat, 28 May 2022 03:43:14 GMT
EXPOSE 4369 5984 9100
# Sat, 28 May 2022 03:43:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875b56da848a25def16ef02568eeffc6bbc68f8a2468a40da18f7804d2dd4dc9`  
		Last Modified: Sat, 28 May 2022 03:43:47 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e008e7e9f9a18c5718a2d3de1662a1db954494a646fdf8ba6d823e164163`  
		Last Modified: Sat, 28 May 2022 03:43:46 GMT  
		Size: 6.0 MB (6043917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459503824efb70b765dc12230fae1a2e7f1d57ba12e7e9167fb178b49e2d7eb`  
		Last Modified: Sat, 28 May 2022 03:43:45 GMT  
		Size: 1.5 MB (1509317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc78eafedf794548c6bb2337ef3e6c836e38b32b8614595cba142a46bf2e9dd7`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c9e549e3260acc9bf35d347a6d917255de993dd25ed0b87d3e42a07e7db8`  
		Last Modified: Sat, 28 May 2022 03:43:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195ecb14f19305eece3c42f9ca34a34d6b56c3068466d8bb2bbd3e718b6946e`  
		Last Modified: Sat, 28 May 2022 03:43:52 GMT  
		Size: 50.1 MB (50080003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfd3f63efba486fe137f4f549db8e61c85af415f596ed332b7c0c8b59ee455`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986d6fa4c295a869df86de585d8914fe5b1a862f8bd8b6e7eb7b271f8095833`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa73f76a3e72dfaf15f902a8ab24390ed60ac0c9ee076c28ea9e6b81e55ce9a`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e53af1ea2a6650916769ea2f4ba0611b52a7bc36e0e0c1d740aeb583a7add7`  
		Last Modified: Sat, 28 May 2022 03:43:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
