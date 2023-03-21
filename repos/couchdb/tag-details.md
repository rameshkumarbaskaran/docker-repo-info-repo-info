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
$ docker pull couchdb@sha256:726500078555bba4e9e2735fba8f0219a2330e80601197f77b3ea7b052d6e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:cfbfb0f2176a8ddce1dcc6f316f7f80937f314a081826ced332acccc4bdf463f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90222546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89136ce418b25fad99f65939fde82ce29e468c9f0df495b23780a9541a74b838`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:21:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:21:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:01 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:01 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:01 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750e4988cdc5e548f72b6d7f18fcbaddc801ef303be35ae09556fd41898683ff`  
		Last Modified: Mon, 20 Mar 2023 22:22:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f302bdf03b732e3eef753e220abfe2cc9c20272d389332d45f2c315c2a4890`  
		Last Modified: Mon, 20 Mar 2023 22:22:50 GMT  
		Size: 52.7 MB (52674805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b8753a6ed2cba26445c4969ef7592117031b3491d3dc070c6578008a7fa402`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac150d8c917223cc50d5dd117b916f6a09978123c9f3dec6dcaf129136a957ba`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533f9b3e8160de41b0177197166c05851a494f05e59e58ce03e0702a45154d9e`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7b7d2d60248ef3fb088e0fc0f22bb75cfeea4ef3ccd5e2b21cc4bfbd79872`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5be64acf57d5f2991219ecf2e2e918f4053a6a4da203551e24bfd72c959b947e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88670295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255331a1a6975bbf99a2262a7fc0d462d3f3c54e4ad114fd1463a0e2fb6e20a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:38 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:40:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:40:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:40:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:40:53 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:40:53 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:40:53 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4125d43b64e1ede5061372eac5d8d2b087312f7319996fb20974a85caa1ca2b6`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd880493a9e6cce11f45f67b70d9597f7b7548b6394536119699df09ffcfb0`  
		Last Modified: Mon, 20 Mar 2023 22:41:38 GMT  
		Size: 52.5 MB (52530089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2dcece77541a2b77d9dfcdfec67a290de44f9aadf8142ef5c0a163ae1dca8`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026f83bc51c9945168f17b4cb18c4978c6854bd15b4df9dd224526d26a928e1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37dde701322e89f3b3989bb60176435c056116b6c1b9db6f4963eb6973b7ee1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2c60e14e30c82431555c8e47192b288d36688c176e70425db6ee4270399a26`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a61c3683b0ca2948f3078b89d06c1b75500eef5c74972583d5e44cda377ba776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95829290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9642c64a707353006d1cffecd1a7a4da3e2bd27829d533c4a337b10972083c`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:16:47 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:16:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:16 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:17 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:17 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f095cf7b5e92264b86d71420ddf1ae59ea1ffd7e653fa4985df3a6b0ef42cf`  
		Last Modified: Mon, 20 Mar 2023 22:18:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625cdce16d9ecdc3ebd8dee77f10730d1b98340f8a79deae3d9c9fbc626e013`  
		Last Modified: Mon, 20 Mar 2023 22:18:29 GMT  
		Size: 53.5 MB (53533461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602d60b8bd03fd76328fee3d9232ce007b6f489bd4186ab1e573332cafb27a55`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5371246bf435da2d0007b058ada6946f5bd70333face6dba0a595e9695478eb0`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84c938a14f7ecd134f28ac7951fcdb3c73179b7713659792f8c4e86a495180`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 2.2 KB (2210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd777621cdc3f8f9dc7f220ac32bd3f8227860f932bb8462275d2f3597e0829`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
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
$ docker pull couchdb@sha256:dda616310897b4498ba5ec232d2e97b70e1d8e52841b3c2dfc46f649fb5a4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:428f9cec6abfc476a6fd0c25d9702e6ce949c559d72eae1d4068e6e1a4892797
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86593237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a13285f52feb1357e57a4dfd17af6ca0c286b3c183ae865282fa7e9f5fd6ce`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:22:05 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:22:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:20 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:21 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:21 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:21 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18dbfb6919d8b517c550c6283f280757d22970870a5194d4c876ea25b2c3ebd`  
		Last Modified: Mon, 20 Mar 2023 22:23:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3356493eb9e2f0ecfbab8e3d043ad7bf96088dd23b3678cf033fe3ee69db09`  
		Last Modified: Mon, 20 Mar 2023 22:23:08 GMT  
		Size: 49.0 MB (49045723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b439a1f74bdb4a88eb270e6b2483596f7833b23223b4bb75df7ab55b4ab2cc`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ccb716988d9e561bafa3657a1272819ae819d831bd4b0d19827f491e93a39`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e447ddc7220192c69506fe54a667ded2831f5d1667ace5fafd7ee724b6f2f7`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0bc891cbbc985427184f47274dac8f42c1134488bb0f75a13547c7498962ae`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c7bfa672b9850d10a0ef35eef0e933fea809d69b0ddc5eb3fede8a0a1633415b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85203417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e723f0e0446fb3ecaf143e4f89b6e1f5a1de1679b062dc561fcf24ad894f5a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:59 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:40:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:41:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:41:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:41:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:41:11 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:41:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:41:11 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:41:12 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:41:12 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11fa14a9dc768becb181b6eaec01357e7e625496b251b350e9f7e942f8a4641`  
		Last Modified: Mon, 20 Mar 2023 22:41:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fbc84a5c7a3a8ecfad0b32c6dad18d008e55f3fd6bfe1b895883542f52a579`  
		Last Modified: Mon, 20 Mar 2023 22:41:56 GMT  
		Size: 49.1 MB (49063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff6ca058235d8ee0053b189875e31ad9466c259c5d3f2d3f3e1e219d773a01`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85be94c4bdfc428632cfd534ab11ded24868bb8915af233fb75383ac0005e225`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893b49f1d197ad05c80d84d95823c616cc3946c55f9d3acbd49fe57446a59a`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704dfb9e82a1349c8c943679907d4ca82e7153ec12efc5ec4892b61272610e25`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fdeaf905d8a3b9d06e4e6849f93676f985ab16ac033ba5f5e587a426508baa7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92380111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9738e44b7a76473ef2f322c46833148b6dace87a1aabe733cf1a302612db6e0e`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:17:27 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:56 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:58 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:58 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:58 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1734a252d77fb3688f52be57a07ad38abfe3bd07823ffd18d5a5c9117cd48ec8`  
		Last Modified: Mon, 20 Mar 2023 22:18:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350edebe1cd9eeb0ca6a9d595f5ee280a18d46d40285f34325e3ad0fb42b4a00`  
		Last Modified: Mon, 20 Mar 2023 22:18:56 GMT  
		Size: 50.1 MB (50084518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d090c1b025d577eeb6279984259e9d16d0e7abf6e8b476845319dea36ea2c1f1`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b3fc4ebb659a720ba490d614a15d7eb339e495441e3e172cc20c3e855846`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a26506d4fbff34e3d802de1e7be5fcfecd057b1404c7899c659c338d6822e13`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad9598fc836f16ec532e8c06f41968e61c307e00e5293be9aa729eb43f4a471`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:dda616310897b4498ba5ec232d2e97b70e1d8e52841b3c2dfc46f649fb5a4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:428f9cec6abfc476a6fd0c25d9702e6ce949c559d72eae1d4068e6e1a4892797
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86593237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a13285f52feb1357e57a4dfd17af6ca0c286b3c183ae865282fa7e9f5fd6ce`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:22:05 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:22:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:20 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:21 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:21 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:21 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18dbfb6919d8b517c550c6283f280757d22970870a5194d4c876ea25b2c3ebd`  
		Last Modified: Mon, 20 Mar 2023 22:23:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3356493eb9e2f0ecfbab8e3d043ad7bf96088dd23b3678cf033fe3ee69db09`  
		Last Modified: Mon, 20 Mar 2023 22:23:08 GMT  
		Size: 49.0 MB (49045723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b439a1f74bdb4a88eb270e6b2483596f7833b23223b4bb75df7ab55b4ab2cc`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168ccb716988d9e561bafa3657a1272819ae819d831bd4b0d19827f491e93a39`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e447ddc7220192c69506fe54a667ded2831f5d1667ace5fafd7ee724b6f2f7`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0bc891cbbc985427184f47274dac8f42c1134488bb0f75a13547c7498962ae`  
		Last Modified: Mon, 20 Mar 2023 22:23:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c7bfa672b9850d10a0ef35eef0e933fea809d69b0ddc5eb3fede8a0a1633415b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85203417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e723f0e0446fb3ecaf143e4f89b6e1f5a1de1679b062dc561fcf24ad894f5a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:59 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:40:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:41:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:41:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:41:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:41:11 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:41:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:41:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:41:11 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:41:12 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:41:12 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11fa14a9dc768becb181b6eaec01357e7e625496b251b350e9f7e942f8a4641`  
		Last Modified: Mon, 20 Mar 2023 22:41:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fbc84a5c7a3a8ecfad0b32c6dad18d008e55f3fd6bfe1b895883542f52a579`  
		Last Modified: Mon, 20 Mar 2023 22:41:56 GMT  
		Size: 49.1 MB (49063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff6ca058235d8ee0053b189875e31ad9466c259c5d3f2d3f3e1e219d773a01`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85be94c4bdfc428632cfd534ab11ded24868bb8915af233fb75383ac0005e225`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893b49f1d197ad05c80d84d95823c616cc3946c55f9d3acbd49fe57446a59a`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704dfb9e82a1349c8c943679907d4ca82e7153ec12efc5ec4892b61272610e25`  
		Last Modified: Mon, 20 Mar 2023 22:41:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fdeaf905d8a3b9d06e4e6849f93676f985ab16ac033ba5f5e587a426508baa7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92380111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9738e44b7a76473ef2f322c46833148b6dace87a1aabe733cf1a302612db6e0e`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:17:27 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Mon, 20 Mar 2023 22:17:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:56 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:58 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:58 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:58 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1734a252d77fb3688f52be57a07ad38abfe3bd07823ffd18d5a5c9117cd48ec8`  
		Last Modified: Mon, 20 Mar 2023 22:18:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350edebe1cd9eeb0ca6a9d595f5ee280a18d46d40285f34325e3ad0fb42b4a00`  
		Last Modified: Mon, 20 Mar 2023 22:18:56 GMT  
		Size: 50.1 MB (50084518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d090c1b025d577eeb6279984259e9d16d0e7abf6e8b476845319dea36ea2c1f1`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b3fc4ebb659a720ba490d614a15d7eb339e495441e3e172cc20c3e855846`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a26506d4fbff34e3d802de1e7be5fcfecd057b1404c7899c659c338d6822e13`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad9598fc836f16ec532e8c06f41968e61c307e00e5293be9aa729eb43f4a471`  
		Last Modified: Mon, 20 Mar 2023 22:18:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:726500078555bba4e9e2735fba8f0219a2330e80601197f77b3ea7b052d6e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:cfbfb0f2176a8ddce1dcc6f316f7f80937f314a081826ced332acccc4bdf463f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90222546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89136ce418b25fad99f65939fde82ce29e468c9f0df495b23780a9541a74b838`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:21:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:21:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:01 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:01 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:01 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750e4988cdc5e548f72b6d7f18fcbaddc801ef303be35ae09556fd41898683ff`  
		Last Modified: Mon, 20 Mar 2023 22:22:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f302bdf03b732e3eef753e220abfe2cc9c20272d389332d45f2c315c2a4890`  
		Last Modified: Mon, 20 Mar 2023 22:22:50 GMT  
		Size: 52.7 MB (52674805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b8753a6ed2cba26445c4969ef7592117031b3491d3dc070c6578008a7fa402`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac150d8c917223cc50d5dd117b916f6a09978123c9f3dec6dcaf129136a957ba`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533f9b3e8160de41b0177197166c05851a494f05e59e58ce03e0702a45154d9e`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7b7d2d60248ef3fb088e0fc0f22bb75cfeea4ef3ccd5e2b21cc4bfbd79872`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5be64acf57d5f2991219ecf2e2e918f4053a6a4da203551e24bfd72c959b947e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88670295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255331a1a6975bbf99a2262a7fc0d462d3f3c54e4ad114fd1463a0e2fb6e20a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:38 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:40:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:40:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:40:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:40:53 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:40:53 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:40:53 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4125d43b64e1ede5061372eac5d8d2b087312f7319996fb20974a85caa1ca2b6`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd880493a9e6cce11f45f67b70d9597f7b7548b6394536119699df09ffcfb0`  
		Last Modified: Mon, 20 Mar 2023 22:41:38 GMT  
		Size: 52.5 MB (52530089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2dcece77541a2b77d9dfcdfec67a290de44f9aadf8142ef5c0a163ae1dca8`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026f83bc51c9945168f17b4cb18c4978c6854bd15b4df9dd224526d26a928e1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37dde701322e89f3b3989bb60176435c056116b6c1b9db6f4963eb6973b7ee1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2c60e14e30c82431555c8e47192b288d36688c176e70425db6ee4270399a26`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a61c3683b0ca2948f3078b89d06c1b75500eef5c74972583d5e44cda377ba776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95829290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9642c64a707353006d1cffecd1a7a4da3e2bd27829d533c4a337b10972083c`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:16:47 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:16:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:16 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:17 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:17 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f095cf7b5e92264b86d71420ddf1ae59ea1ffd7e653fa4985df3a6b0ef42cf`  
		Last Modified: Mon, 20 Mar 2023 22:18:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625cdce16d9ecdc3ebd8dee77f10730d1b98340f8a79deae3d9c9fbc626e013`  
		Last Modified: Mon, 20 Mar 2023 22:18:29 GMT  
		Size: 53.5 MB (53533461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602d60b8bd03fd76328fee3d9232ce007b6f489bd4186ab1e573332cafb27a55`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5371246bf435da2d0007b058ada6946f5bd70333face6dba0a595e9695478eb0`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84c938a14f7ecd134f28ac7951fcdb3c73179b7713659792f8c4e86a495180`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 2.2 KB (2210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd777621cdc3f8f9dc7f220ac32bd3f8227860f932bb8462275d2f3597e0829`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.1`

```console
$ docker pull couchdb@sha256:726500078555bba4e9e2735fba8f0219a2330e80601197f77b3ea7b052d6e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:cfbfb0f2176a8ddce1dcc6f316f7f80937f314a081826ced332acccc4bdf463f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90222546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89136ce418b25fad99f65939fde82ce29e468c9f0df495b23780a9541a74b838`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:21:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:21:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:01 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:01 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:01 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750e4988cdc5e548f72b6d7f18fcbaddc801ef303be35ae09556fd41898683ff`  
		Last Modified: Mon, 20 Mar 2023 22:22:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f302bdf03b732e3eef753e220abfe2cc9c20272d389332d45f2c315c2a4890`  
		Last Modified: Mon, 20 Mar 2023 22:22:50 GMT  
		Size: 52.7 MB (52674805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b8753a6ed2cba26445c4969ef7592117031b3491d3dc070c6578008a7fa402`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac150d8c917223cc50d5dd117b916f6a09978123c9f3dec6dcaf129136a957ba`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533f9b3e8160de41b0177197166c05851a494f05e59e58ce03e0702a45154d9e`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7b7d2d60248ef3fb088e0fc0f22bb75cfeea4ef3ccd5e2b21cc4bfbd79872`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5be64acf57d5f2991219ecf2e2e918f4053a6a4da203551e24bfd72c959b947e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88670295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255331a1a6975bbf99a2262a7fc0d462d3f3c54e4ad114fd1463a0e2fb6e20a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:38 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:40:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:40:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:40:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:40:53 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:40:53 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:40:53 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4125d43b64e1ede5061372eac5d8d2b087312f7319996fb20974a85caa1ca2b6`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd880493a9e6cce11f45f67b70d9597f7b7548b6394536119699df09ffcfb0`  
		Last Modified: Mon, 20 Mar 2023 22:41:38 GMT  
		Size: 52.5 MB (52530089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2dcece77541a2b77d9dfcdfec67a290de44f9aadf8142ef5c0a163ae1dca8`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026f83bc51c9945168f17b4cb18c4978c6854bd15b4df9dd224526d26a928e1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37dde701322e89f3b3989bb60176435c056116b6c1b9db6f4963eb6973b7ee1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2c60e14e30c82431555c8e47192b288d36688c176e70425db6ee4270399a26`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a61c3683b0ca2948f3078b89d06c1b75500eef5c74972583d5e44cda377ba776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95829290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9642c64a707353006d1cffecd1a7a4da3e2bd27829d533c4a337b10972083c`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:16:47 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:16:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:16 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:17 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:17 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f095cf7b5e92264b86d71420ddf1ae59ea1ffd7e653fa4985df3a6b0ef42cf`  
		Last Modified: Mon, 20 Mar 2023 22:18:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625cdce16d9ecdc3ebd8dee77f10730d1b98340f8a79deae3d9c9fbc626e013`  
		Last Modified: Mon, 20 Mar 2023 22:18:29 GMT  
		Size: 53.5 MB (53533461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602d60b8bd03fd76328fee3d9232ce007b6f489bd4186ab1e573332cafb27a55`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5371246bf435da2d0007b058ada6946f5bd70333face6dba0a595e9695478eb0`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84c938a14f7ecd134f28ac7951fcdb3c73179b7713659792f8c4e86a495180`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 2.2 KB (2210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd777621cdc3f8f9dc7f220ac32bd3f8227860f932bb8462275d2f3597e0829`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:726500078555bba4e9e2735fba8f0219a2330e80601197f77b3ea7b052d6e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:cfbfb0f2176a8ddce1dcc6f316f7f80937f314a081826ced332acccc4bdf463f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90222546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89136ce418b25fad99f65939fde82ce29e468c9f0df495b23780a9541a74b838`
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
# Mon, 20 Mar 2023 22:21:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:21:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:21:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:21:46 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:21:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:22:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:22:00 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:22:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:22:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:22:01 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:22:01 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:22:01 GMT
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
	-	`sha256:332a93da608d50d8e2467e3c588c4acb78fd80576a34aab2e6ad203e64e9b193`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 610.2 KB (610218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced3ec0ba6bbfd51995a8998f94e8f53c32cd23f57c96b5d4c22d7ab8f42c32`  
		Last Modified: Mon, 20 Mar 2023 22:22:46 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750e4988cdc5e548f72b6d7f18fcbaddc801ef303be35ae09556fd41898683ff`  
		Last Modified: Mon, 20 Mar 2023 22:22:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f302bdf03b732e3eef753e220abfe2cc9c20272d389332d45f2c315c2a4890`  
		Last Modified: Mon, 20 Mar 2023 22:22:50 GMT  
		Size: 52.7 MB (52674805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b8753a6ed2cba26445c4969ef7592117031b3491d3dc070c6578008a7fa402`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac150d8c917223cc50d5dd117b916f6a09978123c9f3dec6dcaf129136a957ba`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533f9b3e8160de41b0177197166c05851a494f05e59e58ce03e0702a45154d9e`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 2.2 KB (2206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7b7d2d60248ef3fb088e0fc0f22bb75cfeea4ef3ccd5e2b21cc4bfbd79872`  
		Last Modified: Mon, 20 Mar 2023 22:22:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5be64acf57d5f2991219ecf2e2e918f4053a6a4da203551e24bfd72c959b947e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88670295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255331a1a6975bbf99a2262a7fc0d462d3f3c54e4ad114fd1463a0e2fb6e20a`
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
# Mon, 20 Mar 2023 22:40:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:40:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:40:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:40:38 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:40:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:40:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:40:52 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:40:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:40:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:40:53 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:40:53 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:40:53 GMT
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
	-	`sha256:50e9863e93722978d8dc7bac8f1b64d8c91395ca199c458ffe489ce5be975dab`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 566.3 KB (566255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fe9ae8269843a8b140bbc16fe2e7b8db84126d2894b818a46695cf5d98ee9d`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 294.3 KB (294264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4125d43b64e1ede5061372eac5d8d2b087312f7319996fb20974a85caa1ca2b6`  
		Last Modified: Mon, 20 Mar 2023 22:41:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfd880493a9e6cce11f45f67b70d9597f7b7548b6394536119699df09ffcfb0`  
		Last Modified: Mon, 20 Mar 2023 22:41:38 GMT  
		Size: 52.5 MB (52530089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a2dcece77541a2b77d9dfcdfec67a290de44f9aadf8142ef5c0a163ae1dca8`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4026f83bc51c9945168f17b4cb18c4978c6854bd15b4df9dd224526d26a928e1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37dde701322e89f3b3989bb60176435c056116b6c1b9db6f4963eb6973b7ee1`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2c60e14e30c82431555c8e47192b288d36688c176e70425db6ee4270399a26`  
		Last Modified: Mon, 20 Mar 2023 22:41:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:a61c3683b0ca2948f3078b89d06c1b75500eef5c74972583d5e44cda377ba776
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95829290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9642c64a707353006d1cffecd1a7a4da3e2bd27829d533c4a337b10972083c`
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
# Mon, 20 Mar 2023 22:16:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Mon, 20 Mar 2023 22:16:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 20 Mar 2023 22:16:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 20 Mar 2023 22:16:47 GMT
ENV COUCHDB_VERSION=3.3.1
# Mon, 20 Mar 2023 22:16:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Mon, 20 Mar 2023 22:17:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Mon, 20 Mar 2023 22:17:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Mon, 20 Mar 2023 22:17:15 GMT
COPY file:4f56a6457d04af3aef6fcaf07a864b915c40e6514919d19a783d4be98fe5bc89 in /usr/local/bin 
# Mon, 20 Mar 2023 22:17:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Mon, 20 Mar 2023 22:17:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 20 Mar 2023 22:17:16 GMT
VOLUME [/opt/couchdb/data]
# Mon, 20 Mar 2023 22:17:17 GMT
EXPOSE 4369 5984 9100
# Mon, 20 Mar 2023 22:17:17 GMT
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
	-	`sha256:e2842ad19ef92a090e8111ad7e88fcbf2c0fb50caec07709f50d634294c4ced5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 662.1 KB (662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54475fcf0a17094179a6d5e3a9e1c1ff6aeb8e8a76da5630da72ba9c7164b9e5`  
		Last Modified: Mon, 20 Mar 2023 22:18:22 GMT  
		Size: 294.3 KB (294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f095cf7b5e92264b86d71420ddf1ae59ea1ffd7e653fa4985df3a6b0ef42cf`  
		Last Modified: Mon, 20 Mar 2023 22:18:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625cdce16d9ecdc3ebd8dee77f10730d1b98340f8a79deae3d9c9fbc626e013`  
		Last Modified: Mon, 20 Mar 2023 22:18:29 GMT  
		Size: 53.5 MB (53533461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602d60b8bd03fd76328fee3d9232ce007b6f489bd4186ab1e573332cafb27a55`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5371246bf435da2d0007b058ada6946f5bd70333face6dba0a595e9695478eb0`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84c938a14f7ecd134f28ac7951fcdb3c73179b7713659792f8c4e86a495180`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 2.2 KB (2210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd777621cdc3f8f9dc7f220ac32bd3f8227860f932bb8462275d2f3597e0829`  
		Last Modified: Mon, 20 Mar 2023 22:18:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
