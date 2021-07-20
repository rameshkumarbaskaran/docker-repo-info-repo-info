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
$ docker pull odoo@sha256:cddfdf7d283fdec10f1a49c03e8ba25b2c261d5d1039654bd7ab49d6a88a866a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:92fa6a24d0856b4189037a7851acd942636dbc02ea53969565d46b006c4b6189
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538386416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a04fc664e1484dab69ab94499c646d24d4e193e33b3c59dd5a8a4d0d925569`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:22:13 GMT
ADD file:a63c6cc73701d6cb7195338c446b9e92ef6b7a0f9321f6cc1bf8738e3da57c66 in / 
# Wed, 23 Jun 2021 00:22:14 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:51:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:51:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:51:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 23 Jun 2021 07:53:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:54:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:13 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:14 GMT
ENV ODOO_VERSION=12.0
# Tue, 20 Jul 2021 18:25:05 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:25:05 GMT
ARG ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
# Tue, 20 Jul 2021 18:26:09 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:26:12 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:26:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:26:13 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:26:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:26:13 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:26:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:26:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:26:14 GMT
USER odoo
# Tue, 20 Jul 2021 18:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:26:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aed007321795cdc03a0ba9b238567ffa299459e9b0322a3d835a04d06afc2500`  
		Last Modified: Wed, 23 Jun 2021 00:28:29 GMT  
		Size: 22.5 MB (22528174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f8f66a1ee8d03d029b9e9fd4fab492aae82ab75ecc939a565a9ed63bd81f8`  
		Last Modified: Wed, 23 Jun 2021 07:57:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6f54374b12d423468b84b7b20816bca30d69f0367e06c3fcc78a58990776d`  
		Last Modified: Wed, 23 Jun 2021 07:58:33 GMT  
		Size: 219.7 MB (219658352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0f9e42ea609c4a44d52d51b1be4eb6a509244b5ff23b7ce9cc26e2d31f4d9`  
		Last Modified: Wed, 23 Jun 2021 07:57:59 GMT  
		Size: 2.2 MB (2224626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47480c9939297e4d6a19caeef3f46a6554712b96da0972a4b1630a6d1a39808f`  
		Last Modified: Wed, 23 Jun 2021 07:58:05 GMT  
		Size: 22.0 MB (22023550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ff03fd79d8ce42a9078be522a594320413d85c028a345e1dcec6873b275683`  
		Last Modified: Tue, 20 Jul 2021 18:28:40 GMT  
		Size: 271.9 MB (271949052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6904f06aa8308d4cd9460d4bbf30950eb1b4f401bef16e7a70575adce79750`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7cb295d4e6594feed968f6fbf7b730542be1ef61a2b4066cff6e0a2e44d4a7`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e8dca2548ef4d75e3dbb28ddf0f6511999ca8509d053c7d91c361909040f5`  
		Last Modified: Tue, 20 Jul 2021 18:28:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeca10d42bb3e7b6c809ece2204a99ae95bfef5f2de2e95151b5745c3ceaa8e`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:cddfdf7d283fdec10f1a49c03e8ba25b2c261d5d1039654bd7ab49d6a88a866a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:92fa6a24d0856b4189037a7851acd942636dbc02ea53969565d46b006c4b6189
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538386416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a04fc664e1484dab69ab94499c646d24d4e193e33b3c59dd5a8a4d0d925569`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:22:13 GMT
ADD file:a63c6cc73701d6cb7195338c446b9e92ef6b7a0f9321f6cc1bf8738e3da57c66 in / 
# Wed, 23 Jun 2021 00:22:14 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:51:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:51:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:51:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 23 Jun 2021 07:53:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:54:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:13 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:14 GMT
ENV ODOO_VERSION=12.0
# Tue, 20 Jul 2021 18:25:05 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:25:05 GMT
ARG ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
# Tue, 20 Jul 2021 18:26:09 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:26:12 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:26:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:26:13 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:26:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:26:13 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:26:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:26:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:26:14 GMT
USER odoo
# Tue, 20 Jul 2021 18:26:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:26:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aed007321795cdc03a0ba9b238567ffa299459e9b0322a3d835a04d06afc2500`  
		Last Modified: Wed, 23 Jun 2021 00:28:29 GMT  
		Size: 22.5 MB (22528174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f8f66a1ee8d03d029b9e9fd4fab492aae82ab75ecc939a565a9ed63bd81f8`  
		Last Modified: Wed, 23 Jun 2021 07:57:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6f54374b12d423468b84b7b20816bca30d69f0367e06c3fcc78a58990776d`  
		Last Modified: Wed, 23 Jun 2021 07:58:33 GMT  
		Size: 219.7 MB (219658352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0f9e42ea609c4a44d52d51b1be4eb6a509244b5ff23b7ce9cc26e2d31f4d9`  
		Last Modified: Wed, 23 Jun 2021 07:57:59 GMT  
		Size: 2.2 MB (2224626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47480c9939297e4d6a19caeef3f46a6554712b96da0972a4b1630a6d1a39808f`  
		Last Modified: Wed, 23 Jun 2021 07:58:05 GMT  
		Size: 22.0 MB (22023550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ff03fd79d8ce42a9078be522a594320413d85c028a345e1dcec6873b275683`  
		Last Modified: Tue, 20 Jul 2021 18:28:40 GMT  
		Size: 271.9 MB (271949052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6904f06aa8308d4cd9460d4bbf30950eb1b4f401bef16e7a70575adce79750`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7cb295d4e6594feed968f6fbf7b730542be1ef61a2b4066cff6e0a2e44d4a7`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e8dca2548ef4d75e3dbb28ddf0f6511999ca8509d053c7d91c361909040f5`  
		Last Modified: Tue, 20 Jul 2021 18:28:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeca10d42bb3e7b6c809ece2204a99ae95bfef5f2de2e95151b5745c3ceaa8e`  
		Last Modified: Tue, 20 Jul 2021 18:28:12 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:89c73cfee04751757dc4250bdd55c0c6f06e945c35fe1345ad44c4f66962292c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:70e3006b96b9785dac4575863d5934239ae4ee95a70b72a9c725d6a7b7f91af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528299301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e6d81aa7a87486fa85debd56b46c609eb16ba4cfeef4096002531ba5ed590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:49:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:49:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:49:53 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:49:53 GMT
ENV ODOO_VERSION=13.0
# Tue, 20 Jul 2021 18:23:40 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:23:40 GMT
ARG ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
# Tue, 20 Jul 2021 18:24:48 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:24:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:24:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:24:53 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:24:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:24:54 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:24:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:24:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:24:54 GMT
USER odoo
# Tue, 20 Jul 2021 18:24:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:24:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760ec83e05549c1bafe40d795ed53c471a0208b2e5a5fe29f1f4575e4277ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:34 GMT  
		Size: 207.1 MB (207122080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6f5407abbe57f2c624e00f8226cb3f74567fc177824c08838c437a8d05fba`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 2.3 MB (2346852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7db6376102b543b53d50ab5ed822526c9569bbee49c030740510ed71465072`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 885.8 KB (885845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2d4315034da69f1b52f903c8dacb128718ba4b1d939db822914bcd42d50958`  
		Last Modified: Tue, 20 Jul 2021 18:28:01 GMT  
		Size: 290.8 MB (290796242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30f8f988bbd2e4c81528bb4051997e850beff830200c9953c3df422ac5df50`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c0b9d5bb236ab6c51bf729dce0f3e5f0f441b5f096afc8e49c41caf8a39db`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e59cdea9f75a53eac1be7e4e68483ddf5f8b1d0abb5fda1c48a9d041b2795a3`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119769fe5e7faf65fcbf2efcde6971c86c717d972628fbe0b13210609c5e7f22`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:89c73cfee04751757dc4250bdd55c0c6f06e945c35fe1345ad44c4f66962292c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:70e3006b96b9785dac4575863d5934239ae4ee95a70b72a9c725d6a7b7f91af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528299301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1e6d81aa7a87486fa85debd56b46c609eb16ba4cfeef4096002531ba5ed590`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:49:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:49:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:49:53 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:49:53 GMT
ENV ODOO_VERSION=13.0
# Tue, 20 Jul 2021 18:23:40 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:23:40 GMT
ARG ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
# Tue, 20 Jul 2021 18:24:48 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:24:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:24:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:24:53 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:24:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:24:54 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:24:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:24:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:24:54 GMT
USER odoo
# Tue, 20 Jul 2021 18:24:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:24:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760ec83e05549c1bafe40d795ed53c471a0208b2e5a5fe29f1f4575e4277ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:34 GMT  
		Size: 207.1 MB (207122080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6f5407abbe57f2c624e00f8226cb3f74567fc177824c08838c437a8d05fba`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 2.3 MB (2346852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7db6376102b543b53d50ab5ed822526c9569bbee49c030740510ed71465072`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 885.8 KB (885845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2d4315034da69f1b52f903c8dacb128718ba4b1d939db822914bcd42d50958`  
		Last Modified: Tue, 20 Jul 2021 18:28:01 GMT  
		Size: 290.8 MB (290796242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a30f8f988bbd2e4c81528bb4051997e850beff830200c9953c3df422ac5df50`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c0b9d5bb236ab6c51bf729dce0f3e5f0f441b5f096afc8e49c41caf8a39db`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e59cdea9f75a53eac1be7e4e68483ddf5f8b1d0abb5fda1c48a9d041b2795a3`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119769fe5e7faf65fcbf2efcde6971c86c717d972628fbe0b13210609c5e7f22`  
		Last Modified: Tue, 20 Jul 2021 18:27:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:ff250c1facb13f138fd03eae8b08f9885fdafeed90baf703eb94b3b82745e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:b47e65a6bccb12797e1235b4d351ed8735967ea5fc3be0185c886d917f1717fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516572622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15e160ba5ed7e1b744724e950bb408b2e4dcfdd5cc28846abec615068ccd357`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 20 Jul 2021 18:22:14 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:22:15 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Tue, 20 Jul 2021 18:23:24 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:23:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:23:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:23:29 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:23:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:23:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:23:30 GMT
USER odoo
# Tue, 20 Jul 2021 18:23:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:23:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a095a4e8319cd4ba47fb4a11e3935a1b8de87931f0c6bb31bd0048b5f63f9fb6`  
		Last Modified: Tue, 20 Jul 2021 18:27:15 GMT  
		Size: 273.0 MB (273017629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dea2bca23d7ed91e4ea1e1b06a14c11abce287a59a97ec3bfa7df1b622964f1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8a394291dc5571f75eb6574d177fe57d5f4ddbd5a7fc5e4cf208ac7a212be`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1356ed48c125d70fea267e70d0fbcdaa759bf5506f87c0c69a738a244112ea`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117b4950a550b9bd00eca430164635291b37c3fcb5f526eefde5407e0ded9d1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:ff250c1facb13f138fd03eae8b08f9885fdafeed90baf703eb94b3b82745e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:b47e65a6bccb12797e1235b4d351ed8735967ea5fc3be0185c886d917f1717fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516572622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15e160ba5ed7e1b744724e950bb408b2e4dcfdd5cc28846abec615068ccd357`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 20 Jul 2021 18:22:14 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:22:15 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Tue, 20 Jul 2021 18:23:24 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:23:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:23:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:23:29 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:23:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:23:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:23:30 GMT
USER odoo
# Tue, 20 Jul 2021 18:23:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:23:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a095a4e8319cd4ba47fb4a11e3935a1b8de87931f0c6bb31bd0048b5f63f9fb6`  
		Last Modified: Tue, 20 Jul 2021 18:27:15 GMT  
		Size: 273.0 MB (273017629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dea2bca23d7ed91e4ea1e1b06a14c11abce287a59a97ec3bfa7df1b622964f1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8a394291dc5571f75eb6574d177fe57d5f4ddbd5a7fc5e4cf208ac7a212be`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1356ed48c125d70fea267e70d0fbcdaa759bf5506f87c0c69a738a244112ea`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117b4950a550b9bd00eca430164635291b37c3fcb5f526eefde5407e0ded9d1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:ff250c1facb13f138fd03eae8b08f9885fdafeed90baf703eb94b3b82745e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b47e65a6bccb12797e1235b4d351ed8735967ea5fc3be0185c886d917f1717fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516572622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15e160ba5ed7e1b744724e950bb408b2e4dcfdd5cc28846abec615068ccd357`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 20 Jul 2021 18:22:14 GMT
ARG ODOO_RELEASE=20210720
# Tue, 20 Jul 2021 18:22:15 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Tue, 20 Jul 2021 18:23:24 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 20 Jul 2021 18:23:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 20 Jul 2021 18:23:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 20 Jul 2021 18:23:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 Jul 2021 18:23:29 GMT
EXPOSE 8069 8071 8072
# Tue, 20 Jul 2021 18:23:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 Jul 2021 18:23:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 20 Jul 2021 18:23:30 GMT
USER odoo
# Tue, 20 Jul 2021 18:23:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Jul 2021 18:23:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a095a4e8319cd4ba47fb4a11e3935a1b8de87931f0c6bb31bd0048b5f63f9fb6`  
		Last Modified: Tue, 20 Jul 2021 18:27:15 GMT  
		Size: 273.0 MB (273017629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dea2bca23d7ed91e4ea1e1b06a14c11abce287a59a97ec3bfa7df1b622964f1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8a394291dc5571f75eb6574d177fe57d5f4ddbd5a7fc5e4cf208ac7a212be`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1356ed48c125d70fea267e70d0fbcdaa759bf5506f87c0c69a738a244112ea`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d117b4950a550b9bd00eca430164635291b37c3fcb5f526eefde5407e0ded9d1`  
		Last Modified: Tue, 20 Jul 2021 18:26:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
