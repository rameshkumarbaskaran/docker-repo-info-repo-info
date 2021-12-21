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
$ docker pull odoo@sha256:3115d9c75fb17f84105695f3aea1323bf765d257b897ecaecad75a4adfdba343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:ae5bee106df9bc316802ab350b6488309a483552e3d53a8d17810272b524dc59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539398774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936279749ed343a8ff04b7845c9f056d8b8032a34e3d707622f4dc52c60bf062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:25:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:25:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:25:19 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:25:19 GMT
ENV ODOO_VERSION=13.0
# Tue, 21 Dec 2021 19:25:20 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:25:20 GMT
ARG ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
# Tue, 21 Dec 2021 19:26:37 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:26:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:26:43 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:26:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:26:44 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:26:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:26:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:26:44 GMT
USER odoo
# Tue, 21 Dec 2021 19:26:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:26:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d7983b91605c2e8a3cac73cc85ca48790cc3efb1571d857ff46b5671b96cd2`  
		Last Modified: Tue, 21 Dec 2021 19:29:21 GMT  
		Size: 207.1 MB (207130909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0673fc42a3c3aba833b861b907d31819eef5104e4d3d00360399ea3067f7ee0`  
		Last Modified: Tue, 21 Dec 2021 19:28:56 GMT  
		Size: 13.4 MB (13434150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7739cae70db3a175f5335f33dbb8044e12cedf62c7d3f4f6fd31fef19b9d6`  
		Last Modified: Tue, 21 Dec 2021 19:28:53 GMT  
		Size: 424.5 KB (424477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a667545a3e81be6a9e174f8e3131c57d60dafec9fcdcccb8313f49d90c64954`  
		Last Modified: Tue, 21 Dec 2021 19:29:28 GMT  
		Size: 291.3 MB (291253049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8dd7fd4f8691dfe0762fa7dad202e746180270e1d642be1543a3908066cb98`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32956604b132716d77735a183464a138b5eafc222c24e3c6f35c35b4639215e6`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa8d0b7496b74c399d86876e91be8336c0fe81e01582b0b9e316df82759ff87`  
		Last Modified: Tue, 21 Dec 2021 19:28:51 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a20bfb27353ebc5a111de0dad854fbcb8e2ab926ddfda5916bb6c586d6c352`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:3115d9c75fb17f84105695f3aea1323bf765d257b897ecaecad75a4adfdba343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:ae5bee106df9bc316802ab350b6488309a483552e3d53a8d17810272b524dc59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539398774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936279749ed343a8ff04b7845c9f056d8b8032a34e3d707622f4dc52c60bf062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:25:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:25:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:25:19 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:25:19 GMT
ENV ODOO_VERSION=13.0
# Tue, 21 Dec 2021 19:25:20 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:25:20 GMT
ARG ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
# Tue, 21 Dec 2021 19:26:37 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:26:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:26:43 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=02d48b2c7cf5de7e7239d6c7c1fc8456ed3ccdd6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:26:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:26:44 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:26:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:26:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:26:44 GMT
USER odoo
# Tue, 21 Dec 2021 19:26:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:26:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d7983b91605c2e8a3cac73cc85ca48790cc3efb1571d857ff46b5671b96cd2`  
		Last Modified: Tue, 21 Dec 2021 19:29:21 GMT  
		Size: 207.1 MB (207130909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0673fc42a3c3aba833b861b907d31819eef5104e4d3d00360399ea3067f7ee0`  
		Last Modified: Tue, 21 Dec 2021 19:28:56 GMT  
		Size: 13.4 MB (13434150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7739cae70db3a175f5335f33dbb8044e12cedf62c7d3f4f6fd31fef19b9d6`  
		Last Modified: Tue, 21 Dec 2021 19:28:53 GMT  
		Size: 424.5 KB (424477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a667545a3e81be6a9e174f8e3131c57d60dafec9fcdcccb8313f49d90c64954`  
		Last Modified: Tue, 21 Dec 2021 19:29:28 GMT  
		Size: 291.3 MB (291253049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8dd7fd4f8691dfe0762fa7dad202e746180270e1d642be1543a3908066cb98`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32956604b132716d77735a183464a138b5eafc222c24e3c6f35c35b4639215e6`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa8d0b7496b74c399d86876e91be8336c0fe81e01582b0b9e316df82759ff87`  
		Last Modified: Tue, 21 Dec 2021 19:28:51 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a20bfb27353ebc5a111de0dad854fbcb8e2ab926ddfda5916bb6c586d6c352`  
		Last Modified: Tue, 21 Dec 2021 19:28:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:2781a59406dcabd6613612e145a9f2dab16ba2f2b70e9ceb5f998ca5566781d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:a405cac6c86978f346788afd4d17dfc09e752c236892b9f3f33565562baaf990
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529138416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721b644e8da41ca9e115d50bcf683f240db4366cf9648afa85afb4a7d74b132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:21:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:21:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:21:39 GMT
ENV ODOO_VERSION=14.0
# Tue, 21 Dec 2021 19:21:39 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:21:39 GMT
ARG ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
# Tue, 21 Dec 2021 19:23:45 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:23:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:23:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:23:50 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:23:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:23:50 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:23:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:23:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:23:51 GMT
USER odoo
# Tue, 21 Dec 2021 19:23:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:23:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839734d46ac6c7d6d83c758963995a210475151f71764477376223af2bb38950`  
		Last Modified: Tue, 21 Dec 2021 19:28:29 GMT  
		Size: 213.2 MB (213174074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb501610c7e3bdc36fe243d16894877d6e4a1a7dcc18348f023e72526f9147`  
		Last Modified: Tue, 21 Dec 2021 19:28:03 GMT  
		Size: 13.4 MB (13436446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f281d2d1af4d3c80a6a1e6733c78a9432f65f60433a25b542dbe9c75226fd`  
		Last Modified: Tue, 21 Dec 2021 19:28:00 GMT  
		Size: 424.4 KB (424418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede553e74182792429eb96a66c8fe292b02bce89bba3ae22d12d35a30c70964`  
		Last Modified: Tue, 21 Dec 2021 19:28:36 GMT  
		Size: 274.9 MB (274947292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaa81fb898eb2c65f651d52698054f9d12dea63a2027d6504aaa5a169219397`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d0bf4f2bbd308ee563bfd18167b7e1a1ca9eb396bdc94be1545c0f327bcd8`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54cef9e482701dbeb4f2dc2d8217aa333a451cb047b329a5546dc8672901360`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199438c2e0089f3e291bd3e2091b23055dc9ecee6eb15ca0b058ead12008c827`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:2781a59406dcabd6613612e145a9f2dab16ba2f2b70e9ceb5f998ca5566781d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:a405cac6c86978f346788afd4d17dfc09e752c236892b9f3f33565562baaf990
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.1 MB (529138416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2721b644e8da41ca9e115d50bcf683f240db4366cf9648afa85afb4a7d74b132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:21:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:21:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:21:39 GMT
ENV ODOO_VERSION=14.0
# Tue, 21 Dec 2021 19:21:39 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:21:39 GMT
ARG ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
# Tue, 21 Dec 2021 19:23:45 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:23:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:23:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:23:50 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=e97fa0f040b4c7b2529a7ab0a79b8926b575db46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:23:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:23:50 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:23:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:23:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:23:51 GMT
USER odoo
# Tue, 21 Dec 2021 19:23:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:23:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839734d46ac6c7d6d83c758963995a210475151f71764477376223af2bb38950`  
		Last Modified: Tue, 21 Dec 2021 19:28:29 GMT  
		Size: 213.2 MB (213174074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb501610c7e3bdc36fe243d16894877d6e4a1a7dcc18348f023e72526f9147`  
		Last Modified: Tue, 21 Dec 2021 19:28:03 GMT  
		Size: 13.4 MB (13436446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f281d2d1af4d3c80a6a1e6733c78a9432f65f60433a25b542dbe9c75226fd`  
		Last Modified: Tue, 21 Dec 2021 19:28:00 GMT  
		Size: 424.4 KB (424418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ede553e74182792429eb96a66c8fe292b02bce89bba3ae22d12d35a30c70964`  
		Last Modified: Tue, 21 Dec 2021 19:28:36 GMT  
		Size: 274.9 MB (274947292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaa81fb898eb2c65f651d52698054f9d12dea63a2027d6504aaa5a169219397`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d0bf4f2bbd308ee563bfd18167b7e1a1ca9eb396bdc94be1545c0f327bcd8`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54cef9e482701dbeb4f2dc2d8217aa333a451cb047b329a5546dc8672901360`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199438c2e0089f3e291bd3e2091b23055dc9ecee6eb15ca0b058ead12008c827`  
		Last Modified: Tue, 21 Dec 2021 19:27:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:af1c1767faca2249a67560e30b7f0e96a9413dfe15160dbb3709cf3800069487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:b0166c884d85ccf99fcc29f0f0ffe9d61b56a54e2b2c50bc0e388cdbf115ba52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546360735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c963a9620306c5ac3ea03eb18228552b2ae18e20a8337372f84f3f8a81d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Tue, 21 Dec 2021 19:19:48 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:19:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:19:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:19:54 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:19:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:19:54 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:19:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:19:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:19:55 GMT
USER odoo
# Tue, 21 Dec 2021 19:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:19:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f3d83812684614d191ce37d8351e75f8e0b3f4a147aba8a5f5d4bc9eecb41`  
		Last Modified: Tue, 21 Dec 2021 19:27:45 GMT  
		Size: 291.8 MB (291786418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372b4d0f6796c8a803f948792e7d7674e70e3b8958240f0f534651aecc8a5666`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75082d4cef54dcaba9f83fbdf124d9064d016a1212a14844ef7c97c91a0b12`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2beb32d152bea1f6af261c3b25178d862454a5e68967285f786a96396586e4`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f367689813caa53e78c047671fb76eaa6cb25b67da621117a4ed4720e866c`  
		Last Modified: Tue, 21 Dec 2021 19:27:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:af1c1767faca2249a67560e30b7f0e96a9413dfe15160dbb3709cf3800069487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:b0166c884d85ccf99fcc29f0f0ffe9d61b56a54e2b2c50bc0e388cdbf115ba52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546360735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c963a9620306c5ac3ea03eb18228552b2ae18e20a8337372f84f3f8a81d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Tue, 21 Dec 2021 19:19:48 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:19:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:19:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:19:54 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:19:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:19:54 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:19:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:19:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:19:55 GMT
USER odoo
# Tue, 21 Dec 2021 19:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:19:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f3d83812684614d191ce37d8351e75f8e0b3f4a147aba8a5f5d4bc9eecb41`  
		Last Modified: Tue, 21 Dec 2021 19:27:45 GMT  
		Size: 291.8 MB (291786418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372b4d0f6796c8a803f948792e7d7674e70e3b8958240f0f534651aecc8a5666`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75082d4cef54dcaba9f83fbdf124d9064d016a1212a14844ef7c97c91a0b12`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2beb32d152bea1f6af261c3b25178d862454a5e68967285f786a96396586e4`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f367689813caa53e78c047671fb76eaa6cb25b67da621117a4ed4720e866c`  
		Last Modified: Tue, 21 Dec 2021 19:27:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:af1c1767faca2249a67560e30b7f0e96a9413dfe15160dbb3709cf3800069487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b0166c884d85ccf99fcc29f0f0ffe9d61b56a54e2b2c50bc0e388cdbf115ba52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.4 MB (546360735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3c963a9620306c5ac3ea03eb18228552b2ae18e20a8337372f84f3f8a81d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_RELEASE=20211220
# Tue, 21 Dec 2021 19:17:52 GMT
ARG ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
# Tue, 21 Dec 2021 19:19:48 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Dec 2021 19:19:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Dec 2021 19:19:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Dec 2021 19:19:54 GMT
# ARGS: ODOO_RELEASE=20211220 ODOO_SHA=40b41702d22857f29ef3e87056dd826e47c8feb0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Dec 2021 19:19:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Dec 2021 19:19:54 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Dec 2021 19:19:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Dec 2021 19:19:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Dec 2021 19:19:55 GMT
USER odoo
# Tue, 21 Dec 2021 19:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Dec 2021 19:19:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f3d83812684614d191ce37d8351e75f8e0b3f4a147aba8a5f5d4bc9eecb41`  
		Last Modified: Tue, 21 Dec 2021 19:27:45 GMT  
		Size: 291.8 MB (291786418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372b4d0f6796c8a803f948792e7d7674e70e3b8958240f0f534651aecc8a5666`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75082d4cef54dcaba9f83fbdf124d9064d016a1212a14844ef7c97c91a0b12`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2beb32d152bea1f6af261c3b25178d862454a5e68967285f786a96396586e4`  
		Last Modified: Tue, 21 Dec 2021 19:27:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f367689813caa53e78c047671fb76eaa6cb25b67da621117a4ed4720e866c`  
		Last Modified: Tue, 21 Dec 2021 19:27:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
