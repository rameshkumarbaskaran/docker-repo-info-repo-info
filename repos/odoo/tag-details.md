<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:4d3ca3ca30c305b40f9356ea606f38cf91169289722ae3d1ec28eede45b87e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:c9f38e069a04a29b0b52d5a7b79fdf6ff9fc3340bedbf7bb8c31d581d0f3326b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531126416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0092e1cc6a5e7401da47c1abcfb7d90eb99195bce28771c9d6f13a777feaece0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:52:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:52:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:52:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:54:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:54:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:54:22 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:54:22 GMT
ENV ODOO_VERSION=14.0
# Tue, 15 Nov 2022 14:54:22 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:54:23 GMT
ARG ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
# Tue, 15 Nov 2022 14:55:36 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:55:40 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:55:40 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:55:41 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:55:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:55:41 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:55:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:55:41 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:55:41 GMT
USER odoo
# Tue, 15 Nov 2022 14:55:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:55:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b34b977d9e2c14944e351d9e8090d5360032ae3196bf76c9426aee15b5242`  
		Last Modified: Tue, 15 Nov 2022 14:58:04 GMT  
		Size: 213.2 MB (213185691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba36b7486e11dd53416493de75e4889858b80b3e79a5db728c39a06d005c67a`  
		Last Modified: Tue, 15 Nov 2022 14:57:42 GMT  
		Size: 13.5 MB (13515122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574226e6811aa978fe2238c06ed2681ca26ad2af45ff4a66459051ad5956fbf7`  
		Last Modified: Tue, 15 Nov 2022 14:57:40 GMT  
		Size: 454.3 KB (454333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce63e6e251337b4089c320994dabad6398a64c5d51e7501a55f8c7d37448dae`  
		Last Modified: Tue, 15 Nov 2022 14:58:12 GMT  
		Size: 276.8 MB (276828478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a8fd56aa06510c671e0cd9c3440558e25ec5c7a62a2dd63da915d32d432fa`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c345732cebb0f1ee4a692ed21dbc25f9ae5fb6794c812c78039af75643dcfd4`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084d00c360a5071292dc115aea33bee8e1d63e720f02bef32409934ec5a7962`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97c27a4c334f5acf4ec9d76d0e47316e6ff0ebd4364d5c852fe24272b5e8a41`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:4d3ca3ca30c305b40f9356ea606f38cf91169289722ae3d1ec28eede45b87e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:c9f38e069a04a29b0b52d5a7b79fdf6ff9fc3340bedbf7bb8c31d581d0f3326b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531126416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0092e1cc6a5e7401da47c1abcfb7d90eb99195bce28771c9d6f13a777feaece0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:52:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:52:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:52:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:54:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:54:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:54:22 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:54:22 GMT
ENV ODOO_VERSION=14.0
# Tue, 15 Nov 2022 14:54:22 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:54:23 GMT
ARG ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
# Tue, 15 Nov 2022 14:55:36 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:55:40 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:55:40 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:55:41 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=43aca21407e6fa13957a1ab9e56a268f9d0bbc0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:55:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:55:41 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:55:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:55:41 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:55:41 GMT
USER odoo
# Tue, 15 Nov 2022 14:55:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:55:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b34b977d9e2c14944e351d9e8090d5360032ae3196bf76c9426aee15b5242`  
		Last Modified: Tue, 15 Nov 2022 14:58:04 GMT  
		Size: 213.2 MB (213185691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba36b7486e11dd53416493de75e4889858b80b3e79a5db728c39a06d005c67a`  
		Last Modified: Tue, 15 Nov 2022 14:57:42 GMT  
		Size: 13.5 MB (13515122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574226e6811aa978fe2238c06ed2681ca26ad2af45ff4a66459051ad5956fbf7`  
		Last Modified: Tue, 15 Nov 2022 14:57:40 GMT  
		Size: 454.3 KB (454333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce63e6e251337b4089c320994dabad6398a64c5d51e7501a55f8c7d37448dae`  
		Last Modified: Tue, 15 Nov 2022 14:58:12 GMT  
		Size: 276.8 MB (276828478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a8fd56aa06510c671e0cd9c3440558e25ec5c7a62a2dd63da915d32d432fa`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c345732cebb0f1ee4a692ed21dbc25f9ae5fb6794c812c78039af75643dcfd4`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6084d00c360a5071292dc115aea33bee8e1d63e720f02bef32409934ec5a7962`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97c27a4c334f5acf4ec9d76d0e47316e6ff0ebd4364d5c852fe24272b5e8a41`  
		Last Modified: Tue, 15 Nov 2022 14:57:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:f59a0e1663837e1d9afc72d953ed32f8ceb4f30d568ba5c845201179b36092f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:91d6c8a485e29d8bb5b4d75010eb7894ead3bde56281baaf6cfb5ad24061b2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd59d02ecd3feb1c1200b382252c36a32081fef03c11e1a1a9313c398c0d11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:51:06 GMT
ENV ODOO_VERSION=15.0
# Tue, 15 Nov 2022 14:51:06 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:51:06 GMT
ARG ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
# Tue, 15 Nov 2022 14:52:22 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:52:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:52:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:52:27 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:52:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:52:27 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:52:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:52:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:52:28 GMT
USER odoo
# Tue, 15 Nov 2022 14:52:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:52:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1a1221b8715a9e8cf8828d4479c4c1bae1aff556753f2e50a523637ae81189`  
		Last Modified: Tue, 15 Nov 2022 14:57:29 GMT  
		Size: 304.4 MB (304360667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a5853cf42c400acbd65a44d2461e61a8833955eb67a39a33023c4d75256519`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae2ec1b71f44052c32fb7f31c51c3f22873134f5126a11d507d632b4449f20`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac254b0ad610646c845ef2b4a81ec8e842a9d5f51e7facb303d0d1807462f47`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa53f4980e604fab8e3dfd982a811a8b77dc1941212ac6ababca7c77abb2d6`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:f59a0e1663837e1d9afc72d953ed32f8ceb4f30d568ba5c845201179b36092f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:91d6c8a485e29d8bb5b4d75010eb7894ead3bde56281baaf6cfb5ad24061b2e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd59d02ecd3feb1c1200b382252c36a32081fef03c11e1a1a9313c398c0d11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:51:06 GMT
ENV ODOO_VERSION=15.0
# Tue, 15 Nov 2022 14:51:06 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:51:06 GMT
ARG ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
# Tue, 15 Nov 2022 14:52:22 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:52:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:52:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:52:27 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=0d374f0057f67fcece809b1c6acc3b8ad7b0c204
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:52:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:52:27 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:52:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:52:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:52:28 GMT
USER odoo
# Tue, 15 Nov 2022 14:52:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:52:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1a1221b8715a9e8cf8828d4479c4c1bae1aff556753f2e50a523637ae81189`  
		Last Modified: Tue, 15 Nov 2022 14:57:29 GMT  
		Size: 304.4 MB (304360667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a5853cf42c400acbd65a44d2461e61a8833955eb67a39a33023c4d75256519`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae2ec1b71f44052c32fb7f31c51c3f22873134f5126a11d507d632b4449f20`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac254b0ad610646c845ef2b4a81ec8e842a9d5f51e7facb303d0d1807462f47`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79aa53f4980e604fab8e3dfd982a811a8b77dc1941212ac6ababca7c77abb2d6`  
		Last Modified: Tue, 15 Nov 2022 14:56:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:324fa50feca2ee42e483982343afcc5ab2177e2e4bf2615df394d3fe598d8a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:8cb18af9fdf93c76890d44fb78c0ab00281cd9253dbeeb505410b076defe3e75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557942976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6177a2f39ec6785261103b99db9f47a3f5c6ab89c2516094a4b5ecf10d6ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
# Tue, 15 Nov 2022 14:50:52 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:50:57 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:50:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:50:57 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:50:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:50:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:50:58 GMT
USER odoo
# Tue, 15 Nov 2022 14:50:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:50:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32000ab6295be00ce803ab7702f0cfa1156164c59648bdc1036c96aad957b1`  
		Last Modified: Tue, 15 Nov 2022 14:56:43 GMT  
		Size: 303.2 MB (303203101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e31647634da323a5323eb185b908b87cd8b8d5e2fabd6e6059d9891a483dd04`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444eda47df3f1f7145a0062e1630ddf488f14919664f2556f724608a9ba0dfac`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbfab00208a4ed6ee22dd2c2eec7f63e2c1e89b2fabd7da03083a2c15f1c1c`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c48a225516c8193089da6a56f294a9f30fe84bf0ad74251fac7debeff7bf0`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:324fa50feca2ee42e483982343afcc5ab2177e2e4bf2615df394d3fe598d8a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:8cb18af9fdf93c76890d44fb78c0ab00281cd9253dbeeb505410b076defe3e75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557942976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6177a2f39ec6785261103b99db9f47a3f5c6ab89c2516094a4b5ecf10d6ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
# Tue, 15 Nov 2022 14:50:52 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:50:57 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:50:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:50:57 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:50:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:50:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:50:58 GMT
USER odoo
# Tue, 15 Nov 2022 14:50:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:50:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32000ab6295be00ce803ab7702f0cfa1156164c59648bdc1036c96aad957b1`  
		Last Modified: Tue, 15 Nov 2022 14:56:43 GMT  
		Size: 303.2 MB (303203101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e31647634da323a5323eb185b908b87cd8b8d5e2fabd6e6059d9891a483dd04`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444eda47df3f1f7145a0062e1630ddf488f14919664f2556f724608a9ba0dfac`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbfab00208a4ed6ee22dd2c2eec7f63e2c1e89b2fabd7da03083a2c15f1c1c`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c48a225516c8193089da6a56f294a9f30fe84bf0ad74251fac7debeff7bf0`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:324fa50feca2ee42e483982343afcc5ab2177e2e4bf2615df394d3fe598d8a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8cb18af9fdf93c76890d44fb78c0ab00281cd9253dbeeb505410b076defe3e75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557942976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6177a2f39ec6785261103b99db9f47a3f5c6ab89c2516094a4b5ecf10d6ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_RELEASE=20221104
# Tue, 15 Nov 2022 14:49:31 GMT
ARG ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
# Tue, 15 Nov 2022 14:50:52 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 15 Nov 2022 14:50:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 15 Nov 2022 14:50:57 GMT
# ARGS: ODOO_RELEASE=20221104 ODOO_SHA=992e4f25439ce8adf4c235d3a3876f4191404ef8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 15 Nov 2022 14:50:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Nov 2022 14:50:57 GMT
EXPOSE 8069 8071 8072
# Tue, 15 Nov 2022 14:50:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Nov 2022 14:50:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 15 Nov 2022 14:50:58 GMT
USER odoo
# Tue, 15 Nov 2022 14:50:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Nov 2022 14:50:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32000ab6295be00ce803ab7702f0cfa1156164c59648bdc1036c96aad957b1`  
		Last Modified: Tue, 15 Nov 2022 14:56:43 GMT  
		Size: 303.2 MB (303203101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e31647634da323a5323eb185b908b87cd8b8d5e2fabd6e6059d9891a483dd04`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444eda47df3f1f7145a0062e1630ddf488f14919664f2556f724608a9ba0dfac`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbfab00208a4ed6ee22dd2c2eec7f63e2c1e89b2fabd7da03083a2c15f1c1c`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c48a225516c8193089da6a56f294a9f30fe84bf0ad74251fac7debeff7bf0`  
		Last Modified: Tue, 15 Nov 2022 14:56:06 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
