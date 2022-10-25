## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ef21112377bd5df6dacafc462d02123bb108814064cd81218f0d08972d76240a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:c976642fe0bfed70d8481293702fb32f3fcfdac0950f239f069c45daf356be80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87546176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994fdcd357aad6beca4304e782ea3a7229ecba3e960b971af51f441d5239efa6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:53:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 05 Oct 2022 01:53:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 05 Oct 2022 01:53:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 05 Oct 2022 01:53:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 05 Oct 2022 01:53:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 01:53:52 GMT
ENV COUCHDB_VERSION=3.2.2
# Wed, 05 Oct 2022 01:53:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 05 Oct 2022 01:54:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 05 Oct 2022 01:54:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 05 Oct 2022 01:54:07 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Wed, 05 Oct 2022 01:54:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 05 Oct 2022 01:54:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 05 Oct 2022 01:54:07 GMT
VOLUME [/opt/couchdb/data]
# Wed, 05 Oct 2022 01:54:07 GMT
EXPOSE 4369 5984 9100
# Wed, 05 Oct 2022 01:54:08 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50830c09adfb39841093b2852fab7bea49db61e68b181aa91f648c74e4fc3e0b`  
		Last Modified: Wed, 05 Oct 2022 01:55:48 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c824d0a873bcb23ad01abb767d707f3b6f081cb277e8c122922cf47a303ff355`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 5.2 MB (5224222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133338a2a25751a2cd2f69feab9b8f6df2ba1b6de10397de86f03bc729671988`  
		Last Modified: Wed, 05 Oct 2022 01:55:47 GMT  
		Size: 1.6 MB (1553266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161d047ac6b618b63098da64cfe365c125d4f1c4fc18d6d0b37766316b72fa5a`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 295.6 KB (295590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b72fa5f875f42c5673b59fc12f6c245e49d4f7bd00feb59be64338f8f1c1dde`  
		Last Modified: Wed, 05 Oct 2022 01:55:46 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3091ee36bd0f70205d0e31b10bbc8e7b208bc234f6cc6f3cc3f0783949ac4b2a`  
		Last Modified: Wed, 05 Oct 2022 01:55:49 GMT  
		Size: 49.0 MB (49045858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122333888771cf497009bb9f5b7ea36ab9f42124c802dd3cf7a288063965b0d1`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d4e15d74c555d6cda273d6a13afd6916c978a8e719f392f84b1db3428b35f0`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295483f6e8ed514ad1436fee874f7dc7bc996719cab0933ba483af2464386e`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57950f766fe983d4ac0415aa1846954b52f66e8fd0abf3db9a77c7b829f523c2`  
		Last Modified: Wed, 05 Oct 2022 01:55:44 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c6321e09db67f1dc549f0b88f47eecc661909a13df3091aa1c15dc5d612f4517
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86079388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e938314e7b989894f554622a99e2f8542531fc53907665142c0c627e40c9b19e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:39:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 08:39:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 08:40:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 08:40:04 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 08:40:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:40:08 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 08:40:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 08:40:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 08:40:21 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 08:40:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 08:40:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:40:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 08:40:22 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 08:40:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d23f6b06399e9bd464a459acdc4c5c668a317ab7231cffc5f27eac8199f72d`  
		Last Modified: Tue, 25 Oct 2022 08:41:41 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41831134def03097216279113f63f0641dd6a106c6dacab0e44d5bcdc04a1119`  
		Last Modified: Tue, 25 Oct 2022 08:41:40 GMT  
		Size: 5.2 MB (5210639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee1e386badd8830f59d5c191976d414ec54a54f881c953cfca494ecda5c7865`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 1.4 MB (1436840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaddafba9ea8080d1b03937df4a483be6b90049f69d6461597f6075f9fada1b`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 296.2 KB (296190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7f6063276c306b3277136f1c37858808bb1b8026c5c7a1e497e58f6dd92c4`  
		Last Modified: Tue, 25 Oct 2022 08:41:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046b19d7b61b708513238e91d0d40922a634436964b676dcf00d19e2272ad729`  
		Last Modified: Tue, 25 Oct 2022 08:41:42 GMT  
		Size: 49.1 MB (49064645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fd5becf524c2c60380cbf6dc372680e6a8dee96da0ce01757ab6364c8b48`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72aeecb31de29af7924212303cfa1abac0569b9ff4d929e23086918d4da3ea0`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bdd8deb1668c6e9c4ba1901de4d52f1c741db7ccb81d3d6c0e6ce2f3586770`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395df954ad376ace92f48219e833cb04343fb6c72c1fd8379844422774bc0031`  
		Last Modified: Tue, 25 Oct 2022 08:41:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:573d9f033093c79429f5843b2a1845aa5b5c8701a3d8cefa3bf152f2f1bce088
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93234836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5a5850a83bb2bf101cfa7b9bb0103dcd391c3ab793dfc9e5f8b95a52a137e1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:06:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 25 Oct 2022 06:06:53 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 25 Oct 2022 06:07:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 25 Oct 2022 06:07:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 25 Oct 2022 06:07:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:07:25 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 25 Oct 2022 06:07:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Oct 2022 06:07:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 25 Oct 2022 06:07:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 25 Oct 2022 06:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 06:07:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 06:07:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Oct 2022 06:07:51 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Oct 2022 06:07:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff951905b209915c9a1df313fb16760244fac7d51fb589c9f6916ce989182da9`  
		Last Modified: Tue, 25 Oct 2022 06:08:19 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712443240476010b6c006ffa2d932751e6a255ccf2bd596dd1cbcc186e0fb5e`  
		Last Modified: Tue, 25 Oct 2022 06:08:18 GMT  
		Size: 6.0 MB (6045421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f46f597f71b51e9ffcdfe3f8cf65b3491a0ebfa511eb59f6e3ff451da97250`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 1.5 MB (1509798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bfa28563276da0d4ed400b10397b96bda9f17d00515d9d055228fbfe9fbd4`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 296.1 KB (296141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07bf29c43588bb1a85d84ad57b455a4deabff4dd3e3f08943c1856fbb833c10`  
		Last Modified: Tue, 25 Oct 2022 06:08:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60206143ed7547d03f4b565c8a75579fee7d7f413101d112a407be39258a70b1`  
		Last Modified: Tue, 25 Oct 2022 06:08:24 GMT  
		Size: 50.1 MB (50086243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbc205c67ebc790386455cf628f98ef1efd3d8e904116ebcb13960e8f60824`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef686fe48f6ff7d5d868d3cd987b968a42d57e6aa75fe77fee0e915ebcffa789`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62513520123c4ad12dd19aa946930c527f1ed47cf745829a9e3edcc51f36cbe`  
		Last Modified: Tue, 25 Oct 2022 06:08:14 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1f67b4e79b0ebb1f15b26357f97af2973fc445cb7a1f41c9460ce5821d26`  
		Last Modified: Tue, 25 Oct 2022 06:08:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
