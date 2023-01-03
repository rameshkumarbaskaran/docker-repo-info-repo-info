## `couchdb:latest`

```console
$ docker pull couchdb@sha256:09d5e033b3bc4bd43746529188747ea1f3171da37b030ed6d1870f69fcfb4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:ae80ecafc17c7ef87bfdb48d69602430d7b9385dc666c073d19817ad0c456583
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91170554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e62b803500e1bbd5105b8bfe4c1c372c5c3a2fbc2dd89826bdf602c86047ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:12:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:12:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:12:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:12:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:12:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:19:31 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:19:31 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:19:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:19:46 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:19:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:19:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:19:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:19:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:19:48 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:19:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124df2a59285701ac46da37ea68eadf201f1aaeff941740c2a82219fb1420d1`  
		Last Modified: Wed, 21 Dec 2022 02:14:44 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e48a2d4b11ae8c7852a1f8cb9d907c4afb6a89aaf43057567457e4da06bf40`  
		Last Modified: Wed, 21 Dec 2022 02:14:43 GMT  
		Size: 5.2 MB (5224267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9541cf86fdc22d25a92ad1da030839badfb05c5c9378e37eb4550d79abbf15a0`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 1.6 MB (1553298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e857bdeea7bd2aae959e4a1b2cd9874c273c8d2a10bc280c72a744258aa7c58`  
		Last Modified: Wed, 21 Dec 2022 02:14:42 GMT  
		Size: 295.6 KB (295570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c62d73e217ebcfa696424d7c95f8610cc5ee5da6240e78a2e23fbea2a71761`  
		Last Modified: Tue, 03 Jan 2023 19:20:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f73fb31abf025dc7d4587f0e5d256a8559b6913815dbfcb7988b3aecc367ff`  
		Last Modified: Tue, 03 Jan 2023 19:20:33 GMT  
		Size: 52.7 MB (52693343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f4bc08af527a609227c3cc58148897c6eec4393bdc0bb263c6665af5d3ff7f`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc36a9ae0123374334b0e35f54b03c04e941986d0a68a82743982df25965498a`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce58becc6cea75ef160aeb1a391f98a5844102b03218d3d1f54338eb3ff579`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba1b55341bd92f3d1c3aba399c6f8fd91459e2bb0dcdb17800c7e94e8746000`  
		Last Modified: Tue, 03 Jan 2023 19:20:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:49a21e5dcf9e588fc373b349539ca9e379a350eea42759624c3ad32f8c78e10b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750df03b82c0c75a7aed000f336407f5b66bbabaef8324520027019ec3924a2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 13:11:20 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 13:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 13:11:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 13:11:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 13:11:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 13:11:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:39:21 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:39:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:39:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:39:34 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:39:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:39:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:39:35 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:39:35 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:39:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefbfc40db6d5af0cfbab91cca273e685d00e52c30d09ba6e0b1adb55fd3af0a`  
		Last Modified: Wed, 21 Dec 2022 13:13:01 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780f10badf54535539e4e78a8ba58731ee743303c0e6173211feb059e2508c5f`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 5.2 MB (5209393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef06153f5ffd47d8e8f92a942d52c62967059deeb398bd21fb15ceb7d893cda`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 1.4 MB (1435931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01da7b4c89acead9bb1a1eedbcbb4b7ac0525cde63886d25b1fe7bb5c2bed55`  
		Last Modified: Wed, 21 Dec 2022 13:13:00 GMT  
		Size: 295.5 KB (295457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc34651a5eb9515b747b593eea303ee2aefc01bc69aebf056ee34ac9b43d707`  
		Last Modified: Tue, 03 Jan 2023 19:40:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801ea55c77f52bf2940d3992c1e0a9d9483e810751da53de238b4967ebf1432`  
		Last Modified: Tue, 03 Jan 2023 19:40:15 GMT  
		Size: 52.5 MB (52549578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf19cf12b569a6f86a0e2db033a8ff1fa36e551e5d84ef62b4bfa9d56c5a171`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c478b465e93eb79e7b6a55a048593b700d9eda9abcf67dda5727f459cb311035`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f826560d2f39c08cacc334458e5b6e7853c36fa0791ebec275d3838144f3d2fb`  
		Last Modified: Tue, 03 Jan 2023 19:40:11 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33ed4cbbdc7265029ae9819d0a957c291a9d810b1f93f8ea4c48faa474860ab`  
		Last Modified: Tue, 03 Jan 2023 19:40:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ba4c174984c3b25d98685b0b13ededd6c61a16018f36443107e7154101fd5c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96678069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7361ea93710f22f0ae06f5dc0be6774dae6c01c1e5603c373ed60bb195500`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:29:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 21 Dec 2022 02:29:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 21 Dec 2022 02:29:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 21 Dec 2022 02:29:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 21 Dec 2022 02:29:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 03 Jan 2023 19:16:26 GMT
ENV COUCHDB_VERSION=3.3.0
# Tue, 03 Jan 2023 19:16:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 03 Jan 2023 19:16:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 03 Jan 2023 19:16:52 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 03 Jan 2023 19:16:53 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 03 Jan 2023 19:16:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 03 Jan 2023 19:16:54 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 03 Jan 2023 19:16:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 03 Jan 2023 19:16:55 GMT
EXPOSE 4369 5984 9100
# Tue, 03 Jan 2023 19:16:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374f33b884f0d41443d7dd8d478822b3c0432ea11623cbab1fa34657180a7bbc`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16aad892fb1ed5cf4e3237ff63b30713b87a6bdc04df9d71e3859ce59d02fae`  
		Last Modified: Wed, 21 Dec 2022 02:30:59 GMT  
		Size: 6.0 MB (6043774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8586df8521e36d772742c7a0f7c39489eec555098f2786118b3befed5dcdd1c`  
		Last Modified: Wed, 21 Dec 2022 02:30:58 GMT  
		Size: 1.5 MB (1509211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5331ac6cc0f5d67df4cd7d92265cc129ba827606c6faaa64e3f999e6574ae28`  
		Last Modified: Wed, 21 Dec 2022 02:30:57 GMT  
		Size: 295.5 KB (295498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b73dcf43d93f122dbe246f346651a1ff55410df3a658b1e3b9778268ab20170`  
		Last Modified: Tue, 03 Jan 2023 19:17:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b1d0a416e6e7b3b920881c65f33e3c2cf75a302e2aa40687f8329a6f2957e`  
		Last Modified: Tue, 03 Jan 2023 19:18:04 GMT  
		Size: 53.6 MB (53553698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adabbda09d6f13fb0b720e21821ecbc30cd7af4cc89cd3af099df336d7abe9d6`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508abd8673a0eeed40af0dba638a039220a61b27fc5e3ca481936544a917a92`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0281c35302e28b1ceaa9d66e4955f2d41692ebe8d761fa94e956c2bc1a8864b`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e017aeaa6d977407bcd1c2085147004bd2e875a5b405624b5c00484d90dd9e44`  
		Last Modified: Tue, 03 Jan 2023 19:17:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
