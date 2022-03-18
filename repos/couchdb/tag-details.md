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
$ docker pull couchdb@sha256:9787f9488dc4fef67fde95c588a774f80ec55950b5a20a91e9f793ff40ba16a9
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
$ docker pull couchdb@sha256:9787f9488dc4fef67fde95c588a774f80ec55950b5a20a91e9f793ff40ba16a9
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
$ docker pull couchdb@sha256:9787f9488dc4fef67fde95c588a774f80ec55950b5a20a91e9f793ff40ba16a9
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
$ docker pull couchdb@sha256:756bfeed22ecd18c5787a762e5f93a0a578f5e244835bc536002f8e9a5dbb318
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
$ docker pull couchdb@sha256:910fc1e2c4c95579028118dd6ac80d60b5e34135807caae0b3b759bbd3f7558f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93156878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af7fca6e0cc3d261c23d2b84ee250be1f1b53921c4e9e0cbe68619f6680d109`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 07:26:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 02 Mar 2022 07:26:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 02 Mar 2022 07:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 02 Mar 2022 07:27:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 02 Mar 2022 07:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:58 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 02 Mar 2022 07:28:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 02 Mar 2022 07:28:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 02 Mar 2022 07:28:51 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 02 Mar 2022 07:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Mar 2022 07:28:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 02 Mar 2022 07:28:58 GMT
VOLUME [/opt/couchdb/data]
# Wed, 02 Mar 2022 07:29:00 GMT
EXPOSE 4369 5984 9100
# Wed, 02 Mar 2022 07:29:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8e3b76def43005a4bad42db196a1af1f2e2a7571c562c402c6d5fab6b670fa`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b0be0220579d9a54e06e2c75add9959107db00f235745c5094280a38a0d66`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 6.0 MB (6043478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512718ccfd18b0d0555389092336b2345a224cf8741ecacd8cf0aefc13b56ad`  
		Last Modified: Wed, 02 Mar 2022 07:29:27 GMT  
		Size: 1.5 MB (1509175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0d3da23acf1804501e1d63f82b765ae6fff0d46daf6a85271bcd6485a2ac20`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079334cb185001d3836b007108d00ae394390595a59b51c946ddd3d6dcf748a0`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92f960d7dfa5dfa0ceedc8b12ecda5b51ee8a82a42811c576537fc6009f5741`  
		Last Modified: Wed, 02 Mar 2022 07:29:31 GMT  
		Size: 50.0 MB (50028599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b23d01fac8298a56be32af0a4f1e0bf7e2e80a89587293ae671d5da9499b9`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6739034ddd8a12ca87e41304cc52cea8bd9691c386759d8e336397f0e513e7`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641352460d612b4811a827f1e46eaca3d2bee21b5a9fe04e849a4461856173c`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea3c3c346c9f62d3d3be2c25ca691732d97c66ac1dd786e1befc38de0d67a1`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:e45ee411bf737932c635be7b876033a8650036105a1d748e4ade3a612c1aad7e
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
$ docker pull couchdb@sha256:e45ee411bf737932c635be7b876033a8650036105a1d748e4ade3a612c1aad7e
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
$ docker pull couchdb@sha256:756bfeed22ecd18c5787a762e5f93a0a578f5e244835bc536002f8e9a5dbb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

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
$ docker pull couchdb@sha256:910fc1e2c4c95579028118dd6ac80d60b5e34135807caae0b3b759bbd3f7558f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93156878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af7fca6e0cc3d261c23d2b84ee250be1f1b53921c4e9e0cbe68619f6680d109`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 07:26:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 02 Mar 2022 07:26:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 02 Mar 2022 07:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 02 Mar 2022 07:27:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 02 Mar 2022 07:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:58 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 02 Mar 2022 07:28:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 02 Mar 2022 07:28:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 02 Mar 2022 07:28:51 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 02 Mar 2022 07:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Mar 2022 07:28:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 02 Mar 2022 07:28:58 GMT
VOLUME [/opt/couchdb/data]
# Wed, 02 Mar 2022 07:29:00 GMT
EXPOSE 4369 5984 9100
# Wed, 02 Mar 2022 07:29:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8e3b76def43005a4bad42db196a1af1f2e2a7571c562c402c6d5fab6b670fa`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b0be0220579d9a54e06e2c75add9959107db00f235745c5094280a38a0d66`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 6.0 MB (6043478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512718ccfd18b0d0555389092336b2345a224cf8741ecacd8cf0aefc13b56ad`  
		Last Modified: Wed, 02 Mar 2022 07:29:27 GMT  
		Size: 1.5 MB (1509175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0d3da23acf1804501e1d63f82b765ae6fff0d46daf6a85271bcd6485a2ac20`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079334cb185001d3836b007108d00ae394390595a59b51c946ddd3d6dcf748a0`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92f960d7dfa5dfa0ceedc8b12ecda5b51ee8a82a42811c576537fc6009f5741`  
		Last Modified: Wed, 02 Mar 2022 07:29:31 GMT  
		Size: 50.0 MB (50028599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b23d01fac8298a56be32af0a4f1e0bf7e2e80a89587293ae671d5da9499b9`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6739034ddd8a12ca87e41304cc52cea8bd9691c386759d8e336397f0e513e7`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641352460d612b4811a827f1e46eaca3d2bee21b5a9fe04e849a4461856173c`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea3c3c346c9f62d3d3be2c25ca691732d97c66ac1dd786e1befc38de0d67a1`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.1`

```console
$ docker pull couchdb@sha256:756bfeed22ecd18c5787a762e5f93a0a578f5e244835bc536002f8e9a5dbb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

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
$ docker pull couchdb@sha256:910fc1e2c4c95579028118dd6ac80d60b5e34135807caae0b3b759bbd3f7558f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93156878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af7fca6e0cc3d261c23d2b84ee250be1f1b53921c4e9e0cbe68619f6680d109`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 07:26:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 02 Mar 2022 07:26:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 02 Mar 2022 07:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 02 Mar 2022 07:27:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 02 Mar 2022 07:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:58 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 02 Mar 2022 07:28:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 02 Mar 2022 07:28:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 02 Mar 2022 07:28:51 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 02 Mar 2022 07:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Mar 2022 07:28:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 02 Mar 2022 07:28:58 GMT
VOLUME [/opt/couchdb/data]
# Wed, 02 Mar 2022 07:29:00 GMT
EXPOSE 4369 5984 9100
# Wed, 02 Mar 2022 07:29:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8e3b76def43005a4bad42db196a1af1f2e2a7571c562c402c6d5fab6b670fa`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b0be0220579d9a54e06e2c75add9959107db00f235745c5094280a38a0d66`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 6.0 MB (6043478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512718ccfd18b0d0555389092336b2345a224cf8741ecacd8cf0aefc13b56ad`  
		Last Modified: Wed, 02 Mar 2022 07:29:27 GMT  
		Size: 1.5 MB (1509175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0d3da23acf1804501e1d63f82b765ae6fff0d46daf6a85271bcd6485a2ac20`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079334cb185001d3836b007108d00ae394390595a59b51c946ddd3d6dcf748a0`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92f960d7dfa5dfa0ceedc8b12ecda5b51ee8a82a42811c576537fc6009f5741`  
		Last Modified: Wed, 02 Mar 2022 07:29:31 GMT  
		Size: 50.0 MB (50028599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b23d01fac8298a56be32af0a4f1e0bf7e2e80a89587293ae671d5da9499b9`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6739034ddd8a12ca87e41304cc52cea8bd9691c386759d8e336397f0e513e7`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641352460d612b4811a827f1e46eaca3d2bee21b5a9fe04e849a4461856173c`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea3c3c346c9f62d3d3be2c25ca691732d97c66ac1dd786e1befc38de0d67a1`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:756bfeed22ecd18c5787a762e5f93a0a578f5e244835bc536002f8e9a5dbb318
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
$ docker pull couchdb@sha256:910fc1e2c4c95579028118dd6ac80d60b5e34135807caae0b3b759bbd3f7558f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93156878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af7fca6e0cc3d261c23d2b84ee250be1f1b53921c4e9e0cbe68619f6680d109`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 07:26:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 02 Mar 2022 07:26:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 02 Mar 2022 07:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 02 Mar 2022 07:27:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 02 Mar 2022 07:27:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:27:58 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Wed, 02 Mar 2022 07:28:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 02 Mar 2022 07:28:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 02 Mar 2022 07:28:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 02 Mar 2022 07:28:51 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 02 Mar 2022 07:28:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 02 Mar 2022 07:28:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 02 Mar 2022 07:28:58 GMT
VOLUME [/opt/couchdb/data]
# Wed, 02 Mar 2022 07:29:00 GMT
EXPOSE 4369 5984 9100
# Wed, 02 Mar 2022 07:29:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8e3b76def43005a4bad42db196a1af1f2e2a7571c562c402c6d5fab6b670fa`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b0be0220579d9a54e06e2c75add9959107db00f235745c5094280a38a0d66`  
		Last Modified: Wed, 02 Mar 2022 07:29:28 GMT  
		Size: 6.0 MB (6043478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512718ccfd18b0d0555389092336b2345a224cf8741ecacd8cf0aefc13b56ad`  
		Last Modified: Wed, 02 Mar 2022 07:29:27 GMT  
		Size: 1.5 MB (1509175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0d3da23acf1804501e1d63f82b765ae6fff0d46daf6a85271bcd6485a2ac20`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 295.6 KB (295572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079334cb185001d3836b007108d00ae394390595a59b51c946ddd3d6dcf748a0`  
		Last Modified: Wed, 02 Mar 2022 07:29:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92f960d7dfa5dfa0ceedc8b12ecda5b51ee8a82a42811c576537fc6009f5741`  
		Last Modified: Wed, 02 Mar 2022 07:29:31 GMT  
		Size: 50.0 MB (50028599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b23d01fac8298a56be32af0a4f1e0bf7e2e80a89587293ae671d5da9499b9`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6739034ddd8a12ca87e41304cc52cea8bd9691c386759d8e336397f0e513e7`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4641352460d612b4811a827f1e46eaca3d2bee21b5a9fe04e849a4461856173c`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dea3c3c346c9f62d3d3be2c25ca691732d97c66ac1dd786e1befc38de0d67a1`  
		Last Modified: Wed, 02 Mar 2022 07:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
