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
$ docker pull odoo@sha256:6ccabbfc8cc3afab7185a13df9d703858f804bf4bc2730ee6e99dc9e6e7677cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:502cc5cff7b340c52dd9498145d4a71a7da395dbadc3419a71368167351c2d43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.2 MB (531171237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeedbe15174f12451728da24fa0c079979ecffc99342b6b5ef56deb70700086`
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
# Wed, 16 Nov 2022 20:38:04 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:38:04 GMT
ARG ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
# Wed, 16 Nov 2022 20:39:24 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:39:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:39:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:39:29 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:39:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:39:29 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:39:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:39:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:39:30 GMT
USER odoo
# Wed, 16 Nov 2022 20:39:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:39:30 GMT
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
	-	`sha256:4d53d070c0530f1c1e9260d40f2dd2dc10798306010c4e809ccf4871c6288a31`  
		Last Modified: Wed, 16 Nov 2022 20:41:57 GMT  
		Size: 276.9 MB (276873295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac1c232f75a117e3b249674b04d1581a9cb6ad8492ec5fea2b873e6f678355`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bd1e881e0f6abe5e8ce9e17914e973f603b519ce8a2fe38a4d12cb0184cc25`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2608995aada3973e87dca8e8ee71b88482620f2299aa5d9ce9c6376f6e11570`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f445fa28e177c5aedc3e76d4beb92d537f4f5ff88f5d92f2bc74094ae3da4b9`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:6ccabbfc8cc3afab7185a13df9d703858f804bf4bc2730ee6e99dc9e6e7677cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:502cc5cff7b340c52dd9498145d4a71a7da395dbadc3419a71368167351c2d43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.2 MB (531171237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeedbe15174f12451728da24fa0c079979ecffc99342b6b5ef56deb70700086`
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
# Wed, 16 Nov 2022 20:38:04 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:38:04 GMT
ARG ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
# Wed, 16 Nov 2022 20:39:24 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:39:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:39:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:39:29 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=e547e291f4ee0cc779f0d4a30fd6e4463bb21910
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:39:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:39:29 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:39:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:39:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:39:30 GMT
USER odoo
# Wed, 16 Nov 2022 20:39:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:39:30 GMT
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
	-	`sha256:4d53d070c0530f1c1e9260d40f2dd2dc10798306010c4e809ccf4871c6288a31`  
		Last Modified: Wed, 16 Nov 2022 20:41:57 GMT  
		Size: 276.9 MB (276873295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cac1c232f75a117e3b249674b04d1581a9cb6ad8492ec5fea2b873e6f678355`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bd1e881e0f6abe5e8ce9e17914e973f603b519ce8a2fe38a4d12cb0184cc25`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2608995aada3973e87dca8e8ee71b88482620f2299aa5d9ce9c6376f6e11570`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f445fa28e177c5aedc3e76d4beb92d537f4f5ff88f5d92f2bc74094ae3da4b9`  
		Last Modified: Wed, 16 Nov 2022 20:41:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:15c123e9a3cbe27ca02651963bc35304190ed5e3968523d5d54383cf987840a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:77da366600fd48d088f1b44170f5e7e46666ecd7996e14eaa4fc8a453b699fbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559164560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cef4ef5c2a8dc667119cbf625b8c9953b57334c16c68646b7716177a2e63405`
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
# Wed, 16 Nov 2022 20:36:25 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:36:26 GMT
ARG ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
# Wed, 16 Nov 2022 20:37:42 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:37:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:37:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:37:47 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:37:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:37:47 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:37:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:37:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:37:47 GMT
USER odoo
# Wed, 16 Nov 2022 20:37:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:37:48 GMT
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
	-	`sha256:d3dffb15531732ee1ca86f1424ffcbde8565fe91cf93f049719b3314b734ee9d`  
		Last Modified: Wed, 16 Nov 2022 20:41:16 GMT  
		Size: 304.4 MB (304424686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd25fcf67dfe4bf68b076dd9b8b5f776ad850c9bc60a8f1230354bb047f607ce`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94b44697767e311214e3f628da6442ad91b155d4c7f6f65c8fe85a6f599d4c0`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96cd09f9c6976f6ae7a47fb807c967e29f3a99a88d773ea177251d9f580ea71`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c872af70f5339782d54fb5fb538652007213e92fdd14529310a1a2d5e222a6e0`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:15c123e9a3cbe27ca02651963bc35304190ed5e3968523d5d54383cf987840a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:77da366600fd48d088f1b44170f5e7e46666ecd7996e14eaa4fc8a453b699fbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559164560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cef4ef5c2a8dc667119cbf625b8c9953b57334c16c68646b7716177a2e63405`
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
# Wed, 16 Nov 2022 20:36:25 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:36:26 GMT
ARG ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
# Wed, 16 Nov 2022 20:37:42 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:37:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:37:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:37:47 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=2e8e5d5851e711fe1e1b19dad9dce224fa2ef25f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:37:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:37:47 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:37:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:37:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:37:47 GMT
USER odoo
# Wed, 16 Nov 2022 20:37:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:37:48 GMT
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
	-	`sha256:d3dffb15531732ee1ca86f1424ffcbde8565fe91cf93f049719b3314b734ee9d`  
		Last Modified: Wed, 16 Nov 2022 20:41:16 GMT  
		Size: 304.4 MB (304424686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd25fcf67dfe4bf68b076dd9b8b5f776ad850c9bc60a8f1230354bb047f607ce`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94b44697767e311214e3f628da6442ad91b155d4c7f6f65c8fe85a6f599d4c0`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96cd09f9c6976f6ae7a47fb807c967e29f3a99a88d773ea177251d9f580ea71`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c872af70f5339782d54fb5fb538652007213e92fdd14529310a1a2d5e222a6e0`  
		Last Modified: Wed, 16 Nov 2022 20:40:39 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:0dd99946e5fcd1876a5968802972ebd12eb7bb4097db218e4caadbf0a4ee5e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:162a6a9191afa716a63046aeae6f9a0f92a4ee1a543527b29339726cd01f825d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560020637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e60f57a3a099c4118c7014951f04b289d91ab48152e5d0ee9c95c68df58676`
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
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
# Wed, 16 Nov 2022 20:36:03 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:36:08 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:36:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:36:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:36:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:36:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:36:09 GMT
USER odoo
# Wed, 16 Nov 2022 20:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:36:09 GMT
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
	-	`sha256:6388be73d8f7860febc496e3cd34eb8fc4328d1f939bc46064c34d5ee24f2257`  
		Last Modified: Wed, 16 Nov 2022 20:40:27 GMT  
		Size: 305.3 MB (305280770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fde3dfe34eed509dbc4a1646d25894b30b78217fc90516f7437ac009f31c29`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a71fee193949cbe2f7a19b1ea59696db7c285df34d744e906615ac2ff6af0`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2b249cf4d3e37ffc4ef59ae5649efa958e1d47197cb68db6badf90e66378ab`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2d8dca7b6b9d333e18d17690203c88dae8bea4ea3a105f77fa5184e037337a`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0dd99946e5fcd1876a5968802972ebd12eb7bb4097db218e4caadbf0a4ee5e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:162a6a9191afa716a63046aeae6f9a0f92a4ee1a543527b29339726cd01f825d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560020637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e60f57a3a099c4118c7014951f04b289d91ab48152e5d0ee9c95c68df58676`
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
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
# Wed, 16 Nov 2022 20:36:03 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:36:08 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:36:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:36:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:36:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:36:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:36:09 GMT
USER odoo
# Wed, 16 Nov 2022 20:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:36:09 GMT
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
	-	`sha256:6388be73d8f7860febc496e3cd34eb8fc4328d1f939bc46064c34d5ee24f2257`  
		Last Modified: Wed, 16 Nov 2022 20:40:27 GMT  
		Size: 305.3 MB (305280770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fde3dfe34eed509dbc4a1646d25894b30b78217fc90516f7437ac009f31c29`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a71fee193949cbe2f7a19b1ea59696db7c285df34d744e906615ac2ff6af0`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2b249cf4d3e37ffc4ef59ae5649efa958e1d47197cb68db6badf90e66378ab`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2d8dca7b6b9d333e18d17690203c88dae8bea4ea3a105f77fa5184e037337a`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:0dd99946e5fcd1876a5968802972ebd12eb7bb4097db218e4caadbf0a4ee5e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:162a6a9191afa716a63046aeae6f9a0f92a4ee1a543527b29339726cd01f825d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560020637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e60f57a3a099c4118c7014951f04b289d91ab48152e5d0ee9c95c68df58676`
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
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_RELEASE=20221116
# Wed, 16 Nov 2022 20:34:32 GMT
ARG ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
# Wed, 16 Nov 2022 20:36:03 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Nov 2022 20:36:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Nov 2022 20:36:08 GMT
# ARGS: ODOO_RELEASE=20221116 ODOO_SHA=ccf93359e8685c4d47d15636cc0c6a1f8ae9b52e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Nov 2022 20:36:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Nov 2022 20:36:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Nov 2022 20:36:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Nov 2022 20:36:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Nov 2022 20:36:09 GMT
USER odoo
# Wed, 16 Nov 2022 20:36:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Nov 2022 20:36:09 GMT
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
	-	`sha256:6388be73d8f7860febc496e3cd34eb8fc4328d1f939bc46064c34d5ee24f2257`  
		Last Modified: Wed, 16 Nov 2022 20:40:27 GMT  
		Size: 305.3 MB (305280770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fde3dfe34eed509dbc4a1646d25894b30b78217fc90516f7437ac009f31c29`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a71fee193949cbe2f7a19b1ea59696db7c285df34d744e906615ac2ff6af0`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2b249cf4d3e37ffc4ef59ae5649efa958e1d47197cb68db6badf90e66378ab`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2d8dca7b6b9d333e18d17690203c88dae8bea4ea3a105f77fa5184e037337a`  
		Last Modified: Wed, 16 Nov 2022 20:39:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
