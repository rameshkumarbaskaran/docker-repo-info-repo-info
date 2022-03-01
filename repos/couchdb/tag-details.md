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
$ docker pull couchdb@sha256:c6694dc1d2fd41678d2eae43ce9e5224e8a5d0b3debfaf3990b3fe208bcccddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a8910eda154fb2670cebf4cc072a18307c893a00d5d3fb39d83e4bd3e3682222
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72523043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ba16fe8039bb0b2a7105771aa4eeb593488cfbf04163e0953ca12d599013a7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:33:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Jan 2022 02:33:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 26 Jan 2022 02:34:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 26 Jan 2022 02:34:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 26 Jan 2022 02:34:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 26 Jan 2022 02:35:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 26 Jan 2022 02:35:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 26 Jan 2022 02:35:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 26 Jan 2022 02:35:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 26 Jan 2022 02:35:55 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 26 Jan 2022 02:35:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 26 Jan 2022 02:35:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 02:35:57 GMT
VOLUME [/opt/couchdb/data]
# Wed, 26 Jan 2022 02:35:58 GMT
EXPOSE 4369 5984 9100
# Wed, 26 Jan 2022 02:35:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22044b828c1c3fec0f66406d0b4914affa5a4c233a8d1a024e840db18c3717ef`  
		Last Modified: Wed, 26 Jan 2022 02:36:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d29a5665e429cb69b2ed2fc2161bcc92bbd0a38d0641b9f514400bd6a0d1`  
		Last Modified: Wed, 26 Jan 2022 02:36:28 GMT  
		Size: 6.5 MB (6549949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6721695d9885aa7b6fb16b43b993093ab01fe96b75f137ad3e7760abf4b73a`  
		Last Modified: Wed, 26 Jan 2022 02:36:27 GMT  
		Size: 951.2 KB (951153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a62fc4090c90113d86eaece64a0ad9474d88e015afa7c449020962191af77f`  
		Last Modified: Wed, 26 Jan 2022 02:36:26 GMT  
		Size: 79.9 KB (79897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a54380ddace77254d3a7eef5aea81131a1c70a1ab560ab9f7c2288b37fe9288`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fba6e4534a2d397cbc79ca495f925dca6384c78ff2a35736ce104f11a50d32`  
		Last Modified: Wed, 26 Jan 2022 02:37:09 GMT  
		Size: 39.0 MB (39011903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fada3abcceccd793c9fb393c41d7993c4af1d1741878cdd3ecbdbb148f4e90`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f971f5f71777b59bf08438f14025fb9610ec4f00314708fa849d239ebbe6fede`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c341e2778945c5566e24ea5c9c95094d1fa0512c377996f005aa6ff413e237a`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1bc007a15a59f1b8238cbe6cd01e252c5d593ba5ea9b6273e249d41730ae68`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:c6694dc1d2fd41678d2eae43ce9e5224e8a5d0b3debfaf3990b3fe208bcccddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a8910eda154fb2670cebf4cc072a18307c893a00d5d3fb39d83e4bd3e3682222
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72523043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ba16fe8039bb0b2a7105771aa4eeb593488cfbf04163e0953ca12d599013a7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:33:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Jan 2022 02:33:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 26 Jan 2022 02:34:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 26 Jan 2022 02:34:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 26 Jan 2022 02:34:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 26 Jan 2022 02:35:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 26 Jan 2022 02:35:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 26 Jan 2022 02:35:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 26 Jan 2022 02:35:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 26 Jan 2022 02:35:55 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 26 Jan 2022 02:35:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 26 Jan 2022 02:35:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 02:35:57 GMT
VOLUME [/opt/couchdb/data]
# Wed, 26 Jan 2022 02:35:58 GMT
EXPOSE 4369 5984 9100
# Wed, 26 Jan 2022 02:35:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22044b828c1c3fec0f66406d0b4914affa5a4c233a8d1a024e840db18c3717ef`  
		Last Modified: Wed, 26 Jan 2022 02:36:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d29a5665e429cb69b2ed2fc2161bcc92bbd0a38d0641b9f514400bd6a0d1`  
		Last Modified: Wed, 26 Jan 2022 02:36:28 GMT  
		Size: 6.5 MB (6549949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6721695d9885aa7b6fb16b43b993093ab01fe96b75f137ad3e7760abf4b73a`  
		Last Modified: Wed, 26 Jan 2022 02:36:27 GMT  
		Size: 951.2 KB (951153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a62fc4090c90113d86eaece64a0ad9474d88e015afa7c449020962191af77f`  
		Last Modified: Wed, 26 Jan 2022 02:36:26 GMT  
		Size: 79.9 KB (79897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a54380ddace77254d3a7eef5aea81131a1c70a1ab560ab9f7c2288b37fe9288`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fba6e4534a2d397cbc79ca495f925dca6384c78ff2a35736ce104f11a50d32`  
		Last Modified: Wed, 26 Jan 2022 02:37:09 GMT  
		Size: 39.0 MB (39011903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fada3abcceccd793c9fb393c41d7993c4af1d1741878cdd3ecbdbb148f4e90`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f971f5f71777b59bf08438f14025fb9610ec4f00314708fa849d239ebbe6fede`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c341e2778945c5566e24ea5c9c95094d1fa0512c377996f005aa6ff413e237a`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1bc007a15a59f1b8238cbe6cd01e252c5d593ba5ea9b6273e249d41730ae68`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:c6694dc1d2fd41678d2eae43ce9e5224e8a5d0b3debfaf3990b3fe208bcccddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:847e1795b0a0d237d9f94be94629e33d811e0104c8c508897958440e1bdcf06c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84517807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10596e5ba2cc278725271cb50463f181896f424dbf4b06da88ce36c6ac59fd18`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:31 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 01 Mar 2022 05:44:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:50 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:51 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10737976dd7f04dffd2c8080cb3ea3718e864fb550e1f8e3354886937546574`  
		Last Modified: Tue, 01 Mar 2022 05:45:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a11c8284534d8d62c430ef5edd0b754f191ed08eb41a89dd12c88cc42f8876e`  
		Last Modified: Tue, 01 Mar 2022 05:45:52 GMT  
		Size: 49.1 MB (49114456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54d99378c788f80c9ecc1d468356b808769ef6e72ba204e99075047a72d9401`  
		Last Modified: Tue, 01 Mar 2022 05:45:47 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8f2f19f0705503827a4fdc361a6f99896e1875fb4fddbf33721a673720aef6`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bef14bec9c81959285cc9e53e3d5699eabb9be169611e2c125bbfd9f261c52b`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd86d7a071c031c015596ab2ec6dcfe4cfdf70bd5082935f1016dc604a66c4f`  
		Last Modified: Tue, 01 Mar 2022 05:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a8910eda154fb2670cebf4cc072a18307c893a00d5d3fb39d83e4bd3e3682222
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72523043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ba16fe8039bb0b2a7105771aa4eeb593488cfbf04163e0953ca12d599013a7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:33:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Jan 2022 02:33:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 26 Jan 2022 02:34:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 26 Jan 2022 02:34:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 26 Jan 2022 02:34:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:35:33 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 26 Jan 2022 02:35:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 26 Jan 2022 02:35:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 26 Jan 2022 02:35:53 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 26 Jan 2022 02:35:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 26 Jan 2022 02:35:55 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 26 Jan 2022 02:35:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 26 Jan 2022 02:35:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 02:35:57 GMT
VOLUME [/opt/couchdb/data]
# Wed, 26 Jan 2022 02:35:58 GMT
EXPOSE 4369 5984 9100
# Wed, 26 Jan 2022 02:35:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22044b828c1c3fec0f66406d0b4914affa5a4c233a8d1a024e840db18c3717ef`  
		Last Modified: Wed, 26 Jan 2022 02:36:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d29a5665e429cb69b2ed2fc2161bcc92bbd0a38d0641b9f514400bd6a0d1`  
		Last Modified: Wed, 26 Jan 2022 02:36:28 GMT  
		Size: 6.5 MB (6549949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6721695d9885aa7b6fb16b43b993093ab01fe96b75f137ad3e7760abf4b73a`  
		Last Modified: Wed, 26 Jan 2022 02:36:27 GMT  
		Size: 951.2 KB (951153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a62fc4090c90113d86eaece64a0ad9474d88e015afa7c449020962191af77f`  
		Last Modified: Wed, 26 Jan 2022 02:36:26 GMT  
		Size: 79.9 KB (79897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a54380ddace77254d3a7eef5aea81131a1c70a1ab560ab9f7c2288b37fe9288`  
		Last Modified: Wed, 26 Jan 2022 02:37:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fba6e4534a2d397cbc79ca495f925dca6384c78ff2a35736ce104f11a50d32`  
		Last Modified: Wed, 26 Jan 2022 02:37:09 GMT  
		Size: 39.0 MB (39011903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fada3abcceccd793c9fb393c41d7993c4af1d1741878cdd3ecbdbb148f4e90`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f971f5f71777b59bf08438f14025fb9610ec4f00314708fa849d239ebbe6fede`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c341e2778945c5566e24ea5c9c95094d1fa0512c377996f005aa6ff413e237a`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1bc007a15a59f1b8238cbe6cd01e252c5d593ba5ea9b6273e249d41730ae68`  
		Last Modified: Wed, 26 Jan 2022 02:37:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:ed531be8e1522c8377f19a656787707fa8fd12478438a502f7a00176ab3a3309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e5d35957f912e3052da1f811da4b4274634b794e1df0d3010f6f4298e1fbf524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234b78f6be5f35bfc91ce645114ad87939e55ef9b84f78cf2c91c8939199661`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:08:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:08:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:08:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:49 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:08:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:09:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:09:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:09:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:09:13 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:09:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:09:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:15 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:09:16 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5456ab3a7062aab6aaa4c5027fb4dc91c3767d0f67b263e0314e2d1676e66b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220168defc5d939708db54c362b659b652e4efa42a9a5e2f9844ede2e235d997`  
		Last Modified: Tue, 01 Mar 2022 02:10:03 GMT  
		Size: 5.2 MB (5207997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041bf56f1d38e036c637a141a5e8ba27091616520de82ac56cb8129ba805a9f2`  
		Last Modified: Tue, 01 Mar 2022 02:10:02 GMT  
		Size: 1.2 MB (1220992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43455933f95ad347fe7fa5ad03bc08e5fb1cd09821bc8ff69066013b0d65ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 79.1 KB (79102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eaa07951d9f39880560eba53b7c5ee98a8615b11aaa36fc64d0b2dd9221a1f`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2a13362604627b4182542d67eea0a400f2c5c6b0b8548b410eff57379a64f5`  
		Last Modified: Tue, 01 Mar 2022 02:10:05 GMT  
		Size: 49.0 MB (49006669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82342528b131665edf57239753899130d3e1bfce68e051171f434f545ad0cc`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176dba8f6fce2e90ee5ab3ff6729e349225a32e72ac8923c3cc9bfbbe56c2c66`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a70be98bbcf4d0e95881552c73a4addb595b993e1200c67db1c24bb08b6fab`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967c6ba0b8d2a7690631426dc0326a8b6b94bb0075165e5055fe117a4fba482`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:92fdcff2acc7fd2cd527494e222e1d706dc01024461fb474ccc1780073d6cce9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88524339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec66a11c353a0bd55a16bc9e3df7c1f8436b50846e164d74bbfc74a0e46883dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 19:37:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 12 Mar 2021 19:37:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 12 Mar 2021 19:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:40:05 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Mar 2021 19:40:07 GMT
ENV TINI_VERSION=0.18.0
# Fri, 12 Mar 2021 19:42:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Fri, 12 Mar 2021 19:42:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Fri, 12 Mar 2021 19:43:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Fri, 12 Mar 2021 19:43:21 GMT
ENV COUCHDB_VERSION=3.1.1
# Fri, 12 Mar 2021 19:43:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Fri, 12 Mar 2021 19:45:52 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Mar 2021 19:45:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 12 Mar 2021 19:46:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 12 Mar 2021 19:46:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 12 Mar 2021 19:46:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 12 Mar 2021 19:46:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 19:46:26 GMT
VOLUME [/opt/couchdb/data]
# Fri, 12 Mar 2021 19:46:33 GMT
EXPOSE 4369 5984 9100
# Fri, 12 Mar 2021 19:46:38 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5946aff0873110b0478f9227873604e78c676af18e0dfcd1792e829269a797`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459905054f02704e0526a50655150b20d4241a97be26f9464d997ec614782ce4`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 7.6 MB (7597596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fddccd01ec6846d36516b8583c310ef4af1b4df7e5ff47e9a5433bb7b1a6f1`  
		Last Modified: Fri, 12 Mar 2021 19:50:06 GMT  
		Size: 1.1 MB (1116351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9cab3ce9525a6a24f4c1b583168b57d95c20d76c59eeec12e2e975f5bd6a1`  
		Last Modified: Fri, 12 Mar 2021 19:50:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09139ee3a9e5b64209b42b240aa99578fbf71585ea905c2eefccbd7c73cf31f3`  
		Last Modified: Fri, 12 Mar 2021 19:50:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604a9876a71e095a20526d121d304d331595fb5d6a437dad6550e85747fde6e`  
		Last Modified: Fri, 12 Mar 2021 19:50:08 GMT  
		Size: 49.3 MB (49275194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0c6539d199f069a602efa1cda1b72fb94ecd2bbc595b97f2df4e19ccb3e6`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc447f4db7d5f4bbcd08dc6219def27d69bad292d2775d1e9cf212ca4277a1be`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524070537bcddee5cbfd0aef55fc47bd89ae91bd05bd1919fec7dc348e00d28`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c9fce47f6e73a0786f841a42845cb7d720417f296a19ce54fd978cb02f0e`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:e2939ef40dfb498317b8cf1b9180f173ee4ca619ad7ceb5f1ef4f4bf45d2b2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:ca79518cf7009d4d0f0469fddac30481acbbc5c04dd9e4f68698c9fb209b2379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bd847d3676edaaf93238ec7616aeef0990d0d366c26034bf10cefa563907f7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:13 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 05:44:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:29 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30360495bdc30a76fa2b700246ad48767cacf9d445a76c0a5794bb67ffe1ff8a`  
		Last Modified: Tue, 01 Mar 2022 05:45:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66f25dd672892d6a4f8fe8ada5c2761d4e92d82b846c1b3c0c324f20736ea7`  
		Last Modified: Tue, 01 Mar 2022 05:45:36 GMT  
		Size: 44.6 MB (44600228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa53bb7e951e99619bfc60a13fe5fdb4627934cd960bfa56b8d32e1f7f7ff4`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec6b081df4af00c592f2a0bb9b8d16a2e164dbc88510fac16341ee519f518f`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae1344cc973a946de72a34a50f850ee96245021b199d90b188174ded7f00e3`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc978b9768eef46e866245b0df9c77957340e1ec7cc6935b34d15c38ce7623f5`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:708648024b9924a68102ed3187be35a99995452b829a2f6e87a723554056c2c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74611841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821856bdb89c0bce9f85a9c54245f21b887bf078c082fe51d2c7852aa3226ad6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:33:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Jan 2022 02:33:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 26 Jan 2022 02:34:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 26 Jan 2022 02:34:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 26 Jan 2022 02:34:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:56 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 26 Jan 2022 02:34:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 26 Jan 2022 02:35:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 26 Jan 2022 02:35:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 26 Jan 2022 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 26 Jan 2022 02:35:20 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 26 Jan 2022 02:35:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 26 Jan 2022 02:35:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 02:35:22 GMT
VOLUME [/opt/couchdb/data]
# Wed, 26 Jan 2022 02:35:23 GMT
EXPOSE 4369 5984 9100
# Wed, 26 Jan 2022 02:35:24 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22044b828c1c3fec0f66406d0b4914affa5a4c233a8d1a024e840db18c3717ef`  
		Last Modified: Wed, 26 Jan 2022 02:36:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d29a5665e429cb69b2ed2fc2161bcc92bbd0a38d0641b9f514400bd6a0d1`  
		Last Modified: Wed, 26 Jan 2022 02:36:28 GMT  
		Size: 6.5 MB (6549949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6721695d9885aa7b6fb16b43b993093ab01fe96b75f137ad3e7760abf4b73a`  
		Last Modified: Wed, 26 Jan 2022 02:36:27 GMT  
		Size: 951.2 KB (951153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a62fc4090c90113d86eaece64a0ad9474d88e015afa7c449020962191af77f`  
		Last Modified: Wed, 26 Jan 2022 02:36:26 GMT  
		Size: 79.9 KB (79897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7404580d7e167cdbd29f2ce61354a7f004a70675be67a9001ad17488742bff5`  
		Last Modified: Wed, 26 Jan 2022 02:36:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5e29ee260a1e4625f1137ede4535f1ef5fc43d48d42a315f12cff7ca49df47`  
		Last Modified: Wed, 26 Jan 2022 02:36:53 GMT  
		Size: 41.1 MB (41100706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c77f5b3a74ef0d03e9a4a279aa595162ad32c6279a100e5067a9c4ebac29a68`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1146c2b9a27b9224a2020c308f8d0ba764fa8bd7d5014851489c675cfe23633d`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c08ff015700215b1925adb4bb349adde5a16b0a83ff117b8aef0ebe887060e`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a076695fd1fc16a303c5f2cf86b8c0db9bfd6df3894238bf8961b4cb99547c`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:e2939ef40dfb498317b8cf1b9180f173ee4ca619ad7ceb5f1ef4f4bf45d2b2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:ca79518cf7009d4d0f0469fddac30481acbbc5c04dd9e4f68698c9fb209b2379
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80003576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bd847d3676edaaf93238ec7616aeef0990d0d366c26034bf10cefa563907f7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:44:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:44:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:44:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:13 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 01 Mar 2022 05:44:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:44:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:44:28 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 01 Mar 2022 05:44:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:44:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:44:29 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:44:29 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:44:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132993eb143d25686acdeb919d14985e8a65255f56170cc91230c350b203efa`  
		Last Modified: Tue, 01 Mar 2022 05:45:35 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50404ca1e1b3d297bb3c53a42e386f090eaa10f2d4db26fa324c39a836a18ea2`  
		Last Modified: Tue, 01 Mar 2022 05:45:34 GMT  
		Size: 6.7 MB (6691238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185b4237a163f4ee3d4cbb14cccd38dbfff817f923da22f90651149905d5957f`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 1.3 MB (1258328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a7c7c6b65c07b5de14a76f367630dcdc1f47fb75f959826b67e019b0617ec2`  
		Last Modified: Tue, 01 Mar 2022 05:45:33 GMT  
		Size: 293.0 KB (293032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30360495bdc30a76fa2b700246ad48767cacf9d445a76c0a5794bb67ffe1ff8a`  
		Last Modified: Tue, 01 Mar 2022 05:45:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c66f25dd672892d6a4f8fe8ada5c2761d4e92d82b846c1b3c0c324f20736ea7`  
		Last Modified: Tue, 01 Mar 2022 05:45:36 GMT  
		Size: 44.6 MB (44600228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fa53bb7e951e99619bfc60a13fe5fdb4627934cd960bfa56b8d32e1f7f7ff4`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec6b081df4af00c592f2a0bb9b8d16a2e164dbc88510fac16341ee519f518f`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bae1344cc973a946de72a34a50f850ee96245021b199d90b188174ded7f00e3`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc978b9768eef46e866245b0df9c77957340e1ec7cc6935b34d15c38ce7623f5`  
		Last Modified: Tue, 01 Mar 2022 05:45:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:708648024b9924a68102ed3187be35a99995452b829a2f6e87a723554056c2c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74611841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821856bdb89c0bce9f85a9c54245f21b887bf078c082fe51d2c7852aa3226ad6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:33:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 26 Jan 2022 02:33:56 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 26 Jan 2022 02:34:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 26 Jan 2022 02:34:09 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 26 Jan 2022 02:34:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:34:56 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 26 Jan 2022 02:34:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 26 Jan 2022 02:35:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 26 Jan 2022 02:35:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 26 Jan 2022 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 26 Jan 2022 02:35:20 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 26 Jan 2022 02:35:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 26 Jan 2022 02:35:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 26 Jan 2022 02:35:22 GMT
VOLUME [/opt/couchdb/data]
# Wed, 26 Jan 2022 02:35:23 GMT
EXPOSE 4369 5984 9100
# Wed, 26 Jan 2022 02:35:24 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22044b828c1c3fec0f66406d0b4914affa5a4c233a8d1a024e840db18c3717ef`  
		Last Modified: Wed, 26 Jan 2022 02:36:29 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0132d29a5665e429cb69b2ed2fc2161bcc92bbd0a38d0641b9f514400bd6a0d1`  
		Last Modified: Wed, 26 Jan 2022 02:36:28 GMT  
		Size: 6.5 MB (6549949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6721695d9885aa7b6fb16b43b993093ab01fe96b75f137ad3e7760abf4b73a`  
		Last Modified: Wed, 26 Jan 2022 02:36:27 GMT  
		Size: 951.2 KB (951153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a62fc4090c90113d86eaece64a0ad9474d88e015afa7c449020962191af77f`  
		Last Modified: Wed, 26 Jan 2022 02:36:26 GMT  
		Size: 79.9 KB (79897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7404580d7e167cdbd29f2ce61354a7f004a70675be67a9001ad17488742bff5`  
		Last Modified: Wed, 26 Jan 2022 02:36:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5e29ee260a1e4625f1137ede4535f1ef5fc43d48d42a315f12cff7ca49df47`  
		Last Modified: Wed, 26 Jan 2022 02:36:53 GMT  
		Size: 41.1 MB (41100706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c77f5b3a74ef0d03e9a4a279aa595162ad32c6279a100e5067a9c4ebac29a68`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1146c2b9a27b9224a2020c308f8d0ba764fa8bd7d5014851489c675cfe23633d`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c08ff015700215b1925adb4bb349adde5a16b0a83ff117b8aef0ebe887060e`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a076695fd1fc16a303c5f2cf86b8c0db9bfd6df3894238bf8961b4cb99547c`  
		Last Modified: Wed, 26 Jan 2022 02:36:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:d8bdd60ebf94a02a6bf98e26145b6f7ad1c113e63aef0130df6130656af13779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e5d35957f912e3052da1f811da4b4274634b794e1df0d3010f6f4298e1fbf524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234b78f6be5f35bfc91ce645114ad87939e55ef9b84f78cf2c91c8939199661`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:08:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:08:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:08:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:49 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:08:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:09:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:09:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:09:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:09:13 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:09:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:09:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:15 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:09:16 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5456ab3a7062aab6aaa4c5027fb4dc91c3767d0f67b263e0314e2d1676e66b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220168defc5d939708db54c362b659b652e4efa42a9a5e2f9844ede2e235d997`  
		Last Modified: Tue, 01 Mar 2022 02:10:03 GMT  
		Size: 5.2 MB (5207997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041bf56f1d38e036c637a141a5e8ba27091616520de82ac56cb8129ba805a9f2`  
		Last Modified: Tue, 01 Mar 2022 02:10:02 GMT  
		Size: 1.2 MB (1220992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43455933f95ad347fe7fa5ad03bc08e5fb1cd09821bc8ff69066013b0d65ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 79.1 KB (79102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eaa07951d9f39880560eba53b7c5ee98a8615b11aaa36fc64d0b2dd9221a1f`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2a13362604627b4182542d67eea0a400f2c5c6b0b8548b410eff57379a64f5`  
		Last Modified: Tue, 01 Mar 2022 02:10:05 GMT  
		Size: 49.0 MB (49006669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82342528b131665edf57239753899130d3e1bfce68e051171f434f545ad0cc`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176dba8f6fce2e90ee5ab3ff6729e349225a32e72ac8923c3cc9bfbbe56c2c66`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a70be98bbcf4d0e95881552c73a4addb595b993e1200c67db1c24bb08b6fab`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967c6ba0b8d2a7690631426dc0326a8b6b94bb0075165e5055fe117a4fba482`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:d8bdd60ebf94a02a6bf98e26145b6f7ad1c113e63aef0130df6130656af13779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e5d35957f912e3052da1f811da4b4274634b794e1df0d3010f6f4298e1fbf524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234b78f6be5f35bfc91ce645114ad87939e55ef9b84f78cf2c91c8939199661`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:08:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:08:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:08:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:49 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:08:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:09:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:09:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:09:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:09:13 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:09:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:09:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:15 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:09:16 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5456ab3a7062aab6aaa4c5027fb4dc91c3767d0f67b263e0314e2d1676e66b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220168defc5d939708db54c362b659b652e4efa42a9a5e2f9844ede2e235d997`  
		Last Modified: Tue, 01 Mar 2022 02:10:03 GMT  
		Size: 5.2 MB (5207997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041bf56f1d38e036c637a141a5e8ba27091616520de82ac56cb8129ba805a9f2`  
		Last Modified: Tue, 01 Mar 2022 02:10:02 GMT  
		Size: 1.2 MB (1220992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43455933f95ad347fe7fa5ad03bc08e5fb1cd09821bc8ff69066013b0d65ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 79.1 KB (79102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eaa07951d9f39880560eba53b7c5ee98a8615b11aaa36fc64d0b2dd9221a1f`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2a13362604627b4182542d67eea0a400f2c5c6b0b8548b410eff57379a64f5`  
		Last Modified: Tue, 01 Mar 2022 02:10:05 GMT  
		Size: 49.0 MB (49006669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82342528b131665edf57239753899130d3e1bfce68e051171f434f545ad0cc`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176dba8f6fce2e90ee5ab3ff6729e349225a32e72ac8923c3cc9bfbbe56c2c66`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a70be98bbcf4d0e95881552c73a4addb595b993e1200c67db1c24bb08b6fab`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967c6ba0b8d2a7690631426dc0326a8b6b94bb0075165e5055fe117a4fba482`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ed531be8e1522c8377f19a656787707fa8fd12478438a502f7a00176ab3a3309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:822d0f6a1fa1a4468bc77928901cd80cfb9b0679382255660da873c4570f0ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87438641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f265241b13e4aafb4f0fda52c6626eb1885d026244944902e2188c4765c30f0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:43:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 05:43:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 05:43:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 05:43:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 05:43:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:43:28 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 05:43:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 05:43:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 05:43:42 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 05:43:43 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 05:43:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 05:43:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 05:43:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 05:43:44 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 05:43:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f736067abe3ec6aa7995ab61efa1d9a2b46b4c6a43e237fb15d6ba10bccc8a0`  
		Last Modified: Tue, 01 Mar 2022 05:45:13 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cf0cd8366d641805527862400e1bce25dfe0e4d75301bfca351f6cb51adf42`  
		Last Modified: Tue, 01 Mar 2022 05:45:12 GMT  
		Size: 5.2 MB (5223244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765d7966078499cee66919d4eae6c448903398520afd4a9af50e628602308dd`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 1.6 MB (1553184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0aa553e191057af86f122b236ee318ab2840b814e55f6ed1f843dbf2734c3df`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 295.5 KB (295513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6836a13a921ed1c7d33495e61fbf8c4110efd124ba364aa65719668d915df6`  
		Last Modified: Tue, 01 Mar 2022 05:45:11 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670b70ba1f6cf592b77e0fbb8feefaa5d19731d115a8f40e5d7ad276b7572c0`  
		Last Modified: Tue, 01 Mar 2022 05:45:15 GMT  
		Size: 49.0 MB (48993167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abf74c316c94beb45bf67044c6219f3205152bbc1a595080a4d646cad125055`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91336f088c386950fab72a2eff4fb6e543ea167051299e920860f25763ddad4c`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec02748684ecc64a7c390d3f95f2556ed75c995c0018dca6d3a5bcb4f10222e`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b0fab1478c6789e174467f18aec4753c1a77109436988456425cef86c95aa`  
		Last Modified: Tue, 01 Mar 2022 05:45:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e5d35957f912e3052da1f811da4b4274634b794e1df0d3010f6f4298e1fbf524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234b78f6be5f35bfc91ce645114ad87939e55ef9b84f78cf2c91c8939199661`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:08:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:08:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:08:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:49 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:08:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:09:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:09:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:09:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:09:13 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:09:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:09:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:15 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:09:16 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5456ab3a7062aab6aaa4c5027fb4dc91c3767d0f67b263e0314e2d1676e66b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220168defc5d939708db54c362b659b652e4efa42a9a5e2f9844ede2e235d997`  
		Last Modified: Tue, 01 Mar 2022 02:10:03 GMT  
		Size: 5.2 MB (5207997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041bf56f1d38e036c637a141a5e8ba27091616520de82ac56cb8129ba805a9f2`  
		Last Modified: Tue, 01 Mar 2022 02:10:02 GMT  
		Size: 1.2 MB (1220992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43455933f95ad347fe7fa5ad03bc08e5fb1cd09821bc8ff69066013b0d65ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 79.1 KB (79102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eaa07951d9f39880560eba53b7c5ee98a8615b11aaa36fc64d0b2dd9221a1f`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2a13362604627b4182542d67eea0a400f2c5c6b0b8548b410eff57379a64f5`  
		Last Modified: Tue, 01 Mar 2022 02:10:05 GMT  
		Size: 49.0 MB (49006669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82342528b131665edf57239753899130d3e1bfce68e051171f434f545ad0cc`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176dba8f6fce2e90ee5ab3ff6729e349225a32e72ac8923c3cc9bfbbe56c2c66`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a70be98bbcf4d0e95881552c73a4addb595b993e1200c67db1c24bb08b6fab`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967c6ba0b8d2a7690631426dc0326a8b6b94bb0075165e5055fe117a4fba482`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:92fdcff2acc7fd2cd527494e222e1d706dc01024461fb474ccc1780073d6cce9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88524339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec66a11c353a0bd55a16bc9e3df7c1f8436b50846e164d74bbfc74a0e46883dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 19:37:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 12 Mar 2021 19:37:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 12 Mar 2021 19:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:40:05 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Mar 2021 19:40:07 GMT
ENV TINI_VERSION=0.18.0
# Fri, 12 Mar 2021 19:42:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Fri, 12 Mar 2021 19:42:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Fri, 12 Mar 2021 19:43:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Fri, 12 Mar 2021 19:43:21 GMT
ENV COUCHDB_VERSION=3.1.1
# Fri, 12 Mar 2021 19:43:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Fri, 12 Mar 2021 19:45:52 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Mar 2021 19:45:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 12 Mar 2021 19:46:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 12 Mar 2021 19:46:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 12 Mar 2021 19:46:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 12 Mar 2021 19:46:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 19:46:26 GMT
VOLUME [/opt/couchdb/data]
# Fri, 12 Mar 2021 19:46:33 GMT
EXPOSE 4369 5984 9100
# Fri, 12 Mar 2021 19:46:38 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5946aff0873110b0478f9227873604e78c676af18e0dfcd1792e829269a797`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459905054f02704e0526a50655150b20d4241a97be26f9464d997ec614782ce4`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 7.6 MB (7597596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fddccd01ec6846d36516b8583c310ef4af1b4df7e5ff47e9a5433bb7b1a6f1`  
		Last Modified: Fri, 12 Mar 2021 19:50:06 GMT  
		Size: 1.1 MB (1116351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9cab3ce9525a6a24f4c1b583168b57d95c20d76c59eeec12e2e975f5bd6a1`  
		Last Modified: Fri, 12 Mar 2021 19:50:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09139ee3a9e5b64209b42b240aa99578fbf71585ea905c2eefccbd7c73cf31f3`  
		Last Modified: Fri, 12 Mar 2021 19:50:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604a9876a71e095a20526d121d304d331595fb5d6a437dad6550e85747fde6e`  
		Last Modified: Fri, 12 Mar 2021 19:50:08 GMT  
		Size: 49.3 MB (49275194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0c6539d199f069a602efa1cda1b72fb94ecd2bbc595b97f2df4e19ccb3e6`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc447f4db7d5f4bbcd08dc6219def27d69bad292d2775d1e9cf212ca4277a1be`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524070537bcddee5cbfd0aef55fc47bd89ae91bd05bd1919fec7dc348e00d28`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c9fce47f6e73a0786f841a42845cb7d720417f296a19ce54fd978cb02f0e`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
