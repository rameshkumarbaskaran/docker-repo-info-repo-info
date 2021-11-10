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
$ docker pull odoo@sha256:1bef7a11abbe76eefacbe8226c89785c06f820370a10dcacf8f7b5fb59bb0dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:0cd1c5848ad104c007951a80f4c33686180d4473237779666aec15f857baed00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539659640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b415b33abcdb0e3f263154b0ab5af45426788c5a8f112d585e63e1252ee12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:04:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:04:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 12:09:43 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Oct 2021 12:09:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:10:00 GMT
RUN npm install -g rtlcss
# Tue, 12 Oct 2021 12:10:00 GMT
ENV ODOO_VERSION=13.0
# Wed, 10 Nov 2021 20:39:40 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:39:40 GMT
ARG ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
# Wed, 10 Nov 2021 20:40:56 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:41:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:41:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:41:02 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:41:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:41:02 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:41:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:41:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:41:03 GMT
USER odoo
# Wed, 10 Nov 2021 20:41:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:41:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45015eb54192c2e0c507396977810d7fddab577041c6c02a5758bcbf4d855326`  
		Last Modified: Tue, 12 Oct 2021 12:15:15 GMT  
		Size: 207.1 MB (207130926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8865fe285493c649f819eb839e1553c90a3bb6ef50521345f499df0337d093`  
		Last Modified: Tue, 12 Oct 2021 12:14:51 GMT  
		Size: 13.4 MB (13433045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788061f0dbd60660f54795fdbec83e425330c41bd36f2514ddf332ca7304796e`  
		Last Modified: Tue, 12 Oct 2021 12:14:47 GMT  
		Size: 864.8 KB (864751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68300e2c42fd3356a24cdeb5f2ba24d87428ad442ababa52843d420ef3cb396f`  
		Last Modified: Wed, 10 Nov 2021 20:43:36 GMT  
		Size: 291.1 MB (291088948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7dab4f5e96a078034c8034914b99e8e0bedad6b2a7fc89f3bfc79c0a1e02ae`  
		Last Modified: Wed, 10 Nov 2021 20:43:02 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6b57d181c90e898b63bc52b54101f8fcfdb87ad4c9a9114944a5936364d08`  
		Last Modified: Wed, 10 Nov 2021 20:43:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8718dbcc99cd27225ff8ff2cb42314c74298d427ba9788dcd2b9bec196ea93a`  
		Last Modified: Wed, 10 Nov 2021 20:43:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda587f5216fa878de05a6e05077f90e6ce8c85cf33f16e3d621f1e97464d701`  
		Last Modified: Wed, 10 Nov 2021 20:43:03 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:1bef7a11abbe76eefacbe8226c89785c06f820370a10dcacf8f7b5fb59bb0dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:0cd1c5848ad104c007951a80f4c33686180d4473237779666aec15f857baed00
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539659640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572b415b33abcdb0e3f263154b0ab5af45426788c5a8f112d585e63e1252ee12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:04:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:04:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 12:09:43 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Oct 2021 12:09:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:10:00 GMT
RUN npm install -g rtlcss
# Tue, 12 Oct 2021 12:10:00 GMT
ENV ODOO_VERSION=13.0
# Wed, 10 Nov 2021 20:39:40 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:39:40 GMT
ARG ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
# Wed, 10 Nov 2021 20:40:56 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:41:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:41:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:41:02 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=c4ae69b33bd4353f6023bb57419133de389e0849
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:41:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:41:02 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:41:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:41:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:41:03 GMT
USER odoo
# Wed, 10 Nov 2021 20:41:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:41:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45015eb54192c2e0c507396977810d7fddab577041c6c02a5758bcbf4d855326`  
		Last Modified: Tue, 12 Oct 2021 12:15:15 GMT  
		Size: 207.1 MB (207130926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8865fe285493c649f819eb839e1553c90a3bb6ef50521345f499df0337d093`  
		Last Modified: Tue, 12 Oct 2021 12:14:51 GMT  
		Size: 13.4 MB (13433045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788061f0dbd60660f54795fdbec83e425330c41bd36f2514ddf332ca7304796e`  
		Last Modified: Tue, 12 Oct 2021 12:14:47 GMT  
		Size: 864.8 KB (864751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68300e2c42fd3356a24cdeb5f2ba24d87428ad442ababa52843d420ef3cb396f`  
		Last Modified: Wed, 10 Nov 2021 20:43:36 GMT  
		Size: 291.1 MB (291088948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7dab4f5e96a078034c8034914b99e8e0bedad6b2a7fc89f3bfc79c0a1e02ae`  
		Last Modified: Wed, 10 Nov 2021 20:43:02 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6b57d181c90e898b63bc52b54101f8fcfdb87ad4c9a9114944a5936364d08`  
		Last Modified: Wed, 10 Nov 2021 20:43:03 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8718dbcc99cd27225ff8ff2cb42314c74298d427ba9788dcd2b9bec196ea93a`  
		Last Modified: Wed, 10 Nov 2021 20:43:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda587f5216fa878de05a6e05077f90e6ce8c85cf33f16e3d621f1e97464d701`  
		Last Modified: Wed, 10 Nov 2021 20:43:03 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:8fe343c9c42344a130116fc5ff04f9df359867a2e07ab9e6c4bed03e0dd85eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:61d6f63d4f5e0037e0ddf0cf505bea4c0c916da7e98a78aedf99e61f2f2a269f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528529342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ee4d265b8109d7431aab6b58270187fa08cc8d1d1dc1b8c21cca361a46f0ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:04:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:04:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 12:05:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Oct 2021 12:06:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:06:25 GMT
RUN npm install -g rtlcss
# Tue, 12 Oct 2021 12:06:25 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Nov 2021 20:38:02 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:38:02 GMT
ARG ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
# Wed, 10 Nov 2021 20:39:19 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:39:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:39:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:39:22 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:39:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:39:23 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:39:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:39:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:39:23 GMT
USER odoo
# Wed, 10 Nov 2021 20:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:39:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a690652210adb99f7736fa4e78f5c15ebd7443f1779c0f4df93f3ede9b7242f4`  
		Last Modified: Tue, 12 Oct 2021 12:14:26 GMT  
		Size: 213.2 MB (213173260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f39d77a6b54dadd4be888e4329319568a8c6910b227f9968b18b3f32b7e5b8c`  
		Last Modified: Tue, 12 Oct 2021 12:14:00 GMT  
		Size: 13.4 MB (13435702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a022bb6719132cde437ae6e8500998624cebc5c7cfc5a5c69157cb1eeb54eb1`  
		Last Modified: Tue, 12 Oct 2021 12:13:56 GMT  
		Size: 864.7 KB (864743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c55cfef12f9824d52242a37d8a49569990034fc920eb086b13961068701294`  
		Last Modified: Wed, 10 Nov 2021 20:42:53 GMT  
		Size: 273.9 MB (273913662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2947313e0d7c34fe7e776eb7d5360fb0413f687eb47bd32dcffd2b9b10ab823`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426283a3e61c47604d7410e9b4ffce0fcb915ccff95e89e85b37dd5793fe5642`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f2fed166b245f846d1e2859f2b7cb18d931e013c41d1e620cae3461385621`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b34a76b5f5f44c6fa712d164560dc40e9b96da2b68812cbfa6a88b719ead68`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:8fe343c9c42344a130116fc5ff04f9df359867a2e07ab9e6c4bed03e0dd85eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:61d6f63d4f5e0037e0ddf0cf505bea4c0c916da7e98a78aedf99e61f2f2a269f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528529342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ee4d265b8109d7431aab6b58270187fa08cc8d1d1dc1b8c21cca361a46f0ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:04:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:04:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:04:37 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 12:05:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Oct 2021 12:06:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:06:25 GMT
RUN npm install -g rtlcss
# Tue, 12 Oct 2021 12:06:25 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Nov 2021 20:38:02 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:38:02 GMT
ARG ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
# Wed, 10 Nov 2021 20:39:19 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:39:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:39:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:39:22 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=95a45d67d38de6d81399533b8b4e39fca08c1254
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:39:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:39:23 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:39:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:39:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:39:23 GMT
USER odoo
# Wed, 10 Nov 2021 20:39:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:39:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a690652210adb99f7736fa4e78f5c15ebd7443f1779c0f4df93f3ede9b7242f4`  
		Last Modified: Tue, 12 Oct 2021 12:14:26 GMT  
		Size: 213.2 MB (213173260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f39d77a6b54dadd4be888e4329319568a8c6910b227f9968b18b3f32b7e5b8c`  
		Last Modified: Tue, 12 Oct 2021 12:14:00 GMT  
		Size: 13.4 MB (13435702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a022bb6719132cde437ae6e8500998624cebc5c7cfc5a5c69157cb1eeb54eb1`  
		Last Modified: Tue, 12 Oct 2021 12:13:56 GMT  
		Size: 864.7 KB (864743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c55cfef12f9824d52242a37d8a49569990034fc920eb086b13961068701294`  
		Last Modified: Wed, 10 Nov 2021 20:42:53 GMT  
		Size: 273.9 MB (273913662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2947313e0d7c34fe7e776eb7d5360fb0413f687eb47bd32dcffd2b9b10ab823`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426283a3e61c47604d7410e9b4ffce0fcb915ccff95e89e85b37dd5793fe5642`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f2fed166b245f846d1e2859f2b7cb18d931e013c41d1e620cae3461385621`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b34a76b5f5f44c6fa712d164560dc40e9b96da2b68812cbfa6a88b719ead68`  
		Last Modified: Wed, 10 Nov 2021 20:42:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:e39b79832476269b783fc5b9390d785c626940afa11254716ccde910735cff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:dfafa2ba4db5493d045bb2e141fc98cf042075dd6a0dd2430f6ff4a63d72cd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.4 MB (543434189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d42dd6c1193244014421ec356bbac51479900f7c45deb33b98ee24be871ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 01 Nov 2021 18:41:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 01 Nov 2021 18:41:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Nov 2021 18:41:27 GMT
RUN npm install -g rtlcss
# Mon, 01 Nov 2021 18:41:27 GMT
ENV ODOO_VERSION=15.0
# Wed, 10 Nov 2021 20:36:38 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:36:39 GMT
ARG ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
# Wed, 10 Nov 2021 20:37:55 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:37:58 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:37:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:37:58 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:37:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:37:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:37:59 GMT
USER odoo
# Wed, 10 Nov 2021 20:37:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:37:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d273bb832b81c8fc74ca81a08380146f9747b3f7637bf5433fef5384fb5e9`  
		Last Modified: Mon, 01 Nov 2021 18:46:48 GMT  
		Size: 220.3 MB (220290324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891e65741060a6859b64e8966d6bcbe4731e71dbb1cd01aca896ef2b991ba26`  
		Last Modified: Mon, 01 Nov 2021 18:46:18 GMT  
		Size: 2.5 MB (2504919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd209f4a5fab9d306ff448dfa6b447ffbcb548d0ae1feefc6623f66dc2fd43a9`  
		Last Modified: Mon, 01 Nov 2021 18:46:17 GMT  
		Size: 856.1 KB (856062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c882965c72654959d4d8ea746c11a3daa60f13d03c08bd7775dd8aca2b31f`  
		Last Modified: Wed, 10 Nov 2021 20:42:03 GMT  
		Size: 288.4 MB (288423111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d629fc0262d47b2473b0c7bf7b7df1b7b4e2469e043aed5affe2f73fd04f4`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf43b21a47e5221f5164eeb67d74ae60cc1daea45de03a8a1d2799c9ab1c4c75`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75700355c3392d95f62a73a5139fe21fd095cbb992dacf1f4297e6c9cf7db6dc`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e8a3370e53d7d975a7554c9fd8f6ea9b0e8c9388bd5e96dc00d532c6efceee`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e39b79832476269b783fc5b9390d785c626940afa11254716ccde910735cff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:dfafa2ba4db5493d045bb2e141fc98cf042075dd6a0dd2430f6ff4a63d72cd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.4 MB (543434189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d42dd6c1193244014421ec356bbac51479900f7c45deb33b98ee24be871ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 01 Nov 2021 18:41:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 01 Nov 2021 18:41:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Nov 2021 18:41:27 GMT
RUN npm install -g rtlcss
# Mon, 01 Nov 2021 18:41:27 GMT
ENV ODOO_VERSION=15.0
# Wed, 10 Nov 2021 20:36:38 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:36:39 GMT
ARG ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
# Wed, 10 Nov 2021 20:37:55 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:37:58 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:37:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:37:58 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:37:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:37:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:37:59 GMT
USER odoo
# Wed, 10 Nov 2021 20:37:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:37:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d273bb832b81c8fc74ca81a08380146f9747b3f7637bf5433fef5384fb5e9`  
		Last Modified: Mon, 01 Nov 2021 18:46:48 GMT  
		Size: 220.3 MB (220290324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891e65741060a6859b64e8966d6bcbe4731e71dbb1cd01aca896ef2b991ba26`  
		Last Modified: Mon, 01 Nov 2021 18:46:18 GMT  
		Size: 2.5 MB (2504919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd209f4a5fab9d306ff448dfa6b447ffbcb548d0ae1feefc6623f66dc2fd43a9`  
		Last Modified: Mon, 01 Nov 2021 18:46:17 GMT  
		Size: 856.1 KB (856062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c882965c72654959d4d8ea746c11a3daa60f13d03c08bd7775dd8aca2b31f`  
		Last Modified: Wed, 10 Nov 2021 20:42:03 GMT  
		Size: 288.4 MB (288423111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d629fc0262d47b2473b0c7bf7b7df1b7b4e2469e043aed5affe2f73fd04f4`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf43b21a47e5221f5164eeb67d74ae60cc1daea45de03a8a1d2799c9ab1c4c75`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75700355c3392d95f62a73a5139fe21fd095cbb992dacf1f4297e6c9cf7db6dc`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e8a3370e53d7d975a7554c9fd8f6ea9b0e8c9388bd5e96dc00d532c6efceee`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:e39b79832476269b783fc5b9390d785c626940afa11254716ccde910735cff05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:dfafa2ba4db5493d045bb2e141fc98cf042075dd6a0dd2430f6ff4a63d72cd01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.4 MB (543434189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d42dd6c1193244014421ec356bbac51479900f7c45deb33b98ee24be871ff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Oct 2021 12:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Oct 2021 12:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 01 Nov 2021 18:41:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Mon, 01 Nov 2021 18:41:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Nov 2021 18:41:27 GMT
RUN npm install -g rtlcss
# Mon, 01 Nov 2021 18:41:27 GMT
ENV ODOO_VERSION=15.0
# Wed, 10 Nov 2021 20:36:38 GMT
ARG ODOO_RELEASE=20211110
# Wed, 10 Nov 2021 20:36:39 GMT
ARG ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
# Wed, 10 Nov 2021 20:37:55 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Nov 2021 20:37:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Nov 2021 20:37:58 GMT
# ARGS: ODOO_RELEASE=20211110 ODOO_SHA=313cb2c38f939374f524aaebb017ef0e1724e375
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Nov 2021 20:37:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Nov 2021 20:37:58 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Nov 2021 20:37:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Nov 2021 20:37:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Nov 2021 20:37:59 GMT
USER odoo
# Wed, 10 Nov 2021 20:37:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Nov 2021 20:37:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d273bb832b81c8fc74ca81a08380146f9747b3f7637bf5433fef5384fb5e9`  
		Last Modified: Mon, 01 Nov 2021 18:46:48 GMT  
		Size: 220.3 MB (220290324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891e65741060a6859b64e8966d6bcbe4731e71dbb1cd01aca896ef2b991ba26`  
		Last Modified: Mon, 01 Nov 2021 18:46:18 GMT  
		Size: 2.5 MB (2504919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd209f4a5fab9d306ff448dfa6b447ffbcb548d0ae1feefc6623f66dc2fd43a9`  
		Last Modified: Mon, 01 Nov 2021 18:46:17 GMT  
		Size: 856.1 KB (856062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06c882965c72654959d4d8ea746c11a3daa60f13d03c08bd7775dd8aca2b31f`  
		Last Modified: Wed, 10 Nov 2021 20:42:03 GMT  
		Size: 288.4 MB (288423111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d629fc0262d47b2473b0c7bf7b7df1b7b4e2469e043aed5affe2f73fd04f4`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf43b21a47e5221f5164eeb67d74ae60cc1daea45de03a8a1d2799c9ab1c4c75`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75700355c3392d95f62a73a5139fe21fd095cbb992dacf1f4297e6c9cf7db6dc`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e8a3370e53d7d975a7554c9fd8f6ea9b0e8c9388bd5e96dc00d532c6efceee`  
		Last Modified: Wed, 10 Nov 2021 20:41:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
