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
$ docker pull odoo@sha256:e623082be29303c67d95122feb449170ad88725e41086f8611839560103c42f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:f13ee2c19e159808a4ab205e10e934eed2fafdd5e9dfeb477813d8b730d39f4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540321537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14a46751d90d941046a628d1d0a8440819f903bbd67e5b14949b9573972aff3`
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
# Wed, 27 Jul 2022 18:42:06 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:42:06 GMT
ARG ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
# Wed, 27 Jul 2022 18:43:21 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:43:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:43:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:43:25 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:43:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:43:26 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:43:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:43:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:43:26 GMT
USER odoo
# Wed, 27 Jul 2022 18:43:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:43:26 GMT
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
	-	`sha256:f8b45c61d554a17f988c64c84ab88b645ee589876e7018e715fda98706936c98`  
		Last Modified: Wed, 27 Jul 2022 18:45:47 GMT  
		Size: 292.1 MB (292085221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eb0930cbea76e5d35a24f4cd9d2ca8c6fb4a5613decf4ca7651fa25825e558`  
		Last Modified: Wed, 27 Jul 2022 18:45:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7432fa0469902e190ef4bd0f6efc533eb458440f420658aea82093a1dfcb56`  
		Last Modified: Wed, 27 Jul 2022 18:45:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179ee130a65a5655ae7c02bae113702f343c305b944c0c9511f2769cd0b254c3`  
		Last Modified: Wed, 27 Jul 2022 18:45:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046af49de7e7fa3e2a30d9c596c533ba57b1708d0b4c041f44ba3b7bcd97180c`  
		Last Modified: Wed, 27 Jul 2022 18:45:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e623082be29303c67d95122feb449170ad88725e41086f8611839560103c42f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:f13ee2c19e159808a4ab205e10e934eed2fafdd5e9dfeb477813d8b730d39f4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540321537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14a46751d90d941046a628d1d0a8440819f903bbd67e5b14949b9573972aff3`
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
# Wed, 27 Jul 2022 18:42:06 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:42:06 GMT
ARG ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
# Wed, 27 Jul 2022 18:43:21 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:43:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:43:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:43:25 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=2671e352d9f46cc4ef24334cde0d4051634e9c61
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:43:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:43:26 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:43:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:43:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:43:26 GMT
USER odoo
# Wed, 27 Jul 2022 18:43:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:43:26 GMT
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
	-	`sha256:f8b45c61d554a17f988c64c84ab88b645ee589876e7018e715fda98706936c98`  
		Last Modified: Wed, 27 Jul 2022 18:45:47 GMT  
		Size: 292.1 MB (292085221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eb0930cbea76e5d35a24f4cd9d2ca8c6fb4a5613decf4ca7651fa25825e558`  
		Last Modified: Wed, 27 Jul 2022 18:45:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7432fa0469902e190ef4bd0f6efc533eb458440f420658aea82093a1dfcb56`  
		Last Modified: Wed, 27 Jul 2022 18:45:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179ee130a65a5655ae7c02bae113702f343c305b944c0c9511f2769cd0b254c3`  
		Last Modified: Wed, 27 Jul 2022 18:45:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046af49de7e7fa3e2a30d9c596c533ba57b1708d0b4c041f44ba3b7bcd97180c`  
		Last Modified: Wed, 27 Jul 2022 18:45:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:8be2592e8bd2cbf3876cfe935f8c32b2b6ab763aacd42a0134c25602003f871f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:5b0a1d6eacd747b285a1b87d6b7377f4c0437f8e5be5a4780e36a4a4fe2b10e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530759322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28717b82f2d3cc09716dfd8bb30d5d8d366a1c6f39878b76b06311536be867c`
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
# Wed, 27 Jul 2022 18:40:43 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:40:43 GMT
ARG ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
# Wed, 27 Jul 2022 18:41:57 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:42:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:42:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:42:02 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:42:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:42:02 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:42:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:42:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:42:02 GMT
USER odoo
# Wed, 27 Jul 2022 18:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:42:02 GMT
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
	-	`sha256:cfb25280340001b5f8e0acc076879559e8555afab2df39a4da0283a50964c71c`  
		Last Modified: Wed, 27 Jul 2022 18:45:03 GMT  
		Size: 276.5 MB (276483633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2012003d0ea294de3b2030ee6750d3f8c816c4ef6d0bec5cb35729a449878b`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9cf29b2fd989db99d31072192595718e344da676909618bfc067e4d3cd9f21`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338d01c0c011529b657f8d55c691f2095eb389172c051ed86c65b77a33867818`  
		Last Modified: Wed, 27 Jul 2022 18:44:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4a791859c38a435b739ac4cdec4812fecba1f7d516c8d628e5acb0aea9f66`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:8be2592e8bd2cbf3876cfe935f8c32b2b6ab763aacd42a0134c25602003f871f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:5b0a1d6eacd747b285a1b87d6b7377f4c0437f8e5be5a4780e36a4a4fe2b10e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530759322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28717b82f2d3cc09716dfd8bb30d5d8d366a1c6f39878b76b06311536be867c`
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
# Wed, 27 Jul 2022 18:40:43 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:40:43 GMT
ARG ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
# Wed, 27 Jul 2022 18:41:57 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:42:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:42:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:42:02 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bd11bdc60157ae345991e230fa4fb77b79dd1467
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:42:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:42:02 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:42:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:42:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:42:02 GMT
USER odoo
# Wed, 27 Jul 2022 18:42:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:42:02 GMT
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
	-	`sha256:cfb25280340001b5f8e0acc076879559e8555afab2df39a4da0283a50964c71c`  
		Last Modified: Wed, 27 Jul 2022 18:45:03 GMT  
		Size: 276.5 MB (276483633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2012003d0ea294de3b2030ee6750d3f8c816c4ef6d0bec5cb35729a449878b`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9cf29b2fd989db99d31072192595718e344da676909618bfc067e4d3cd9f21`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338d01c0c011529b657f8d55c691f2095eb389172c051ed86c65b77a33867818`  
		Last Modified: Wed, 27 Jul 2022 18:44:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4a791859c38a435b739ac4cdec4812fecba1f7d516c8d628e5acb0aea9f66`  
		Last Modified: Wed, 27 Jul 2022 18:44:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:212de9c02986585eafb2bed5562fccb43d54da3d1a334eab8dbee16e70f49f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:0df4d6ddbc9a1d40fc0a8578d6b61b729adb53107b2e5bd4b5f640abf9cfe7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556220535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3931abd75d285e6ce903293ff46637dce75ef5e248a9e54bfbace05bc0cf31`
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
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Wed, 27 Jul 2022 18:40:24 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:40:29 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:40:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:40:29 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:40:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:40:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:40:29 GMT
USER odoo
# Wed, 27 Jul 2022 18:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:40:29 GMT
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
	-	`sha256:17fa7bd06e54f6197ee7d411f728cb5bcc1d780ca73e6c1649f619fca1741f30`  
		Last Modified: Wed, 27 Jul 2022 18:44:16 GMT  
		Size: 301.5 MB (301547683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838c89457ebf5051582e52fa9e8d69f2fb2703f127279a8241f54e476abc8e94`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5e02771a9a53febf8f695520b33a763fbc45551ae9f236741b41df30cfe4d`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aea699b8910abe88c21ab862ea33466886e53e36290643fb9dae06de18f342`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a89bf710d6c558e778b3671653ac9f667144c7b2d372fc3891e75499a3c45`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:212de9c02986585eafb2bed5562fccb43d54da3d1a334eab8dbee16e70f49f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:0df4d6ddbc9a1d40fc0a8578d6b61b729adb53107b2e5bd4b5f640abf9cfe7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556220535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3931abd75d285e6ce903293ff46637dce75ef5e248a9e54bfbace05bc0cf31`
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
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Wed, 27 Jul 2022 18:40:24 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:40:29 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:40:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:40:29 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:40:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:40:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:40:29 GMT
USER odoo
# Wed, 27 Jul 2022 18:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:40:29 GMT
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
	-	`sha256:17fa7bd06e54f6197ee7d411f728cb5bcc1d780ca73e6c1649f619fca1741f30`  
		Last Modified: Wed, 27 Jul 2022 18:44:16 GMT  
		Size: 301.5 MB (301547683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838c89457ebf5051582e52fa9e8d69f2fb2703f127279a8241f54e476abc8e94`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5e02771a9a53febf8f695520b33a763fbc45551ae9f236741b41df30cfe4d`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aea699b8910abe88c21ab862ea33466886e53e36290643fb9dae06de18f342`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a89bf710d6c558e778b3671653ac9f667144c7b2d372fc3891e75499a3c45`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:212de9c02986585eafb2bed5562fccb43d54da3d1a334eab8dbee16e70f49f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:0df4d6ddbc9a1d40fc0a8578d6b61b729adb53107b2e5bd4b5f640abf9cfe7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.2 MB (556220535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3931abd75d285e6ce903293ff46637dce75ef5e248a9e54bfbace05bc0cf31`
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
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_RELEASE=20220727
# Wed, 27 Jul 2022 18:39:04 GMT
ARG ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
# Wed, 27 Jul 2022 18:40:24 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 27 Jul 2022 18:40:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 27 Jul 2022 18:40:29 GMT
# ARGS: ODOO_RELEASE=20220727 ODOO_SHA=bf4eae33f81c54c73b83d9c05a318b6e00b43e80
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 27 Jul 2022 18:40:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 27 Jul 2022 18:40:29 GMT
EXPOSE 8069 8071 8072
# Wed, 27 Jul 2022 18:40:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 27 Jul 2022 18:40:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 27 Jul 2022 18:40:29 GMT
USER odoo
# Wed, 27 Jul 2022 18:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Jul 2022 18:40:29 GMT
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
	-	`sha256:17fa7bd06e54f6197ee7d411f728cb5bcc1d780ca73e6c1649f619fca1741f30`  
		Last Modified: Wed, 27 Jul 2022 18:44:16 GMT  
		Size: 301.5 MB (301547683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838c89457ebf5051582e52fa9e8d69f2fb2703f127279a8241f54e476abc8e94`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5e02771a9a53febf8f695520b33a763fbc45551ae9f236741b41df30cfe4d`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8aea699b8910abe88c21ab862ea33466886e53e36290643fb9dae06de18f342`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a89bf710d6c558e778b3671653ac9f667144c7b2d372fc3891e75499a3c45`  
		Last Modified: Wed, 27 Jul 2022 18:43:40 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
