<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:6c37f29128e2e111f1eee8a95f7623b85359167d188fae5cc4ad13150727266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:a50543dcc7c1135bc114fa3760a3b66e8f71636874b72388976b5dbfcc17557c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540322589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b02547f45a53cd6a285a8046c16b16d65a72245fb4e6d822a440f5a3980574d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:42:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:42:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:42:50 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:42:50 GMT
ENV ODOO_VERSION=13.0
# Tue, 02 Aug 2022 05:42:50 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:42:51 GMT
ARG ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
# Tue, 02 Aug 2022 05:44:03 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:44:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:44:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:44:08 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:44:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:44:08 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:44:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:44:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:44:08 GMT
USER odoo
# Tue, 02 Aug 2022 05:44:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:44:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718371f43c618dd7c037dc9e6f276d3bdfb4242e47d30ede3d8e797f7e6f78a`  
		Last Modified: Tue, 02 Aug 2022 05:46:33 GMT  
		Size: 207.1 MB (207143577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563a78258fd2c7c9ee449d16fdd0f86d7c54d1784ca7c103dd02900afc29168`  
		Last Modified: Tue, 02 Aug 2022 05:46:13 GMT  
		Size: 13.4 MB (13442945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350b162f7b9f79c7d63f4e71229b205d9070f98f801cf71ad2b9211e8ede686`  
		Last Modified: Tue, 02 Aug 2022 05:46:09 GMT  
		Size: 508.4 KB (508417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914346e045042a2c82f2a14359c82cf2dcc91bb413c739853c78f18101a37f60`  
		Last Modified: Tue, 02 Aug 2022 05:46:39 GMT  
		Size: 292.1 MB (292085104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4434ad30744498b355a9b5a5b7a73fefdfa5e32ae5ec3b1435e4ab28324fb4`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75c880aa38d8d446fecaefb226f8ece408096db778ad7a7728eda03e50c370`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a195351ae94fdebce634ab5d7e9173eb657e654fa2fa5569db2f5387b3accd8`  
		Last Modified: Tue, 02 Aug 2022 05:46:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd81426a884a4620fe8a493a28dd023cf2fdd17c4d924ea393927d79928fefa5`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:6c37f29128e2e111f1eee8a95f7623b85359167d188fae5cc4ad13150727266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:a50543dcc7c1135bc114fa3760a3b66e8f71636874b72388976b5dbfcc17557c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540322589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b02547f45a53cd6a285a8046c16b16d65a72245fb4e6d822a440f5a3980574d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:42:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:42:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:42:50 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:42:50 GMT
ENV ODOO_VERSION=13.0
# Tue, 02 Aug 2022 05:42:50 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:42:51 GMT
ARG ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
# Tue, 02 Aug 2022 05:44:03 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:44:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:44:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:44:08 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:44:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:44:08 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:44:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:44:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:44:08 GMT
USER odoo
# Tue, 02 Aug 2022 05:44:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:44:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718371f43c618dd7c037dc9e6f276d3bdfb4242e47d30ede3d8e797f7e6f78a`  
		Last Modified: Tue, 02 Aug 2022 05:46:33 GMT  
		Size: 207.1 MB (207143577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563a78258fd2c7c9ee449d16fdd0f86d7c54d1784ca7c103dd02900afc29168`  
		Last Modified: Tue, 02 Aug 2022 05:46:13 GMT  
		Size: 13.4 MB (13442945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350b162f7b9f79c7d63f4e71229b205d9070f98f801cf71ad2b9211e8ede686`  
		Last Modified: Tue, 02 Aug 2022 05:46:09 GMT  
		Size: 508.4 KB (508417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914346e045042a2c82f2a14359c82cf2dcc91bb413c739853c78f18101a37f60`  
		Last Modified: Tue, 02 Aug 2022 05:46:39 GMT  
		Size: 292.1 MB (292085104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4434ad30744498b355a9b5a5b7a73fefdfa5e32ae5ec3b1435e4ab28324fb4`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c75c880aa38d8d446fecaefb226f8ece408096db778ad7a7728eda03e50c370`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a195351ae94fdebce634ab5d7e9173eb657e654fa2fa5569db2f5387b3accd8`  
		Last Modified: Tue, 02 Aug 2022 05:46:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd81426a884a4620fe8a493a28dd023cf2fdd17c4d924ea393927d79928fefa5`  
		Last Modified: Tue, 02 Aug 2022 05:46:06 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:7170e2e7f22cfac76b7a27950010d41e77dab4fa1cf300b1fd491214096a415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:b7147f14c15a0a1775f9ff464da472aff646cfd2f63e58f07743a96b921b2ce8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530761398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824d4df5baa0bffb5b6061b1ceaa0bc916c5ecf6e20ac9cde84123aa9cf392ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:40:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:40:09 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:40:09 GMT
ENV ODOO_VERSION=14.0
# Tue, 02 Aug 2022 05:40:09 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:40:09 GMT
ARG ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
# Tue, 02 Aug 2022 05:41:21 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:41:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:41:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:41:26 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:41:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:41:26 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:41:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:41:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:41:26 GMT
USER odoo
# Tue, 02 Aug 2022 05:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:41:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2a9029ee3604b9372e42d87384e5e066e9148be333e0dc03e9c8f855e427b`  
		Last Modified: Tue, 02 Aug 2022 05:45:48 GMT  
		Size: 213.2 MB (213182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d65776201572904d097cfdcb3376d445b11bfc305826f497d3cafee088aeb73`  
		Last Modified: Tue, 02 Aug 2022 05:45:26 GMT  
		Size: 13.4 MB (13444602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470b77fa97db81c4c7ed1ba15b82f7fd432abb5d20e2953a06898a889d44ca6b`  
		Last Modified: Tue, 02 Aug 2022 05:45:23 GMT  
		Size: 508.2 KB (508239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d379b9df62d6176cc3574029981a9616f212f694abac3ff0c2496f1085fdcc`  
		Last Modified: Tue, 02 Aug 2022 05:45:55 GMT  
		Size: 276.5 MB (276483557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471fdb18c79ce00b581ff629619eb0036a43984663200fb5469d088a0fd7cd94`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc5a5735b1907503298caf99bfba5eaa3dae45568c5ccfc1e6b827712df68e`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413477edc7d3364b425f4f540d96cd1b18fc8eab816217afef40a59eda31888`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5315d88b9cf86609914e4b13a77212608dc85fc796a92e5976555d3352900`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:7170e2e7f22cfac76b7a27950010d41e77dab4fa1cf300b1fd491214096a415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:b7147f14c15a0a1775f9ff464da472aff646cfd2f63e58f07743a96b921b2ce8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530761398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824d4df5baa0bffb5b6061b1ceaa0bc916c5ecf6e20ac9cde84123aa9cf392ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:40:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:40:09 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:40:09 GMT
ENV ODOO_VERSION=14.0
# Tue, 02 Aug 2022 05:40:09 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:40:09 GMT
ARG ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
# Tue, 02 Aug 2022 05:41:21 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:41:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:41:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:41:26 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:41:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:41:26 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:41:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:41:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:41:26 GMT
USER odoo
# Tue, 02 Aug 2022 05:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:41:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2a9029ee3604b9372e42d87384e5e066e9148be333e0dc03e9c8f855e427b`  
		Last Modified: Tue, 02 Aug 2022 05:45:48 GMT  
		Size: 213.2 MB (213182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d65776201572904d097cfdcb3376d445b11bfc305826f497d3cafee088aeb73`  
		Last Modified: Tue, 02 Aug 2022 05:45:26 GMT  
		Size: 13.4 MB (13444602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470b77fa97db81c4c7ed1ba15b82f7fd432abb5d20e2953a06898a889d44ca6b`  
		Last Modified: Tue, 02 Aug 2022 05:45:23 GMT  
		Size: 508.2 KB (508239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d379b9df62d6176cc3574029981a9616f212f694abac3ff0c2496f1085fdcc`  
		Last Modified: Tue, 02 Aug 2022 05:45:55 GMT  
		Size: 276.5 MB (276483557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471fdb18c79ce00b581ff629619eb0036a43984663200fb5469d088a0fd7cd94`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc5a5735b1907503298caf99bfba5eaa3dae45568c5ccfc1e6b827712df68e`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8413477edc7d3364b425f4f540d96cd1b18fc8eab816217afef40a59eda31888`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c5315d88b9cf86609914e4b13a77212608dc85fc796a92e5976555d3352900`  
		Last Modified: Tue, 02 Aug 2022 05:45:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:78363e01fc63e389efd1400fbf838f189950289abc5c05f7f987c5e8c93359ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:9977c6306424d0f7f94ac9f20b4a9c9207e42d4e496cc956fab27c5696817dee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556228891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801823ce6d56fb63d05c3eaf4b0fe6131ac62c428bead12bf24ce4b79565233c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Tue, 02 Aug 2022 05:38:38 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:38:43 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:38:43 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:38:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:38:43 GMT
USER odoo
# Tue, 02 Aug 2022 05:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:38:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29cabba1582aa633f647f8397f855b9eebffeabf6201b601666660148618f37`  
		Last Modified: Tue, 02 Aug 2022 05:45:08 GMT  
		Size: 301.5 MB (301547764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16bf0de4cdac436d6447393f99e7907a5e8c19faa39758239042dbc45c260e`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144388658ec9d279aadc2efe07f9b33a2ee7de6520fb76f671305108ff3f1da6`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc20c9811767d44cad7c08557a0fb4d996017021a0c77496bb986e4ce2a81a14`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35b27263c1eb8787b7e6d6f531777416a0b227c47b318ead06f49d155be177`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:78363e01fc63e389efd1400fbf838f189950289abc5c05f7f987c5e8c93359ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:9977c6306424d0f7f94ac9f20b4a9c9207e42d4e496cc956fab27c5696817dee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556228891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801823ce6d56fb63d05c3eaf4b0fe6131ac62c428bead12bf24ce4b79565233c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Tue, 02 Aug 2022 05:38:38 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:38:43 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:38:43 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:38:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:38:43 GMT
USER odoo
# Tue, 02 Aug 2022 05:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:38:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29cabba1582aa633f647f8397f855b9eebffeabf6201b601666660148618f37`  
		Last Modified: Tue, 02 Aug 2022 05:45:08 GMT  
		Size: 301.5 MB (301547764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16bf0de4cdac436d6447393f99e7907a5e8c19faa39758239042dbc45c260e`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144388658ec9d279aadc2efe07f9b33a2ee7de6520fb76f671305108ff3f1da6`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc20c9811767d44cad7c08557a0fb4d996017021a0c77496bb986e4ce2a81a14`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35b27263c1eb8787b7e6d6f531777416a0b227c47b318ead06f49d155be177`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:78363e01fc63e389efd1400fbf838f189950289abc5c05f7f987c5e8c93359ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9977c6306424d0f7f94ac9f20b4a9c9207e42d4e496cc956fab27c5696817dee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556228891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801823ce6d56fb63d05c3eaf4b0fe6131ac62c428bead12bf24ce4b79565233c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_RELEASE=20220727
# Tue, 02 Aug 2022 05:37:21 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Tue, 02 Aug 2022 05:38:38 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 02 Aug 2022 05:38:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 02 Aug 2022 05:38:43 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 02 Aug 2022 05:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Aug 2022 05:38:43 GMT
EXPOSE 8069 8071 8072
# Tue, 02 Aug 2022 05:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Aug 2022 05:38:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 02 Aug 2022 05:38:43 GMT
USER odoo
# Tue, 02 Aug 2022 05:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Aug 2022 05:38:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29cabba1582aa633f647f8397f855b9eebffeabf6201b601666660148618f37`  
		Last Modified: Tue, 02 Aug 2022 05:45:08 GMT  
		Size: 301.5 MB (301547764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b16bf0de4cdac436d6447393f99e7907a5e8c19faa39758239042dbc45c260e`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144388658ec9d279aadc2efe07f9b33a2ee7de6520fb76f671305108ff3f1da6`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc20c9811767d44cad7c08557a0fb4d996017021a0c77496bb986e4ce2a81a14`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35b27263c1eb8787b7e6d6f531777416a0b227c47b318ead06f49d155be177`  
		Last Modified: Tue, 02 Aug 2022 05:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
