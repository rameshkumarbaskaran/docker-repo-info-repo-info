<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.0`](#couchdb320)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:64f70fc244c2636f3c906181e2e41a5e0c39fbba507aaaa30c5e48441110726b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:d88f859b0e2d27a94bd6862849a6a0fba3d10d7b2c0aeb79b8c2c5ac2dabf651
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84502946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec8a29dd01e00c0d102328f515fe8adc9bda383e5a3db59d5d0fb3c1038879`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:33:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Oct 2021 12:33:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:33:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Oct 2021 12:33:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:33:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:33:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:33:36 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:33:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb406db451bbcfa9ec9d447c1262d9b9d20b830136f5310aa2af479e7c8612`  
		Last Modified: Tue, 12 Oct 2021 12:34:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc319e2994b8d2619b9216755ca3e9950d86fa85073fce0b349fa8b385640a0`  
		Last Modified: Tue, 12 Oct 2021 12:34:40 GMT  
		Size: 49.1 MB (49113726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21da0b575b0674310c4d5f47ed094df2abac3d16714fe1e4f1cf77a86264bf`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c546c3ea3ffcd2faa2227c1e3effe181f868847e8e06e0851a2c9dbfabad510`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b95b675d3c59325b31adebcf8db7d307f6219ecdf4261d2dbb0d726fb9c6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707fc9e3679465e141fed2979b76f9e3f5cc9e21a12f0e1c875ea0e5a341eca6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:64f70fc244c2636f3c906181e2e41a5e0c39fbba507aaaa30c5e48441110726b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:d88f859b0e2d27a94bd6862849a6a0fba3d10d7b2c0aeb79b8c2c5ac2dabf651
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84502946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec8a29dd01e00c0d102328f515fe8adc9bda383e5a3db59d5d0fb3c1038879`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:33:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Oct 2021 12:33:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:33:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Oct 2021 12:33:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:33:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:33:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:33:36 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:33:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb406db451bbcfa9ec9d447c1262d9b9d20b830136f5310aa2af479e7c8612`  
		Last Modified: Tue, 12 Oct 2021 12:34:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc319e2994b8d2619b9216755ca3e9950d86fa85073fce0b349fa8b385640a0`  
		Last Modified: Tue, 12 Oct 2021 12:34:40 GMT  
		Size: 49.1 MB (49113726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21da0b575b0674310c4d5f47ed094df2abac3d16714fe1e4f1cf77a86264bf`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c546c3ea3ffcd2faa2227c1e3effe181f868847e8e06e0851a2c9dbfabad510`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b95b675d3c59325b31adebcf8db7d307f6219ecdf4261d2dbb0d726fb9c6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707fc9e3679465e141fed2979b76f9e3f5cc9e21a12f0e1c875ea0e5a341eca6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:64f70fc244c2636f3c906181e2e41a5e0c39fbba507aaaa30c5e48441110726b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:d88f859b0e2d27a94bd6862849a6a0fba3d10d7b2c0aeb79b8c2c5ac2dabf651
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84502946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ec8a29dd01e00c0d102328f515fe8adc9bda383e5a3db59d5d0fb3c1038879`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:33:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 12 Oct 2021 12:33:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:33:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:33:34 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Oct 2021 12:33:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:33:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:33:36 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:33:36 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:33:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eb406db451bbcfa9ec9d447c1262d9b9d20b830136f5310aa2af479e7c8612`  
		Last Modified: Tue, 12 Oct 2021 12:34:35 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc319e2994b8d2619b9216755ca3e9950d86fa85073fce0b349fa8b385640a0`  
		Last Modified: Tue, 12 Oct 2021 12:34:40 GMT  
		Size: 49.1 MB (49113726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d21da0b575b0674310c4d5f47ed094df2abac3d16714fe1e4f1cf77a86264bf`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c546c3ea3ffcd2faa2227c1e3effe181f868847e8e06e0851a2c9dbfabad510`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc90b95b675d3c59325b31adebcf8db7d307f6219ecdf4261d2dbb0d726fb9c6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707fc9e3679465e141fed2979b76f9e3f5cc9e21a12f0e1c875ea0e5a341eca6`  
		Last Modified: Tue, 12 Oct 2021 12:34:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9dd9ffe56508bd6f0789584e3eefb1b06119a07b47908cb290419df8fd3ebbc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087a7767afc8a39e4e3196e4074b4795563e2b29fd05915d53057b68b649725`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:14:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 28 Sep 2021 02:14:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 28 Sep 2021 02:14:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 28 Sep 2021 02:14:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 28 Sep 2021 02:14:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 28 Sep 2021 02:14:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 28 Sep 2021 02:14:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 28 Sep 2021 02:14:19 GMT
VOLUME [/opt/couchdb/data]
# Tue, 28 Sep 2021 02:14:19 GMT
EXPOSE 4369 5984 9100
# Tue, 28 Sep 2021 02:14:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e28e896b4ae04dbf8ef8ce85c5ca01b73a5da373c5ee4f330a3cc82752bd72`  
		Last Modified: Tue, 28 Sep 2021 02:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f60f5bc43bec3cc68bb513b4fd76f28f8ed5a701bcea76de1e786331fab6d`  
		Last Modified: Tue, 28 Sep 2021 02:15:14 GMT  
		Size: 39.0 MB (39012565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de5ecee5454b78e9edd7e565df2f104c1955ceae4ceab9b1a5725b3ae0bd80e`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c950fa2453ec470f652eec7abd5358f5ed9c06fa300dcb51fcdf945d29eac7a`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d10b6a90ff4a25500f82ffec4a5930bb8e14fdc6950c717b11b4f18e2ec66`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adcf5258254be8c5a9897cbeb5e02b334ac4751faa9d033ef2d522c3b45e6e4`  
		Last Modified: Tue, 28 Sep 2021 02:15:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:ba44493ea1fc1ba06de88bafd915a4556a7400329c9c8412a45316a78e6c4086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:e150f08d4781b3d0ba2b2328896615436add41ebbc1ae8f46dbba0d5b50ef756
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80541108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2fff885de6eb95e7060e056bff8a68415b76592d6a9a799dac45ba5989085b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:29 GMT
ENV COUCHDB_VERSION=3.2.0
# Tue, 12 Oct 2021 12:32:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:32:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:32:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:32:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:32:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:32:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:32:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937941c5ec804af4fe48f885c0f4a7cf4bb52686fa4f351789e0822a0a53010`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9def6a2a7f7afb329b52aa79f6e7e364e4c0b1fc5f6456560d340092b1b11c1`  
		Last Modified: Tue, 12 Oct 2021 12:34:01 GMT  
		Size: 45.2 MB (45151893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab67db1541e933f5d72714f7addf00e24526db1fb69a90ee4a23eb797acf32`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80723a7fbea8d1f758f276151c162b1bc34bcb58360f6056c219e4fab23328fc`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57f490f20804c696113a543f5d12073356e77950f65b8da9b5e95546e7dd0a5`  
		Last Modified: Tue, 12 Oct 2021 12:33:55 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceefecb83d7b123a6fa5a0374e5bea18fba9de64bcedacdc4f36d1160d93c528`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a6500b9a69dd7649d736440910d269f6c44b82381b65975d25ee107fb65bab5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75649500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae92e937268d84ab86d7800081ab4e3aef19c02e8aab0cac503efe8a3811b5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:39:23 GMT
ENV COUCHDB_VERSION=3.2.0
# Fri, 08 Oct 2021 23:39:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 08 Oct 2021 23:39:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 08 Oct 2021 23:39:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 08 Oct 2021 23:39:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:39:38 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 Oct 2021 23:39:39 GMT
EXPOSE 4369 5984 9100
# Fri, 08 Oct 2021 23:39:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548288e8f973bece9d8cf1f3e7cb603dfb20101fc3e89cc3d45d6fcd44f88e9b`  
		Last Modified: Fri, 08 Oct 2021 23:40:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78b96a773b05f4fa42b178b6768370880b5c8b573929a6ad4790a5864d6135`  
		Last Modified: Fri, 08 Oct 2021 23:40:20 GMT  
		Size: 41.7 MB (41720301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3efd2f4358be175d41ec4a71b2f89f0456b2ad94308d78a74e9fdbd5b96a1e`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1e000d414b41f1540610350026b49645f3feb786be6710f97947e12a31509d`  
		Last Modified: Fri, 08 Oct 2021 23:40:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdc6c77c3660993e9d8e1f96ddeaea7479a0eb925942abdf115849fce89ebc8`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285c88dfdc22e30a79414c8eba0487288ad68dce6a23cd00e8996f67439480fd`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:21651f3b3de68ca24ce09d8cb8fcbc2e97e96f955dc515dddabeda06a6811793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:e22d9bb30b308002f721172b041de5f0e0f0c3d878f46f6953bec061d4f874a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79988449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be61a4391f21295d1d0190e854f76d8b92a30b0bd8a74a7576a9e98251805756`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:54 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 12 Oct 2021 12:32:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:33:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:33:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:33:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:33:10 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:33:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:33:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:33:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:33:12 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8d680eceb1e6eac3a2c1dc667249e8f684e9cb3bc60b720c8e818d7f56097e`  
		Last Modified: Tue, 12 Oct 2021 12:34:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a822819d8da2a339ec86da95dcf6f3e3596417fa067abd578ce85ccdb37773`  
		Last Modified: Tue, 12 Oct 2021 12:34:23 GMT  
		Size: 44.6 MB (44599232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a3ca2015db31129d6082d2c9b5fbab4c6872e8ba658a94ced052ebb634e799`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fddea528a9a4c5cdbb27e5e7aaa6f26061b166bfc48392c98e2201ad7e6bbd`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e1db98c95c74f8321c8188ed21d1c538f7c6fa389f4a74511c46dc59f0b2c3`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5b3f121da878e849adde075e83e34836c2496d85b085efff24da11d1f1b027`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bdf1c42056bae05aaaf57734c8cca2005dfacc3e285b06a554d7cccc3f765f7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75030301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ba89aa18fe2bb1f1befd832cdbffec76955bc0a3a826408ade0bb6e44c9822`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 18:06:16 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 01 Oct 2021 18:06:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 01 Oct 2021 18:06:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 01 Oct 2021 18:06:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 01 Oct 2021 18:06:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 01 Oct 2021 18:06:31 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 01 Oct 2021 18:06:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 01 Oct 2021 18:06:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 Oct 2021 18:06:32 GMT
VOLUME [/opt/couchdb/data]
# Fri, 01 Oct 2021 18:06:32 GMT
EXPOSE 4369 5984 9100
# Fri, 01 Oct 2021 18:06:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c17be680e8abb031c343c28e3bec734d06aaef7d857100e9ca069efbfce1fe`  
		Last Modified: Fri, 01 Oct 2021 18:07:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a3c3719889f22faf7df5cbd4e669f316a6ed3d50802fecc63631ea8a3d27ad`  
		Last Modified: Fri, 01 Oct 2021 18:07:07 GMT  
		Size: 41.1 MB (41101108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f766420e41cbe8582945cbab15e4b1844023f05c9d1ba5cba1a60af82ec63d49`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79ec33a988044fa394bc821fd7ad664aa20afad9c4bc2128e8dcfec98aeaf77`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cecd0f86c2a51f34a9bbb326fedc8e20862120c68e429a083d53b22a2ed8c0`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0def41fde10366687b31bf643203baeb6d344405017642ee1a4dcf46d718d72`  
		Last Modified: Fri, 01 Oct 2021 18:07:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:21651f3b3de68ca24ce09d8cb8fcbc2e97e96f955dc515dddabeda06a6811793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:e22d9bb30b308002f721172b041de5f0e0f0c3d878f46f6953bec061d4f874a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79988449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be61a4391f21295d1d0190e854f76d8b92a30b0bd8a74a7576a9e98251805756`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:54 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 12 Oct 2021 12:32:55 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:33:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:33:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:33:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:33:10 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:33:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:33:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:33:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:33:12 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8d680eceb1e6eac3a2c1dc667249e8f684e9cb3bc60b720c8e818d7f56097e`  
		Last Modified: Tue, 12 Oct 2021 12:34:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a822819d8da2a339ec86da95dcf6f3e3596417fa067abd578ce85ccdb37773`  
		Last Modified: Tue, 12 Oct 2021 12:34:23 GMT  
		Size: 44.6 MB (44599232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a3ca2015db31129d6082d2c9b5fbab4c6872e8ba658a94ced052ebb634e799`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fddea528a9a4c5cdbb27e5e7aaa6f26061b166bfc48392c98e2201ad7e6bbd`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e1db98c95c74f8321c8188ed21d1c538f7c6fa389f4a74511c46dc59f0b2c3`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5b3f121da878e849adde075e83e34836c2496d85b085efff24da11d1f1b027`  
		Last Modified: Tue, 12 Oct 2021 12:34:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bdf1c42056bae05aaaf57734c8cca2005dfacc3e285b06a554d7cccc3f765f7e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75030301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ba89aa18fe2bb1f1befd832cdbffec76955bc0a3a826408ade0bb6e44c9822`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 18:06:16 GMT
ENV COUCHDB_VERSION=3.1.2
# Fri, 01 Oct 2021 18:06:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 01 Oct 2021 18:06:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 01 Oct 2021 18:06:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 01 Oct 2021 18:06:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 01 Oct 2021 18:06:31 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 01 Oct 2021 18:06:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 01 Oct 2021 18:06:32 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 01 Oct 2021 18:06:32 GMT
VOLUME [/opt/couchdb/data]
# Fri, 01 Oct 2021 18:06:32 GMT
EXPOSE 4369 5984 9100
# Fri, 01 Oct 2021 18:06:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c17be680e8abb031c343c28e3bec734d06aaef7d857100e9ca069efbfce1fe`  
		Last Modified: Fri, 01 Oct 2021 18:07:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a3c3719889f22faf7df5cbd4e669f316a6ed3d50802fecc63631ea8a3d27ad`  
		Last Modified: Fri, 01 Oct 2021 18:07:07 GMT  
		Size: 41.1 MB (41101108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f766420e41cbe8582945cbab15e4b1844023f05c9d1ba5cba1a60af82ec63d49`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79ec33a988044fa394bc821fd7ad664aa20afad9c4bc2128e8dcfec98aeaf77`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cecd0f86c2a51f34a9bbb326fedc8e20862120c68e429a083d53b22a2ed8c0`  
		Last Modified: Fri, 01 Oct 2021 18:07:01 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0def41fde10366687b31bf643203baeb6d344405017642ee1a4dcf46d718d72`  
		Last Modified: Fri, 01 Oct 2021 18:07:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:ba44493ea1fc1ba06de88bafd915a4556a7400329c9c8412a45316a78e6c4086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:e150f08d4781b3d0ba2b2328896615436add41ebbc1ae8f46dbba0d5b50ef756
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80541108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2fff885de6eb95e7060e056bff8a68415b76592d6a9a799dac45ba5989085b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:29 GMT
ENV COUCHDB_VERSION=3.2.0
# Tue, 12 Oct 2021 12:32:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:32:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:32:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:32:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:32:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:32:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:32:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937941c5ec804af4fe48f885c0f4a7cf4bb52686fa4f351789e0822a0a53010`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9def6a2a7f7afb329b52aa79f6e7e364e4c0b1fc5f6456560d340092b1b11c1`  
		Last Modified: Tue, 12 Oct 2021 12:34:01 GMT  
		Size: 45.2 MB (45151893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab67db1541e933f5d72714f7addf00e24526db1fb69a90ee4a23eb797acf32`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80723a7fbea8d1f758f276151c162b1bc34bcb58360f6056c219e4fab23328fc`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57f490f20804c696113a543f5d12073356e77950f65b8da9b5e95546e7dd0a5`  
		Last Modified: Tue, 12 Oct 2021 12:33:55 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceefecb83d7b123a6fa5a0374e5bea18fba9de64bcedacdc4f36d1160d93c528`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a6500b9a69dd7649d736440910d269f6c44b82381b65975d25ee107fb65bab5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75649500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae92e937268d84ab86d7800081ab4e3aef19c02e8aab0cac503efe8a3811b5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:39:23 GMT
ENV COUCHDB_VERSION=3.2.0
# Fri, 08 Oct 2021 23:39:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 08 Oct 2021 23:39:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 08 Oct 2021 23:39:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 08 Oct 2021 23:39:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:39:38 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 Oct 2021 23:39:39 GMT
EXPOSE 4369 5984 9100
# Fri, 08 Oct 2021 23:39:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548288e8f973bece9d8cf1f3e7cb603dfb20101fc3e89cc3d45d6fcd44f88e9b`  
		Last Modified: Fri, 08 Oct 2021 23:40:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78b96a773b05f4fa42b178b6768370880b5c8b573929a6ad4790a5864d6135`  
		Last Modified: Fri, 08 Oct 2021 23:40:20 GMT  
		Size: 41.7 MB (41720301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3efd2f4358be175d41ec4a71b2f89f0456b2ad94308d78a74e9fdbd5b96a1e`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1e000d414b41f1540610350026b49645f3feb786be6710f97947e12a31509d`  
		Last Modified: Fri, 08 Oct 2021 23:40:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdc6c77c3660993e9d8e1f96ddeaea7479a0eb925942abdf115849fce89ebc8`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285c88dfdc22e30a79414c8eba0487288ad68dce6a23cd00e8996f67439480fd`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.0`

```console
$ docker pull couchdb@sha256:ba44493ea1fc1ba06de88bafd915a4556a7400329c9c8412a45316a78e6c4086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.0` - linux; amd64

```console
$ docker pull couchdb@sha256:e150f08d4781b3d0ba2b2328896615436add41ebbc1ae8f46dbba0d5b50ef756
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80541108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2fff885de6eb95e7060e056bff8a68415b76592d6a9a799dac45ba5989085b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:29 GMT
ENV COUCHDB_VERSION=3.2.0
# Tue, 12 Oct 2021 12:32:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:32:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:32:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:32:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:32:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:32:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:32:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937941c5ec804af4fe48f885c0f4a7cf4bb52686fa4f351789e0822a0a53010`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9def6a2a7f7afb329b52aa79f6e7e364e4c0b1fc5f6456560d340092b1b11c1`  
		Last Modified: Tue, 12 Oct 2021 12:34:01 GMT  
		Size: 45.2 MB (45151893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab67db1541e933f5d72714f7addf00e24526db1fb69a90ee4a23eb797acf32`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80723a7fbea8d1f758f276151c162b1bc34bcb58360f6056c219e4fab23328fc`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57f490f20804c696113a543f5d12073356e77950f65b8da9b5e95546e7dd0a5`  
		Last Modified: Tue, 12 Oct 2021 12:33:55 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceefecb83d7b123a6fa5a0374e5bea18fba9de64bcedacdc4f36d1160d93c528`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a6500b9a69dd7649d736440910d269f6c44b82381b65975d25ee107fb65bab5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75649500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae92e937268d84ab86d7800081ab4e3aef19c02e8aab0cac503efe8a3811b5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:39:23 GMT
ENV COUCHDB_VERSION=3.2.0
# Fri, 08 Oct 2021 23:39:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 08 Oct 2021 23:39:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 08 Oct 2021 23:39:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 08 Oct 2021 23:39:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:39:38 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 Oct 2021 23:39:39 GMT
EXPOSE 4369 5984 9100
# Fri, 08 Oct 2021 23:39:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548288e8f973bece9d8cf1f3e7cb603dfb20101fc3e89cc3d45d6fcd44f88e9b`  
		Last Modified: Fri, 08 Oct 2021 23:40:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78b96a773b05f4fa42b178b6768370880b5c8b573929a6ad4790a5864d6135`  
		Last Modified: Fri, 08 Oct 2021 23:40:20 GMT  
		Size: 41.7 MB (41720301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3efd2f4358be175d41ec4a71b2f89f0456b2ad94308d78a74e9fdbd5b96a1e`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1e000d414b41f1540610350026b49645f3feb786be6710f97947e12a31509d`  
		Last Modified: Fri, 08 Oct 2021 23:40:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdc6c77c3660993e9d8e1f96ddeaea7479a0eb925942abdf115849fce89ebc8`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285c88dfdc22e30a79414c8eba0487288ad68dce6a23cd00e8996f67439480fd`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ba44493ea1fc1ba06de88bafd915a4556a7400329c9c8412a45316a78e6c4086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:e150f08d4781b3d0ba2b2328896615436add41ebbc1ae8f46dbba0d5b50ef756
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80541108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2fff885de6eb95e7060e056bff8a68415b76592d6a9a799dac45ba5989085b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:32:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Oct 2021 12:32:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Oct 2021 12:32:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 12 Oct 2021 12:32:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 12 Oct 2021 12:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:32:29 GMT
ENV COUCHDB_VERSION=3.2.0
# Tue, 12 Oct 2021 12:32:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 12 Oct 2021 12:32:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Oct 2021 12:32:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Oct 2021 12:32:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 12:32:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:32:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Oct 2021 12:32:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Oct 2021 12:32:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a46377fe8ce67057386a4c7aa933b926be606ba3070c3342e42f63e68d052c`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4bf1b8a9bee200ee03e321a3d81949a87a559329ccffe9da773bd2d9d09fab`  
		Last Modified: Tue, 12 Oct 2021 12:34:00 GMT  
		Size: 6.7 MB (6691348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59081fa6a5d78e2274b9368f09dff77dc9e27812416dc235da1682d043b6129d`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 1.3 MB (1258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc87af85d712b9d439d847c5575c30770dcd0910cd5aea578135b4a2d4e5f16e`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 293.0 KB (292995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937941c5ec804af4fe48f885c0f4a7cf4bb52686fa4f351789e0822a0a53010`  
		Last Modified: Tue, 12 Oct 2021 12:33:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9def6a2a7f7afb329b52aa79f6e7e364e4c0b1fc5f6456560d340092b1b11c1`  
		Last Modified: Tue, 12 Oct 2021 12:34:01 GMT  
		Size: 45.2 MB (45151893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ab67db1541e933f5d72714f7addf00e24526db1fb69a90ee4a23eb797acf32`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80723a7fbea8d1f758f276151c162b1bc34bcb58360f6056c219e4fab23328fc`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57f490f20804c696113a543f5d12073356e77950f65b8da9b5e95546e7dd0a5`  
		Last Modified: Tue, 12 Oct 2021 12:33:55 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceefecb83d7b123a6fa5a0374e5bea18fba9de64bcedacdc4f36d1160d93c528`  
		Last Modified: Tue, 12 Oct 2021 12:33:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a6500b9a69dd7649d736440910d269f6c44b82381b65975d25ee107fb65bab5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75649500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ae92e937268d84ab86d7800081ab4e3aef19c02e8aab0cac503efe8a3811b5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:13:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 28 Sep 2021 02:13:21 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 28 Sep 2021 02:13:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:13:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 28 Sep 2021 02:13:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 28 Sep 2021 02:13:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Fri, 08 Oct 2021 23:39:23 GMT
ENV COUCHDB_VERSION=3.2.0
# Fri, 08 Oct 2021 23:39:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Fri, 08 Oct 2021 23:39:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 08 Oct 2021 23:39:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 08 Oct 2021 23:39:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 08 Oct 2021 23:39:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 08 Oct 2021 23:39:38 GMT
VOLUME [/opt/couchdb/data]
# Fri, 08 Oct 2021 23:39:39 GMT
EXPOSE 4369 5984 9100
# Fri, 08 Oct 2021 23:39:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccce50a09ce93b18af732f0cccc8bc50f337920af8abdceb6899462acf0d0f1`  
		Last Modified: Tue, 28 Sep 2021 02:14:49 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe94af3886b0bb198cc647f566a4d700267dd1162f81fd578bd8218a898c01`  
		Last Modified: Tue, 28 Sep 2021 02:14:48 GMT  
		Size: 6.6 MB (6550861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c0e24b6130ef05d86938e8f18a781c86cbd4b340809dfe0253927c98f2ee4`  
		Last Modified: Tue, 28 Sep 2021 02:14:47 GMT  
		Size: 1.2 MB (1163444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64a60e19b9cb05869c7102040626818240c5cf125ed25c9237bd8b7a36547a6`  
		Last Modified: Tue, 28 Sep 2021 02:14:46 GMT  
		Size: 292.8 KB (292825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548288e8f973bece9d8cf1f3e7cb603dfb20101fc3e89cc3d45d6fcd44f88e9b`  
		Last Modified: Fri, 08 Oct 2021 23:40:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc78b96a773b05f4fa42b178b6768370880b5c8b573929a6ad4790a5864d6135`  
		Last Modified: Fri, 08 Oct 2021 23:40:20 GMT  
		Size: 41.7 MB (41720301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3efd2f4358be175d41ec4a71b2f89f0456b2ad94308d78a74e9fdbd5b96a1e`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1e000d414b41f1540610350026b49645f3feb786be6710f97947e12a31509d`  
		Last Modified: Fri, 08 Oct 2021 23:40:15 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdc6c77c3660993e9d8e1f96ddeaea7479a0eb925942abdf115849fce89ebc8`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285c88dfdc22e30a79414c8eba0487288ad68dce6a23cd00e8996f67439480fd`  
		Last Modified: Fri, 08 Oct 2021 23:40:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
