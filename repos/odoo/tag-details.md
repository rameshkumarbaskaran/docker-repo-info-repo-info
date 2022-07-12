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
$ docker pull odoo@sha256:4bb343ebfda27627236a88580b902bf5bd840d23a4ab3a8dcbed6f7e8c36f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:f19e2e147122f025955b0816d967e84185a5f1273cdf24f0d64232e9259adda1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540258816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27320ce31761277bc3c32120d10aba6ce72eb2340ba812fbfea74d529ede88ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:07:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:12:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:12:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:12:13 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:12:13 GMT
ENV ODOO_VERSION=13.0
# Tue, 12 Jul 2022 05:12:13 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:12:13 GMT
ARG ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
# Tue, 12 Jul 2022 05:13:29 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:13:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:13:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:13:33 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:13:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:13:33 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:13:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:13:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:13:34 GMT
USER odoo
# Tue, 12 Jul 2022 05:13:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:13:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7852edb0bc3cf7963a8d53091d65864192ba609316a32de7d373812c11a43e28`  
		Last Modified: Tue, 12 Jul 2022 05:15:58 GMT  
		Size: 207.1 MB (207143706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eea1562761dce01430688c0be779ab4da5abf82e2aa502688ff39d9785fa17f`  
		Last Modified: Tue, 12 Jul 2022 05:15:36 GMT  
		Size: 13.4 MB (13442978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c92a3860784edf4233f1a93fc66b06c2d4a3cb36d3a60f468648fa36cad3a5`  
		Last Modified: Tue, 12 Jul 2022 05:15:33 GMT  
		Size: 507.3 KB (507319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e903734b9df784cb47b163c34ddf38ea99d96e42a67c4551b4389fc0d0bee40`  
		Last Modified: Tue, 12 Jul 2022 05:16:04 GMT  
		Size: 292.0 MB (292022500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a580eb61cf6a903eaf048111d4b7937aa7ec69e52387e88e8368246c140ea07b`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86472d5d859e18f8f42b5e19f70731e348f068c5504f71d12022678bf73c1b`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad1be2c0244a07d5cc2a7d3d2534164b70c2806fb4c2320cd0e983ee8d6b633`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dcd8ec1bf0b62a74bdeefae2089854d73d562bd12a469bea49e2003c816bd0`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:4bb343ebfda27627236a88580b902bf5bd840d23a4ab3a8dcbed6f7e8c36f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:f19e2e147122f025955b0816d967e84185a5f1273cdf24f0d64232e9259adda1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540258816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27320ce31761277bc3c32120d10aba6ce72eb2340ba812fbfea74d529ede88ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:07:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:12:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:12:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:12:13 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:12:13 GMT
ENV ODOO_VERSION=13.0
# Tue, 12 Jul 2022 05:12:13 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:12:13 GMT
ARG ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
# Tue, 12 Jul 2022 05:13:29 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:13:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:13:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:13:33 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:13:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:13:33 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:13:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:13:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:13:34 GMT
USER odoo
# Tue, 12 Jul 2022 05:13:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:13:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7852edb0bc3cf7963a8d53091d65864192ba609316a32de7d373812c11a43e28`  
		Last Modified: Tue, 12 Jul 2022 05:15:58 GMT  
		Size: 207.1 MB (207143706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eea1562761dce01430688c0be779ab4da5abf82e2aa502688ff39d9785fa17f`  
		Last Modified: Tue, 12 Jul 2022 05:15:36 GMT  
		Size: 13.4 MB (13442978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c92a3860784edf4233f1a93fc66b06c2d4a3cb36d3a60f468648fa36cad3a5`  
		Last Modified: Tue, 12 Jul 2022 05:15:33 GMT  
		Size: 507.3 KB (507319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e903734b9df784cb47b163c34ddf38ea99d96e42a67c4551b4389fc0d0bee40`  
		Last Modified: Tue, 12 Jul 2022 05:16:04 GMT  
		Size: 292.0 MB (292022500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a580eb61cf6a903eaf048111d4b7937aa7ec69e52387e88e8368246c140ea07b`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae86472d5d859e18f8f42b5e19f70731e348f068c5504f71d12022678bf73c1b`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad1be2c0244a07d5cc2a7d3d2534164b70c2806fb4c2320cd0e983ee8d6b633`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dcd8ec1bf0b62a74bdeefae2089854d73d562bd12a469bea49e2003c816bd0`  
		Last Modified: Tue, 12 Jul 2022 05:15:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:73f0be8654adabe5c9c76f648805a1a229a29a50ebbbe3d1566bd4d0c49b3fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:0d4ef230c6dde4652c3701a83408590a1237c18ae45996eedff1e28257153f4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.6 MB (530613002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8c5377f6e898adf708f7e83f52228a3d7191af400bc8a9830b723f3ea46d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:07:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:09:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:09:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:33 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:09:33 GMT
ENV ODOO_VERSION=14.0
# Tue, 12 Jul 2022 05:09:33 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:09:33 GMT
ARG ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
# Tue, 12 Jul 2022 05:10:44 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:10:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:10:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:10:48 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:10:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:10:48 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:10:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:10:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:10:49 GMT
USER odoo
# Tue, 12 Jul 2022 05:10:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db92b31c88865d67202221ad996ca6f787faca3044b81dfa2f2d0aba24d76c`  
		Last Modified: Tue, 12 Jul 2022 05:15:14 GMT  
		Size: 213.2 MB (213181225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a26123be6a074f5572314d58f00bdce78d718ad7637c765aed5cb40216aa68f`  
		Last Modified: Tue, 12 Jul 2022 05:14:51 GMT  
		Size: 13.4 MB (13444821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6a2f05ad0ade1ec05cf84832a9f66415f833cf01f60102a4206e5254e1d73`  
		Last Modified: Tue, 12 Jul 2022 05:14:48 GMT  
		Size: 507.3 KB (507328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6663b7137290bf80ae5dd8977b4c73026510d39444356c0d36064c592c9fd0`  
		Last Modified: Tue, 12 Jul 2022 05:15:21 GMT  
		Size: 276.3 MB (276337312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b3e8ee0b2bab92de9a02c8b6114c7e5e70e0815bb23a9547ded6d2b6a1323`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8108ef329ec9a4dc3f50d4f8f0c0f48f4beef0ad1791d801dadef3b5e41379b2`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e95a73e9788a7d67361a90d4ac874131eec409839dcd43bdf3b2a1aa459c591`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24036e5c48fd6e554982f8d524ab7a1b3c5d62c8c3a01b8eea6088c62198067`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:73f0be8654adabe5c9c76f648805a1a229a29a50ebbbe3d1566bd4d0c49b3fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:0d4ef230c6dde4652c3701a83408590a1237c18ae45996eedff1e28257153f4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.6 MB (530613002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c8c5377f6e898adf708f7e83f52228a3d7191af400bc8a9830b723f3ea46d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:07:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:07:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:09:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:09:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:09:33 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:09:33 GMT
ENV ODOO_VERSION=14.0
# Tue, 12 Jul 2022 05:09:33 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:09:33 GMT
ARG ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
# Tue, 12 Jul 2022 05:10:44 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:10:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:10:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:10:48 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:10:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:10:48 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:10:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:10:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:10:49 GMT
USER odoo
# Tue, 12 Jul 2022 05:10:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:10:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7db92b31c88865d67202221ad996ca6f787faca3044b81dfa2f2d0aba24d76c`  
		Last Modified: Tue, 12 Jul 2022 05:15:14 GMT  
		Size: 213.2 MB (213181225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a26123be6a074f5572314d58f00bdce78d718ad7637c765aed5cb40216aa68f`  
		Last Modified: Tue, 12 Jul 2022 05:14:51 GMT  
		Size: 13.4 MB (13444821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6a2f05ad0ade1ec05cf84832a9f66415f833cf01f60102a4206e5254e1d73`  
		Last Modified: Tue, 12 Jul 2022 05:14:48 GMT  
		Size: 507.3 KB (507328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6663b7137290bf80ae5dd8977b4c73026510d39444356c0d36064c592c9fd0`  
		Last Modified: Tue, 12 Jul 2022 05:15:21 GMT  
		Size: 276.3 MB (276337312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783b3e8ee0b2bab92de9a02c8b6114c7e5e70e0815bb23a9547ded6d2b6a1323`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8108ef329ec9a4dc3f50d4f8f0c0f48f4beef0ad1791d801dadef3b5e41379b2`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e95a73e9788a7d67361a90d4ac874131eec409839dcd43bdf3b2a1aa459c591`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24036e5c48fd6e554982f8d524ab7a1b3c5d62c8c3a01b8eea6088c62198067`  
		Last Modified: Tue, 12 Jul 2022 05:14:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:7f504868a038ef6ffdb21cd0157992a4a8c4786cc44338287c9c79829ba58f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:86beac119c4a2c8875beb22846589be3a4c416de72fe5932913c4e0c10f9656e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555997148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f4691df7b83f9262f500a4626fd95336bff3e4e819dff39a9314b0f259762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:04:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:04:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:04:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:05:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:05:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:05:45 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Tue, 12 Jul 2022 05:07:00 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:07:04 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:07:05 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:07:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:07:05 GMT
USER odoo
# Tue, 12 Jul 2022 05:07:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:07:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd973b6810fdbba62ef6caa3ec20f653447cd19ce0363dc02605f788609e3250`  
		Last Modified: Tue, 12 Jul 2022 05:14:24 GMT  
		Size: 220.3 MB (220289612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f428c41f4b038745626ff998e2d14ffd12d10db8fd0ca26db599d6427281e19`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 2.5 MB (2513248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3d7b1346d040310c399b056054bed18f042bdc35c215a26e90aaa77cc27c0`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 500.9 KB (500921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef71235ae8aed2a0852fac4e0bb02ec93adb286841ec0b1116b1c91bec4ebd94`  
		Last Modified: Tue, 12 Jul 2022 05:14:32 GMT  
		Size: 301.3 MB (301324297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f6abab6ef9b470c117bf9f8e500212183ab5296b3893c89567724a918277`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fe699d0f7d0e568d895d7b54d49852a77d728947b1808168f079b77e1f3f1`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d92d364f0ec62e24e0b325c6d6c352966a63d091e9aebf9ff42f68b30f0b19`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d468e3f46819db39e9e41b14d2ae73b47cea5c4a7d0402da22885a0bc448bd94`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:7f504868a038ef6ffdb21cd0157992a4a8c4786cc44338287c9c79829ba58f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:86beac119c4a2c8875beb22846589be3a4c416de72fe5932913c4e0c10f9656e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555997148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f4691df7b83f9262f500a4626fd95336bff3e4e819dff39a9314b0f259762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:04:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:04:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:04:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:05:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:05:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:05:45 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Tue, 12 Jul 2022 05:07:00 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:07:04 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:07:05 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:07:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:07:05 GMT
USER odoo
# Tue, 12 Jul 2022 05:07:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:07:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd973b6810fdbba62ef6caa3ec20f653447cd19ce0363dc02605f788609e3250`  
		Last Modified: Tue, 12 Jul 2022 05:14:24 GMT  
		Size: 220.3 MB (220289612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f428c41f4b038745626ff998e2d14ffd12d10db8fd0ca26db599d6427281e19`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 2.5 MB (2513248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3d7b1346d040310c399b056054bed18f042bdc35c215a26e90aaa77cc27c0`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 500.9 KB (500921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef71235ae8aed2a0852fac4e0bb02ec93adb286841ec0b1116b1c91bec4ebd94`  
		Last Modified: Tue, 12 Jul 2022 05:14:32 GMT  
		Size: 301.3 MB (301324297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f6abab6ef9b470c117bf9f8e500212183ab5296b3893c89567724a918277`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fe699d0f7d0e568d895d7b54d49852a77d728947b1808168f079b77e1f3f1`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d92d364f0ec62e24e0b325c6d6c352966a63d091e9aebf9ff42f68b30f0b19`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d468e3f46819db39e9e41b14d2ae73b47cea5c4a7d0402da22885a0bc448bd94`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7f504868a038ef6ffdb21cd0157992a4a8c4786cc44338287c9c79829ba58f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:86beac119c4a2c8875beb22846589be3a4c416de72fe5932913c4e0c10f9656e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (555997148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f4691df7b83f9262f500a4626fd95336bff3e4e819dff39a9314b0f259762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:10 GMT
ADD file:d978f6d3025a06f5142a0c13c98bf12fbd47cdf9162ed31fbc05c86983b0a679 in / 
# Tue, 12 Jul 2022 01:20:10 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 05:04:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jul 2022 05:04:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jul 2022 05:04:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 05:05:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jul 2022 05:05:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 05:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Jul 2022 05:05:45 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_RELEASE=20220708
# Tue, 12 Jul 2022 05:05:45 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Tue, 12 Jul 2022 05:07:00 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Jul 2022 05:07:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Jul 2022 05:07:04 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Jul 2022 05:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Jul 2022 05:07:05 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Jul 2022 05:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Jul 2022 05:07:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Jul 2022 05:07:05 GMT
USER odoo
# Tue, 12 Jul 2022 05:07:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jul 2022 05:07:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:461246efe0a75316d99afdbf348f7063b57b0caeee8daab775f1f08152ea36f4`  
		Last Modified: Tue, 12 Jul 2022 01:24:34 GMT  
		Size: 31.4 MB (31366610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd973b6810fdbba62ef6caa3ec20f653447cd19ce0363dc02605f788609e3250`  
		Last Modified: Tue, 12 Jul 2022 05:14:24 GMT  
		Size: 220.3 MB (220289612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f428c41f4b038745626ff998e2d14ffd12d10db8fd0ca26db599d6427281e19`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 2.5 MB (2513248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb3d7b1346d040310c399b056054bed18f042bdc35c215a26e90aaa77cc27c0`  
		Last Modified: Tue, 12 Jul 2022 05:13:58 GMT  
		Size: 500.9 KB (500921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef71235ae8aed2a0852fac4e0bb02ec93adb286841ec0b1116b1c91bec4ebd94`  
		Last Modified: Tue, 12 Jul 2022 05:14:32 GMT  
		Size: 301.3 MB (301324297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f6abab6ef9b470c117bf9f8e500212183ab5296b3893c89567724a918277`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fe699d0f7d0e568d895d7b54d49852a77d728947b1808168f079b77e1f3f1`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d92d364f0ec62e24e0b325c6d6c352966a63d091e9aebf9ff42f68b30f0b19`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d468e3f46819db39e9e41b14d2ae73b47cea5c4a7d0402da22885a0bc448bd94`  
		Last Modified: Tue, 12 Jul 2022 05:13:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
