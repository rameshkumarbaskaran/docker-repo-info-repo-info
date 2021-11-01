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
$ docker pull odoo@sha256:e4f8be58b45648c708f17c03b7956daa51a8cfb734d129203d5140199ff6debe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:fca9402d575a0131ef7eb510b660cb62d72d9d4df2d94e4881fb0c7772b6314d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539615715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78f4972fa4c4058b0eb67fa5bd669cfb32ace1b1ec0389f095db85e6e32afe3`
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
# Mon, 01 Nov 2021 18:44:24 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:44:24 GMT
ARG ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
# Mon, 01 Nov 2021 18:45:42 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:45:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:45:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:45:48 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:45:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:45:49 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:45:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:45:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:45:49 GMT
USER odoo
# Mon, 01 Nov 2021 18:45:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:45:50 GMT
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
	-	`sha256:9983055c000eb48340921f78bdcf279b8d5beb6c55abc2f8f7294e53befce77f`  
		Last Modified: Mon, 01 Nov 2021 18:48:26 GMT  
		Size: 291.0 MB (291045018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00da0c14e70bde3fec687d48737d0dac75916bcda62a0f65312627aadf429ce3`  
		Last Modified: Mon, 01 Nov 2021 18:47:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b9cee3e5391ceadf5fa5259a1b92fb446f559d961ddf11b9575b906cda41e`  
		Last Modified: Mon, 01 Nov 2021 18:47:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a490fe3bf701027712cd8b7b5ea68bd25bc2495a8a12dec723c4fe982d7ee1b`  
		Last Modified: Mon, 01 Nov 2021 18:47:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe05bbd798e701a5f1fc13a8c33d4fe79a80cfa76de3091ede65f559add61ae`  
		Last Modified: Mon, 01 Nov 2021 18:47:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e4f8be58b45648c708f17c03b7956daa51a8cfb734d129203d5140199ff6debe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:fca9402d575a0131ef7eb510b660cb62d72d9d4df2d94e4881fb0c7772b6314d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539615715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78f4972fa4c4058b0eb67fa5bd669cfb32ace1b1ec0389f095db85e6e32afe3`
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
# Mon, 01 Nov 2021 18:44:24 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:44:24 GMT
ARG ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
# Mon, 01 Nov 2021 18:45:42 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:45:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:45:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:45:48 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=0fb155addb2544456788eafa3d2681a8db028c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:45:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:45:49 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:45:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:45:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:45:49 GMT
USER odoo
# Mon, 01 Nov 2021 18:45:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:45:50 GMT
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
	-	`sha256:9983055c000eb48340921f78bdcf279b8d5beb6c55abc2f8f7294e53befce77f`  
		Last Modified: Mon, 01 Nov 2021 18:48:26 GMT  
		Size: 291.0 MB (291045018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00da0c14e70bde3fec687d48737d0dac75916bcda62a0f65312627aadf429ce3`  
		Last Modified: Mon, 01 Nov 2021 18:47:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b9cee3e5391ceadf5fa5259a1b92fb446f559d961ddf11b9575b906cda41e`  
		Last Modified: Mon, 01 Nov 2021 18:47:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a490fe3bf701027712cd8b7b5ea68bd25bc2495a8a12dec723c4fe982d7ee1b`  
		Last Modified: Mon, 01 Nov 2021 18:47:53 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe05bbd798e701a5f1fc13a8c33d4fe79a80cfa76de3091ede65f559add61ae`  
		Last Modified: Mon, 01 Nov 2021 18:47:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:fe8cd924e90b49858fc7854d557235814c4bd511d8ef1ee11a7842467b5fbe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:807da396e9fd0fcb651bfb51604ed9705168c39c6fa74e2bb7f983d023251d9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528318219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fc019b88586a5d74defa65297cf711da6a5467ed42fe3eaa0f55ee07a499b5`
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
# Mon, 01 Nov 2021 18:43:01 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:43:02 GMT
ARG ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
# Mon, 01 Nov 2021 18:44:13 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:44:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:44:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:44:17 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:44:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:44:17 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:44:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:44:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:44:18 GMT
USER odoo
# Mon, 01 Nov 2021 18:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:44:18 GMT
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
	-	`sha256:a44b20c2a46c194febb7b406c566d560d3579392ef8d04f715ebbc33205bd46f`  
		Last Modified: Mon, 01 Nov 2021 18:47:42 GMT  
		Size: 273.7 MB (273702542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bced8f5ad8a92cf8fc561932c12618f638a9dbeda2630aa0b75d2fcf789597`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67d8f37ad49715c056fa5d09717204f8a36b4625409d9a82cb28d9bd5702937`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1344e51373e2494ddb9660fa4c9dad9afdf71462d5b8ee2cdfa2ef1ca67b23`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fcda487847ce6d41e967d2868ca132f05bb4f35b3d13d08a8e0967eef97ecf`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:fe8cd924e90b49858fc7854d557235814c4bd511d8ef1ee11a7842467b5fbe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:807da396e9fd0fcb651bfb51604ed9705168c39c6fa74e2bb7f983d023251d9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528318219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fc019b88586a5d74defa65297cf711da6a5467ed42fe3eaa0f55ee07a499b5`
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
# Mon, 01 Nov 2021 18:43:01 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:43:02 GMT
ARG ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
# Mon, 01 Nov 2021 18:44:13 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:44:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:44:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:44:17 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=9b1b93782b939f6246f3e230c655d68caff449d2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:44:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:44:17 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:44:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:44:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:44:18 GMT
USER odoo
# Mon, 01 Nov 2021 18:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:44:18 GMT
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
	-	`sha256:a44b20c2a46c194febb7b406c566d560d3579392ef8d04f715ebbc33205bd46f`  
		Last Modified: Mon, 01 Nov 2021 18:47:42 GMT  
		Size: 273.7 MB (273702542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bced8f5ad8a92cf8fc561932c12618f638a9dbeda2630aa0b75d2fcf789597`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67d8f37ad49715c056fa5d09717204f8a36b4625409d9a82cb28d9bd5702937`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1344e51373e2494ddb9660fa4c9dad9afdf71462d5b8ee2cdfa2ef1ca67b23`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fcda487847ce6d41e967d2868ca132f05bb4f35b3d13d08a8e0967eef97ecf`  
		Last Modified: Mon, 01 Nov 2021 18:47:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:cef84f3dd21de701ce1c1500b7557b8050fce5c8d53bd668a00c79aebbf0fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:b6cdd0e2de596e440cb30043ee53f99c3096fce0fb6e7b23a6a804104e9fce07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542592410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae3f4898cd2a040419215578ff13034a38282cff1be6af78da806217409f6b`
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
# Mon, 01 Nov 2021 18:41:27 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:41:28 GMT
ARG ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
# Mon, 01 Nov 2021 18:42:42 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:42:47 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:42:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:42:47 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:42:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:42:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:42:48 GMT
USER odoo
# Mon, 01 Nov 2021 18:42:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:42:48 GMT
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
	-	`sha256:7737a242428cd8250f85c14d968cc493d487f384432acfc1e3372d2d8e84cc14`  
		Last Modified: Mon, 01 Nov 2021 18:46:53 GMT  
		Size: 287.6 MB (287581332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf627bb0177b3581e858b43ef5b204bd578754745eca507109b34fadf6bc959`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d45e604ee8cbd9ff88f4efff193c71b9ba248a54844d79ece8466fb16a7b184`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afafacabc64ee82578c66cf2f453bcfc5a79a0b40779ae02ddc369a97d358bc`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecd849609950186ce8c926d417767e2bab6477ba87eb23198f692ee880454b`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:cef84f3dd21de701ce1c1500b7557b8050fce5c8d53bd668a00c79aebbf0fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:b6cdd0e2de596e440cb30043ee53f99c3096fce0fb6e7b23a6a804104e9fce07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542592410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae3f4898cd2a040419215578ff13034a38282cff1be6af78da806217409f6b`
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
# Mon, 01 Nov 2021 18:41:27 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:41:28 GMT
ARG ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
# Mon, 01 Nov 2021 18:42:42 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:42:47 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:42:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:42:47 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:42:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:42:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:42:48 GMT
USER odoo
# Mon, 01 Nov 2021 18:42:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:42:48 GMT
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
	-	`sha256:7737a242428cd8250f85c14d968cc493d487f384432acfc1e3372d2d8e84cc14`  
		Last Modified: Mon, 01 Nov 2021 18:46:53 GMT  
		Size: 287.6 MB (287581332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf627bb0177b3581e858b43ef5b204bd578754745eca507109b34fadf6bc959`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d45e604ee8cbd9ff88f4efff193c71b9ba248a54844d79ece8466fb16a7b184`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afafacabc64ee82578c66cf2f453bcfc5a79a0b40779ae02ddc369a97d358bc`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecd849609950186ce8c926d417767e2bab6477ba87eb23198f692ee880454b`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:cef84f3dd21de701ce1c1500b7557b8050fce5c8d53bd668a00c79aebbf0fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b6cdd0e2de596e440cb30043ee53f99c3096fce0fb6e7b23a6a804104e9fce07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542592410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae3f4898cd2a040419215578ff13034a38282cff1be6af78da806217409f6b`
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
# Mon, 01 Nov 2021 18:41:27 GMT
ARG ODOO_RELEASE=20211029
# Mon, 01 Nov 2021 18:41:28 GMT
ARG ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
# Mon, 01 Nov 2021 18:42:42 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 01 Nov 2021 18:42:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 01 Nov 2021 18:42:47 GMT
# ARGS: ODOO_RELEASE=20211029 ODOO_SHA=1b0d6aac881aa968a77e57f529d357688786a12c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 01 Nov 2021 18:42:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 01 Nov 2021 18:42:47 GMT
EXPOSE 8069 8071 8072
# Mon, 01 Nov 2021 18:42:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 01 Nov 2021 18:42:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 01 Nov 2021 18:42:48 GMT
USER odoo
# Mon, 01 Nov 2021 18:42:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Nov 2021 18:42:48 GMT
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
	-	`sha256:7737a242428cd8250f85c14d968cc493d487f384432acfc1e3372d2d8e84cc14`  
		Last Modified: Mon, 01 Nov 2021 18:46:53 GMT  
		Size: 287.6 MB (287581332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf627bb0177b3581e858b43ef5b204bd578754745eca507109b34fadf6bc959`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d45e604ee8cbd9ff88f4efff193c71b9ba248a54844d79ece8466fb16a7b184`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afafacabc64ee82578c66cf2f453bcfc5a79a0b40779ae02ddc369a97d358bc`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecd849609950186ce8c926d417767e2bab6477ba87eb23198f692ee880454b`  
		Last Modified: Mon, 01 Nov 2021 18:46:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
