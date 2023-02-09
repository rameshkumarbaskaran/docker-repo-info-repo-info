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
$ docker pull couchdb@sha256:dbdc83addb0617bd2c15df8dd0030e57247e4f3a1b23249bbda0d81cb444fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:fc9d5c8b5add16d454c00eb141ec35eb14b47e4e767c2bd195f0d65b7a6a8964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408e3fa433f2afba8d7f76673d33861543bbcfffe66849d21fbf2669a73403f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:45:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:45:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:45:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:45:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:45:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:48 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 09:45:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:46:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 09:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:46:09 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:46:09 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac729d2a283867f9e363c476aa79fc9820f59ba1e95bea0b85214968147e4343`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28f4a773fed044da74bbc78ef4eea06ad96191f6b41914ac5052eecf8654b10`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 6.7 MB (6703802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad8a46fddc13bf2f1c9bff7193c14445d15eee0c1ed52788850acaa452ce0f`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 1.3 MB (1259581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e1a7a96866d8b941f299fe0fb0f6a21406565c8745747d9bfef3435bf00dd`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 294.3 KB (294314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2fcd76f6c6a65777c1aa7bd3f5a3cc77adc5b384c48473dd3840117a1bf30c`  
		Last Modified: Thu, 09 Feb 2023 09:47:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e81d2db713da91217db52bdfd249f9eee03e3e820eb5f1c9761f228696833`  
		Last Modified: Thu, 09 Feb 2023 09:47:17 GMT  
		Size: 49.1 MB (49132298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97251e135cc9f24b1c3b07091fd0b70ad6030901efb0c075716be19e33a91f5e`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbf75e3caffedc51a7b150058e69cb41c1011accd485dba3af6b8c3cf70987`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d90d3d52fd1cf395d7252f2bbca42f9babf3504c08734a35f124a8ab2b44697`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec71c1292d2a1be6aaf6ad7211469232287e0a1ab46471cddbb44f794b2826d6`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:18ebb64f4ca27a098d8d0e7c5c91ffdd08acc7cb65a17d8282500bef740f5cb8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72995208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b43cee9fd6b7e4b99034b01169a4b19bf076a06acb57b76544c7467756004a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:38:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:38:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:38:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:38:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:38:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 13:38:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:39:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 13:39:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:39:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:39:05 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:39:05 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:39:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aee1b8a3c1042190ef5a7ad2017145c92c8500e06474c874a014231b3316aa9`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79a4eead140ecb1871f08ef0f7a36d0c49c13175525de21c6d867a6515177`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 6.6 MB (6577109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca3ba0dd68bdf1d65bde8e42c9cfd435f1f0cdb2d234f69fb61bf5590f52c2`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 1.2 MB (1164507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad75529a1f5bd861854989809c93483e2267245c535df80e7156c83b44d8723`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01784a8cc55d7c2aad75202929ce4bbd31b68b3a5310d668295b57a1f1e9b668`  
		Last Modified: Thu, 09 Feb 2023 13:40:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf10def1e72089b84a2e0cf189913a1df3bb063af2cc8394baec9dfaf7dd508`  
		Last Modified: Thu, 09 Feb 2023 13:40:11 GMT  
		Size: 39.0 MB (39029555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021bcabf1b011cbf1c4ddac97d55197ff6b0965d39a09644eea7fb92ed491680`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e1f0663c8d87d858a66753ed7d1f6572f2d06bd5a526a95b36d98594f81a5`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e3147f28b75c3ea28728a9b2af2d39410fed52577222b78e7c9ea325c429e`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbe67db724b32b783545bae3febd5050d2255443f0a8c379739f4a7c149f293`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:dbdc83addb0617bd2c15df8dd0030e57247e4f3a1b23249bbda0d81cb444fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:fc9d5c8b5add16d454c00eb141ec35eb14b47e4e767c2bd195f0d65b7a6a8964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408e3fa433f2afba8d7f76673d33861543bbcfffe66849d21fbf2669a73403f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:45:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:45:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:45:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:45:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:45:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:48 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 09:45:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:46:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 09:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:46:09 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:46:09 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac729d2a283867f9e363c476aa79fc9820f59ba1e95bea0b85214968147e4343`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28f4a773fed044da74bbc78ef4eea06ad96191f6b41914ac5052eecf8654b10`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 6.7 MB (6703802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad8a46fddc13bf2f1c9bff7193c14445d15eee0c1ed52788850acaa452ce0f`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 1.3 MB (1259581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e1a7a96866d8b941f299fe0fb0f6a21406565c8745747d9bfef3435bf00dd`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 294.3 KB (294314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2fcd76f6c6a65777c1aa7bd3f5a3cc77adc5b384c48473dd3840117a1bf30c`  
		Last Modified: Thu, 09 Feb 2023 09:47:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e81d2db713da91217db52bdfd249f9eee03e3e820eb5f1c9761f228696833`  
		Last Modified: Thu, 09 Feb 2023 09:47:17 GMT  
		Size: 49.1 MB (49132298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97251e135cc9f24b1c3b07091fd0b70ad6030901efb0c075716be19e33a91f5e`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbf75e3caffedc51a7b150058e69cb41c1011accd485dba3af6b8c3cf70987`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d90d3d52fd1cf395d7252f2bbca42f9babf3504c08734a35f124a8ab2b44697`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec71c1292d2a1be6aaf6ad7211469232287e0a1ab46471cddbb44f794b2826d6`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:18ebb64f4ca27a098d8d0e7c5c91ffdd08acc7cb65a17d8282500bef740f5cb8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72995208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b43cee9fd6b7e4b99034b01169a4b19bf076a06acb57b76544c7467756004a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:38:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:38:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:38:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:38:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:38:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 13:38:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:39:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 13:39:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:39:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:39:05 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:39:05 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:39:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aee1b8a3c1042190ef5a7ad2017145c92c8500e06474c874a014231b3316aa9`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79a4eead140ecb1871f08ef0f7a36d0c49c13175525de21c6d867a6515177`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 6.6 MB (6577109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca3ba0dd68bdf1d65bde8e42c9cfd435f1f0cdb2d234f69fb61bf5590f52c2`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 1.2 MB (1164507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad75529a1f5bd861854989809c93483e2267245c535df80e7156c83b44d8723`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01784a8cc55d7c2aad75202929ce4bbd31b68b3a5310d668295b57a1f1e9b668`  
		Last Modified: Thu, 09 Feb 2023 13:40:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf10def1e72089b84a2e0cf189913a1df3bb063af2cc8394baec9dfaf7dd508`  
		Last Modified: Thu, 09 Feb 2023 13:40:11 GMT  
		Size: 39.0 MB (39029555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021bcabf1b011cbf1c4ddac97d55197ff6b0965d39a09644eea7fb92ed491680`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e1f0663c8d87d858a66753ed7d1f6572f2d06bd5a526a95b36d98594f81a5`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e3147f28b75c3ea28728a9b2af2d39410fed52577222b78e7c9ea325c429e`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbe67db724b32b783545bae3febd5050d2255443f0a8c379739f4a7c149f293`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:dbdc83addb0617bd2c15df8dd0030e57247e4f3a1b23249bbda0d81cb444fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:fc9d5c8b5add16d454c00eb141ec35eb14b47e4e767c2bd195f0d65b7a6a8964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84537541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408e3fa433f2afba8d7f76673d33861543bbcfffe66849d21fbf2669a73403f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:45:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:45:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:45:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:45:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:45:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:48 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 09:45:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:46:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:46:08 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 09:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:46:09 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:46:09 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac729d2a283867f9e363c476aa79fc9820f59ba1e95bea0b85214968147e4343`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28f4a773fed044da74bbc78ef4eea06ad96191f6b41914ac5052eecf8654b10`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 6.7 MB (6703802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad8a46fddc13bf2f1c9bff7193c14445d15eee0c1ed52788850acaa452ce0f`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 1.3 MB (1259581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e1a7a96866d8b941f299fe0fb0f6a21406565c8745747d9bfef3435bf00dd`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 294.3 KB (294314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2fcd76f6c6a65777c1aa7bd3f5a3cc77adc5b384c48473dd3840117a1bf30c`  
		Last Modified: Thu, 09 Feb 2023 09:47:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e81d2db713da91217db52bdfd249f9eee03e3e820eb5f1c9761f228696833`  
		Last Modified: Thu, 09 Feb 2023 09:47:17 GMT  
		Size: 49.1 MB (49132298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97251e135cc9f24b1c3b07091fd0b70ad6030901efb0c075716be19e33a91f5e`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbf75e3caffedc51a7b150058e69cb41c1011accd485dba3af6b8c3cf70987`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d90d3d52fd1cf395d7252f2bbca42f9babf3504c08734a35f124a8ab2b44697`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec71c1292d2a1be6aaf6ad7211469232287e0a1ab46471cddbb44f794b2826d6`  
		Last Modified: Thu, 09 Feb 2023 09:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:18ebb64f4ca27a098d8d0e7c5c91ffdd08acc7cb65a17d8282500bef740f5cb8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72995208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b43cee9fd6b7e4b99034b01169a4b19bf076a06acb57b76544c7467756004a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:38:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:38:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:38:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:38:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:38:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:52 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 09 Feb 2023 13:38:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:39:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:39:04 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 09 Feb 2023 13:39:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:39:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:39:05 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:39:05 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:39:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aee1b8a3c1042190ef5a7ad2017145c92c8500e06474c874a014231b3316aa9`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79a4eead140ecb1871f08ef0f7a36d0c49c13175525de21c6d867a6515177`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 6.6 MB (6577109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca3ba0dd68bdf1d65bde8e42c9cfd435f1f0cdb2d234f69fb61bf5590f52c2`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 1.2 MB (1164507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad75529a1f5bd861854989809c93483e2267245c535df80e7156c83b44d8723`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01784a8cc55d7c2aad75202929ce4bbd31b68b3a5310d668295b57a1f1e9b668`  
		Last Modified: Thu, 09 Feb 2023 13:40:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf10def1e72089b84a2e0cf189913a1df3bb063af2cc8394baec9dfaf7dd508`  
		Last Modified: Thu, 09 Feb 2023 13:40:11 GMT  
		Size: 39.0 MB (39029555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021bcabf1b011cbf1c4ddac97d55197ff6b0965d39a09644eea7fb92ed491680`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e1f0663c8d87d858a66753ed7d1f6572f2d06bd5a526a95b36d98594f81a5`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87e3147f28b75c3ea28728a9b2af2d39410fed52577222b78e7c9ea325c429e`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbe67db724b32b783545bae3febd5050d2255443f0a8c379739f4a7c149f293`  
		Last Modified: Thu, 09 Feb 2023 13:40:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:6fe524f87c20a0d4f6920176cbff03f5d93d3e59e721be8c2a55b9ab04d95dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:c87c0b765c6cfe23561354f6b65c144d3a4a434c2fcc3c0387af6579ff3605d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3263c547000f0245836d8529790dce4a86314f29bfebdc51087085c22d919`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:23 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 09:44:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:44:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:44:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:44:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:44:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:44:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:44:39 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:44:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1027b762cc1e59ed2e554a3270bdb420664faa7075e47505085c244f35869a21`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644fbc84104dc655bdd2bb4be14754764d745b27b96f861ceb7d81cfd53cdcfb`  
		Last Modified: Thu, 09 Feb 2023 09:46:30 GMT  
		Size: 52.7 MB (52676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8ab0a8f425c2b4cb93bdd5bc4cb16a30133aecda1218d06747d42991106ec`  
		Last Modified: Thu, 09 Feb 2023 09:46:25 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3518f4c3e75c54acebad4f7c502275d0930edb50ccf69654e34bb221782db08a`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7c6f882dacf6fc131f0726dd7a4c32cce4bec5b7286c69151f4e02539620ea`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e027ade58faf21563babcbb4f5644d0815d9698e0febf31720cd5b800a2f1`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1e5ae5c1018aa7ffac0a966f0b93f626fe1c3ecd2eb74027df90f835fc44df03
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82e36049948ec0642106125f326a103110fa86398d11b0ef673476de21774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:43 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 13:37:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:37:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:37:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:37:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:37:56 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:37:56 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:37:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f98b31af11297aaa7eb2cd0d795ff8b2741e8b5386b6b2af6ef7b9a0b1699`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e964753acddc0f3887bebeeeb9d2f59a9c599626089435b5c304abaa33ace7a`  
		Last Modified: Thu, 09 Feb 2023 13:39:27 GMT  
		Size: 52.5 MB (52531739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3865d8e42284b4b7956e56adf6c7437adbb519a75369988c47ced075375078`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1ed4d8adeb2b889db515882b22a39b2a844eeaacaeb24b7a716274085e2db`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42068c71f1e69e3289401c91c462dbbcd14fcb04a5a3f230bcec583dbde39a2`  
		Last Modified: Thu, 09 Feb 2023 13:39:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b380f7228b5b2b7bd574dfac69b654e94c0a45880dbcde5d48db0e90ac1d8d`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:dc6b9603c51dd627dce7ad6cf1427e0bd16649b7431e5a799ba605da366d2697
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96680301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29c43d24cfd2f19f5f0d47d47b2a1e1dddcff60c32493f4c1420f96c476e701`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:37 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 12:43:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:13 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae7ed316b81470abfbad370c51a167ee4ba9d2655c4cf24d429bc6739fd610f`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d71b22b508dea267878375a95968cf553818e77553729ac36aab97276e2f`  
		Last Modified: Thu, 09 Feb 2023 12:45:30 GMT  
		Size: 53.5 MB (53534909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a76c0084e4b7d85a870a6ad54ecc136a307b2b0458dee0b27b3ed0070b33a`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5df9216ab383d80b8afb8cdf70a95208c4e8b81fd293e654043f0beeeebd8f`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eebfdb28157d57ca5bf1a49bdcb5ad098304748a321b481251cd6c46ab80606`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a50c8cecaf109722b468414f95f1e73d531c4c997c0ee26b8f0575ba51a0aa`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:b945478043dbd8154cb2a43dc7a9bea9a55023c0f27cbce2c3c7c4c69463d036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:b491c09a88cd31480bb207d1bfe2c77177056273b786de652f6892188acc3d45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80024421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b058008662dab849e59e40101f657bc93e04281069c2b2480982bf5e801d0ba2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:45:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:45:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:45:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:45:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:45:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:28 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 09 Feb 2023 09:45:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:45:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:45:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:45:43 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 09 Feb 2023 09:45:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:45:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:45:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:45:44 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:45:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac729d2a283867f9e363c476aa79fc9820f59ba1e95bea0b85214968147e4343`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28f4a773fed044da74bbc78ef4eea06ad96191f6b41914ac5052eecf8654b10`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 6.7 MB (6703802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad8a46fddc13bf2f1c9bff7193c14445d15eee0c1ed52788850acaa452ce0f`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 1.3 MB (1259581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e1a7a96866d8b941f299fe0fb0f6a21406565c8745747d9bfef3435bf00dd`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 294.3 KB (294314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072336ac542ce2a9b4897d6753b8e99ffd4846efd3741dffaba18d208dcf0edd`  
		Last Modified: Thu, 09 Feb 2023 09:46:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068c24c7124881f09569f1dc321e8940a062d0beaf0ce7bf01aba9a5777a6dbb`  
		Last Modified: Thu, 09 Feb 2023 09:47:03 GMT  
		Size: 44.6 MB (44619176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cad6d3e1fd037ea7713f2a688f81e218c4b8c49b5e5ba90cb8902da6d6042d3`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9726d29448d106e8d84c1c23fa5026a4bab837c5ffc7cbc5b443126ec4cbb35a`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be3967e8e35c2c7f5de00c56078632987439550d13c47c9b1a2c1309977fe4`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19a6b6646f89688402c68f86a58d94a4158b70d789c15b060029f752529dd`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2614c0d3ccb7c1229ca94ce47d2fbdd875bbd5c3fd63e04c9850712fe35ddac0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75090010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1242bca72c16a2b53e0aa124453d05a5d03e68ed74e52ecf8f6f683602b2ef45`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:38:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:38:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:38:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:38:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:38:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 09 Feb 2023 13:38:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:38:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:38:47 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:38:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:38:47 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 09 Feb 2023 13:38:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:38:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:38:48 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:38:48 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:38:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aee1b8a3c1042190ef5a7ad2017145c92c8500e06474c874a014231b3316aa9`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79a4eead140ecb1871f08ef0f7a36d0c49c13175525de21c6d867a6515177`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 6.6 MB (6577109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca3ba0dd68bdf1d65bde8e42c9cfd435f1f0cdb2d234f69fb61bf5590f52c2`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 1.2 MB (1164507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad75529a1f5bd861854989809c93483e2267245c535df80e7156c83b44d8723`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300a4ac8415bd2527731c5b0acef7953cee519e39f6e8bbdbf01752515411503`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc0ff1e5a6a14cbac4daca81d8ebcccff30ba548d866a298a3e8e0799f3b664`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 41.1 MB (41124362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb880062322fc3acb0f1a5ae4480dd3cc87ed64f05a956e45451cc54132f1284`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3e35751822aed6de6d16280a01e24c984938e1bc01a674fd7b4e88df16311`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a8ed414348edf3155cd80647c851ad48b1c26a1324bfea3a0e687ed2f2e19`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e82e4c4100d5154460d7d35d085ff1dd2d36160e09d709b5b5492f14617fa1`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:b945478043dbd8154cb2a43dc7a9bea9a55023c0f27cbce2c3c7c4c69463d036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:b491c09a88cd31480bb207d1bfe2c77177056273b786de652f6892188acc3d45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80024421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b058008662dab849e59e40101f657bc93e04281069c2b2480982bf5e801d0ba2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:45:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:45:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:45:17 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:45:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:45:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:45:28 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 09 Feb 2023 09:45:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:45:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:45:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:45:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:45:43 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 09 Feb 2023 09:45:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:45:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:45:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:45:44 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:45:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac729d2a283867f9e363c476aa79fc9820f59ba1e95bea0b85214968147e4343`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28f4a773fed044da74bbc78ef4eea06ad96191f6b41914ac5052eecf8654b10`  
		Last Modified: Thu, 09 Feb 2023 09:47:01 GMT  
		Size: 6.7 MB (6703802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad8a46fddc13bf2f1c9bff7193c14445d15eee0c1ed52788850acaa452ce0f`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 1.3 MB (1259581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3e1a7a96866d8b941f299fe0fb0f6a21406565c8745747d9bfef3435bf00dd`  
		Last Modified: Thu, 09 Feb 2023 09:47:00 GMT  
		Size: 294.3 KB (294314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072336ac542ce2a9b4897d6753b8e99ffd4846efd3741dffaba18d208dcf0edd`  
		Last Modified: Thu, 09 Feb 2023 09:46:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068c24c7124881f09569f1dc321e8940a062d0beaf0ce7bf01aba9a5777a6dbb`  
		Last Modified: Thu, 09 Feb 2023 09:47:03 GMT  
		Size: 44.6 MB (44619176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cad6d3e1fd037ea7713f2a688f81e218c4b8c49b5e5ba90cb8902da6d6042d3`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9726d29448d106e8d84c1c23fa5026a4bab837c5ffc7cbc5b443126ec4cbb35a`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be3967e8e35c2c7f5de00c56078632987439550d13c47c9b1a2c1309977fe4`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 2.1 KB (2063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b19a6b6646f89688402c68f86a58d94a4158b70d789c15b060029f752529dd`  
		Last Modified: Thu, 09 Feb 2023 09:46:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2614c0d3ccb7c1229ca94ce47d2fbdd875bbd5c3fd63e04c9850712fe35ddac0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75090010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1242bca72c16a2b53e0aa124453d05a5d03e68ed74e52ecf8f6f683602b2ef45`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:59 GMT
ADD file:442c85d39a4dbb97fb311e1f30e76f5d197339db3967532742e299fa73410f89 in / 
# Thu, 09 Feb 2023 03:58:59 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:38:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:38:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:38:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:38:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:38:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:35 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 09 Feb 2023 13:38:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:38:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:38:47 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:38:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:38:47 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 09 Feb 2023 13:38:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:38:48 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:38:48 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:38:48 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:38:48 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebcd4e3db076a77234a526ba23bdac8b205f7d74fd052a936cfa190b42cf49aa`  
		Last Modified: Thu, 09 Feb 2023 04:03:14 GMT  
		Size: 25.9 MB (25922825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aee1b8a3c1042190ef5a7ad2017145c92c8500e06474c874a014231b3316aa9`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79a4eead140ecb1871f08ef0f7a36d0c49c13175525de21c6d867a6515177`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 6.6 MB (6577109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca3ba0dd68bdf1d65bde8e42c9cfd435f1f0cdb2d234f69fb61bf5590f52c2`  
		Last Modified: Thu, 09 Feb 2023 13:39:57 GMT  
		Size: 1.2 MB (1164507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad75529a1f5bd861854989809c93483e2267245c535df80e7156c83b44d8723`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 294.2 KB (294169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300a4ac8415bd2527731c5b0acef7953cee519e39f6e8bbdbf01752515411503`  
		Last Modified: Thu, 09 Feb 2023 13:39:56 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc0ff1e5a6a14cbac4daca81d8ebcccff30ba548d866a298a3e8e0799f3b664`  
		Last Modified: Thu, 09 Feb 2023 13:39:58 GMT  
		Size: 41.1 MB (41124362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb880062322fc3acb0f1a5ae4480dd3cc87ed64f05a956e45451cc54132f1284`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3e35751822aed6de6d16280a01e24c984938e1bc01a674fd7b4e88df16311`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a8ed414348edf3155cd80647c851ad48b1c26a1324bfea3a0e687ed2f2e19`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e82e4c4100d5154460d7d35d085ff1dd2d36160e09d709b5b5492f14617fa1`  
		Last Modified: Thu, 09 Feb 2023 13:39:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:f798db6ce53e323d9fdc38b524f00e7e9c7a2b746c28130fd3c42e3a1e98614b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a9374fca37b228787ce3748a45550976516962c023f432ef114101eb342f5f3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f8a53e42a2204634e821304fa2ab05f3d41fcde8991f13d743ee98f8ff563`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:47 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 09:44:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:45:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:45:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:45:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:45:01 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:45:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:45:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:45:02 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:45:02 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:45:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acee21edbfbe6573a294eb80c60c7dc38ffea44c08eece87dff35a5f82a5a91`  
		Last Modified: Thu, 09 Feb 2023 09:46:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec20cd59ed4404a0cc5fee5a8298d3c23272153c91a25c9c82636cf07703bec`  
		Last Modified: Thu, 09 Feb 2023 09:46:49 GMT  
		Size: 49.0 MB (49047434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6523992e391a5cf83318f42929fcad83f55aa97374c345e78ba0974efe33d1`  
		Last Modified: Thu, 09 Feb 2023 09:46:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f586cd38adf3cb29bbabf94549a51e043f72a3a902a3336dd5b424bf4c9b87f`  
		Last Modified: Thu, 09 Feb 2023 09:46:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7236ac55d2997fb0df53b7077da07eee43f63639b85073f16a0e3bef0d9655`  
		Last Modified: Thu, 09 Feb 2023 09:46:44 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83070691eba38139e0e34ad0552db91e38fa970e686d524f94c8f438ff3df247`  
		Last Modified: Thu, 09 Feb 2023 09:46:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e09252bc88975c7f52bafe3a2e2bc2f79ba509e2891de13cb51d04167943844d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86076271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2679e193fc928827801c98ea02247a5c3b6606e3ac59832f591ea86012b3c33a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:02 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 13:38:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:38:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:38:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:38:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:38:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:38:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:38:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:38:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:38:15 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:38:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c5e45cf7407e8d3896cb247de03485145ab396bc34c225dd1844753b519ab5`  
		Last Modified: Thu, 09 Feb 2023 13:39:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820e16ea29bdd62cc638fc0342880a10e15a42bcf7c9204ee1455e5672c68466`  
		Last Modified: Thu, 09 Feb 2023 13:39:45 GMT  
		Size: 49.1 MB (49065739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f478eeb7f76e27f61153bd21bba550550e850fe249fbf8ffe7bd0630a2fdfc6`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bb052e262042a1f075479da668387adae41bfe4c39ba2892fbecf2dc14e2a1`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffacc2efe7df09092aaad8ddbb7926352252be834f0ffd0294420960156eadb6`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 2.2 KB (2191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cf9faae45da9338c72ca39b478127c47b11cc4c62da439fc8c4e5068d0715b`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:200d42077dc8f6c81e756978f931f625e7a7a73750db1552d19d20f2a1c44463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93231224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4c20daa55a652c68011eed07a3c2961131b69baaa63dae1bc96cdb4f16d6fd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:44:18 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 12:44:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:47 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:51 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6245eb57863467654abdc449d0fd023dda9916b49423d7c2b86f5e77801ce653`  
		Last Modified: Thu, 09 Feb 2023 12:45:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb50c4ea0d66c58d4cc9b1b86e2fccc37dab89a79cd7e4e99c881e367fa005c`  
		Last Modified: Thu, 09 Feb 2023 12:45:58 GMT  
		Size: 50.1 MB (50086073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e516ba60e1b46bb21131656d57cf39fb16a91c219cf803794c0038707c057ff7`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d88197ca4424482a4dc36a1cb8f02c2d667ac265e1a57508e877ca0593fb0`  
		Last Modified: Thu, 09 Feb 2023 12:45:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97e7c64291782036ef630aefc6907d3bd4d44ac0ba6d8bd960ac5ee5f694ea`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754f4977066ba116d6e611d8d9f006aa755c6df6634998d7828e9a722720c9ab`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:f798db6ce53e323d9fdc38b524f00e7e9c7a2b746c28130fd3c42e3a1e98614b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a9374fca37b228787ce3748a45550976516962c023f432ef114101eb342f5f3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87539585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371f8a53e42a2204634e821304fa2ab05f3d41fcde8991f13d743ee98f8ff563`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:47 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 09:44:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:45:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:45:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:45:01 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:45:01 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:45:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:45:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:45:02 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:45:02 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:45:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acee21edbfbe6573a294eb80c60c7dc38ffea44c08eece87dff35a5f82a5a91`  
		Last Modified: Thu, 09 Feb 2023 09:46:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec20cd59ed4404a0cc5fee5a8298d3c23272153c91a25c9c82636cf07703bec`  
		Last Modified: Thu, 09 Feb 2023 09:46:49 GMT  
		Size: 49.0 MB (49047434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6523992e391a5cf83318f42929fcad83f55aa97374c345e78ba0974efe33d1`  
		Last Modified: Thu, 09 Feb 2023 09:46:43 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f586cd38adf3cb29bbabf94549a51e043f72a3a902a3336dd5b424bf4c9b87f`  
		Last Modified: Thu, 09 Feb 2023 09:46:44 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7236ac55d2997fb0df53b7077da07eee43f63639b85073f16a0e3bef0d9655`  
		Last Modified: Thu, 09 Feb 2023 09:46:44 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83070691eba38139e0e34ad0552db91e38fa970e686d524f94c8f438ff3df247`  
		Last Modified: Thu, 09 Feb 2023 09:46:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e09252bc88975c7f52bafe3a2e2bc2f79ba509e2891de13cb51d04167943844d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86076271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2679e193fc928827801c98ea02247a5c3b6606e3ac59832f591ea86012b3c33a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:38:02 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 13:38:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:38:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:38:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:38:14 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:38:14 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:38:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:38:15 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:38:15 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:38:15 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:38:15 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c5e45cf7407e8d3896cb247de03485145ab396bc34c225dd1844753b519ab5`  
		Last Modified: Thu, 09 Feb 2023 13:39:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820e16ea29bdd62cc638fc0342880a10e15a42bcf7c9204ee1455e5672c68466`  
		Last Modified: Thu, 09 Feb 2023 13:39:45 GMT  
		Size: 49.1 MB (49065739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f478eeb7f76e27f61153bd21bba550550e850fe249fbf8ffe7bd0630a2fdfc6`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bb052e262042a1f075479da668387adae41bfe4c39ba2892fbecf2dc14e2a1`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffacc2efe7df09092aaad8ddbb7926352252be834f0ffd0294420960156eadb6`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 2.2 KB (2191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cf9faae45da9338c72ca39b478127c47b11cc4c62da439fc8c4e5068d0715b`  
		Last Modified: Thu, 09 Feb 2023 13:39:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:200d42077dc8f6c81e756978f931f625e7a7a73750db1552d19d20f2a1c44463
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93231224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4c20daa55a652c68011eed07a3c2961131b69baaa63dae1bc96cdb4f16d6fd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:44:18 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Thu, 09 Feb 2023 12:44:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:45 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:47 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:47 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:50 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:50 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:51 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6245eb57863467654abdc449d0fd023dda9916b49423d7c2b86f5e77801ce653`  
		Last Modified: Thu, 09 Feb 2023 12:45:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb50c4ea0d66c58d4cc9b1b86e2fccc37dab89a79cd7e4e99c881e367fa005c`  
		Last Modified: Thu, 09 Feb 2023 12:45:58 GMT  
		Size: 50.1 MB (50086073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e516ba60e1b46bb21131656d57cf39fb16a91c219cf803794c0038707c057ff7`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d88197ca4424482a4dc36a1cb8f02c2d667ac265e1a57508e877ca0593fb0`  
		Last Modified: Thu, 09 Feb 2023 12:45:49 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97e7c64291782036ef630aefc6907d3bd4d44ac0ba6d8bd960ac5ee5f694ea`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754f4977066ba116d6e611d8d9f006aa755c6df6634998d7828e9a722720c9ab`  
		Last Modified: Thu, 09 Feb 2023 12:45:48 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:6fe524f87c20a0d4f6920176cbff03f5d93d3e59e721be8c2a55b9ab04d95dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:c87c0b765c6cfe23561354f6b65c144d3a4a434c2fcc3c0387af6579ff3605d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3263c547000f0245836d8529790dce4a86314f29bfebdc51087085c22d919`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:23 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 09:44:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:44:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:44:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:44:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:44:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:44:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:44:39 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:44:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1027b762cc1e59ed2e554a3270bdb420664faa7075e47505085c244f35869a21`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644fbc84104dc655bdd2bb4be14754764d745b27b96f861ceb7d81cfd53cdcfb`  
		Last Modified: Thu, 09 Feb 2023 09:46:30 GMT  
		Size: 52.7 MB (52676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8ab0a8f425c2b4cb93bdd5bc4cb16a30133aecda1218d06747d42991106ec`  
		Last Modified: Thu, 09 Feb 2023 09:46:25 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3518f4c3e75c54acebad4f7c502275d0930edb50ccf69654e34bb221782db08a`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7c6f882dacf6fc131f0726dd7a4c32cce4bec5b7286c69151f4e02539620ea`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e027ade58faf21563babcbb4f5644d0815d9698e0febf31720cd5b800a2f1`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1e5ae5c1018aa7ffac0a966f0b93f626fe1c3ecd2eb74027df90f835fc44df03
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82e36049948ec0642106125f326a103110fa86398d11b0ef673476de21774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:43 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 13:37:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:37:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:37:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:37:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:37:56 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:37:56 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:37:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f98b31af11297aaa7eb2cd0d795ff8b2741e8b5386b6b2af6ef7b9a0b1699`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e964753acddc0f3887bebeeeb9d2f59a9c599626089435b5c304abaa33ace7a`  
		Last Modified: Thu, 09 Feb 2023 13:39:27 GMT  
		Size: 52.5 MB (52531739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3865d8e42284b4b7956e56adf6c7437adbb519a75369988c47ced075375078`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1ed4d8adeb2b889db515882b22a39b2a844eeaacaeb24b7a716274085e2db`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42068c71f1e69e3289401c91c462dbbcd14fcb04a5a3f230bcec583dbde39a2`  
		Last Modified: Thu, 09 Feb 2023 13:39:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b380f7228b5b2b7bd574dfac69b654e94c0a45880dbcde5d48db0e90ac1d8d`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:dc6b9603c51dd627dce7ad6cf1427e0bd16649b7431e5a799ba605da366d2697
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96680301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29c43d24cfd2f19f5f0d47d47b2a1e1dddcff60c32493f4c1420f96c476e701`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:37 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 12:43:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:13 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae7ed316b81470abfbad370c51a167ee4ba9d2655c4cf24d429bc6739fd610f`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d71b22b508dea267878375a95968cf553818e77553729ac36aab97276e2f`  
		Last Modified: Thu, 09 Feb 2023 12:45:30 GMT  
		Size: 53.5 MB (53534909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a76c0084e4b7d85a870a6ad54ecc136a307b2b0458dee0b27b3ed0070b33a`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5df9216ab383d80b8afb8cdf70a95208c4e8b81fd293e654043f0beeeebd8f`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eebfdb28157d57ca5bf1a49bdcb5ad098304748a321b481251cd6c46ab80606`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a50c8cecaf109722b468414f95f1e73d531c4c997c0ee26b8f0575ba51a0aa`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.1`

```console
$ docker pull couchdb@sha256:6fe524f87c20a0d4f6920176cbff03f5d93d3e59e721be8c2a55b9ab04d95dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:c87c0b765c6cfe23561354f6b65c144d3a4a434c2fcc3c0387af6579ff3605d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3263c547000f0245836d8529790dce4a86314f29bfebdc51087085c22d919`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:23 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 09:44:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:44:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:44:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:44:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:44:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:44:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:44:39 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:44:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1027b762cc1e59ed2e554a3270bdb420664faa7075e47505085c244f35869a21`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644fbc84104dc655bdd2bb4be14754764d745b27b96f861ceb7d81cfd53cdcfb`  
		Last Modified: Thu, 09 Feb 2023 09:46:30 GMT  
		Size: 52.7 MB (52676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8ab0a8f425c2b4cb93bdd5bc4cb16a30133aecda1218d06747d42991106ec`  
		Last Modified: Thu, 09 Feb 2023 09:46:25 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3518f4c3e75c54acebad4f7c502275d0930edb50ccf69654e34bb221782db08a`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7c6f882dacf6fc131f0726dd7a4c32cce4bec5b7286c69151f4e02539620ea`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e027ade58faf21563babcbb4f5644d0815d9698e0febf31720cd5b800a2f1`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1e5ae5c1018aa7ffac0a966f0b93f626fe1c3ecd2eb74027df90f835fc44df03
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82e36049948ec0642106125f326a103110fa86398d11b0ef673476de21774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:43 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 13:37:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:37:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:37:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:37:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:37:56 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:37:56 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:37:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f98b31af11297aaa7eb2cd0d795ff8b2741e8b5386b6b2af6ef7b9a0b1699`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e964753acddc0f3887bebeeeb9d2f59a9c599626089435b5c304abaa33ace7a`  
		Last Modified: Thu, 09 Feb 2023 13:39:27 GMT  
		Size: 52.5 MB (52531739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3865d8e42284b4b7956e56adf6c7437adbb519a75369988c47ced075375078`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1ed4d8adeb2b889db515882b22a39b2a844eeaacaeb24b7a716274085e2db`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42068c71f1e69e3289401c91c462dbbcd14fcb04a5a3f230bcec583dbde39a2`  
		Last Modified: Thu, 09 Feb 2023 13:39:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b380f7228b5b2b7bd574dfac69b654e94c0a45880dbcde5d48db0e90ac1d8d`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:dc6b9603c51dd627dce7ad6cf1427e0bd16649b7431e5a799ba605da366d2697
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96680301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29c43d24cfd2f19f5f0d47d47b2a1e1dddcff60c32493f4c1420f96c476e701`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:37 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 12:43:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:13 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae7ed316b81470abfbad370c51a167ee4ba9d2655c4cf24d429bc6739fd610f`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d71b22b508dea267878375a95968cf553818e77553729ac36aab97276e2f`  
		Last Modified: Thu, 09 Feb 2023 12:45:30 GMT  
		Size: 53.5 MB (53534909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a76c0084e4b7d85a870a6ad54ecc136a307b2b0458dee0b27b3ed0070b33a`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5df9216ab383d80b8afb8cdf70a95208c4e8b81fd293e654043f0beeeebd8f`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eebfdb28157d57ca5bf1a49bdcb5ad098304748a321b481251cd6c46ab80606`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a50c8cecaf109722b468414f95f1e73d531c4c997c0ee26b8f0575ba51a0aa`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:6fe524f87c20a0d4f6920176cbff03f5d93d3e59e721be8c2a55b9ab04d95dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:c87c0b765c6cfe23561354f6b65c144d3a4a434c2fcc3c0387af6579ff3605d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3263c547000f0245836d8529790dce4a86314f29bfebdc51087085c22d919`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:44:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 09:44:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 09:44:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 09:44:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 09:44:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:44:23 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 09:44:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 09:44:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 09:44:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 09:44:38 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 09:44:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 09:44:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 09:44:38 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 09:44:39 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 09:44:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345cb2c67b59cd95add5b6be1729d91b01d262a2608a908cb694fe66abca041`  
		Last Modified: Thu, 09 Feb 2023 09:46:28 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b099decb39c6e5245f15055a881c64ac470fac937c698c3dbaee1d6bd6b4c1e1`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 5.2 MB (5224297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fb61b503efee85952ba73c92cc7b7423655632230e1371d61cd5cabdb53890`  
		Last Modified: Thu, 09 Feb 2023 09:46:27 GMT  
		Size: 1.6 MB (1553314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2e3947bc9363c6751cbf0ef33583a86e265aee42701a08f8fab8d2788b025`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 295.6 KB (295585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1027b762cc1e59ed2e554a3270bdb420664faa7075e47505085c244f35869a21`  
		Last Modified: Thu, 09 Feb 2023 09:46:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644fbc84104dc655bdd2bb4be14754764d745b27b96f861ceb7d81cfd53cdcfb`  
		Last Modified: Thu, 09 Feb 2023 09:46:30 GMT  
		Size: 52.7 MB (52676291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8ab0a8f425c2b4cb93bdd5bc4cb16a30133aecda1218d06747d42991106ec`  
		Last Modified: Thu, 09 Feb 2023 09:46:25 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3518f4c3e75c54acebad4f7c502275d0930edb50ccf69654e34bb221782db08a`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7c6f882dacf6fc131f0726dd7a4c32cce4bec5b7286c69151f4e02539620ea`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 2.2 KB (2186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e027ade58faf21563babcbb4f5644d0815d9698e0febf31720cd5b800a2f1`  
		Last Modified: Thu, 09 Feb 2023 09:46:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:1e5ae5c1018aa7ffac0a966f0b93f626fe1c3ecd2eb74027df90f835fc44df03
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89542496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82e36049948ec0642106125f326a103110fa86398d11b0ef673476de21774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:37:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 13:37:29 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 13:37:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 13:37:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 13:37:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:37:43 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 13:37:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 13:37:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 13:37:55 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 13:37:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 13:37:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 13:37:56 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 13:37:56 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 13:37:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6091f9f6c73b4b952be2bbc2cd89a8fc504064bf7483b83b7ea81f13fa4d54`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e00b3493fef81fb1cab07d097825491e38cb83abd318e8c4d1ee8c5b856710`  
		Last Modified: Thu, 09 Feb 2023 13:39:26 GMT  
		Size: 5.2 MB (5209406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0f2fc9cbc7001e7f9e0948436f0dd3a05468c357b0bee7bab813dec0619529`  
		Last Modified: Thu, 09 Feb 2023 13:39:25 GMT  
		Size: 1.4 MB (1435933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806951d526ba39c29e24fec1009ff647797fc0fab6abec6327d5cdb57cac82c8`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 295.5 KB (295507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f98b31af11297aaa7eb2cd0d795ff8b2741e8b5386b6b2af6ef7b9a0b1699`  
		Last Modified: Thu, 09 Feb 2023 13:39:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e964753acddc0f3887bebeeeb9d2f59a9c599626089435b5c304abaa33ace7a`  
		Last Modified: Thu, 09 Feb 2023 13:39:27 GMT  
		Size: 52.5 MB (52531739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3865d8e42284b4b7956e56adf6c7437adbb519a75369988c47ced075375078`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa1ed4d8adeb2b889db515882b22a39b2a844eeaacaeb24b7a716274085e2db`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42068c71f1e69e3289401c91c462dbbcd14fcb04a5a3f230bcec583dbde39a2`  
		Last Modified: Thu, 09 Feb 2023 13:39:23 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b380f7228b5b2b7bd574dfac69b654e94c0a45880dbcde5d48db0e90ac1d8d`  
		Last Modified: Thu, 09 Feb 2023 13:39:22 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:dc6b9603c51dd627dce7ad6cf1427e0bd16649b7431e5a799ba605da366d2697
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96680301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29c43d24cfd2f19f5f0d47d47b2a1e1dddcff60c32493f4c1420f96c476e701`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 09 Feb 2023 06:21:49 GMT
ADD file:b09577b8131a90731fdfb00b824a97dc65ccb51d484cb9004382035d64a5741c in / 
# Thu, 09 Feb 2023 06:21:52 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:42:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 09 Feb 2023 12:42:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 09 Feb 2023 12:43:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 09 Feb 2023 12:43:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 09 Feb 2023 12:43:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:37 GMT
ENV COUCHDB_VERSION=3.3.1
# Thu, 09 Feb 2023 12:43:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 09 Feb 2023 12:44:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 09 Feb 2023 12:44:08 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Thu, 09 Feb 2023 12:44:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 09 Feb 2023 12:44:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 09 Feb 2023 12:44:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 09 Feb 2023 12:44:13 GMT
EXPOSE 4369 5984 9100
# Thu, 09 Feb 2023 12:44:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4ea90e1a094ae86c7950bbec99e7a79b08fae641ad5f3bc3af9081c925894c41`  
		Last Modified: Thu, 09 Feb 2023 06:28:27 GMT  
		Size: 35.3 MB (35289252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344273d532420eb3b27c79a3c0db475a147ebd5ca66d69e0940b4321316869f5`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9112b74f6c8f09d809d4bf9c2dcaca397649e22122786475bd8bda6f592ac4`  
		Last Modified: Thu, 09 Feb 2023 12:45:21 GMT  
		Size: 6.0 MB (6043938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366411d7a2535a8e47184df9d6bffa84e30071bac9479232f978ff7fecf64f21`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 1.5 MB (1509238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59167078773abee879f6d35220f0e798f539873532f8a6c2b9a1a135eb8a3772`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 295.6 KB (295578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae7ed316b81470abfbad370c51a167ee4ba9d2655c4cf24d429bc6739fd610f`  
		Last Modified: Thu, 09 Feb 2023 12:45:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d71b22b508dea267878375a95968cf553818e77553729ac36aab97276e2f`  
		Last Modified: Thu, 09 Feb 2023 12:45:30 GMT  
		Size: 53.5 MB (53534909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a76c0084e4b7d85a870a6ad54ecc136a307b2b0458dee0b27b3ed0070b33a`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5df9216ab383d80b8afb8cdf70a95208c4e8b81fd293e654043f0beeeebd8f`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eebfdb28157d57ca5bf1a49bdcb5ad098304748a321b481251cd6c46ab80606`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a50c8cecaf109722b468414f95f1e73d531c4c997c0ee26b8f0575ba51a0aa`  
		Last Modified: Thu, 09 Feb 2023 12:45:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
