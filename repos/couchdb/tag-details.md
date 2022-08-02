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
$ docker pull couchdb@sha256:ca12901aa1fa2651b1683b48fadfc26e40230561c9024deec4e819d7ecf68b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:00fed57ff785e7ac767ea7b6be760c37c46e6e5d21ca58a0f9fb77ae6723e184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa222f0cc6f4de0864706232a3867e177a73d6a7de728b8fb202642ce5d9943`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:19:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:19:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:19:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:20:07 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 18:20:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:20:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 18:20:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:20:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:20:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:20:27 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:20:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8deafc71857a9493fb9dd4af9571fb327c17dd1fa535e3f5aaeec54d2c214`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708e66027fb9c6c15781b54b737eea4cad93510f07571ba8ddf09ba4babb008`  
		Last Modified: Tue, 02 Aug 2022 18:21:09 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f196edfed9de53ef5d6b6b372582e5620a03ac87d5dfec6fe05deafb2a7ab`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 1.3 MB (1258357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01265ddc12047f0874faef77f33e75cc4e88e0bb5b26de2bb85c07db6fe72953`  
		Last Modified: Tue, 02 Aug 2022 18:21:07 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fec3e024ef16a53cd064f9f1244b6921e7738bf7b2b3dfb97a0ed095bfbfe0`  
		Last Modified: Tue, 02 Aug 2022 18:21:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc703ac5bb8039b84abc537530bac13e4d4167c4a3b1fcdaa13ffa92b61b5fd7`  
		Last Modified: Tue, 02 Aug 2022 18:21:26 GMT  
		Size: 49.1 MB (49126970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f9be5f2279f106b5a17c49af174b21bff8673538627b0aa13cad4fc5c40fc`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bbbae87d1dc7e76b42c2e0f1890bdac0bb8eb624407589ea2648e4ba298b64`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74483b23bfda67a7ab55582f356d2e4b0ef6d6c32c3fdae334ea535172916752`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6821c33fc76a0123172734c9488ec9c21dd8642715c38f5178cc4e7b866162`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4d27419ac8548d5697a69904409954b075eff3c85f130b61dc24734fd0b02da1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279fccb83aaef6ba53144c947958807e2351eb025796431109aac874500def7a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:54:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:54:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:54:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:54:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:54:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:55:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 01:55:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:55:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:55:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:55:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:55:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:55:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:55:28 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:55:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbb2e29bd8913eeb0828eb30855bd8099016bbccb4656f7a85247aff324e02`  
		Last Modified: Tue, 02 Aug 2022 01:56:25 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192633bb64010e741a13bef0a4f95d38e465792d3a07eac67e0d4b6f66c33390`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 6.6 MB (6557119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf7a28b3a5155810d9966f34c4a4c0331f957d4458341c8e3683e074b5e376`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 951.2 KB (951168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ee939b6b94519e887f775efeeb8e38f7c6753a794a56656ca795a354437b8e`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 80.0 KB (79958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b37c305cd45c9aef4b1a597fc55fa8d3fa7e4f9897fa193afd26353b0cb078`  
		Last Modified: Tue, 02 Aug 2022 01:56:40 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457dc458bba7846a4079f786880799c5f68a2fd7d81ae7624bb5173592aba1ea`  
		Last Modified: Tue, 02 Aug 2022 01:56:42 GMT  
		Size: 39.0 MB (39023658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ba602d04fc89ca241f7f72d4089adde2e712789f5cb20abdc08e0b3631f3ef`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd028aa13d7ec3c819b6f22e8e4abba06c33d9114c0ab5aea6477dd04611ded`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbccfa07785ac255a6a516db7d50c754ca2a142980319abb5e4825d021e9677`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a882295cd756e516c322046d3077da8fb85a77e71fcc9babb9d16f54b81e3c`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ca12901aa1fa2651b1683b48fadfc26e40230561c9024deec4e819d7ecf68b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:00fed57ff785e7ac767ea7b6be760c37c46e6e5d21ca58a0f9fb77ae6723e184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa222f0cc6f4de0864706232a3867e177a73d6a7de728b8fb202642ce5d9943`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:19:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:19:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:19:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:20:07 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 18:20:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:20:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 18:20:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:20:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:20:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:20:27 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:20:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8deafc71857a9493fb9dd4af9571fb327c17dd1fa535e3f5aaeec54d2c214`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708e66027fb9c6c15781b54b737eea4cad93510f07571ba8ddf09ba4babb008`  
		Last Modified: Tue, 02 Aug 2022 18:21:09 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f196edfed9de53ef5d6b6b372582e5620a03ac87d5dfec6fe05deafb2a7ab`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 1.3 MB (1258357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01265ddc12047f0874faef77f33e75cc4e88e0bb5b26de2bb85c07db6fe72953`  
		Last Modified: Tue, 02 Aug 2022 18:21:07 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fec3e024ef16a53cd064f9f1244b6921e7738bf7b2b3dfb97a0ed095bfbfe0`  
		Last Modified: Tue, 02 Aug 2022 18:21:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc703ac5bb8039b84abc537530bac13e4d4167c4a3b1fcdaa13ffa92b61b5fd7`  
		Last Modified: Tue, 02 Aug 2022 18:21:26 GMT  
		Size: 49.1 MB (49126970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f9be5f2279f106b5a17c49af174b21bff8673538627b0aa13cad4fc5c40fc`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bbbae87d1dc7e76b42c2e0f1890bdac0bb8eb624407589ea2648e4ba298b64`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74483b23bfda67a7ab55582f356d2e4b0ef6d6c32c3fdae334ea535172916752`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6821c33fc76a0123172734c9488ec9c21dd8642715c38f5178cc4e7b866162`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4d27419ac8548d5697a69904409954b075eff3c85f130b61dc24734fd0b02da1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279fccb83aaef6ba53144c947958807e2351eb025796431109aac874500def7a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:54:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:54:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:54:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:54:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:54:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:55:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 01:55:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:55:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:55:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:55:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:55:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:55:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:55:28 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:55:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbb2e29bd8913eeb0828eb30855bd8099016bbccb4656f7a85247aff324e02`  
		Last Modified: Tue, 02 Aug 2022 01:56:25 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192633bb64010e741a13bef0a4f95d38e465792d3a07eac67e0d4b6f66c33390`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 6.6 MB (6557119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf7a28b3a5155810d9966f34c4a4c0331f957d4458341c8e3683e074b5e376`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 951.2 KB (951168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ee939b6b94519e887f775efeeb8e38f7c6753a794a56656ca795a354437b8e`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 80.0 KB (79958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b37c305cd45c9aef4b1a597fc55fa8d3fa7e4f9897fa193afd26353b0cb078`  
		Last Modified: Tue, 02 Aug 2022 01:56:40 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457dc458bba7846a4079f786880799c5f68a2fd7d81ae7624bb5173592aba1ea`  
		Last Modified: Tue, 02 Aug 2022 01:56:42 GMT  
		Size: 39.0 MB (39023658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ba602d04fc89ca241f7f72d4089adde2e712789f5cb20abdc08e0b3631f3ef`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd028aa13d7ec3c819b6f22e8e4abba06c33d9114c0ab5aea6477dd04611ded`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbccfa07785ac255a6a516db7d50c754ca2a142980319abb5e4825d021e9677`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a882295cd756e516c322046d3077da8fb85a77e71fcc9babb9d16f54b81e3c`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ca12901aa1fa2651b1683b48fadfc26e40230561c9024deec4e819d7ecf68b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:00fed57ff785e7ac767ea7b6be760c37c46e6e5d21ca58a0f9fb77ae6723e184
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84524080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa222f0cc6f4de0864706232a3867e177a73d6a7de728b8fb202642ce5d9943`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:19:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:19:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:19:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:20:07 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 18:20:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:20:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:20:26 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 18:20:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:20:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:20:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:20:27 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:20:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8deafc71857a9493fb9dd4af9571fb327c17dd1fa535e3f5aaeec54d2c214`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708e66027fb9c6c15781b54b737eea4cad93510f07571ba8ddf09ba4babb008`  
		Last Modified: Tue, 02 Aug 2022 18:21:09 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f196edfed9de53ef5d6b6b372582e5620a03ac87d5dfec6fe05deafb2a7ab`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 1.3 MB (1258357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01265ddc12047f0874faef77f33e75cc4e88e0bb5b26de2bb85c07db6fe72953`  
		Last Modified: Tue, 02 Aug 2022 18:21:07 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fec3e024ef16a53cd064f9f1244b6921e7738bf7b2b3dfb97a0ed095bfbfe0`  
		Last Modified: Tue, 02 Aug 2022 18:21:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc703ac5bb8039b84abc537530bac13e4d4167c4a3b1fcdaa13ffa92b61b5fd7`  
		Last Modified: Tue, 02 Aug 2022 18:21:26 GMT  
		Size: 49.1 MB (49126970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f9be5f2279f106b5a17c49af174b21bff8673538627b0aa13cad4fc5c40fc`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bbbae87d1dc7e76b42c2e0f1890bdac0bb8eb624407589ea2648e4ba298b64`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74483b23bfda67a7ab55582f356d2e4b0ef6d6c32c3fdae334ea535172916752`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6821c33fc76a0123172734c9488ec9c21dd8642715c38f5178cc4e7b866162`  
		Last Modified: Tue, 02 Aug 2022 18:21:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4d27419ac8548d5697a69904409954b075eff3c85f130b61dc24734fd0b02da1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72533193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279fccb83aaef6ba53144c947958807e2351eb025796431109aac874500def7a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:54:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:54:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:54:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:54:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:54:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:55:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 02 Aug 2022 01:55:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:55:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:55:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:55:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:55:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 02 Aug 2022 01:55:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:55:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:55:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:55:28 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:55:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbb2e29bd8913eeb0828eb30855bd8099016bbccb4656f7a85247aff324e02`  
		Last Modified: Tue, 02 Aug 2022 01:56:25 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192633bb64010e741a13bef0a4f95d38e465792d3a07eac67e0d4b6f66c33390`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 6.6 MB (6557119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf7a28b3a5155810d9966f34c4a4c0331f957d4458341c8e3683e074b5e376`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 951.2 KB (951168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ee939b6b94519e887f775efeeb8e38f7c6753a794a56656ca795a354437b8e`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 80.0 KB (79958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b37c305cd45c9aef4b1a597fc55fa8d3fa7e4f9897fa193afd26353b0cb078`  
		Last Modified: Tue, 02 Aug 2022 01:56:40 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457dc458bba7846a4079f786880799c5f68a2fd7d81ae7624bb5173592aba1ea`  
		Last Modified: Tue, 02 Aug 2022 01:56:42 GMT  
		Size: 39.0 MB (39023658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ba602d04fc89ca241f7f72d4089adde2e712789f5cb20abdc08e0b3631f3ef`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd028aa13d7ec3c819b6f22e8e4abba06c33d9114c0ab5aea6477dd04611ded`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbccfa07785ac255a6a516db7d50c754ca2a142980319abb5e4825d021e9677`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a882295cd756e516c322046d3077da8fb85a77e71fcc9babb9d16f54b81e3c`  
		Last Modified: Tue, 02 Aug 2022 01:56:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:1b1108a42af5f6276fe032adf69f94eb5809dc61e8419af353d507b492e40cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:51c570af32e3e38f0340c7f877e3d6293806b287b5c7f0b2384ae92d1c4ab38f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3554da7e97670f838d6148f5379c8c0a50d38db1e7a08a3d0919971cee0fe766`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:18:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:18:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:18:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:18:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:03 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 18:19:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:19:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 18:19:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:19:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:19:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:19:20 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:19:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba008c5417ddd884ac31c06e8477ed1c51aaae71d18348213a7e5c4733f27126`  
		Last Modified: Tue, 02 Aug 2022 18:20:48 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f992d762b0ee06214c3ee95f2e1c01ec3e979f8df505e081c974fc1b8fdd9`  
		Last Modified: Tue, 02 Aug 2022 18:20:47 GMT  
		Size: 5.2 MB (5224198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b808c60d05957e9ac5537c470816d315cf91d19167448f0753d406e37ea5ec9`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 1.6 MB (1553273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540df1b1f892c29da1bec00c365b0f311f36dfe80c1fc1748c5c2fcfac5ba970`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 295.6 KB (295561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb3cee704b6a5e2d08b3e54b732ce160cd3b85ce52d22df6e2d4ab43be147c`  
		Last Modified: Tue, 02 Aug 2022 18:20:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d91b4d3132238a8db164b5eacd442a54aebb9e8ef13675dd5921a1ed3ace4d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:49 GMT  
		Size: 49.0 MB (49042037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84737806b6353f840b06e63e4e6a8ef83bbc5218959f1eab925e3c4eafd3a21`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af06c642ed032413d823b53e744f702cded73eb8048c42116e491d6208fd2d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2093006093e8cfbaff58d9cae02c71fbdb26c789966b26c41de6e4b202de1881`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d483b7339e66ea7dbc3c932b864efa1bb362adcd9b316d0df762893834ae10`  
		Last Modified: Tue, 02 Aug 2022 18:20:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2cc537fd46496d460ec408ea389dd4cc27c180608e89c59761c4682d6dac0cbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85622605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faece9a6aa805f3e9d71e0136a8c7add2db196a28de98b26dc652d2eb88bf4ee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:53:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:53:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:53:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:53:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:53:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:29 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:53:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:53:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:53:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:53:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:53:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:53:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:53:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:53:50 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:53:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f36ebccf7ea0ca6c4e42a56d3e761f51620dde7809ff4cd6c9c47f4d92dda45`  
		Last Modified: Tue, 02 Aug 2022 01:56:00 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57988538f1066bad59a075d99704fbc2ed80b7f279168e98ae1ac061cddb0e54`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 5.2 MB (5207882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6f84207bfc6da3f978a06e64089cd163b0b7cfce56aa03f050fffcf6aa1fa`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 1.2 MB (1221114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f79004f600a1443f5dd0ab501f8d2726ae96d9790d635ef946c8ab58fc7639`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 79.2 KB (79204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea246a4776bb764303aebd0c230598840bac0a3067bf67395be8aa1d4a9796c0`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec05def1afee67aa528ce2ecc14afe3dd947292160af59436483a6eb8307d8`  
		Last Modified: Tue, 02 Aug 2022 01:56:02 GMT  
		Size: 49.1 MB (49053054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f205452c1f21b508f3eff3ca454e831b24598073851b7c10ad77092021c63b80`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb0d06feb8b8d747a8a616d3dbdb4dbff7f3d1c07726fc7fabbd0d857588a65`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833640fe1553f0d57940524d810c11944b07d0171e7979f091beca62d8c235a2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c60df208533e1fc53978ad88b63060ba603756eef0b46beaa35572ff7fc1aa2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1e403730c20e44b3297dc2ca59567dc4f7f8608ea517c016cf6b814fa428f6f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9532ba1899566dfcf8498c068f3eca6b79c8afa3fae5d939c52255a7ae9d96b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:45:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:46:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:46:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:46:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:24 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:46:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:46:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:46:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:46:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:46:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:46:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:46:51 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:46:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd616d47d2a8f573397f07010fd143095697a31e5f728cac1c1b7269738c47a`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1a77f89868067efb94d63fe88604742503d85f515b25f7ab84711a016d3e4f`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 6.0 MB (6043687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f741e9865e3fdcb0bd227a5993c271ef87a11ea1804cdbbdd3814773c085fd4`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 1.5 MB (1509129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a56ea83b77070cf87034a857804e0e5dc6e22a75e16d352364a0c6f2cf81cd`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 295.5 KB (295465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe12fc56262eb1a9961df421373e9e93f9755a2e423207066c543f023b488f7`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cf6274a3105c304db4a54d429807a6d97294428538c809f791158d3a610942`  
		Last Modified: Tue, 02 Aug 2022 01:47:24 GMT  
		Size: 50.1 MB (50081019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48855ad409841498cce766b60da4e1cd5f59a6da57e69031b5cb1e70944c7e06`  
		Last Modified: Tue, 02 Aug 2022 01:47:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93f33d896f43831a247689b5fe6b3c85972c92c57c27a55ae2ca50fd89216c`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2efe54a8f4ae1598aa0cad697c24d96e9bd6701de850e533e452cb0ddc5df62`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa6fb130ed09e3914ae920a1e5cd0affdd896fa22de827e2b222afb58a04e4`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:f612a6eaffb4ab2cf1bbdbae7b7c57a361cac74ed8242f40b7675428ff232873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:70bb65280f47c2e234e967a6088e1f94dc469732a51b21fa65572d5583e06a5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab998de590bbcb12b3a39c1b550f6219c4c6b82fe5c9ebe41b4f08349a0ebe2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:19:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:19:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:19:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:46 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 02 Aug 2022 18:19:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:20:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:20:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:20:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:20:01 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 02 Aug 2022 18:20:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:20:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:20:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:20:02 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:20:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8deafc71857a9493fb9dd4af9571fb327c17dd1fa535e3f5aaeec54d2c214`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708e66027fb9c6c15781b54b737eea4cad93510f07571ba8ddf09ba4babb008`  
		Last Modified: Tue, 02 Aug 2022 18:21:09 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f196edfed9de53ef5d6b6b372582e5620a03ac87d5dfec6fe05deafb2a7ab`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 1.3 MB (1258357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01265ddc12047f0874faef77f33e75cc4e88e0bb5b26de2bb85c07db6fe72953`  
		Last Modified: Tue, 02 Aug 2022 18:21:07 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6afea4ee44eb1b3bb5496911c2aaeb6df8de94c677fa6b1581b0ce9d37bf8cc`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd052e404d35e28d187102e2ad0dd610f39074bb2ea57909015e9f569c61f828`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 44.6 MB (44612374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec9b1d60e24a119570ad5f3556d29f39a554f5dd3cfbc491daf76f92c4bc987`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4adc22edd48cc60a25821e8e60a2e4af32135657c7662f66f76dba4428c51a`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c5b198eb0bb880b85f8acc205005cf337bf74ff637e10776dec96594a08162`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368f712416cb92c41e9b5ec6400888d6ae6884d07123db569059f973d9959b97`  
		Last Modified: Tue, 02 Aug 2022 18:21:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2a4273e1c132ca7d51a766e8924507ecb2fa433447ad227a94b9ebd735b1bb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a97102b89f803528279a50487b76e5cf67c9db39b6e50eaaa512ca9c876c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:54:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:54:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:54:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:54:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:54:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:23 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 02 Aug 2022 01:54:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:54:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:54:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:54:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:54:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 02 Aug 2022 01:54:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:54:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:54:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:54:48 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:54:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbb2e29bd8913eeb0828eb30855bd8099016bbccb4656f7a85247aff324e02`  
		Last Modified: Tue, 02 Aug 2022 01:56:25 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192633bb64010e741a13bef0a4f95d38e465792d3a07eac67e0d4b6f66c33390`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 6.6 MB (6557119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf7a28b3a5155810d9966f34c4a4c0331f957d4458341c8e3683e074b5e376`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 951.2 KB (951168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ee939b6b94519e887f775efeeb8e38f7c6753a794a56656ca795a354437b8e`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 80.0 KB (79958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c1e56d17f55a93521148990b2f560a6401fc7bd06faec0f376e4a453cac903`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f09ea26de4b63303321d6c9ea720b4e8116a8cdc261bc1dd0060fc58d7ebd3c`  
		Last Modified: Tue, 02 Aug 2022 01:56:26 GMT  
		Size: 41.1 MB (41112637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9354706eff555a86dfa9987feb6ca7ce1176d000dab12847b18f8349666d2d`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84a0c3df2496088046a0d00a1ef05a3c452627e37d79a60db80c6499c634cf`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6541aa9f62e6abcfcca9b7d5155e5f035aef4d612c0aad572e69ee1ad006956a`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7e0309716beca4eb00c072e238149bb9236708376e0b9b80ae104c047b960f`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:f612a6eaffb4ab2cf1bbdbae7b7c57a361cac74ed8242f40b7675428ff232873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:70bb65280f47c2e234e967a6088e1f94dc469732a51b21fa65572d5583e06a5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80009488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab998de590bbcb12b3a39c1b550f6219c4c6b82fe5c9ebe41b4f08349a0ebe2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:19:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:19:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:19:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:46 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 02 Aug 2022 18:19:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:20:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:20:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:20:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:20:01 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 02 Aug 2022 18:20:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:20:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:20:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:20:02 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:20:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8deafc71857a9493fb9dd4af9571fb327c17dd1fa535e3f5aaeec54d2c214`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9708e66027fb9c6c15781b54b737eea4cad93510f07571ba8ddf09ba4babb008`  
		Last Modified: Tue, 02 Aug 2022 18:21:09 GMT  
		Size: 6.7 MB (6698648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567f196edfed9de53ef5d6b6b372582e5620a03ac87d5dfec6fe05deafb2a7ab`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 1.3 MB (1258357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01265ddc12047f0874faef77f33e75cc4e88e0bb5b26de2bb85c07db6fe72953`  
		Last Modified: Tue, 02 Aug 2022 18:21:07 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6afea4ee44eb1b3bb5496911c2aaeb6df8de94c677fa6b1581b0ce9d37bf8cc`  
		Last Modified: Tue, 02 Aug 2022 18:21:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd052e404d35e28d187102e2ad0dd610f39074bb2ea57909015e9f569c61f828`  
		Last Modified: Tue, 02 Aug 2022 18:21:10 GMT  
		Size: 44.6 MB (44612374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec9b1d60e24a119570ad5f3556d29f39a554f5dd3cfbc491daf76f92c4bc987`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4adc22edd48cc60a25821e8e60a2e4af32135657c7662f66f76dba4428c51a`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c5b198eb0bb880b85f8acc205005cf337bf74ff637e10776dec96594a08162`  
		Last Modified: Tue, 02 Aug 2022 18:21:05 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368f712416cb92c41e9b5ec6400888d6ae6884d07123db569059f973d9959b97`  
		Last Modified: Tue, 02 Aug 2022 18:21:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f2a4273e1c132ca7d51a766e8924507ecb2fa433447ad227a94b9ebd735b1bb2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a97102b89f803528279a50487b76e5cf67c9db39b6e50eaaa512ca9c876c9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:03 GMT
ADD file:d973e057fdca9166fb9f39e73d7d5d4ca8ac2af6a55813580bf14a13cef4c159 in / 
# Tue, 02 Aug 2022 00:41:04 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:54:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:54:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:54:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:54:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:54:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:54:23 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 02 Aug 2022 01:54:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:54:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:54:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:54:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:54:45 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 02 Aug 2022 01:54:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:54:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:54:47 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:54:48 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:54:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6d588874b4737b02fc84169cf7d3d1d70f20c7f5dbd1ddfe27de4aff25e23314`  
		Last Modified: Tue, 02 Aug 2022 00:46:56 GMT  
		Size: 25.9 MB (25914363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbb2e29bd8913eeb0828eb30855bd8099016bbccb4656f7a85247aff324e02`  
		Last Modified: Tue, 02 Aug 2022 01:56:25 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192633bb64010e741a13bef0a4f95d38e465792d3a07eac67e0d4b6f66c33390`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 6.6 MB (6557119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf7a28b3a5155810d9966f34c4a4c0331f957d4458341c8e3683e074b5e376`  
		Last Modified: Tue, 02 Aug 2022 01:56:24 GMT  
		Size: 951.2 KB (951168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ee939b6b94519e887f775efeeb8e38f7c6753a794a56656ca795a354437b8e`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 80.0 KB (79958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c1e56d17f55a93521148990b2f560a6401fc7bd06faec0f376e4a453cac903`  
		Last Modified: Tue, 02 Aug 2022 01:56:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f09ea26de4b63303321d6c9ea720b4e8116a8cdc261bc1dd0060fc58d7ebd3c`  
		Last Modified: Tue, 02 Aug 2022 01:56:26 GMT  
		Size: 41.1 MB (41112637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9354706eff555a86dfa9987feb6ca7ce1176d000dab12847b18f8349666d2d`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84a0c3df2496088046a0d00a1ef05a3c452627e37d79a60db80c6499c634cf`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6541aa9f62e6abcfcca9b7d5155e5f035aef4d612c0aad572e69ee1ad006956a`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7e0309716beca4eb00c072e238149bb9236708376e0b9b80ae104c047b960f`  
		Last Modified: Tue, 02 Aug 2022 01:56:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:1b1108a42af5f6276fe032adf69f94eb5809dc61e8419af353d507b492e40cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:51c570af32e3e38f0340c7f877e3d6293806b287b5c7f0b2384ae92d1c4ab38f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3554da7e97670f838d6148f5379c8c0a50d38db1e7a08a3d0919971cee0fe766`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:18:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:18:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:18:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:18:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:03 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 18:19:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:19:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 18:19:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:19:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:19:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:19:20 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:19:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba008c5417ddd884ac31c06e8477ed1c51aaae71d18348213a7e5c4733f27126`  
		Last Modified: Tue, 02 Aug 2022 18:20:48 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f992d762b0ee06214c3ee95f2e1c01ec3e979f8df505e081c974fc1b8fdd9`  
		Last Modified: Tue, 02 Aug 2022 18:20:47 GMT  
		Size: 5.2 MB (5224198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b808c60d05957e9ac5537c470816d315cf91d19167448f0753d406e37ea5ec9`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 1.6 MB (1553273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540df1b1f892c29da1bec00c365b0f311f36dfe80c1fc1748c5c2fcfac5ba970`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 295.6 KB (295561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb3cee704b6a5e2d08b3e54b732ce160cd3b85ce52d22df6e2d4ab43be147c`  
		Last Modified: Tue, 02 Aug 2022 18:20:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d91b4d3132238a8db164b5eacd442a54aebb9e8ef13675dd5921a1ed3ace4d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:49 GMT  
		Size: 49.0 MB (49042037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84737806b6353f840b06e63e4e6a8ef83bbc5218959f1eab925e3c4eafd3a21`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af06c642ed032413d823b53e744f702cded73eb8048c42116e491d6208fd2d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2093006093e8cfbaff58d9cae02c71fbdb26c789966b26c41de6e4b202de1881`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d483b7339e66ea7dbc3c932b864efa1bb362adcd9b316d0df762893834ae10`  
		Last Modified: Tue, 02 Aug 2022 18:20:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2cc537fd46496d460ec408ea389dd4cc27c180608e89c59761c4682d6dac0cbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85622605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faece9a6aa805f3e9d71e0136a8c7add2db196a28de98b26dc652d2eb88bf4ee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:53:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:53:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:53:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:53:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:53:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:29 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:53:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:53:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:53:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:53:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:53:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:53:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:53:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:53:50 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:53:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f36ebccf7ea0ca6c4e42a56d3e761f51620dde7809ff4cd6c9c47f4d92dda45`  
		Last Modified: Tue, 02 Aug 2022 01:56:00 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57988538f1066bad59a075d99704fbc2ed80b7f279168e98ae1ac061cddb0e54`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 5.2 MB (5207882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6f84207bfc6da3f978a06e64089cd163b0b7cfce56aa03f050fffcf6aa1fa`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 1.2 MB (1221114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f79004f600a1443f5dd0ab501f8d2726ae96d9790d635ef946c8ab58fc7639`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 79.2 KB (79204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea246a4776bb764303aebd0c230598840bac0a3067bf67395be8aa1d4a9796c0`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec05def1afee67aa528ce2ecc14afe3dd947292160af59436483a6eb8307d8`  
		Last Modified: Tue, 02 Aug 2022 01:56:02 GMT  
		Size: 49.1 MB (49053054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f205452c1f21b508f3eff3ca454e831b24598073851b7c10ad77092021c63b80`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb0d06feb8b8d747a8a616d3dbdb4dbff7f3d1c07726fc7fabbd0d857588a65`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833640fe1553f0d57940524d810c11944b07d0171e7979f091beca62d8c235a2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c60df208533e1fc53978ad88b63060ba603756eef0b46beaa35572ff7fc1aa2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1e403730c20e44b3297dc2ca59567dc4f7f8608ea517c016cf6b814fa428f6f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9532ba1899566dfcf8498c068f3eca6b79c8afa3fae5d939c52255a7ae9d96b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:45:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:46:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:46:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:46:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:24 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:46:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:46:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:46:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:46:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:46:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:46:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:46:51 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:46:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd616d47d2a8f573397f07010fd143095697a31e5f728cac1c1b7269738c47a`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1a77f89868067efb94d63fe88604742503d85f515b25f7ab84711a016d3e4f`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 6.0 MB (6043687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f741e9865e3fdcb0bd227a5993c271ef87a11ea1804cdbbdd3814773c085fd4`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 1.5 MB (1509129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a56ea83b77070cf87034a857804e0e5dc6e22a75e16d352364a0c6f2cf81cd`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 295.5 KB (295465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe12fc56262eb1a9961df421373e9e93f9755a2e423207066c543f023b488f7`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cf6274a3105c304db4a54d429807a6d97294428538c809f791158d3a610942`  
		Last Modified: Tue, 02 Aug 2022 01:47:24 GMT  
		Size: 50.1 MB (50081019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48855ad409841498cce766b60da4e1cd5f59a6da57e69031b5cb1e70944c7e06`  
		Last Modified: Tue, 02 Aug 2022 01:47:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93f33d896f43831a247689b5fe6b3c85972c92c57c27a55ae2ca50fd89216c`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2efe54a8f4ae1598aa0cad697c24d96e9bd6701de850e533e452cb0ddc5df62`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa6fb130ed09e3914ae920a1e5cd0affdd896fa22de827e2b222afb58a04e4`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:1b1108a42af5f6276fe032adf69f94eb5809dc61e8419af353d507b492e40cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:51c570af32e3e38f0340c7f877e3d6293806b287b5c7f0b2384ae92d1c4ab38f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3554da7e97670f838d6148f5379c8c0a50d38db1e7a08a3d0919971cee0fe766`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:18:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:18:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:18:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:18:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:03 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 18:19:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:19:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 18:19:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:19:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:19:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:19:20 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:19:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba008c5417ddd884ac31c06e8477ed1c51aaae71d18348213a7e5c4733f27126`  
		Last Modified: Tue, 02 Aug 2022 18:20:48 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f992d762b0ee06214c3ee95f2e1c01ec3e979f8df505e081c974fc1b8fdd9`  
		Last Modified: Tue, 02 Aug 2022 18:20:47 GMT  
		Size: 5.2 MB (5224198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b808c60d05957e9ac5537c470816d315cf91d19167448f0753d406e37ea5ec9`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 1.6 MB (1553273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540df1b1f892c29da1bec00c365b0f311f36dfe80c1fc1748c5c2fcfac5ba970`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 295.6 KB (295561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb3cee704b6a5e2d08b3e54b732ce160cd3b85ce52d22df6e2d4ab43be147c`  
		Last Modified: Tue, 02 Aug 2022 18:20:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d91b4d3132238a8db164b5eacd442a54aebb9e8ef13675dd5921a1ed3ace4d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:49 GMT  
		Size: 49.0 MB (49042037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84737806b6353f840b06e63e4e6a8ef83bbc5218959f1eab925e3c4eafd3a21`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af06c642ed032413d823b53e744f702cded73eb8048c42116e491d6208fd2d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2093006093e8cfbaff58d9cae02c71fbdb26c789966b26c41de6e4b202de1881`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d483b7339e66ea7dbc3c932b864efa1bb362adcd9b316d0df762893834ae10`  
		Last Modified: Tue, 02 Aug 2022 18:20:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2cc537fd46496d460ec408ea389dd4cc27c180608e89c59761c4682d6dac0cbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85622605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faece9a6aa805f3e9d71e0136a8c7add2db196a28de98b26dc652d2eb88bf4ee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:53:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:53:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:53:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:53:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:53:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:29 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:53:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:53:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:53:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:53:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:53:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:53:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:53:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:53:50 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:53:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f36ebccf7ea0ca6c4e42a56d3e761f51620dde7809ff4cd6c9c47f4d92dda45`  
		Last Modified: Tue, 02 Aug 2022 01:56:00 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57988538f1066bad59a075d99704fbc2ed80b7f279168e98ae1ac061cddb0e54`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 5.2 MB (5207882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6f84207bfc6da3f978a06e64089cd163b0b7cfce56aa03f050fffcf6aa1fa`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 1.2 MB (1221114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f79004f600a1443f5dd0ab501f8d2726ae96d9790d635ef946c8ab58fc7639`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 79.2 KB (79204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea246a4776bb764303aebd0c230598840bac0a3067bf67395be8aa1d4a9796c0`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec05def1afee67aa528ce2ecc14afe3dd947292160af59436483a6eb8307d8`  
		Last Modified: Tue, 02 Aug 2022 01:56:02 GMT  
		Size: 49.1 MB (49053054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f205452c1f21b508f3eff3ca454e831b24598073851b7c10ad77092021c63b80`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb0d06feb8b8d747a8a616d3dbdb4dbff7f3d1c07726fc7fabbd0d857588a65`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833640fe1553f0d57940524d810c11944b07d0171e7979f091beca62d8c235a2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c60df208533e1fc53978ad88b63060ba603756eef0b46beaa35572ff7fc1aa2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1e403730c20e44b3297dc2ca59567dc4f7f8608ea517c016cf6b814fa428f6f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9532ba1899566dfcf8498c068f3eca6b79c8afa3fae5d939c52255a7ae9d96b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:45:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:46:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:46:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:46:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:24 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:46:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:46:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:46:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:46:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:46:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:46:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:46:51 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:46:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd616d47d2a8f573397f07010fd143095697a31e5f728cac1c1b7269738c47a`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1a77f89868067efb94d63fe88604742503d85f515b25f7ab84711a016d3e4f`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 6.0 MB (6043687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f741e9865e3fdcb0bd227a5993c271ef87a11ea1804cdbbdd3814773c085fd4`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 1.5 MB (1509129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a56ea83b77070cf87034a857804e0e5dc6e22a75e16d352364a0c6f2cf81cd`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 295.5 KB (295465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe12fc56262eb1a9961df421373e9e93f9755a2e423207066c543f023b488f7`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cf6274a3105c304db4a54d429807a6d97294428538c809f791158d3a610942`  
		Last Modified: Tue, 02 Aug 2022 01:47:24 GMT  
		Size: 50.1 MB (50081019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48855ad409841498cce766b60da4e1cd5f59a6da57e69031b5cb1e70944c7e06`  
		Last Modified: Tue, 02 Aug 2022 01:47:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93f33d896f43831a247689b5fe6b3c85972c92c57c27a55ae2ca50fd89216c`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2efe54a8f4ae1598aa0cad697c24d96e9bd6701de850e533e452cb0ddc5df62`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa6fb130ed09e3914ae920a1e5cd0affdd896fa22de827e2b222afb58a04e4`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1b1108a42af5f6276fe032adf69f94eb5809dc61e8419af353d507b492e40cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:51c570af32e3e38f0340c7f877e3d6293806b287b5c7f0b2384ae92d1c4ab38f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87488966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3554da7e97670f838d6148f5379c8c0a50d38db1e7a08a3d0919971cee0fe766`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 18:18:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 18:18:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 18:18:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:18:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 18:18:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 18:19:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 18:19:03 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 18:19:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 18:19:18 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 18:19:19 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 18:19:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 18:19:19 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 18:19:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 18:19:20 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 18:19:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba008c5417ddd884ac31c06e8477ed1c51aaae71d18348213a7e5c4733f27126`  
		Last Modified: Tue, 02 Aug 2022 18:20:48 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f992d762b0ee06214c3ee95f2e1c01ec3e979f8df505e081c974fc1b8fdd9`  
		Last Modified: Tue, 02 Aug 2022 18:20:47 GMT  
		Size: 5.2 MB (5224198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b808c60d05957e9ac5537c470816d315cf91d19167448f0753d406e37ea5ec9`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 1.6 MB (1553273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540df1b1f892c29da1bec00c365b0f311f36dfe80c1fc1748c5c2fcfac5ba970`  
		Last Modified: Tue, 02 Aug 2022 18:20:46 GMT  
		Size: 295.6 KB (295561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb3cee704b6a5e2d08b3e54b732ce160cd3b85ce52d22df6e2d4ab43be147c`  
		Last Modified: Tue, 02 Aug 2022 18:20:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d91b4d3132238a8db164b5eacd442a54aebb9e8ef13675dd5921a1ed3ace4d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:49 GMT  
		Size: 49.0 MB (49042037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84737806b6353f840b06e63e4e6a8ef83bbc5218959f1eab925e3c4eafd3a21`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af06c642ed032413d823b53e744f702cded73eb8048c42116e491d6208fd2d8`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2093006093e8cfbaff58d9cae02c71fbdb26c789966b26c41de6e4b202de1881`  
		Last Modified: Tue, 02 Aug 2022 18:20:43 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d483b7339e66ea7dbc3c932b864efa1bb362adcd9b316d0df762893834ae10`  
		Last Modified: Tue, 02 Aug 2022 18:20:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2cc537fd46496d460ec408ea389dd4cc27c180608e89c59761c4682d6dac0cbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85622605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faece9a6aa805f3e9d71e0136a8c7add2db196a28de98b26dc652d2eb88bf4ee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:53:11 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:53:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:53:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:53:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:53:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:53:29 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:53:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:53:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:53:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:53:46 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:53:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:53:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:53:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:53:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:53:50 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:53:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f36ebccf7ea0ca6c4e42a56d3e761f51620dde7809ff4cd6c9c47f4d92dda45`  
		Last Modified: Tue, 02 Aug 2022 01:56:00 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57988538f1066bad59a075d99704fbc2ed80b7f279168e98ae1ac061cddb0e54`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 5.2 MB (5207882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6f84207bfc6da3f978a06e64089cd163b0b7cfce56aa03f050fffcf6aa1fa`  
		Last Modified: Tue, 02 Aug 2022 01:55:59 GMT  
		Size: 1.2 MB (1221114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f79004f600a1443f5dd0ab501f8d2726ae96d9790d635ef946c8ab58fc7639`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 79.2 KB (79204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea246a4776bb764303aebd0c230598840bac0a3067bf67395be8aa1d4a9796c0`  
		Last Modified: Tue, 02 Aug 2022 01:55:58 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afec05def1afee67aa528ce2ecc14afe3dd947292160af59436483a6eb8307d8`  
		Last Modified: Tue, 02 Aug 2022 01:56:02 GMT  
		Size: 49.1 MB (49053054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f205452c1f21b508f3eff3ca454e831b24598073851b7c10ad77092021c63b80`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb0d06feb8b8d747a8a616d3dbdb4dbff7f3d1c07726fc7fabbd0d857588a65`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833640fe1553f0d57940524d810c11944b07d0171e7979f091beca62d8c235a2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c60df208533e1fc53978ad88b63060ba603756eef0b46beaa35572ff7fc1aa2`  
		Last Modified: Tue, 02 Aug 2022 01:55:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:1e403730c20e44b3297dc2ca59567dc4f7f8608ea517c016cf6b814fa428f6f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93209223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9532ba1899566dfcf8498c068f3eca6b79c8afa3fae5d939c52255a7ae9d96b4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 Aug 2022 01:17:30 GMT
ADD file:3a95a896d463569ce82199957052b3467123a4bd3385a0a4e397cf08402a99c3 in / 
# Tue, 02 Aug 2022 01:17:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:45:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 02 Aug 2022 01:45:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 02 Aug 2022 01:46:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 02 Aug 2022 01:46:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 02 Aug 2022 01:46:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:46:24 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 02 Aug 2022 01:46:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 02 Aug 2022 01:46:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 02 Aug 2022 01:46:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 02 Aug 2022 01:46:49 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 02 Aug 2022 01:46:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 01:46:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 01:46:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 02 Aug 2022 01:46:51 GMT
EXPOSE 4369 5984 9100
# Tue, 02 Aug 2022 01:46:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5241cd116d6e6e2d62f3d8c2245b74daca9f6cc154eaccd738feb41984c74714`  
		Last Modified: Tue, 02 Aug 2022 01:24:39 GMT  
		Size: 35.3 MB (35272771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd616d47d2a8f573397f07010fd143095697a31e5f728cac1c1b7269738c47a`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1a77f89868067efb94d63fe88604742503d85f515b25f7ab84711a016d3e4f`  
		Last Modified: Tue, 02 Aug 2022 01:47:19 GMT  
		Size: 6.0 MB (6043687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f741e9865e3fdcb0bd227a5993c271ef87a11ea1804cdbbdd3814773c085fd4`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 1.5 MB (1509129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a56ea83b77070cf87034a857804e0e5dc6e22a75e16d352364a0c6f2cf81cd`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 295.5 KB (295465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe12fc56262eb1a9961df421373e9e93f9755a2e423207066c543f023b488f7`  
		Last Modified: Tue, 02 Aug 2022 01:47:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cf6274a3105c304db4a54d429807a6d97294428538c809f791158d3a610942`  
		Last Modified: Tue, 02 Aug 2022 01:47:24 GMT  
		Size: 50.1 MB (50081019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48855ad409841498cce766b60da4e1cd5f59a6da57e69031b5cb1e70944c7e06`  
		Last Modified: Tue, 02 Aug 2022 01:47:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93f33d896f43831a247689b5fe6b3c85972c92c57c27a55ae2ca50fd89216c`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2efe54a8f4ae1598aa0cad697c24d96e9bd6701de850e533e452cb0ddc5df62`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa6fb130ed09e3914ae920a1e5cd0affdd896fa22de827e2b222afb58a04e4`  
		Last Modified: Tue, 02 Aug 2022 01:47:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
