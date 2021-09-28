<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:latest`](#odoolatest)

## `odoo:12`

```console
$ docker pull odoo@sha256:abc40903d5fc5341053c1c8056405cffe6fdc66ee32d10de294d5cd7d8398a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:f02031542b5f16dddda08ae9f0b15eeeb7d0706836c8b0f2cd6761e84f2abfa4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538416281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16159b9a8c2cc37e99a7453fb8a5228b293849e4c41303028bd34dadaa954d3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 09:04:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 09:04:53 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:04:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 28 Sep 2021 09:07:07 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 09:07:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:07:46 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:07:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 28 Sep 2021 09:07:46 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 09:07:46 GMT
ARG ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
# Tue, 28 Sep 2021 09:09:27 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:09:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:09:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:09:32 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:09:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:09:33 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:09:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:09:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:09:34 GMT
USER odoo
# Tue, 28 Sep 2021 09:09:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:09:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5788ecc3532a07db45efea6a2c973faee8385402c0498b6cd805140e3ff3aa`  
		Last Modified: Tue, 28 Sep 2021 09:11:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d29df4b5fe46f143c4fcdd612f91cb00e025018292c0e2ea4f4aa8fb40b628c`  
		Last Modified: Tue, 28 Sep 2021 09:12:29 GMT  
		Size: 219.7 MB (219657423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa757125f4784d18e2db094bd9c15892e1e3a68f8405c3cfd6e44f57dfd10b5`  
		Last Modified: Tue, 28 Sep 2021 09:11:46 GMT  
		Size: 2.2 MB (2227263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e75deb22b82657afe043a6b3b90c7531f3f68e0b794caa5a715a2656cc863`  
		Last Modified: Tue, 28 Sep 2021 09:11:54 GMT  
		Size: 22.0 MB (22019278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24eb3eed61964deb67410aea773bfc0e8e47b2ef1b86af298ba3c6cfb87cf87e`  
		Last Modified: Tue, 28 Sep 2021 09:12:35 GMT  
		Size: 272.0 MB (271981923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa3149dd0835340ce8f99503e24e15512f292c8230657629dc079efc6ffe69`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3418f5106602ab9b50fbc9a8d1364ee7ba9e8a3b3e62e7603aa391d1de55b4de`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c377fe4e2c2e860dd3dca08830915b934d3d392b4da09f47c95bea2e71b0f698`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21277a5342bb10ef4640e50c2beb47fc83e8c58ae076e305b42fd9e8f4d1e680`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:abc40903d5fc5341053c1c8056405cffe6fdc66ee32d10de294d5cd7d8398a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:f02031542b5f16dddda08ae9f0b15eeeb7d0706836c8b0f2cd6761e84f2abfa4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538416281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16159b9a8c2cc37e99a7453fb8a5228b293849e4c41303028bd34dadaa954d3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:04:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 09:04:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 09:04:53 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:04:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 28 Sep 2021 09:07:07 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 09:07:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:07:46 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:07:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 28 Sep 2021 09:07:46 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 09:07:46 GMT
ARG ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
# Tue, 28 Sep 2021 09:09:27 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:09:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:09:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:09:32 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=be20135cab2e42ffa3029b5c196868b08a929659
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:09:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:09:33 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:09:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:09:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:09:34 GMT
USER odoo
# Tue, 28 Sep 2021 09:09:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:09:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5788ecc3532a07db45efea6a2c973faee8385402c0498b6cd805140e3ff3aa`  
		Last Modified: Tue, 28 Sep 2021 09:11:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d29df4b5fe46f143c4fcdd612f91cb00e025018292c0e2ea4f4aa8fb40b628c`  
		Last Modified: Tue, 28 Sep 2021 09:12:29 GMT  
		Size: 219.7 MB (219657423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa757125f4784d18e2db094bd9c15892e1e3a68f8405c3cfd6e44f57dfd10b5`  
		Last Modified: Tue, 28 Sep 2021 09:11:46 GMT  
		Size: 2.2 MB (2227263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e75deb22b82657afe043a6b3b90c7531f3f68e0b794caa5a715a2656cc863`  
		Last Modified: Tue, 28 Sep 2021 09:11:54 GMT  
		Size: 22.0 MB (22019278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24eb3eed61964deb67410aea773bfc0e8e47b2ef1b86af298ba3c6cfb87cf87e`  
		Last Modified: Tue, 28 Sep 2021 09:12:35 GMT  
		Size: 272.0 MB (271981923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa3149dd0835340ce8f99503e24e15512f292c8230657629dc079efc6ffe69`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3418f5106602ab9b50fbc9a8d1364ee7ba9e8a3b3e62e7603aa391d1de55b4de`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c377fe4e2c2e860dd3dca08830915b934d3d392b4da09f47c95bea2e71b0f698`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21277a5342bb10ef4640e50c2beb47fc83e8c58ae076e305b42fd9e8f4d1e680`  
		Last Modified: Tue, 28 Sep 2021 09:11:43 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:358863d25e31a03d081f261c9c0deede144bb9b94a3c1c10b3298d4d1e1c8115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:6ef4eeb3e2d49916c9b365f0fa68504218e8b1264ddb14932b80819753e4fb05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528467691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba950b63396e3b862a664c014aa840633c4670257634e560e23ad22cb1976be4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:02:35 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 09:02:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:02:55 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 09:02:55 GMT
ENV ODOO_VERSION=13.0
# Tue, 28 Sep 2021 09:02:55 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 09:02:55 GMT
ARG ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
# Tue, 28 Sep 2021 09:04:34 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:04:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:04:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:04:40 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:04:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:04:41 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:04:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:04:41 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:04:42 GMT
USER odoo
# Tue, 28 Sep 2021 09:04:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:04:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c839a5f094fb26110db82ce8478b2716b5ae4a3b1f4787dcf4e42a3ee806fa7`  
		Last Modified: Tue, 28 Sep 2021 09:11:24 GMT  
		Size: 207.1 MB (207131178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9702631183b797e14e02f699e03b5970d762468d09fdf90f68293fa1d190b699`  
		Last Modified: Tue, 28 Sep 2021 09:10:56 GMT  
		Size: 2.3 MB (2347886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d624dc0f4f384ddbee9fa140b492064255415e389bc2188ab634fc3f01234b`  
		Last Modified: Tue, 28 Sep 2021 09:10:56 GMT  
		Size: 882.8 KB (882781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5def30e9d1a905b826890c018d1ff1fca3ab41718b82215f7208c8dc352ea793`  
		Last Modified: Tue, 28 Sep 2021 09:11:32 GMT  
		Size: 291.0 MB (290957388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39b8269ef4ad36e8dce52641088cac12b61774b01f8904928e674e40ff90d72`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e78d0e5f083bc1d6ebbbc093a255f0c72cb6e367e76392cdcb0c64e6303087`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c03492e99ecb1ff9a6786eb82aa10eed4a266c1cc929c31eb07147e92d4b6d9`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f87be0861e6f67a95cc9c60ba906cf29ae090e9e14d73d5d179c52a372534`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:358863d25e31a03d081f261c9c0deede144bb9b94a3c1c10b3298d4d1e1c8115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:6ef4eeb3e2d49916c9b365f0fa68504218e8b1264ddb14932b80819753e4fb05
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528467691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba950b63396e3b862a664c014aa840633c4670257634e560e23ad22cb1976be4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:02:35 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 09:02:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:02:55 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 09:02:55 GMT
ENV ODOO_VERSION=13.0
# Tue, 28 Sep 2021 09:02:55 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 09:02:55 GMT
ARG ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
# Tue, 28 Sep 2021 09:04:34 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:04:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:04:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:04:40 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=af7bac90a379d12116f75616fb6bef1e3bc4c733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:04:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:04:41 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:04:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:04:41 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:04:42 GMT
USER odoo
# Tue, 28 Sep 2021 09:04:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:04:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c839a5f094fb26110db82ce8478b2716b5ae4a3b1f4787dcf4e42a3ee806fa7`  
		Last Modified: Tue, 28 Sep 2021 09:11:24 GMT  
		Size: 207.1 MB (207131178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9702631183b797e14e02f699e03b5970d762468d09fdf90f68293fa1d190b699`  
		Last Modified: Tue, 28 Sep 2021 09:10:56 GMT  
		Size: 2.3 MB (2347886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d624dc0f4f384ddbee9fa140b492064255415e389bc2188ab634fc3f01234b`  
		Last Modified: Tue, 28 Sep 2021 09:10:56 GMT  
		Size: 882.8 KB (882781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5def30e9d1a905b826890c018d1ff1fca3ab41718b82215f7208c8dc352ea793`  
		Last Modified: Tue, 28 Sep 2021 09:11:32 GMT  
		Size: 291.0 MB (290957388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39b8269ef4ad36e8dce52641088cac12b61774b01f8904928e674e40ff90d72`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e78d0e5f083bc1d6ebbbc093a255f0c72cb6e367e76392cdcb0c64e6303087`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c03492e99ecb1ff9a6786eb82aa10eed4a266c1cc929c31eb07147e92d4b6d9`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f87be0861e6f67a95cc9c60ba906cf29ae090e9e14d73d5d179c52a372534`  
		Last Modified: Tue, 28 Sep 2021 09:10:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:0123fb5ec226a75b4c6f3166c6ebee8c133adea50efb49378b1e5b6a52dab16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:d4671d3fbde2e39f434959f01b91f6551eab2ba7343c287d0eb9a017424c6d8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516997258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53998176ca6ea910168fca4d57a2520518de2052b41f6526900f2003978fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 08:59:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 08:59:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:59:24 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 08:59:24 GMT
ENV ODOO_VERSION=14.0
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 28 Sep 2021 09:00:38 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:00:43 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:00:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:00:43 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:00:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:00:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:00:44 GMT
USER odoo
# Tue, 28 Sep 2021 09:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:00:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202cc4801528046f1295d1e9fde12d1ca51922bb3bbb78f28414392e496affb`  
		Last Modified: Tue, 28 Sep 2021 09:10:33 GMT  
		Size: 213.2 MB (213172416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f9940244ebdbb6e2808ac61f977f7a881c116cf6b1a5ff5400656affb2122`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 2.4 MB (2350586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07d3bb02ae4b65c91447226f5c9402577d6f42a0cc8060e112b073485266a8`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 882.7 KB (882660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79eecf29fa0fb1a9bb616898f6ac47b44549f8376427246889b4a13aeb6007`  
		Last Modified: Tue, 28 Sep 2021 09:10:40 GMT  
		Size: 273.4 MB (273443143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b37ca5246526d8c602ce02dc80380f82fa333de01bb48063a3675d5b12fd4`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbac68a7e779e4d5d201f4f1a81aaadcf5a4d0be5e7edb041e1df9639d8c2f9`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1329d58b792ba188877914ebda45349a38eea132d7dfd5f1bed26948e522f62`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b366991d41c0934ac1a1421f007ad21ff87ec7c19018012471bc443f50af2a7`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:0123fb5ec226a75b4c6f3166c6ebee8c133adea50efb49378b1e5b6a52dab16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:d4671d3fbde2e39f434959f01b91f6551eab2ba7343c287d0eb9a017424c6d8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516997258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53998176ca6ea910168fca4d57a2520518de2052b41f6526900f2003978fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 08:59:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 08:59:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:59:24 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 08:59:24 GMT
ENV ODOO_VERSION=14.0
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 28 Sep 2021 09:00:38 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:00:43 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:00:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:00:43 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:00:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:00:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:00:44 GMT
USER odoo
# Tue, 28 Sep 2021 09:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:00:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202cc4801528046f1295d1e9fde12d1ca51922bb3bbb78f28414392e496affb`  
		Last Modified: Tue, 28 Sep 2021 09:10:33 GMT  
		Size: 213.2 MB (213172416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f9940244ebdbb6e2808ac61f977f7a881c116cf6b1a5ff5400656affb2122`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 2.4 MB (2350586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07d3bb02ae4b65c91447226f5c9402577d6f42a0cc8060e112b073485266a8`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 882.7 KB (882660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79eecf29fa0fb1a9bb616898f6ac47b44549f8376427246889b4a13aeb6007`  
		Last Modified: Tue, 28 Sep 2021 09:10:40 GMT  
		Size: 273.4 MB (273443143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b37ca5246526d8c602ce02dc80380f82fa333de01bb48063a3675d5b12fd4`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbac68a7e779e4d5d201f4f1a81aaadcf5a4d0be5e7edb041e1df9639d8c2f9`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1329d58b792ba188877914ebda45349a38eea132d7dfd5f1bed26948e522f62`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b366991d41c0934ac1a1421f007ad21ff87ec7c19018012471bc443f50af2a7`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:0123fb5ec226a75b4c6f3166c6ebee8c133adea50efb49378b1e5b6a52dab16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d4671d3fbde2e39f434959f01b91f6551eab2ba7343c287d0eb9a017424c6d8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516997258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53998176ca6ea910168fca4d57a2520518de2052b41f6526900f2003978fec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:57:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 28 Sep 2021 08:57:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 28 Sep 2021 08:57:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 08:59:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 28 Sep 2021 08:59:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:59:24 GMT
RUN npm install -g rtlcss
# Tue, 28 Sep 2021 08:59:24 GMT
ENV ODOO_VERSION=14.0
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_RELEASE=20210921
# Tue, 28 Sep 2021 08:59:24 GMT
ARG ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
# Tue, 28 Sep 2021 09:00:38 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 28 Sep 2021 09:00:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 28 Sep 2021 09:00:43 GMT
# ARGS: ODOO_RELEASE=20210921 ODOO_SHA=e5d55b36442cf67744d41e89237e4ccbe4de5a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 28 Sep 2021 09:00:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 28 Sep 2021 09:00:43 GMT
EXPOSE 8069 8071 8072
# Tue, 28 Sep 2021 09:00:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 28 Sep 2021 09:00:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 28 Sep 2021 09:00:44 GMT
USER odoo
# Tue, 28 Sep 2021 09:00:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 09:00:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202cc4801528046f1295d1e9fde12d1ca51922bb3bbb78f28414392e496affb`  
		Last Modified: Tue, 28 Sep 2021 09:10:33 GMT  
		Size: 213.2 MB (213172416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f9940244ebdbb6e2808ac61f977f7a881c116cf6b1a5ff5400656affb2122`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 2.4 MB (2350586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07d3bb02ae4b65c91447226f5c9402577d6f42a0cc8060e112b073485266a8`  
		Last Modified: Tue, 28 Sep 2021 09:10:05 GMT  
		Size: 882.7 KB (882660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79eecf29fa0fb1a9bb616898f6ac47b44549f8376427246889b4a13aeb6007`  
		Last Modified: Tue, 28 Sep 2021 09:10:40 GMT  
		Size: 273.4 MB (273443143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b37ca5246526d8c602ce02dc80380f82fa333de01bb48063a3675d5b12fd4`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbac68a7e779e4d5d201f4f1a81aaadcf5a4d0be5e7edb041e1df9639d8c2f9`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1329d58b792ba188877914ebda45349a38eea132d7dfd5f1bed26948e522f62`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b366991d41c0934ac1a1421f007ad21ff87ec7c19018012471bc443f50af2a7`  
		Last Modified: Tue, 28 Sep 2021 09:10:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
