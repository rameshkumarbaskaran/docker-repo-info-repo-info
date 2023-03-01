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
-	[`couchdb:3.3.1`](#couchdb331)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:a0305043da0c1e04c6eac1c78f61f4a2d32cecf031e23edb745d219c2ad33194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:f00fa296cbd0f10526356b265b0824774d97e45d93ef344ca502ba708e936c40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39085525a132628f4a60c2a8ccbb94ac8ac7c22af508c40a80ed238e47870fc1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:57:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:57:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:57:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:57:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:57:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:58:10 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 04:58:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:58:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 04:58:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:58:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:58:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:58:30 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:58:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381c1268083c6f22290329c5445e6bdd0d24301dbe0499de5c3b39c43e6a837`  
		Last Modified: Wed, 01 Mar 2023 04:59:23 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80bd75fe65477bba2d539bc9e5e36f67000b64d7090024c548384eaaed1c9a`  
		Last Modified: Wed, 01 Mar 2023 04:59:22 GMT  
		Size: 6.7 MB (6705930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77c9625dab9ea7df1d54ebd8e3c4e7b603e00f5ab2a83e4631631aa7f28797`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 1.3 MB (1259600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda150e57a9a14bfbde395fa9ae9838bb488a7ad4990455bf9df265d69bea56`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 294.4 KB (294355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721b5a4b16de8b99e4ddee9d018035a4a60663d93f2c764f612fb34dfda44597`  
		Last Modified: Wed, 01 Mar 2023 04:59:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd94bdc5adc2d30a569c12f937e9bbaaf7ea83c01fe830f07f974b84d2b33ad`  
		Last Modified: Wed, 01 Mar 2023 04:59:39 GMT  
		Size: 49.1 MB (49132144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c390e14a6265b20a844647eaf7ed464dd270bb5a4c8b8ad9d87c7c44ea46a09c`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c12b03ed830f425d2ca6239332392aa2cd342f85d2ef5855d5a15a3925cfbcc`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51274e515eb0e24f0ff3d10302bee9884b68bf8607bdc8255079e8b8504a65e0`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcaf5f59e6a480f794e59ab9cd6e40f191ccc6fdae41419af23d7023408a91b`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ea7b89c57661b743d97ce50a81b24533b6ad78eea4c237090b4bb1b4de72da44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72997261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071dbafc8ee72b35d2774709ddc014915b1ea4b29f4c914f0ffc76192af2c845`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:01:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:01:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:01:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:01:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:01:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:02:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 13:02:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:02:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 13:02:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:02:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:02:19 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:02:19 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:02:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6759d0399eeb0f700a9b9ce8ac2a6434521a39edd2c8d47b8c92c96f16df8457`  
		Last Modified: Wed, 01 Mar 2023 13:03:12 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe820e62570423958042a1e3878aac6a571079ee3d518a5e649b0958deeefc`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 6.6 MB (6579452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a247326076072850c80eb99fb5139cf988dc11020995fccdb020dc57e571c4`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 1.2 MB (1164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace80db58c9be6fa388162aa3678dba8385d28f7022cba310faccebdbccc62b`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5de621ffd97e5656bcca3d5d3e385935ca23892f98767fd83629331975b0718`  
		Last Modified: Wed, 01 Mar 2023 13:03:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbf36cda8047ccda1da0cb7d771fe3c0bfa2b0676612e74892db968eeaf8ed`  
		Last Modified: Wed, 01 Mar 2023 13:03:24 GMT  
		Size: 39.0 MB (39029350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ef8d5f305333f3b52585331b86e0a4b6ce982ee2e5130cb4d77cd2c5903e1c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bec3c44ac5d8ec73c5a35785b6f43cebf7fa8e9273d01c43e3aa19aa8fb648`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10211858e516ea36fb3c31e5f65541e85397e5daa0e1c3461f7188eab8908a5a`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabf0b267fbb86f841b2d667849dd0e0443cd81fd3db55ed8893834ddaeb23c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:a0305043da0c1e04c6eac1c78f61f4a2d32cecf031e23edb745d219c2ad33194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:f00fa296cbd0f10526356b265b0824774d97e45d93ef344ca502ba708e936c40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39085525a132628f4a60c2a8ccbb94ac8ac7c22af508c40a80ed238e47870fc1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:57:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:57:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:57:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:57:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:57:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:58:10 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 04:58:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:58:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 04:58:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:58:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:58:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:58:30 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:58:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381c1268083c6f22290329c5445e6bdd0d24301dbe0499de5c3b39c43e6a837`  
		Last Modified: Wed, 01 Mar 2023 04:59:23 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80bd75fe65477bba2d539bc9e5e36f67000b64d7090024c548384eaaed1c9a`  
		Last Modified: Wed, 01 Mar 2023 04:59:22 GMT  
		Size: 6.7 MB (6705930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77c9625dab9ea7df1d54ebd8e3c4e7b603e00f5ab2a83e4631631aa7f28797`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 1.3 MB (1259600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda150e57a9a14bfbde395fa9ae9838bb488a7ad4990455bf9df265d69bea56`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 294.4 KB (294355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721b5a4b16de8b99e4ddee9d018035a4a60663d93f2c764f612fb34dfda44597`  
		Last Modified: Wed, 01 Mar 2023 04:59:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd94bdc5adc2d30a569c12f937e9bbaaf7ea83c01fe830f07f974b84d2b33ad`  
		Last Modified: Wed, 01 Mar 2023 04:59:39 GMT  
		Size: 49.1 MB (49132144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c390e14a6265b20a844647eaf7ed464dd270bb5a4c8b8ad9d87c7c44ea46a09c`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c12b03ed830f425d2ca6239332392aa2cd342f85d2ef5855d5a15a3925cfbcc`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51274e515eb0e24f0ff3d10302bee9884b68bf8607bdc8255079e8b8504a65e0`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcaf5f59e6a480f794e59ab9cd6e40f191ccc6fdae41419af23d7023408a91b`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ea7b89c57661b743d97ce50a81b24533b6ad78eea4c237090b4bb1b4de72da44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72997261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071dbafc8ee72b35d2774709ddc014915b1ea4b29f4c914f0ffc76192af2c845`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:01:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:01:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:01:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:01:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:01:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:02:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 13:02:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:02:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 13:02:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:02:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:02:19 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:02:19 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:02:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6759d0399eeb0f700a9b9ce8ac2a6434521a39edd2c8d47b8c92c96f16df8457`  
		Last Modified: Wed, 01 Mar 2023 13:03:12 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe820e62570423958042a1e3878aac6a571079ee3d518a5e649b0958deeefc`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 6.6 MB (6579452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a247326076072850c80eb99fb5139cf988dc11020995fccdb020dc57e571c4`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 1.2 MB (1164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace80db58c9be6fa388162aa3678dba8385d28f7022cba310faccebdbccc62b`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5de621ffd97e5656bcca3d5d3e385935ca23892f98767fd83629331975b0718`  
		Last Modified: Wed, 01 Mar 2023 13:03:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbf36cda8047ccda1da0cb7d771fe3c0bfa2b0676612e74892db968eeaf8ed`  
		Last Modified: Wed, 01 Mar 2023 13:03:24 GMT  
		Size: 39.0 MB (39029350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ef8d5f305333f3b52585331b86e0a4b6ce982ee2e5130cb4d77cd2c5903e1c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bec3c44ac5d8ec73c5a35785b6f43cebf7fa8e9273d01c43e3aa19aa8fb648`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10211858e516ea36fb3c31e5f65541e85397e5daa0e1c3461f7188eab8908a5a`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabf0b267fbb86f841b2d667849dd0e0443cd81fd3db55ed8893834ddaeb23c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:a0305043da0c1e04c6eac1c78f61f4a2d32cecf031e23edb745d219c2ad33194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f00fa296cbd0f10526356b265b0824774d97e45d93ef344ca502ba708e936c40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39085525a132628f4a60c2a8ccbb94ac8ac7c22af508c40a80ed238e47870fc1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:57:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:57:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:57:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:57:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:57:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:58:10 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 04:58:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:58:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:58:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 04:58:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:58:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:58:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:58:30 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:58:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381c1268083c6f22290329c5445e6bdd0d24301dbe0499de5c3b39c43e6a837`  
		Last Modified: Wed, 01 Mar 2023 04:59:23 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80bd75fe65477bba2d539bc9e5e36f67000b64d7090024c548384eaaed1c9a`  
		Last Modified: Wed, 01 Mar 2023 04:59:22 GMT  
		Size: 6.7 MB (6705930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77c9625dab9ea7df1d54ebd8e3c4e7b603e00f5ab2a83e4631631aa7f28797`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 1.3 MB (1259600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda150e57a9a14bfbde395fa9ae9838bb488a7ad4990455bf9df265d69bea56`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 294.4 KB (294355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721b5a4b16de8b99e4ddee9d018035a4a60663d93f2c764f612fb34dfda44597`  
		Last Modified: Wed, 01 Mar 2023 04:59:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd94bdc5adc2d30a569c12f937e9bbaaf7ea83c01fe830f07f974b84d2b33ad`  
		Last Modified: Wed, 01 Mar 2023 04:59:39 GMT  
		Size: 49.1 MB (49132144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c390e14a6265b20a844647eaf7ed464dd270bb5a4c8b8ad9d87c7c44ea46a09c`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c12b03ed830f425d2ca6239332392aa2cd342f85d2ef5855d5a15a3925cfbcc`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51274e515eb0e24f0ff3d10302bee9884b68bf8607bdc8255079e8b8504a65e0`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcaf5f59e6a480f794e59ab9cd6e40f191ccc6fdae41419af23d7023408a91b`  
		Last Modified: Wed, 01 Mar 2023 04:59:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ea7b89c57661b743d97ce50a81b24533b6ad78eea4c237090b4bb1b4de72da44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72997261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071dbafc8ee72b35d2774709ddc014915b1ea4b29f4c914f0ffc76192af2c845`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:01:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:01:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:01:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:01:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:01:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:02:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Mar 2023 13:02:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:02:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:02:18 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Mar 2023 13:02:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:02:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:02:19 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:02:19 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:02:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6759d0399eeb0f700a9b9ce8ac2a6434521a39edd2c8d47b8c92c96f16df8457`  
		Last Modified: Wed, 01 Mar 2023 13:03:12 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe820e62570423958042a1e3878aac6a571079ee3d518a5e649b0958deeefc`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 6.6 MB (6579452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a247326076072850c80eb99fb5139cf988dc11020995fccdb020dc57e571c4`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 1.2 MB (1164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace80db58c9be6fa388162aa3678dba8385d28f7022cba310faccebdbccc62b`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5de621ffd97e5656bcca3d5d3e385935ca23892f98767fd83629331975b0718`  
		Last Modified: Wed, 01 Mar 2023 13:03:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acbf36cda8047ccda1da0cb7d771fe3c0bfa2b0676612e74892db968eeaf8ed`  
		Last Modified: Wed, 01 Mar 2023 13:03:24 GMT  
		Size: 39.0 MB (39029350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ef8d5f305333f3b52585331b86e0a4b6ce982ee2e5130cb4d77cd2c5903e1c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bec3c44ac5d8ec73c5a35785b6f43cebf7fa8e9273d01c43e3aa19aa8fb648`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10211858e516ea36fb3c31e5f65541e85397e5daa0e1c3461f7188eab8908a5a`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabf0b267fbb86f841b2d667849dd0e0443cd81fd3db55ed8893834ddaeb23c`  
		Last Modified: Wed, 01 Mar 2023 13:03:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:1a39612483d4b9ccea7510e5897f8e3a6b648e9eb0051b7d0235feff56dc37da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:dee3f17fa11aa1d43c0bd60c282d68b95f2cb0ea10582055a712be2c323cf481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c023ab20b99cef1ccbfa589fb35f923d1048860f5f55217e69ba05e18e39631a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 04:56:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:01 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:01 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0506641807b420c32835a9af376fe4810365cc6932f83148cf11374bf4bdd`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e0fd8fcee53fd180b1f321220a7b173c73c189d01741c93f21d83b664dcf1`  
		Last Modified: Wed, 01 Mar 2023 04:58:51 GMT  
		Size: 52.7 MB (52676453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f243172300bd45fa27ff12f5b283e411a5825f2ae436f9545f9c30fbdcf1031`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdece4117c4fa382060db81e46bea365c1dc59ce1b4371caf5036535c9846134`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e870857342e5e9d5e0441a5d7eefc223938f717850bb9228d9aa5840386ef4c`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64097a0563ea7989e391d5759e050d96127903a994698b8d099486bad2502afb`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:42a35a53cac6df4d96eff2d7dca342d15bafe40a3897c33b261854bba16bf36f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae12060d508ec49c33b314b12ed252bb5cbbf527895730793b40394eeda0703f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:57 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 13:00:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:10 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107e3a3014720b3d5930175da26ce494637fff8039a588d39f7f5fb7f1b4bf3c`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768f5ac066c518e4b28cc66c0e303234d27d40b1d0c8fdec79f23c545ea853c`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 52.5 MB (52531794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed05acc732ccd6950ec274672e98ae030bb645d792103d2d7b9c0add6b1a2e`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51013d82b48e0a2d2624178cc5605aceac7c9ab707f04e61eb3772c8de42de`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c2fb0ba9cdfd3eca3eb6ff449f31c05dd13a4ee411b791fbb44d952ccab96`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bda250c3f269b7b0eb2135c0a0f024cb406c32c0b76355c548f10d5f1ef4c8`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:aa9693a4ea6a67e2d48c99e32ac51914c414b4332b30be1c9b2bd42c2a616074
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96679233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ec5c87509de09ccb8fe5339cfd2c6265f9d69bd7aa889186ee6306ad81311c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:44:16 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 05:44:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:44:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:44:52 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:44:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:44:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:44:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:44:57 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:44:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57156270861ebec15e15824b98ce258087d77093da47aa2505c0f10323dbf576`  
		Last Modified: Wed, 01 Mar 2023 05:46:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170b2c08141c093d2a5f59fade4fed001a14775b4ae0553f26009520440c5074`  
		Last Modified: Wed, 01 Mar 2023 05:46:12 GMT  
		Size: 53.5 MB (53534942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0690b576b7faaf6377d377ccda31c9f40557af57ac472a66e767d1c2003508cf`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de86fd9c9910a4e1ed03a633ffd1f982abc032eddc6482211b9e52712fc457`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332b0bd48c4b5ddcdc504dd68272e7cffed2eeb6543dbf6c2766ee2190566153`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3fbf8e1caf707e5e47d41e751e4316e5a73e5c95cbb2b8b717847eb2807b8e`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:4a992f2f661e586256a2d5f4017cd63a476c3f3b62490771ee6670a9d58376e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:be908c1b586be1c5633621a3aa135ae30190014deb6b0d5998c119199724c9f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80026341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79064f60a232ebcc1807a42c78b66c75b943a335579e9e8bc7cb03010069de82`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:57:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:57:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:57:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:57:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:57:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Mar 2023 04:57:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:58:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:58:03 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:58:03 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Mar 2023 04:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:58:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:58:04 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:58:04 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:58:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381c1268083c6f22290329c5445e6bdd0d24301dbe0499de5c3b39c43e6a837`  
		Last Modified: Wed, 01 Mar 2023 04:59:23 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80bd75fe65477bba2d539bc9e5e36f67000b64d7090024c548384eaaed1c9a`  
		Last Modified: Wed, 01 Mar 2023 04:59:22 GMT  
		Size: 6.7 MB (6705930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77c9625dab9ea7df1d54ebd8e3c4e7b603e00f5ab2a83e4631631aa7f28797`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 1.3 MB (1259600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda150e57a9a14bfbde395fa9ae9838bb488a7ad4990455bf9df265d69bea56`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 294.4 KB (294355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dea979ca4ebb90a90a89878291feea493733f5318c4d0264c38db50cd0095ad`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17435058b174559c6dd62ef7958d24be86a8d7e649d6a55fbf2330405a323b`  
		Last Modified: Wed, 01 Mar 2023 04:59:24 GMT  
		Size: 44.6 MB (44619554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7df995c3f74ff9b041d920545b7451c510a48acf3c55ce68a29ac74635ae546`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d69b8d9e468b7b50efc01be45f0d5ada072a78850abd7d21180fb918f7816d`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185dec2968e2084b7f11871f446afd513d7af246f6f2ec666ac7d2f7529938f`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a1c990f13bd06299f57c8bd8959051c2bfe8c1281efd077269c2505c8b31f`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0436fea5383841f640f3c67f8e9c180518ee41ffeffc8d9b46ca4ea1ec07809a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0c71e0699b58cbadc26292b9aac02773859d11d528715ab27b352cbce4290`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:01:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:01:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:01:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:01:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:01:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:50 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Mar 2023 13:01:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:02:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:02:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:02:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:02:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Mar 2023 13:02:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:02:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:02:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:02:03 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:02:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6759d0399eeb0f700a9b9ce8ac2a6434521a39edd2c8d47b8c92c96f16df8457`  
		Last Modified: Wed, 01 Mar 2023 13:03:12 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe820e62570423958042a1e3878aac6a571079ee3d518a5e649b0958deeefc`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 6.6 MB (6579452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a247326076072850c80eb99fb5139cf988dc11020995fccdb020dc57e571c4`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 1.2 MB (1164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace80db58c9be6fa388162aa3678dba8385d28f7022cba310faccebdbccc62b`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11d35eeba918575d5c78b08bd873cb609e1dd7de4039ed4e7fde1a9655f6fee`  
		Last Modified: Wed, 01 Mar 2023 13:03:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913390e565908a1cde895cd2228112cbb865040a57aafcdbc70f3517216859a8`  
		Last Modified: Wed, 01 Mar 2023 13:03:13 GMT  
		Size: 41.1 MB (41125870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5405f7852d9ad5045236f53e4662f0356b00cada7d223812ab2aedc7e8b30b2e`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c39ac9cf22dc7bc4a74a244936a8952f03b8fdf9868d67726adaa8072ba283`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a51f93869e0195860058e9e05e4da9ecb1a8220ee4ff2e0454e3e423dc8e77f`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e37b09e566e2d6ef8a535b536d4b6481bbc5ef7cb410313006ce11818af20e`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:4a992f2f661e586256a2d5f4017cd63a476c3f3b62490771ee6670a9d58376e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:be908c1b586be1c5633621a3aa135ae30190014deb6b0d5998c119199724c9f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80026341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79064f60a232ebcc1807a42c78b66c75b943a335579e9e8bc7cb03010069de82`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:57:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:57:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:57:38 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:57:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:57:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:48 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Mar 2023 04:57:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:58:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:58:03 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:58:03 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:58:03 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Mar 2023 04:58:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:58:04 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:58:04 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:58:04 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:58:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381c1268083c6f22290329c5445e6bdd0d24301dbe0499de5c3b39c43e6a837`  
		Last Modified: Wed, 01 Mar 2023 04:59:23 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80bd75fe65477bba2d539bc9e5e36f67000b64d7090024c548384eaaed1c9a`  
		Last Modified: Wed, 01 Mar 2023 04:59:22 GMT  
		Size: 6.7 MB (6705930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77c9625dab9ea7df1d54ebd8e3c4e7b603e00f5ab2a83e4631631aa7f28797`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 1.3 MB (1259600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda150e57a9a14bfbde395fa9ae9838bb488a7ad4990455bf9df265d69bea56`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 294.4 KB (294355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dea979ca4ebb90a90a89878291feea493733f5318c4d0264c38db50cd0095ad`  
		Last Modified: Wed, 01 Mar 2023 04:59:21 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a17435058b174559c6dd62ef7958d24be86a8d7e649d6a55fbf2330405a323b`  
		Last Modified: Wed, 01 Mar 2023 04:59:24 GMT  
		Size: 44.6 MB (44619554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7df995c3f74ff9b041d920545b7451c510a48acf3c55ce68a29ac74635ae546`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d69b8d9e468b7b50efc01be45f0d5ada072a78850abd7d21180fb918f7816d`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185dec2968e2084b7f11871f446afd513d7af246f6f2ec666ac7d2f7529938f`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3a1c990f13bd06299f57c8bd8959051c2bfe8c1281efd077269c2505c8b31f`  
		Last Modified: Wed, 01 Mar 2023 04:59:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0436fea5383841f640f3c67f8e9c180518ee41ffeffc8d9b46ca4ea1ec07809a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75093777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0c71e0699b58cbadc26292b9aac02773859d11d528715ab27b352cbce4290`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:01:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:01:33 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:01:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:01:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:01:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:50 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Mar 2023 13:01:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:02:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:02:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:02:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:02:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Mar 2023 13:02:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:02:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:02:03 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:02:03 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:02:03 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6759d0399eeb0f700a9b9ce8ac2a6434521a39edd2c8d47b8c92c96f16df8457`  
		Last Modified: Wed, 01 Mar 2023 13:03:12 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe820e62570423958042a1e3878aac6a571079ee3d518a5e649b0958deeefc`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 6.6 MB (6579452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a247326076072850c80eb99fb5139cf988dc11020995fccdb020dc57e571c4`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 1.2 MB (1164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ace80db58c9be6fa388162aa3678dba8385d28f7022cba310faccebdbccc62b`  
		Last Modified: Wed, 01 Mar 2023 13:03:11 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11d35eeba918575d5c78b08bd873cb609e1dd7de4039ed4e7fde1a9655f6fee`  
		Last Modified: Wed, 01 Mar 2023 13:03:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913390e565908a1cde895cd2228112cbb865040a57aafcdbc70f3517216859a8`  
		Last Modified: Wed, 01 Mar 2023 13:03:13 GMT  
		Size: 41.1 MB (41125870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5405f7852d9ad5045236f53e4662f0356b00cada7d223812ab2aedc7e8b30b2e`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c39ac9cf22dc7bc4a74a244936a8952f03b8fdf9868d67726adaa8072ba283`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a51f93869e0195860058e9e05e4da9ecb1a8220ee4ff2e0454e3e423dc8e77f`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e37b09e566e2d6ef8a535b536d4b6481bbc5ef7cb410313006ce11818af20e`  
		Last Modified: Wed, 01 Mar 2023 13:03:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:2f75fc7e2cd0b10c6dbd20bec00df82d0b961ea4441b56efcb3cdcb36e4ed794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:c19738d414c68d642761754f7722e951f9f9b61cfe10abee235ef14aa220a80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87538923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2958c1a2f02e17c9b2091a820af930f1bfcf9baac6f99f422364c5599f69c663`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:10 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 04:57:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:24 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:24 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:24 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eab40b1a4155afe9258d02a26fb6d5eb5a9b2ae2b6610573e071b0e6d419e6`  
		Last Modified: Wed, 01 Mar 2023 04:59:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e83a5471e8e5bac7dd5130fcdbad25ed5ac5469c46e6b518671d1cc11df24d`  
		Last Modified: Wed, 01 Mar 2023 04:59:10 GMT  
		Size: 49.0 MB (49047109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8b4a8cba587b7f91cbaacaa2d1eef2747c8d54c580ea4e7239ef111b4ea3b`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2850017aae386fac5c0507c14be2ee49fddfe3dc3f2e14bba79f5480ac7d2bc2`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18f1503e1f33858dc96ebc2d0100d5770d532fca48d057d28258145db547190`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce387e8260bd073472b122c9e811807ab1c48ab390e0618b2dc6202ef7ae9b7e`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:70dd709a206a923f828a42ac89ae3f4ceef58f5769cee60f1e4e138f54f8ccd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86076082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963f45bd43028d25049da3153261fd7bab93baadbad526973031123fc2068010`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:17 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 13:01:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:29 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:29 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:29 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:29 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3428ac86f5e5b2cea7576e4bc6d3458067c21fe9784ec52f7989f4824df9f500`  
		Last Modified: Wed, 01 Mar 2023 13:02:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ac4e9104128782feb6301327657132f9c3a8c7fb8a88499681c7f8d4fcea8`  
		Last Modified: Wed, 01 Mar 2023 13:03:00 GMT  
		Size: 49.1 MB (49065201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad0a77073059080b237541257132513c2d135e5813f54bc723fac891283eae4`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2136f995f13b28860c86c7cf2eed8f9e9a26c36c6402a01990b78b39dc0b2201`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d668f9fbd432431ef0e0aaed43198e4c43f2bd9018a35a942211df191189366`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8e2d889813f5b78bc4d75daf61748a90ad75125476fcd2a476335bf78091f`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c399bf2156b7112b21119165223d1e9a2d34e6a8301b07cc94a2a412eeb4f3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93230624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6db186358f76c416c7cdb96c50bf21052c524ebecbc30cee46c42beb24fca00`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:45:05 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 05:45:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:45:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:45:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:45:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:45:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:45:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:45:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:45:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:45:40 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:45:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca762f444998d4bd3016122f9886d4e7c14da812ddbc7f7de8e575f4b2bae68`  
		Last Modified: Wed, 01 Mar 2023 05:46:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71af86e7969357b8a270a9d615903fb9a2cc829c6371012bdd30c6b8651ea1`  
		Last Modified: Wed, 01 Mar 2023 05:46:43 GMT  
		Size: 50.1 MB (50086567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a98c3c152489f0d0fe21ceac6aa20723c329bb4301b0947aa29ee6f923a0e52`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b42d18f1c4c133b6947441af70f66a78abd7ccadb1f7044e040252a24615781`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fc695927445d03aad064debcfbc03a0347a572662d7710e2e5aab06ded9f1b`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd64d5384a509a49a41e2a092f9ced334fba5563ff436cd3177217ce7d8fc3b2`  
		Last Modified: Wed, 01 Mar 2023 05:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:2f75fc7e2cd0b10c6dbd20bec00df82d0b961ea4441b56efcb3cdcb36e4ed794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:c19738d414c68d642761754f7722e951f9f9b61cfe10abee235ef14aa220a80e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87538923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2958c1a2f02e17c9b2091a820af930f1bfcf9baac6f99f422364c5599f69c663`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:57:10 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 04:57:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:23 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:24 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:24 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:24 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:24 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eab40b1a4155afe9258d02a26fb6d5eb5a9b2ae2b6610573e071b0e6d419e6`  
		Last Modified: Wed, 01 Mar 2023 04:59:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e83a5471e8e5bac7dd5130fcdbad25ed5ac5469c46e6b518671d1cc11df24d`  
		Last Modified: Wed, 01 Mar 2023 04:59:10 GMT  
		Size: 49.0 MB (49047109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8b4a8cba587b7f91cbaacaa2d1eef2747c8d54c580ea4e7239ef111b4ea3b`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2850017aae386fac5c0507c14be2ee49fddfe3dc3f2e14bba79f5480ac7d2bc2`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18f1503e1f33858dc96ebc2d0100d5770d532fca48d057d28258145db547190`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce387e8260bd073472b122c9e811807ab1c48ab390e0618b2dc6202ef7ae9b7e`  
		Last Modified: Wed, 01 Mar 2023 04:59:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:70dd709a206a923f828a42ac89ae3f4ceef58f5769cee60f1e4e138f54f8ccd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86076082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963f45bd43028d25049da3153261fd7bab93baadbad526973031123fc2068010`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:01:17 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 13:01:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:29 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:29 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:29 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:29 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3428ac86f5e5b2cea7576e4bc6d3458067c21fe9784ec52f7989f4824df9f500`  
		Last Modified: Wed, 01 Mar 2023 13:02:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ac4e9104128782feb6301327657132f9c3a8c7fb8a88499681c7f8d4fcea8`  
		Last Modified: Wed, 01 Mar 2023 13:03:00 GMT  
		Size: 49.1 MB (49065201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad0a77073059080b237541257132513c2d135e5813f54bc723fac891283eae4`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2136f995f13b28860c86c7cf2eed8f9e9a26c36c6402a01990b78b39dc0b2201`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d668f9fbd432431ef0e0aaed43198e4c43f2bd9018a35a942211df191189366`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec8e2d889813f5b78bc4d75daf61748a90ad75125476fcd2a476335bf78091f`  
		Last Modified: Wed, 01 Mar 2023 13:02:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c399bf2156b7112b21119165223d1e9a2d34e6a8301b07cc94a2a412eeb4f3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93230624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6db186358f76c416c7cdb96c50bf21052c524ebecbc30cee46c42beb24fca00`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:45:05 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 01 Mar 2023 05:45:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:45:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:45:36 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:45:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:45:37 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:45:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:45:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:45:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:45:40 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:45:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca762f444998d4bd3016122f9886d4e7c14da812ddbc7f7de8e575f4b2bae68`  
		Last Modified: Wed, 01 Mar 2023 05:46:35 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71af86e7969357b8a270a9d615903fb9a2cc829c6371012bdd30c6b8651ea1`  
		Last Modified: Wed, 01 Mar 2023 05:46:43 GMT  
		Size: 50.1 MB (50086567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a98c3c152489f0d0fe21ceac6aa20723c329bb4301b0947aa29ee6f923a0e52`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b42d18f1c4c133b6947441af70f66a78abd7ccadb1f7044e040252a24615781`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fc695927445d03aad064debcfbc03a0347a572662d7710e2e5aab06ded9f1b`  
		Last Modified: Wed, 01 Mar 2023 05:46:34 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd64d5384a509a49a41e2a092f9ced334fba5563ff436cd3177217ce7d8fc3b2`  
		Last Modified: Wed, 01 Mar 2023 05:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:1a39612483d4b9ccea7510e5897f8e3a6b648e9eb0051b7d0235feff56dc37da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:dee3f17fa11aa1d43c0bd60c282d68b95f2cb0ea10582055a712be2c323cf481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c023ab20b99cef1ccbfa589fb35f923d1048860f5f55217e69ba05e18e39631a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 04:56:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:01 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:01 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0506641807b420c32835a9af376fe4810365cc6932f83148cf11374bf4bdd`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e0fd8fcee53fd180b1f321220a7b173c73c189d01741c93f21d83b664dcf1`  
		Last Modified: Wed, 01 Mar 2023 04:58:51 GMT  
		Size: 52.7 MB (52676453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f243172300bd45fa27ff12f5b283e411a5825f2ae436f9545f9c30fbdcf1031`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdece4117c4fa382060db81e46bea365c1dc59ce1b4371caf5036535c9846134`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e870857342e5e9d5e0441a5d7eefc223938f717850bb9228d9aa5840386ef4c`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64097a0563ea7989e391d5759e050d96127903a994698b8d099486bad2502afb`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:42a35a53cac6df4d96eff2d7dca342d15bafe40a3897c33b261854bba16bf36f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae12060d508ec49c33b314b12ed252bb5cbbf527895730793b40394eeda0703f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:57 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 13:00:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:10 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107e3a3014720b3d5930175da26ce494637fff8039a588d39f7f5fb7f1b4bf3c`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768f5ac066c518e4b28cc66c0e303234d27d40b1d0c8fdec79f23c545ea853c`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 52.5 MB (52531794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed05acc732ccd6950ec274672e98ae030bb645d792103d2d7b9c0add6b1a2e`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51013d82b48e0a2d2624178cc5605aceac7c9ab707f04e61eb3772c8de42de`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c2fb0ba9cdfd3eca3eb6ff449f31c05dd13a4ee411b791fbb44d952ccab96`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bda250c3f269b7b0eb2135c0a0f024cb406c32c0b76355c548f10d5f1ef4c8`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:aa9693a4ea6a67e2d48c99e32ac51914c414b4332b30be1c9b2bd42c2a616074
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96679233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ec5c87509de09ccb8fe5339cfd2c6265f9d69bd7aa889186ee6306ad81311c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:44:16 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 05:44:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:44:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:44:52 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:44:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:44:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:44:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:44:57 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:44:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57156270861ebec15e15824b98ce258087d77093da47aa2505c0f10323dbf576`  
		Last Modified: Wed, 01 Mar 2023 05:46:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170b2c08141c093d2a5f59fade4fed001a14775b4ae0553f26009520440c5074`  
		Last Modified: Wed, 01 Mar 2023 05:46:12 GMT  
		Size: 53.5 MB (53534942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0690b576b7faaf6377d377ccda31c9f40557af57ac472a66e767d1c2003508cf`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de86fd9c9910a4e1ed03a633ffd1f982abc032eddc6482211b9e52712fc457`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332b0bd48c4b5ddcdc504dd68272e7cffed2eeb6543dbf6c2766ee2190566153`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3fbf8e1caf707e5e47d41e751e4316e5a73e5c95cbb2b8b717847eb2807b8e`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.1`

```console
$ docker pull couchdb@sha256:1a39612483d4b9ccea7510e5897f8e3a6b648e9eb0051b7d0235feff56dc37da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:dee3f17fa11aa1d43c0bd60c282d68b95f2cb0ea10582055a712be2c323cf481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c023ab20b99cef1ccbfa589fb35f923d1048860f5f55217e69ba05e18e39631a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 04:56:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:01 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:01 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0506641807b420c32835a9af376fe4810365cc6932f83148cf11374bf4bdd`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e0fd8fcee53fd180b1f321220a7b173c73c189d01741c93f21d83b664dcf1`  
		Last Modified: Wed, 01 Mar 2023 04:58:51 GMT  
		Size: 52.7 MB (52676453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f243172300bd45fa27ff12f5b283e411a5825f2ae436f9545f9c30fbdcf1031`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdece4117c4fa382060db81e46bea365c1dc59ce1b4371caf5036535c9846134`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e870857342e5e9d5e0441a5d7eefc223938f717850bb9228d9aa5840386ef4c`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64097a0563ea7989e391d5759e050d96127903a994698b8d099486bad2502afb`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:42a35a53cac6df4d96eff2d7dca342d15bafe40a3897c33b261854bba16bf36f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae12060d508ec49c33b314b12ed252bb5cbbf527895730793b40394eeda0703f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:57 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 13:00:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:10 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107e3a3014720b3d5930175da26ce494637fff8039a588d39f7f5fb7f1b4bf3c`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768f5ac066c518e4b28cc66c0e303234d27d40b1d0c8fdec79f23c545ea853c`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 52.5 MB (52531794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed05acc732ccd6950ec274672e98ae030bb645d792103d2d7b9c0add6b1a2e`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51013d82b48e0a2d2624178cc5605aceac7c9ab707f04e61eb3772c8de42de`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c2fb0ba9cdfd3eca3eb6ff449f31c05dd13a4ee411b791fbb44d952ccab96`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bda250c3f269b7b0eb2135c0a0f024cb406c32c0b76355c548f10d5f1ef4c8`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:aa9693a4ea6a67e2d48c99e32ac51914c414b4332b30be1c9b2bd42c2a616074
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96679233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ec5c87509de09ccb8fe5339cfd2c6265f9d69bd7aa889186ee6306ad81311c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:44:16 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 05:44:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:44:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:44:52 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:44:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:44:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:44:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:44:57 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:44:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57156270861ebec15e15824b98ce258087d77093da47aa2505c0f10323dbf576`  
		Last Modified: Wed, 01 Mar 2023 05:46:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170b2c08141c093d2a5f59fade4fed001a14775b4ae0553f26009520440c5074`  
		Last Modified: Wed, 01 Mar 2023 05:46:12 GMT  
		Size: 53.5 MB (53534942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0690b576b7faaf6377d377ccda31c9f40557af57ac472a66e767d1c2003508cf`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de86fd9c9910a4e1ed03a633ffd1f982abc032eddc6482211b9e52712fc457`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332b0bd48c4b5ddcdc504dd68272e7cffed2eeb6543dbf6c2766ee2190566153`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3fbf8e1caf707e5e47d41e751e4316e5a73e5c95cbb2b8b717847eb2807b8e`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1a39612483d4b9ccea7510e5897f8e3a6b648e9eb0051b7d0235feff56dc37da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:dee3f17fa11aa1d43c0bd60c282d68b95f2cb0ea10582055a712be2c323cf481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c023ab20b99cef1ccbfa589fb35f923d1048860f5f55217e69ba05e18e39631a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:56:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 04:56:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 04:56:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 04:56:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 04:56:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:56:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 04:56:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 04:57:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 04:57:00 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 04:57:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 04:57:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 04:57:01 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 04:57:01 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 04:57:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6637e7f130a96ee279b7cd93c77afc7a28fd7f831b19520de38e2b6b45ba2939`  
		Last Modified: Wed, 01 Mar 2023 04:58:49 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4dc9bd71357404364ed9c84296ea0170e4b13240b108fc598fcbc0400a3880`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 5.2 MB (5224334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde3e5409fa60225a360de6fc7cff74d8fdf8e3744088a5d03c3a9f8f22a12e`  
		Last Modified: Wed, 01 Mar 2023 04:58:48 GMT  
		Size: 1.6 MB (1553317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e818344b5f6306fba9c7fd2a9425930d01c149a178358a242bae48ac6fec38`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 295.6 KB (295619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0506641807b420c32835a9af376fe4810365cc6932f83148cf11374bf4bdd`  
		Last Modified: Wed, 01 Mar 2023 04:58:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6e0fd8fcee53fd180b1f321220a7b173c73c189d01741c93f21d83b664dcf1`  
		Last Modified: Wed, 01 Mar 2023 04:58:51 GMT  
		Size: 52.7 MB (52676453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f243172300bd45fa27ff12f5b283e411a5825f2ae436f9545f9c30fbdcf1031`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdece4117c4fa382060db81e46bea365c1dc59ce1b4371caf5036535c9846134`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e870857342e5e9d5e0441a5d7eefc223938f717850bb9228d9aa5840386ef4c`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64097a0563ea7989e391d5759e050d96127903a994698b8d099486bad2502afb`  
		Last Modified: Wed, 01 Mar 2023 04:58:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:42a35a53cac6df4d96eff2d7dca342d15bafe40a3897c33b261854bba16bf36f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae12060d508ec49c33b314b12ed252bb5cbbf527895730793b40394eeda0703f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:00:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 13:00:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 13:00:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 13:00:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 13:00:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:00:57 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 13:00:58 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 13:01:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 13:01:10 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 13:01:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 13:01:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 13:01:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 13:01:10 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 13:01:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5062435b3525c590327308b13c7117ff3a0462e7dd8ac2b02b934c832e0b6882`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870190223a80d6ce34a8ac53a6aade325a75a20aeca43cbff5549ee2dcd3c1ad`  
		Last Modified: Wed, 01 Mar 2023 13:02:40 GMT  
		Size: 5.2 MB (5209450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f60ff1a19713aa957bf160225cf839f644a6c5f50a26f52d379d94f2a23b66`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 1.4 MB (1435930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03feb731ed174a80ed59c6097a718e831156aafb6428dbc6bbfd65abc4217836`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 295.5 KB (295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107e3a3014720b3d5930175da26ce494637fff8039a588d39f7f5fb7f1b4bf3c`  
		Last Modified: Wed, 01 Mar 2023 13:02:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6768f5ac066c518e4b28cc66c0e303234d27d40b1d0c8fdec79f23c545ea853c`  
		Last Modified: Wed, 01 Mar 2023 13:02:41 GMT  
		Size: 52.5 MB (52531794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed05acc732ccd6950ec274672e98ae030bb645d792103d2d7b9c0add6b1a2e`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51013d82b48e0a2d2624178cc5605aceac7c9ab707f04e61eb3772c8de42de`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8c2fb0ba9cdfd3eca3eb6ff449f31c05dd13a4ee411b791fbb44d952ccab96`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bda250c3f269b7b0eb2135c0a0f024cb406c32c0b76355c548f10d5f1ef4c8`  
		Last Modified: Wed, 01 Mar 2023 13:02:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:aa9693a4ea6a67e2d48c99e32ac51914c414b4332b30be1c9b2bd42c2a616074
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96679233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ec5c87509de09ccb8fe5339cfd2c6265f9d69bd7aa889186ee6306ad81311c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:33 GMT
ADD file:6fdf0b2f8ea4be2d01e25a9d85db8f8c7e3b2a641c9c7665e34f4fad771815e0 in / 
# Wed, 01 Mar 2023 04:47:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:43:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Mar 2023 05:43:26 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Mar 2023 05:43:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:43:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Mar 2023 05:43:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Mar 2023 05:44:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:44:16 GMT
ENV COUCHDB_VERSION=3.3.1
# Wed, 01 Mar 2023 05:44:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Mar 2023 05:44:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Mar 2023 05:44:51 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Mar 2023 05:44:52 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 01 Mar 2023 05:44:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Mar 2023 05:44:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:44:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Mar 2023 05:44:57 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Mar 2023 05:44:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:93ab3a60c2a8cbc1150cb2bd54222db8b79c525c0243534a10d6294ef7ff83ac`  
		Last Modified: Wed, 01 Mar 2023 04:53:54 GMT  
		Size: 35.3 MB (35288103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7db168bb798ef118541ed78f0f09ab50044e5c6830937388a72cc43d78035b4`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b49f4851c4778b84f6d8d20589ed144f5d5aed34469fb055ba5961d658a92d`  
		Last Modified: Wed, 01 Mar 2023 05:46:05 GMT  
		Size: 6.0 MB (6043951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbef0173a07bc581e30e85a57b1e68802fcc0a024f244fa68c5b459d9c237577`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 1.5 MB (1509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553cf561c481aa0f831976d5481d1c2f5564fded0f487d629e780599b8b950cb`  
		Last Modified: Wed, 01 Mar 2023 05:46:04 GMT  
		Size: 295.6 KB (295602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57156270861ebec15e15824b98ce258087d77093da47aa2505c0f10323dbf576`  
		Last Modified: Wed, 01 Mar 2023 05:46:03 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170b2c08141c093d2a5f59fade4fed001a14775b4ae0553f26009520440c5074`  
		Last Modified: Wed, 01 Mar 2023 05:46:12 GMT  
		Size: 53.5 MB (53534942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0690b576b7faaf6377d377ccda31c9f40557af57ac472a66e767d1c2003508cf`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de86fd9c9910a4e1ed03a633ffd1f982abc032eddc6482211b9e52712fc457`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332b0bd48c4b5ddcdc504dd68272e7cffed2eeb6543dbf6c2766ee2190566153`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3fbf8e1caf707e5e47d41e751e4316e5a73e5c95cbb2b8b717847eb2807b8e`  
		Last Modified: Wed, 01 Mar 2023 05:46:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
