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
$ docker pull couchdb@sha256:291d93cafd82232c1c9331c82d8c300c54ce652eb0f706862a6765268c09c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:202c00e38dab9e0a1b4576057e8570b7767ff8768d95c76153b0e33e1790dbf6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67111255e70659562b908fda3c157b78e1d5b2f4b928ba9646559ef128ef8e59`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 02 Dec 2021 03:59:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 04:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 02 Dec 2021 04:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 04:00:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:00:19 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 04:00:19 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 04:00:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ee2a6c6321bb98473070bf36746a5fe84f1903e1c3ecd9b2ff1c20bf3775e3`  
		Last Modified: Thu, 02 Dec 2021 04:01:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bf68be8d4c0978b1d50f1b5876c649d686317a6049080faef114dffbd0c2bc`  
		Last Modified: Thu, 02 Dec 2021 04:01:31 GMT  
		Size: 49.1 MB (49113821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0472396d00fc8494998a67c99dcf52be7733e2f046cb500c15e16d8612f2e`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf5364c7e42615110763f6b626b006bfefd5e43bb3bad9707b0b95fece955b`  
		Last Modified: Thu, 02 Dec 2021 04:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4719d0f7cd526efec2ba629e4734529cef44a2af61f50529d1bd376db11b2a51`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be803775575ea7160cc895f602a77188a1a25e91d4ee10df4bd2511431566a4a`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:291d93cafd82232c1c9331c82d8c300c54ce652eb0f706862a6765268c09c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:202c00e38dab9e0a1b4576057e8570b7767ff8768d95c76153b0e33e1790dbf6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67111255e70659562b908fda3c157b78e1d5b2f4b928ba9646559ef128ef8e59`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 02 Dec 2021 03:59:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 04:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 02 Dec 2021 04:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 04:00:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:00:19 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 04:00:19 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 04:00:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ee2a6c6321bb98473070bf36746a5fe84f1903e1c3ecd9b2ff1c20bf3775e3`  
		Last Modified: Thu, 02 Dec 2021 04:01:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bf68be8d4c0978b1d50f1b5876c649d686317a6049080faef114dffbd0c2bc`  
		Last Modified: Thu, 02 Dec 2021 04:01:31 GMT  
		Size: 49.1 MB (49113821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0472396d00fc8494998a67c99dcf52be7733e2f046cb500c15e16d8612f2e`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf5364c7e42615110763f6b626b006bfefd5e43bb3bad9707b0b95fece955b`  
		Last Modified: Thu, 02 Dec 2021 04:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4719d0f7cd526efec2ba629e4734529cef44a2af61f50529d1bd376db11b2a51`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be803775575ea7160cc895f602a77188a1a25e91d4ee10df4bd2511431566a4a`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:291d93cafd82232c1c9331c82d8c300c54ce652eb0f706862a6765268c09c361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:202c00e38dab9e0a1b4576057e8570b7767ff8768d95c76153b0e33e1790dbf6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67111255e70659562b908fda3c157b78e1d5b2f4b928ba9646559ef128ef8e59`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 02 Dec 2021 03:59:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 04:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 04:00:17 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 02 Dec 2021 04:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 04:00:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 04:00:19 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 04:00:19 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 04:00:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ee2a6c6321bb98473070bf36746a5fe84f1903e1c3ecd9b2ff1c20bf3775e3`  
		Last Modified: Thu, 02 Dec 2021 04:01:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bf68be8d4c0978b1d50f1b5876c649d686317a6049080faef114dffbd0c2bc`  
		Last Modified: Thu, 02 Dec 2021 04:01:31 GMT  
		Size: 49.1 MB (49113821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0472396d00fc8494998a67c99dcf52be7733e2f046cb500c15e16d8612f2e`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccf5364c7e42615110763f6b626b006bfefd5e43bb3bad9707b0b95fece955b`  
		Last Modified: Thu, 02 Dec 2021 04:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4719d0f7cd526efec2ba629e4734529cef44a2af61f50529d1bd376db11b2a51`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be803775575ea7160cc895f602a77188a1a25e91d4ee10df4bd2511431566a4a`  
		Last Modified: Thu, 02 Dec 2021 04:01:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a2234d5ef9cfaf5250ea7fe5c5aace9f2970510e264c192437d43bb7f50b1124
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72522890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87390f597386e9612170756997a4b24dad965808b0a0563b78a74535774c0fef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:06 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 17 Nov 2021 03:14:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:14:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:14:27 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:14:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:14:29 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 17 Nov 2021 03:14:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:14:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:14:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:32 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dde381ec5a1278d2a68005ae0d1fae341c35a340efb3d9b90be4fe049c4ef8a`  
		Last Modified: Wed, 17 Nov 2021 03:15:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474d94037945201cc5d7571f55def71d28fc890d3bc387495108a7a0bee632d`  
		Last Modified: Wed, 17 Nov 2021 03:15:45 GMT  
		Size: 39.0 MB (39011901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3b7c8996739229afa8080719316aa93ea6f0cba82b9d12e581dcb4999f345`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09df975511d34ed7f321268c943fd807a0e9fe1458bdd8bb4fd7ec82dffcfd03`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5607f62215bb22d77ff6f9f8bb4949ab62b0980260bf0e4c49e1a7567ccf128a`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e953c19ec4cff6a88215e2380d9df7cd5907027ea651ffece0a60c7b7a3302`  
		Last Modified: Wed, 17 Nov 2021 03:15:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:c20ed43c7bf849abeeff63506ed5f1661d66c99206882ac062aaa0b633580dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:f9233a3c37fc3a10a128c63ee24d6d710ecb256efcea6470cf1481a88497c14f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54858da96e40fd74eb5ba582c8555ce4d7e6a8d1680922378e6ee368ea7116`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:01 GMT
ENV COUCHDB_VERSION=3.2.0
# Thu, 02 Dec 2021 03:59:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:22 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c15fe4082d8bc4ffe30e811af7011a5a2d3838d55adb4e8ed5726d005543a34`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb97c47e07838a0f160aebf72818bc31d97a769d7ccd3e7cee6e376abeacf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:49 GMT  
		Size: 45.2 MB (45151962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314989771b01cbcd55238bde9274da680acf89f4af915d1afec64fcf4c34caec`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7045cb60dfcd780b48dce1b614f91f784c903bbe054158c9a06884aa16273e`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478ee4109a6eb9fde5f2cb0044c0f3b29b4b7b0a5c2f4f8143f23f65c27d64f`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097296e42e603863e72b649d7e75e356ff483c5062c9438e8022dd6bab7fe6f6`  
		Last Modified: Thu, 02 Dec 2021 04:00:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:19c00963a6fff966ebfdc633b9d4483aa27a9c8e2210b1cfb7d19cc809acf4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:fdb62ff5ce4d44a880046e0ac30933889b4f260236caf923ad945cac941eafbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ff697fa5558306b2afa4e682d4b6380a9738cdbc5d9a2b014c7a0fc241a91f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:27 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 02 Dec 2021 03:59:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:46 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:47 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee142f85ca1332628ddc4730e56d9a9ffeb106490c130516755dd1fe0667b80`  
		Last Modified: Thu, 02 Dec 2021 04:01:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4c913cc766f03be3365121cd0b59e89c01ee7ecdce226860f56e74e5c64a1`  
		Last Modified: Thu, 02 Dec 2021 04:01:13 GMT  
		Size: 44.6 MB (44600031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f7c0c283a9da41259c0ea6a5279ffebabc10018e320e1c71a3e5dbdb197791`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b090f6094bb41cf4a08e9288fd6812b8adb0644e5d793f7c1e6568ef2e97ee0`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2edb36e304a7ada2e1f1b37b3db3c65eff8b1b14000581ef64cb4419daa603e`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c8efda332d8c32ebbcbc7df3b733e6caba419dc9d2f73cbf3214314a38610c`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4d8a1503ca18c1599eba18e97ea21f228e920c878c5a5f7b1d69be01e1fa028
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89f734b1ac6c68282b0b172ad767b2a25e273b044473eec4cb7799c1d5d8de7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:13:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:13:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:00 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d364f5670abffa7a117aff9a0b2fee592035bd61977f33d207385acea580116`  
		Last Modified: Wed, 17 Nov 2021 03:15:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f10831ac14d41ed907e4f278276ba6e26edbb08cc2e0b5e7bb5d9bcc6ea445`  
		Last Modified: Wed, 17 Nov 2021 03:15:28 GMT  
		Size: 41.1 MB (41101292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948b99fd9aa4a4e910f342b607ef4b97636f303a5418b495c5f688f3651bd008`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0137091501598bb5ba6d1bc7177f360aebd145dd89b4f66b3ffe64d74926807`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7725280cc9bcd2bd19da4451bb3639ebf0acabd14b68b947205d63a6203b12`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd45677a03cb8eac3e45939d3b2e2428af023d360c11760a0e1f40e5c162486`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:19c00963a6fff966ebfdc633b9d4483aa27a9c8e2210b1cfb7d19cc809acf4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:fdb62ff5ce4d44a880046e0ac30933889b4f260236caf923ad945cac941eafbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ff697fa5558306b2afa4e682d4b6380a9738cdbc5d9a2b014c7a0fc241a91f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:27 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 02 Dec 2021 03:59:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:46 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:47 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee142f85ca1332628ddc4730e56d9a9ffeb106490c130516755dd1fe0667b80`  
		Last Modified: Thu, 02 Dec 2021 04:01:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4c913cc766f03be3365121cd0b59e89c01ee7ecdce226860f56e74e5c64a1`  
		Last Modified: Thu, 02 Dec 2021 04:01:13 GMT  
		Size: 44.6 MB (44600031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f7c0c283a9da41259c0ea6a5279ffebabc10018e320e1c71a3e5dbdb197791`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b090f6094bb41cf4a08e9288fd6812b8adb0644e5d793f7c1e6568ef2e97ee0`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2edb36e304a7ada2e1f1b37b3db3c65eff8b1b14000581ef64cb4419daa603e`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c8efda332d8c32ebbcbc7df3b733e6caba419dc9d2f73cbf3214314a38610c`  
		Last Modified: Thu, 02 Dec 2021 04:01:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c4d8a1503ca18c1599eba18e97ea21f228e920c878c5a5f7b1d69be01e1fa028
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74612278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89f734b1ac6c68282b0b172ad767b2a25e273b044473eec4cb7799c1d5d8de7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:13:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 17 Nov 2021 03:13:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:14:00 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:14:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d364f5670abffa7a117aff9a0b2fee592035bd61977f33d207385acea580116`  
		Last Modified: Wed, 17 Nov 2021 03:15:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f10831ac14d41ed907e4f278276ba6e26edbb08cc2e0b5e7bb5d9bcc6ea445`  
		Last Modified: Wed, 17 Nov 2021 03:15:28 GMT  
		Size: 41.1 MB (41101292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948b99fd9aa4a4e910f342b607ef4b97636f303a5418b495c5f688f3651bd008`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0137091501598bb5ba6d1bc7177f360aebd145dd89b4f66b3ffe64d74926807`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7725280cc9bcd2bd19da4451bb3639ebf0acabd14b68b947205d63a6203b12`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd45677a03cb8eac3e45939d3b2e2428af023d360c11760a0e1f40e5c162486`  
		Last Modified: Wed, 17 Nov 2021 03:15:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:c20ed43c7bf849abeeff63506ed5f1661d66c99206882ac062aaa0b633580dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:f9233a3c37fc3a10a128c63ee24d6d710ecb256efcea6470cf1481a88497c14f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54858da96e40fd74eb5ba582c8555ce4d7e6a8d1680922378e6ee368ea7116`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:01 GMT
ENV COUCHDB_VERSION=3.2.0
# Thu, 02 Dec 2021 03:59:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:22 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c15fe4082d8bc4ffe30e811af7011a5a2d3838d55adb4e8ed5726d005543a34`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb97c47e07838a0f160aebf72818bc31d97a769d7ccd3e7cee6e376abeacf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:49 GMT  
		Size: 45.2 MB (45151962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314989771b01cbcd55238bde9274da680acf89f4af915d1afec64fcf4c34caec`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7045cb60dfcd780b48dce1b614f91f784c903bbe054158c9a06884aa16273e`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478ee4109a6eb9fde5f2cb0044c0f3b29b4b7b0a5c2f4f8143f23f65c27d64f`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097296e42e603863e72b649d7e75e356ff483c5062c9438e8022dd6bab7fe6f6`  
		Last Modified: Thu, 02 Dec 2021 04:00:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.0`

```console
$ docker pull couchdb@sha256:c20ed43c7bf849abeeff63506ed5f1661d66c99206882ac062aaa0b633580dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.0` - linux; amd64

```console
$ docker pull couchdb@sha256:f9233a3c37fc3a10a128c63ee24d6d710ecb256efcea6470cf1481a88497c14f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54858da96e40fd74eb5ba582c8555ce4d7e6a8d1680922378e6ee368ea7116`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:01 GMT
ENV COUCHDB_VERSION=3.2.0
# Thu, 02 Dec 2021 03:59:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:22 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c15fe4082d8bc4ffe30e811af7011a5a2d3838d55adb4e8ed5726d005543a34`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb97c47e07838a0f160aebf72818bc31d97a769d7ccd3e7cee6e376abeacf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:49 GMT  
		Size: 45.2 MB (45151962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314989771b01cbcd55238bde9274da680acf89f4af915d1afec64fcf4c34caec`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7045cb60dfcd780b48dce1b614f91f784c903bbe054158c9a06884aa16273e`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478ee4109a6eb9fde5f2cb0044c0f3b29b4b7b0a5c2f4f8143f23f65c27d64f`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097296e42e603863e72b649d7e75e356ff483c5062c9438e8022dd6bab7fe6f6`  
		Last Modified: Thu, 02 Dec 2021 04:00:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:c20ed43c7bf849abeeff63506ed5f1661d66c99206882ac062aaa0b633580dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:f9233a3c37fc3a10a128c63ee24d6d710ecb256efcea6470cf1481a88497c14f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80555600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c54858da96e40fd74eb5ba582c8555ce4d7e6a8d1680922378e6ee368ea7116`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 02 Dec 2021 03:58:31 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 02 Dec 2021 03:58:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:58:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 02 Dec 2021 03:58:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 02 Dec 2021 03:59:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:01 GMT
ENV COUCHDB_VERSION=3.2.0
# Thu, 02 Dec 2021 03:59:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 02 Dec 2021 03:59:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 02 Dec 2021 03:59:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 02 Dec 2021 03:59:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 02 Dec 2021 03:59:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 02 Dec 2021 03:59:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 02 Dec 2021 03:59:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 02 Dec 2021 03:59:22 GMT
EXPOSE 4369 5984 9100
# Thu, 02 Dec 2021 03:59:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc792cd9b52792ad0938a5e388d9be2fc702025774b84de794a632c3e0fc02f0`  
		Last Modified: Thu, 02 Dec 2021 04:00:48 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f87e7045bce9bef72fd9b5bce42edd9ce50aef6775f3694194a1a82c18bf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:47 GMT  
		Size: 6.7 MB (6691479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf38738ecf8be506b95c3b574b38b0c85c9a3cb22aeaac83ebd8440141cc1f82`  
		Last Modified: Thu, 02 Dec 2021 04:00:46 GMT  
		Size: 1.3 MB (1258356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff34fe25c165c10968d4888c5428741e30d459237de0007534284fa46f4577d`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 293.1 KB (293059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c15fe4082d8bc4ffe30e811af7011a5a2d3838d55adb4e8ed5726d005543a34`  
		Last Modified: Thu, 02 Dec 2021 04:00:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb97c47e07838a0f160aebf72818bc31d97a769d7ccd3e7cee6e376abeacf70`  
		Last Modified: Thu, 02 Dec 2021 04:00:49 GMT  
		Size: 45.2 MB (45151962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314989771b01cbcd55238bde9274da680acf89f4af915d1afec64fcf4c34caec`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7045cb60dfcd780b48dce1b614f91f784c903bbe054158c9a06884aa16273e`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478ee4109a6eb9fde5f2cb0044c0f3b29b4b7b0a5c2f4f8143f23f65c27d64f`  
		Last Modified: Thu, 02 Dec 2021 04:00:42 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097296e42e603863e72b649d7e75e356ff483c5062c9438e8022dd6bab7fe6f6`  
		Last Modified: Thu, 02 Dec 2021 04:00:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2030d9ddbcb3ed7120aeeebdc4b089b0d969ad833a1a792297c0797c08bf33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75231135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f19af1927bdddc0bceb963c64ece13b6daa206f047105a8a225966ffa901bcb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:12:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 17 Nov 2021 03:12:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 17 Nov 2021 03:12:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 17 Nov 2021 03:12:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 17 Nov 2021 03:12:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:12:58 GMT
ENV COUCHDB_VERSION=3.2.0
# Wed, 17 Nov 2021 03:12:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 17 Nov 2021 03:13:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 17 Nov 2021 03:13:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 17 Nov 2021 03:13:20 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 17 Nov 2021 03:13:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 17 Nov 2021 03:13:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 17 Nov 2021 03:13:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 03:13:23 GMT
VOLUME [/opt/couchdb/data]
# Wed, 17 Nov 2021 03:13:24 GMT
EXPOSE 4369 5984 9100
# Wed, 17 Nov 2021 03:13:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8586d870cce2b3747aefbecbeb5cf188837dac915ccdda5ebf8c5c24b81b9bc`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719dad8854a23fb371a115a3b5837e840faa6171ae4900b7ba0a5e0eafdcf9a0`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 6.5 MB (6549927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d5a3a703f256b8253d08aba77147e55b76f848724defda52031f9c42e45938`  
		Last Modified: Wed, 17 Nov 2021 03:15:03 GMT  
		Size: 951.1 KB (951146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f099fb3aa5cdc75f08a65ddf68c330305b54f2bf05e0f259daba549c01597f`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 79.9 KB (79874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f10d6d3037836c6c8aa5c296f0f70e385564599dbbafe34639ded032c0e9c6`  
		Last Modified: Wed, 17 Nov 2021 03:15:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95555d888dc786cead48d13eadcb9e9fc7e69b2ad36a9b2bd3ee118469e0dd7c`  
		Last Modified: Wed, 17 Nov 2021 03:15:05 GMT  
		Size: 41.7 MB (41720155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f922085445cffcaed101abaf1c2aed29901463589f4ca49f7be8dac5d197e12f`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0e02dae87f84ebee883fd339617c2324b116a2439ae1a225d22ce5dce53b11`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78060cecbefc0e301d5732233088293e426decdfb208b0e80307ba8c2ad95355`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9c11ef87ada6fcbf0f410909cc4aa6f1d28ed15ac59d1787f5624afdfb073e`  
		Last Modified: Wed, 17 Nov 2021 03:15:00 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
